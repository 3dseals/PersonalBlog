title: RuoYi-Cloud微服务框架入门与部署
date: 2023-09-10 15:00:00
tags: RuoYi SpringCloud Nacos 微服务 Java
categories: 框架介绍
---

## 前言

RuoYi-Cloud是基于Spring Cloud的微服务权限管理系统，采用前后端分离架构。本文介绍如何使用Nacos进行微服务管理，以及单机调试与微服务模式部署的方法。

## 技术栈

| 技术 | 说明 |
|------|------|
| Spring Cloud | 微服务框架 |
| Spring Cloud Alibaba | 阿里巴巴微服务组件 |
| Nacos | 服务注册与配置中心 |
| Gateway | 网关服务 |
| Sentinel | 流量控制 |
| Seata | 分布式事务 |
| MySQL | 数据库 |
| Redis | 缓存 |

## 项目结构

```
ruoyi-cloud/
├── ruoyi-api/                    # API模块
│   ├── ruoyi-api-system/        # 系统API
│   └── ruoyi-api-file/          # 文件API
├── ruoyi-auth/                   # 认证中心
├── ruoyi-common/                 # 通用模块
│   ├── ruoyi-common-core/       # 核心模块
│   ├── ruoyi-common-redis/      # Redis模块
│   ├── ruoyi-common-security/   # 安全模块
│   └── ruoyi-common-swagger/    # Swagger模块
├── ruoyi-gateway/                # 网关服务
├── ruoyi-modules/                # 业务模块
│   ├── ruoyi-system/            # 系统模块
│   ├── ruoyi-gen/               # 代码生成
│   ├── ruoyi-job/               # 定时任务
│   └── ruoyi-file/              # 文件服务
├── ruoyi-visual/                 # 可视化模块
│   └── ruoyi-monitor/           # 监控中心
└── ruoyi-ui/                     # 前端项目
```

## 自定义模块结构

按照你提供的结构，创建自定义业务模块：


```
${artifactId}/
├─ pom.xml                           # 根pom（带profiles）
├─ ${artifactId}-api/                # API聚合模块
│   ├─ ${artifactId}-local-api/      # 单机启动模块
│   │   ├─ pom.xml
│   │   └─ src/main/java/...
│   ├─ ${artifactId}-cloud-api/      # 微服务启动模块
│   │   ├─ pom.xml
│   │   └─ src/main/java/...
│   └─ pom.xml
├─ ${artifactId}-biz/                # 业务逻辑模块
│   ├─ pom.xml
│   └─ src/main/java/...
└─ ${artifactId}-start/              # 启动模块
    ├─ pom.xml
    └─ src/main/java/...
```

## Nacos配置

### 1. 安装Nacos

```bash
# 下载Nacos
wget https://github.com/alibaba/nacos/releases/download/2.2.0/nacos-server-2.2.0.tar.gz
tar -xvf nacos-server-2.2.0.tar.gz
cd nacos/bin

# 单机模式启动
./startup.sh -m standalone

# Windows
startup.cmd -m standalone
```

访问 http://localhost:8848/nacos，默认账号密码：nacos/nacos

### 2. 服务注册配置

```yaml
# application.yml
spring:
  application:
    name: ruoyi-system
  cloud:
    nacos:
      discovery:
        server-addr: 127.0.0.1:8848
        namespace: dev
      config:
        server-addr: 127.0.0.1:8848
        namespace: dev
        file-extension: yml
```

### 3. 配置中心使用

在Nacos控制台创建配置：
- Data ID: `ruoyi-system-dev.yml`
- Group: `DEFAULT_GROUP`

```yaml
# Nacos配置内容
server:
  port: 9201

spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/ry-cloud?useUnicode=true
    username: root
    password: password
```

## 单机调试模式

### Profile配置

根pom.xml配置profiles：

```xml
<profiles>
    <!-- 单机模式 -->
    <profile>
        <id>local</id>
        <properties>
            <profile.active>local</profile.active>
        </properties>
        <activation>
            <activeByDefault>true</activeByDefault>
        </activation>
    </profile>
    <!-- 微服务模式 -->
    <profile>
        <id>cloud</id>
        <properties>
            <profile.active>cloud</profile.active>
        </properties>
    </profile>
</profiles>
```

### 单机启动配置

`application-local.yml`:

```yaml
spring:
  profiles:
    active: local
  cloud:
    nacos:
      discovery:
        enabled: false  # 禁用服务注册
      config:
        enabled: false  # 禁用配置中心

# 直接配置数据源
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/ry-cloud
    username: root
    password: password
```

### 单机启动命令

```bash
# 使用local profile启动
mvn spring-boot:run -Plocal

# 或者IDEA中设置Active Profiles为local
```

## 微服务模式部署

### 1. 启动顺序

```
1. Nacos (服务注册与配置中心)
2. MySQL + Redis
3. ruoyi-gateway (网关)
4. ruoyi-auth (认证中心)
5. ruoyi-system (系统服务)
6. 其他业务服务
```

### 2. Docker Compose部署

```yaml
version: '3'
services:
  nacos:
    image: nacos/nacos-server:v2.2.0
    environment:
      - MODE=standalone
    ports:
      - "8848:8848"
    
  mysql:
    image: mysql:8.0
    environment:
      - MYSQL_ROOT_PASSWORD=root
    ports:
      - "3306:3306"
    
  redis:
    image: redis:6.0
    ports:
      - "6379:6379"
    
  ruoyi-gateway:
    build: ./ruoyi-gateway
    ports:
      - "8080:8080"
    depends_on:
      - nacos
      
  ruoyi-auth:
    build: ./ruoyi-auth
    depends_on:
      - nacos
      - redis
      
  ruoyi-system:
    build: ./ruoyi-modules/ruoyi-system
    depends_on:
      - nacos
      - mysql
```

### 3. 微服务启动命令

```bash
# 使用cloud profile启动
mvn spring-boot:run -Pcloud

# 打包
mvn clean package -Pcloud

# 运行jar
java -jar ruoyi-gateway.jar --spring.profiles.active=cloud
```

## 服务调用

### Feign客户端定义

```java
// ruoyi-api-system模块
@FeignClient(contextId = "remoteUserService", 
             value = "ruoyi-system",
             fallbackFactory = RemoteUserFallbackFactory.class)
public interface RemoteUserService {
    
    @GetMapping("/user/info/{username}")
    R<LoginUser> getUserInfo(@PathVariable("username") String username);
}
```

### 服务调用

```java
@Service
public class SysLoginService {
    
    @Autowired
    private RemoteUserService remoteUserService;
    
    public LoginUser login(String username) {
        R<LoginUser> result = remoteUserService.getUserInfo(username);
        return result.getData();
    }
}
```

## 常见问题

### 1. Nacos连接失败
检查Nacos是否启动，namespace是否正确配置

### 2. 服务注册不上
检查spring.application.name是否配置，网络是否通畅

### 3. 配置不生效
确认Data ID格式：`${spring.application.name}-${profile}.${file-extension}`

## 总结

RuoYi-Cloud通过Nacos实现了服务注册与配置管理，支持单机和微服务两种部署模式。开发时使用单机模式方便调试，生产环境使用微服务模式实现高可用。

## 参考资料

- [RuoYi-Cloud官方文档](http://doc.ruoyi.vip/ruoyi-cloud/)
- [Nacos官方文档](https://nacos.io/zh-cn/docs/quick-start.html)
- [Spring Cloud Alibaba](https://spring-cloud-alibaba-group.github.io/github-pages/hoxton/zh-cn/)
