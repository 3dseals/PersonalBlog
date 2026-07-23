---
title: 个人简历
date: 2025-12-30 11:00:00
comments: false
---

<style>
/* ========== 下载PDF按钮 ========== */
.resume-header-top {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
  position: relative;
  z-index: 1;
}
.pdf-download-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 8px 20px;
  background: rgba(255,255,255,0.15);
  color: #7dd3fc;
  border: 1px solid rgba(125,211,252,0.3);
  border-radius: 24px;
  font-size: 0.85em;
  font-family: inherit;
  cursor: pointer;
  backdrop-filter: blur(4px);
  transition: all 0.3s ease;
  text-decoration: none;
  white-space: nowrap;
}
.pdf-download-btn:hover {
  background: rgba(255,255,255,0.25);
  color: #fff;
  border-color: rgba(255,255,255,0.5);
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(125,211,252,0.25);
}

/* ========== 打印/PDF导出样式 ========== */
@media print {
  /* 隐藏tranquilpeak主题导航与装饰元素 */
  #sidebar, .sidebar,
  #header, header,
  #bottom-bar, .post-bottom-bar,
  .post-header-cover, .header-cover,
  .share-options-bar,
  .post-actions-wrap, .post-footer,
  .post-meta, .post-header,
  .pagination, footer, .footer,
  nav, #main-nav, .main-nav,
  .cover, .about,
  .share-options, .post-nav,
  .comment, .comments, #comments,
  .pdf-download-btn,
  .post-toc, .toc,
  .alert {
    display: none !important;
  }

  body, html {
    margin: 0 !important;
    padding: 0 !important;
    background: #fff !important;
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }

  #blog, #main {
    margin: 0 !important;
    padding: 0 !important;
  }

  .post, .post-content, .post-body, .page, .main {
    margin: 0 !important;
    padding: 0 !important;
    max-width: 100% !important;
    width: 100% !important;
    box-shadow: none !important;
    border: none !important;
  }

  .resume-header {
    margin: 0 0 20px 0 !important;
    border-radius: 0 !important;
    padding: 30px 20px !important;
  }

  .timeline-item, .project-card, .advantage-card {
    break-inside: avoid;
    page-break-inside: avoid;
  }

  .section-title {
    break-after: avoid;
    page-break-after: avoid;
    margin: 24px 0 16px 0 !important;
  }

  @page {
    margin: 1cm;
    size: A4;
  }
}

/* ========== 简历全局美化样式 ========== */
.post-body {
  font-family: 'PingFang SC', 'Microsoft YaHei', -apple-system, BlinkMacSystemFont, sans-serif;
}

/* 简历头部区域 */
.resume-header {
  text-align: center;
  padding: 40px 30px;
  background: linear-gradient(135deg, #0f2027 0%, #203a43 50%, #2c5364 100%);
  border-radius: 16px;
  margin-bottom: 32px;
  position: relative;
  overflow: hidden;
}
.resume-header::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.05) 0%, transparent 70%);
  animation: headerGlow 8s ease-in-out infinite;
}
@keyframes headerGlow {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(5%, 5%); }
}
.resume-header h1 {
  color: #fff !important;
  font-size: 2.4em !important;
  margin: 0 0 12px 0 !important;
  letter-spacing: 4px;
  position: relative;
  z-index: 1;
  border: none !important;
}
.resume-header .subtitle {
  color: rgba(255,255,255,0.75);
  font-size: 1.05em;
  letter-spacing: 2px;
  position: relative;
  z-index: 1;
}
.resume-header .tag-list {
  margin-top: 18px;
  position: relative;
  z-index: 1;
}
.resume-header .tag-list span {
  display: inline-block;
  background: rgba(255,255,255,0.12);
  color: #7dd3fc;
  padding: 5px 16px;
  border-radius: 20px;
  font-size: 0.85em;
  margin: 4px 6px;
  backdrop-filter: blur(4px);
  border: 1px solid rgba(125,211,252,0.2);
}

/* 通用Section标题 */
.section-title {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.5em !important;
  color: #1e3a5f !important;
  border-bottom: 3px solid;
  border-image: linear-gradient(90deg, #3b82f6, #06b6d4, transparent) 1;
  padding-bottom: 10px;
  margin: 40px 0 24px 0 !important;
}
.section-title .icon {
  font-size: 1.2em;
}

/* 信息卡片网格 */
.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 14px;
  margin-bottom: 24px;
}
.info-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 14px 18px;
  background: linear-gradient(135deg, #f8fafc, #f1f5f9);
  border-radius: 10px;
  border-left: 3px solid #3b82f6;
  transition: all 0.3s ease;
}
.info-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(59,130,246,0.12);
}
.info-item .label {
  font-size: 0.85em;
  color: #64748b;
  min-width: 60px;
}
.info-item .value {
  font-weight: 600;
  color: #1e293b;
}
.info-item .value a {
  color: #3b82f6;
  text-decoration: none;
}
.info-item .value a:hover {
  text-decoration: underline;
}

/* 联系方式卡片 */
.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 12px;
  margin-bottom: 24px;
}
.contact-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 16px;
  background: #fff;
  border-radius: 10px;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}
.contact-item:hover {
  border-color: #3b82f6;
  box-shadow: 0 2px 8px rgba(59,130,246,0.1);
}
.contact-item .contact-icon {
  font-size: 1.4em;
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #eff6ff, #dbeafe);
  border-radius: 8px;
}
.contact-item .contact-text {
  color: #334155;
  font-size: 0.95em;
}
.contact-item .contact-text a {
  color: #3b82f6;
  text-decoration: none;
}

/* 核心优势卡片 */
.advantage-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin-bottom: 24px;
}
.advantage-card {
  padding: 24px;
  border-radius: 12px;
  background: #fff;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}
.advantage-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
}
.advantage-card:nth-child(1)::before { background: linear-gradient(90deg, #3b82f6, #06b6d4); }
.advantage-card:nth-child(2)::before { background: linear-gradient(90deg, #8b5cf6, #ec4899); }
.advantage-card:nth-child(3)::before { background: linear-gradient(90deg, #f59e0b, #ef4444); }
.advantage-card:nth-child(4)::before { background: linear-gradient(90deg, #10b981, #06b6d4); }
.advantage-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.08);
}
.advantage-card h4 {
  margin: 0 0 14px 0 !important;
  font-size: 1.1em;
  color: #1e293b;
}
.advantage-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.advantage-card ul li {
  padding: 5px 0;
  color: #475569;
  font-size: 0.92em;
  position: relative;
  padding-left: 18px;
}
.advantage-card ul li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: #3b82f6;
  font-weight: bold;
}

/* 技术栈区域 */
.tech-section {
  margin-bottom: 28px;
}
.tech-category {
  margin-bottom: 24px;
}
.tech-category h4 {
  color: #334155 !important;
  font-size: 1em;
  margin-bottom: 12px !important;
  padding-left: 12px;
  border-left: 3px solid #3b82f6;
}
.skill-bar {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
  gap: 12px;
}
.skill-name {
  min-width: 120px;
  font-size: 0.9em;
  color: #475569;
  font-weight: 500;
}
.skill-track {
  flex: 1;
  height: 22px;
  background: #f1f5f9;
  border-radius: 11px;
  overflow: hidden;
  position: relative;
}
.skill-fill {
  height: 100%;
  border-radius: 11px;
  transition: width 1.5s ease;
  position: relative;
}
.skill-fill.expert { background: linear-gradient(90deg, #3b82f6, #06b6d4); }
.skill-fill.proficient { background: linear-gradient(90deg, #8b5cf6, #a78bfa); }
.skill-fill.skilled { background: linear-gradient(90deg, #f59e0b, #fbbf24); }
.skill-level {
  font-size: 0.78em;
  color: #94a3b8;
  min-width: 36px;
  text-align: right;
}

/* 工作经历时间线 */
.timeline {
  position: relative;
  padding-left: 32px;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 10px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: linear-gradient(180deg, #3b82f6, #06b6d4, #8b5cf6);
}
.timeline-item {
  position: relative;
  margin-bottom: 32px;
  padding: 24px;
  background: #fff;
  border-radius: 12px;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}
.timeline-item:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  border-color: #93c5fd;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -28px;
  top: 28px;
  width: 12px;
  height: 12px;
  background: #3b82f6;
  border-radius: 50%;
  border: 3px solid #dbeafe;
  z-index: 1;
}
.timeline-item .period {
  display: inline-block;
  background: linear-gradient(135deg, #3b82f6, #2563eb);
  color: #fff;
  padding: 4px 14px;
  border-radius: 20px;
  font-size: 0.85em;
  margin-bottom: 8px;
}
.timeline-item .company {
  font-size: 1.2em;
  font-weight: 700;
  color: #1e293b;
  margin: 6px 0;
}
.timeline-item .position {
  color: #3b82f6;
  font-weight: 600;
  font-size: 0.95em;
  margin-bottom: 8px;
}
.timeline-item .company-desc {
  color: #64748b;
  font-size: 0.88em;
  font-style: italic;
  margin-bottom: 12px;
  padding: 8px 12px;
  background: #f8fafc;
  border-radius: 8px;
}
.timeline-item .duties {
  list-style: none;
  padding: 0;
  margin: 0;
}
.timeline-item .duties li {
  padding: 4px 0 4px 20px;
  color: #475569;
  font-size: 0.92em;
  position: relative;
}
.timeline-item .duties li::before {
  content: '✦';
  position: absolute;
  left: 0;
  color: #06b6d4;
  font-size: 0.7em;
  top: 7px;
}
.timeline-item .highlight {
  color: #ea580c !important;
  font-weight: 600;
}

/* 项目经历卡片 */
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
  gap: 20px;
  margin-bottom: 24px;
}
.project-card {
  padding: 24px;
  border-radius: 12px;
  background: #fff;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}
.project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.08);
}
.project-card .project-year {
  position: absolute;
  top: 16px;
  right: 16px;
  background: linear-gradient(135deg, #f1f5f9, #e2e8f0);
  color: #475569;
  padding: 3px 12px;
  border-radius: 12px;
  font-size: 0.8em;
  font-weight: 600;
}
.project-card .project-name {
  font-size: 1.2em;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 6px;
}
.project-card .project-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 14px;
}
.project-card .project-meta span {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 6px;
  font-size: 0.78em;
  font-weight: 500;
}
.project-card .project-meta .type {
  background: #eff6ff;
  color: #2563eb;
}
.project-card .project-meta .role {
  background: #f0fdf4;
  color: #16a34a;
}
.project-card .project-meta .revenue {
  background: #fff7ed;
  color: #ea580c;
}
.project-card .tech-list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.project-card .tech-list li {
  padding: 4px 0 4px 16px;
  color: #475569;
  font-size: 0.88em;
  position: relative;
}
.project-card .tech-list li::before {
  content: '›';
  position: absolute;
  left: 2px;
  color: #3b82f6;
  font-weight: bold;
  font-size: 1.2em;
  top: 2px;
}

/* 技术总结表格 */
.tech-summary-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 1px 3px rgba(0,0,0,0.06);
  margin-bottom: 24px;
}
.tech-summary-table thead th {
  background: linear-gradient(135deg, #1e3a5f, #2c5364);
  color: #fff;
  padding: 14px 18px;
  font-weight: 600;
  font-size: 0.95em;
  text-align: left;
}
.tech-summary-table tbody td {
  padding: 12px 18px;
  border-bottom: 1px solid #f1f5f9;
  font-size: 0.9em;
}
.tech-summary-table tbody tr:nth-child(even) {
  background: #f8fafc;
}
.tech-summary-table tbody tr:hover {
  background: #eff6ff;
}
.tech-summary-table tbody td:first-child {
  font-weight: 600;
  color: #1e3a5f;
  white-space: nowrap;
}
.tech-summary-table tbody td:last-child {
  color: #475569;
}

/* 致谢区域 */
.thanks-section {
  text-align: center;
  padding: 36px 30px;
  background: linear-gradient(135deg, #f8fafc, #eff6ff);
  border-radius: 16px;
  margin-top: 32px;
  border: 1px solid #dbeafe;
}
.thanks-section p {
  color: #475569;
  line-height: 1.8;
  max-width: 640px;
  margin: 0 auto 12px auto;
  font-size: 0.95em;
}
.thanks-section .signature {
  font-weight: 700;
  color: #1e3a5f;
  font-size: 1.1em;
  margin-top: 16px;
}

/* 响应式 */
@media (max-width: 640px) {
  .resume-header h1 { font-size: 1.6em !important; }
  .info-grid, .contact-grid { grid-template-columns: 1fr; }
  .advantage-cards { grid-template-columns: 1fr; }
  .project-grid { grid-template-columns: 1fr; }
  .timeline { padding-left: 24px; }
  .skill-name { min-width: 90px; font-size: 0.82em; }
}
</style>

<div class="resume-header">
  <div class="resume-header-top">
    <h1>王子亮</h1>
    <button class="pdf-download-btn" onclick="window.print()" title="点击后在打印对话框中选择另存为PDF">&#128196; 下载PDF</button>
  </div>
  <div class="subtitle">高并发服务端架构 · 服务端研发</div>
  <div class="tag-list">
    <span>15年+研发经验</span>
    <span>高并发服务端架构</span>
    <span>Java Spring Cloud / Golang</span>
    <span>多租户SaaS系统</span>
    <span>团队管理 & 进度管控</span>
  </div>
</div>

<h2 class="section-title"><span class="icon">📋</span> 基本信息</h2>

<div class="info-grid">
  <div class="info-item">
    <span class="label">姓名</span>
    <span class="value">王子亮 / 男 / 1987</span>
  </div>
  <div class="info-item">
    <span class="label">学历</span>
    <span class="value">本科 211 · 哈尔滨工程大学 · 计算机科学与技术</span>
  </div>
  <div class="info-item">
    <span class="label">工作年限</span>
    <span class="value">15年+</span>
  </div>
  <div class="info-item">
    <span class="label">期望职位</span>
    <span class="value">高并发服务端架构师 / 服务端架构设计研发</span>
  </div>
  <div class="info-item">
    <span class="label">期望薪资</span>
    <span class="value">30K</span>
  </div>
  <div class="info-item">
    <span class="label">期望城市</span>
    <span class="value">成都</span>
  </div>
</div>

<h2 class="section-title"><span class="icon">📞</span> 联系方式</h2>

<div class="contact-grid">
  <div class="contact-item">
    <div class="contact-icon">📱</div>
    <div class="contact-text">15802857662</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">📧</div>
    <div class="contact-text">lional.king@gmail.com</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">💬</div>
    <div class="contact-text">QQ: 870966629</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🔗</div>
    <div class="contact-text"><a href="https://ibunnyteam.github.io" target="_blank">ibunnyteam.github.io</a></div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🐙</div>
    <div class="contact-text"><a href="https://github.com/3dseals" target="_blank">github.com/3dseals</a></div>
  </div>
</div>

<br>

<h2 class="section-title"><span class="icon">💡</span> 核心优势</h2>

<div class="advantage-cards">
  <div class="advantage-card">
    <h4>🚀 高并发服务端架构</h4>
    <ul>
      <li><strong>Java微服务 & SaaS</strong>：精通 Spring Boot / Spring Cloud (Nacos, Gateway, Feign)；设计多租户 SaaS 隔离架构与基于 <strong>Seata</strong> 的高并发分布式订单系统</li>
      <li><strong>ET分布式游戏服务端</strong>：熟练运用 <strong>ET 框架 (C# / ECS)</strong> 研发高并发分布式微服务服务端，支持平滑横向扩展与集群部署</li>
      <li><strong>Golang高性能组件</strong>：熟练掌握 Golang (Leaf / Gin / gRPC)，自研分布式网关、高性能协程池与 Redis 级联缓存组件</li>
      <li><strong>消息队列与高吞吐</strong>：基于 RocketMQ / Kafka 实现高并发流量削峰填谷、异步解耦与千万级数据推送</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🤝 团队管理与项目进度管控</h4>
    <ul>
      <li>主导 5-20 人研发团队搭建与管理，建立规范化敏捷开发（Scrum/Kanban）与 WBS 任务拆解体系</li>
      <li><strong>项目进度全流程管控</strong>：精准制定里程碑交付节点、进度风险预警与技术攻关机制，确保项目按期交付</li>
      <li>推行 Code Review 与 CI/CD 自动化部署流水线，有效降低生产故障率与技术债务</li>
      <li>推动 AI 工具（Cursor/Claude Code等）落地，建立 AI 协作规范，提升团队整体研发效能 <strong>50%+</strong></li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>📊 商业成果 & 全栈覆盖</h4>
    <ul>
      <li>累计参与项目流水超 <strong>1亿+</strong>（主导核心项目流水超 5000 万）</li>
      <li>具备游戏、直播互动、AI 社交、H5 小游戏等多品类高并发项目从0到1研发落地经验</li>
      <li>兼具客户端（Unity3D/Cocos）与服务端全栈视野，能从技术成本、需求规划与运维全维度把控项目</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🤖 AI工具深度实践</h4>
    <ul>
      <li>深度使用 <strong>Cursor / Claude Code / Codex / Antigravity</strong> 四大主流 AI 编程工具</li>
      <li>推动 AI Agent 编程落地实践，建立团队 AI 辅助开发标准范式与最佳实践</li>
    </ul>
  </div>
</div>

<br>

<h2 class="section-title"><span class="icon">💼</span> 工作经历</h2>

<div class="timeline">

<div class="timeline-item">
  <span class="period">2024.07 - 至今</span>
  <div class="company">四川循东科技有限公司</div>
  <div class="position">高并发服务端技术负责人 / 资深服务端架构师</div>
  <div class="company-desc">专注于AI驱动的虚拟社交与数字娱乐领域，主打多租户高并发小游戏聚合平台及H5游戏矩阵</div>
  <ul class="duties">
    <li><strong>高并发SaaS架构与多租户隔离</strong>：负责高并发服务端架构设计与选型，基于 Spring Boot / Spring Cloud 搭建多租户 SaaS 服务体系，实现租户数据、权限与动态路由的高效隔离</li>
    <li><strong>Seata分布式订单与消息队列</strong>：在多租户高并发充值、秒杀与订单结算场景引入 <strong>Seata (AT/TCC 模式)</strong> 分布式事务框架，保障高并发订单一致性；结合 RocketMQ / Redis 实现请求削峰与高吞吐结算</li>
    <li><strong>团队管理与项目进度管控</strong>：负责研发团队日常管理，制定敏捷开发流程、WBS任务拆解与里程碑交付节点；建立了进度风险预警与技术攻关机制，确保项目节点按期保质完成</li>
    <li><strong>AI赋能与流程优化</strong>：全面推动 AI 辅助编程实践（Cursor / Claude Code 等），建立团队代码规范与 CI/CD 交付标准，提升团队研发交付效率 50%+</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2023.03 - 2024.06</span>
  <div class="company">麓卓互动科技有限公司（成都分公司）</div>
  <div class="position">高并发服务端技术负责人</div>
  <div class="company-desc">专注于AI社交与元宇宙领域，打造3D虚拟社交直播游戏应用《Party Yoo》</div>
  <ul class="duties">
    <li><strong>ET框架分布式服务端架构</strong>：负责《Party Yoo》服务端架构设计与研发，基于 <strong>ET 框架 (C# / ECS 架构)</strong> 构建高并发分布式微服务服务端，支持平滑横向扩展与集群部署</li>
    <li><strong>实时游戏对战与直播互动</strong>：基于 ET 框架网络协议 (KCP/Protobuf/WebSocket) 研发直播间实时互动游戏与多人对战匹配系统，保障低延迟与房间状态同步</li>
    <li><strong>消息队列与高可用保障</strong>：整合 Kafka / RocketMQ 消息队列应对直播间高并发事件削峰填谷；结合 Redis 分布式缓存实现百万级在线支撑</li>
    <li><strong>团队管理与项目进度管控</strong>：负责服务端团队（10+人）管理，推行 OKR 管理与敏捷迭代，精准管控开发周期与风险节点，成功保障产品在印尼等海外市场内测上线</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2013.05 - 2023.02</span>
  <div class="company">成都黑骑士网络科技</div>
  <div class="position">技术合伙人 / 服务端架构师 / 资深服务端研发工程师</div>
  <div class="company-desc">创业型手游与高并发服务端研发公司，多款自研上线游戏流水累计超 5000 万</div>
  <ul class="duties">
    <li><strong>团队组建与进度管控</strong>：从0到1搭建 15+人 技术团队，建立完整研发规范、Code Review 机制与全流程项目进度管控体系，把控产品全生命周期</li>
    <li><strong>Golang高并发服务端与自研组件</strong>：负责核心 Golang 高并发服务端架构设计与关键组件研发，基于 Leaf 游戏框架及自研 org 架构，实现高并发分布式网关、Worker Pool 协程池组件、Redis 级联缓存与高并发限流组件</li>
    <li><strong>全栈架构与高并发游戏研发</strong>：主导《Survive 活下去》、《无尽之界》等多款高并发分布式服务端（Golang / Node.js）及全栈研发，支撑全球同服与高并发长连接实时数据同步</li>
    <li><strong>商业化成果</strong>：掌控整体技术成本、云服务器部署及高并发线上运维，<span class="highlight">核心项目累计流水超 5000 万</span></li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2011.12 - 2013.04</span>
  <div class="company">上海慕和网络</div>
  <div class="position">游戏开发工程师</div>
  <div class="company-desc">手游公司（月流水达1500万，后被收购）</div>
  <ul class="duties">
    <li>参与多款 SLG 游戏服务端与游戏引擎、支付 SDK 研发，见证公司从 50 人扩展至 400 人的高速成长期</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2010.07 - 2011.11</span>
  <div class="company">TCL通讯</div>
  <div class="position">Android开发工程师</div>
  <div class="company-desc">专注于Android手机研发</div>
  <ul class="duties">
    <li>参与 Android 系统核心模块（Contacts、Launcher）定制开发，深入系统底层机制，为后续研发奠定扎实基础</li>
  </ul>
</div>

</div>

<h2 class="section-title"><span class="icon">🎮</span> 项目经历</h2>

<div class="project-grid">

<div class="project-card">
  <span class="project-year">2024 - 至今</span>
  <div class="project-name">高并发多租户 SaaS 小游戏聚合分发平台</div>
  <div class="project-meta">
    <span class="type">高并发SaaS平台</span>
    <span class="role">技术负责人 & 架构师</span>
  </div>
  <ul class="tech-list">
    <li><strong>高并发SaaS架构</strong>：基于 Java Spring Boot / Spring Cloud 打造多租户 SaaS 架构，支持多品类 H5 游戏快速接入与分发</li>
    <li><strong>Seata高并发订单系统</strong>：在平台充值、秒杀与虚拟资产交易场景引入 <strong>Seata (AT/TCC 模式)</strong> 分布式事务框架，保障高并发多租户订单一致性</li>
    <li><strong>租户隔离与消息队列</strong>：实现多租户动态数据源路由隔离与权限隔离；引入 RocketMQ 构建高吞吐数据埋点与实时分析管道</li>
    <li><strong>项目进度管控</strong>：实施敏捷 WBS 任务拆解与里程碑交付管控，推行 AI 辅助开发，大幅缩短业务模块交付周期</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2023 - 2024</span>
  <div class="project-name">Party Yoo — 3D虚拟社交直播高并发微服务平台</div>
  <div class="project-meta">
    <span class="type">高并发分布式 / 实时社交</span>
    <span class="role">高并发服务端技术负责人</span>
  </div>
  <ul class="tech-list">
    <li><strong>ET框架分布式微服务架构</strong>：服务端基于 <strong>ET 框架 (C# / ECS)</strong> 构建，支持微服务化分布式部署与平滑横向扩展</li>
    <li><strong>实时游戏对战与直播互动</strong>：基于 ET 框架底层网络 (KCP/Protobuf/WebSocket) 实现直播间内嵌游戏与低延迟实时多人对战匹配</li>
    <li><strong>消息队列与高并发削峰</strong>：结合 Kafka / RocketMQ 进行高并发事件削峰填谷；使用 Redis 分布式缓存支撑百万级社交数据访问</li>
    <li><strong>团队管理与进度管控</strong>：全面把控服务端研发进度节点，推行 OKR 绩效管理，成功保障产品在东南亚海外市场内测上线</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2020 - 2022</span>
  <div class="project-name">高并发 Golang 游戏服务端及分布式组件库</div>
  <div class="project-meta">
    <span class="type">Golang高并发 / 分布式架构</span>
    <span class="role">服务端架构师 / 技术负责人</span>
  </div>
  <ul class="tech-list">
    <li><strong>Golang高性能服务端架构</strong>：基于 Golang (Leaf 框架 / 孪生 org 架构 / Gin) 构建高性能分布式服务端，基于 gRPC/Protobuf 实现低延迟跨服务通信</li>
    <li><strong>自研分布式网关组件</strong>：基于 Go 协程路由与 JWT 鉴权，实现高并发请求路由分发与动态负载均衡</li>
    <li><strong>Worker Pool 协程池组件</strong>：自研通用协程池与任务调度器，有效降低高并发场景下的 Go 协程频繁创建与 GC 压力</li>
    <li><strong>Redis级联缓存组件</strong>：设计 Redis + LocalCache 双层缓存体系，包含防击穿/防雪崩机制，支持 QPS 达数十万级</li>
    <li><strong>高并发限流组件</strong>：基于 Golang 令牌桶/漏桶算法实现接口级与用户级的高并发防刷限流</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2010 - 2020</span>
  <div class="project-name">自研上线游戏矩阵及早期技术积累</div>
  <div class="project-meta">
    <span class="type">多款上线大作 / 核心基础库</span>
    <span class="role">架构设计 & 全栈开发</span>
    <span class="revenue">💰 累计流水 5000万+</span>
  </div>
  <ul class="tech-list">
    <li><strong>《Survive 活下去》(2017-2020)</strong>：分布式 Node.js/Golang + Redis 高并发 IO 架构，支持全球同服与消息推送（年流水 500万+）</li>
    <li><strong>《三国诸侯纷争》(2019)</strong>：Unity3D + Java NIO / Protobuf 高并发 SLG 策略游戏（半年流水 200万+）</li>
    <li><strong>《沙巴克传奇》(2016)</strong>：Cocos2d-Lua + C++/Lua 服务端，PHP 支付与账户平台（半年流水 500万+）</li>
    <li><strong>支付中心 SDK 聚合平台 (2012)</strong>：架构设计与核心开发，支持 100+ 款游戏接入统一支付与广告接口</li>
    <li><strong>引擎与系统研发 (2010-2013)</strong>：Ejecta-X 跨平台 H5 引擎研发；TCL Android 手机系统核心模块开发</li>
  </ul>
</div>

</div>

<h2 class="section-title"><span class="icon">📚</span> 技术总结</h2>

<table class="tech-summary-table">
<thead>
<tr><th>领域</th><th>技术栈 & 架构范式</th></tr>
</thead>
<tbody>
<tr><td>高并发服务端框架</td><td>Java (Spring Boot / Spring Cloud) / ET框架 (C# / ECS) / Golang (Leaf / org框架 / Gin) / Node.js / Skynet</td></tr>
<tr><td>微服务 & SaaS 组件</td><td>Nacos / Spring Cloud Gateway / Feign / Sentinel / XXL-Job / 多租户 SaaS 隔离架构</td></tr>
<tr><td>分布式事务 & 消息队列</td><td>Seata (AT/TCC 模式) / RocketMQ / Kafka / RabbitMQ</td></tr>
<tr><td>Golang 高并发组件</td><td>自研分布式网关 / Worker Pool 协程池 / Redis 级联缓存 / 令牌桶漏桶限流组件</td></tr>
<tr><td>数据库 & 存储缓存</td><td>MySQL (多租户隔离/分库分表) / Redis (分布式锁/缓存级联) / MongoDB / Memcached</td></tr>
<tr><td>网络协议 & 实时通信</td><td>Protobuf / gRPC / Netty / WebSocket / HTTP / RPC</td></tr>
<tr><td>团队管理 & 项目管控</td><td>敏捷开发 (Scrum/Kanban) / WBS 任务拆解 / OKR/KPI / 里程碑交付与进度风险管控 / AI 赋能</td></tr>
<tr><td>客户端 & 全栈开发</td><td>Unity3D / Cocos2d-x / Cocos Creator / React.js / HTML5</td></tr>
<tr><td>DevOps & 工具链</td><td>Docker / Jenkins / Git / SVN / Redmine / Webpack</td></tr>
</tbody>
</table>

<br>
<br>
<br>

<div class="thanks-section">
  <h2 style="color: #1e3a5f; margin-bottom: 16px;">🙏 致谢</h2>
  <p>感谢您花时间阅读我的简历。</p>
  <p>15年+的技术积累与团队管理经验，让我具备了高并发服务端架构设计、微服务与分布式组件研发以及项目进度全流程管控的深厚能力。我热爱技术，享受解决高并发与复杂系统难题的过程，也乐于带领团队高效成长。</p>
  <p>期待能有机会与您共事，共同创造价值。</p>
  <div class="signature">— 王子亮</div>
</div>

<br>
<br>
