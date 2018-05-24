# [personal blog](https://ibunnyteam.github.io)

```hexo s```
####
hexo s是hexo server的缩写，命令效果一致；启动本地服务器，用于预览主题。

```hexo n```
####
hexo n是hexo new的缩写，命令效果一致。
如hexo n "标题"，是新建一篇标题文章，因为标题里有空格，所以加上了引号。

```hexo d```
####
hexo d是hexo deploy的缩写，命令效果一致。
动态博客中通过发布文章页面设置的各种属性，在hexo里要这样设置。
使用hexo d命令可以自动生成网站静态文件，并部署到设定的仓库。

```hexo clean```
####
hexo clean命令是用于清除缓存文件db.json和已生成的静态文件public。
网站显示异常时可以执行这条命令试试。

```hexo g```
####
hexo g是hexo generate的缩写，命令效果一致。
生成网站静态文件到默认设置的public文件夹。便于查看网站生成的静态文件或者手动部署网站；如果使用自动部署，不需要先执行该命令；

```hexo n page```
####
hexo n page aboutme
新建一个标题为aboutme的页面，默认链接地址为主页地址/aboutme/标题可以为中文，
但一般习惯用英文；页面标题和文章一样可以随意修改；
页面不会出现在首页文章列表和归档中，也不支持设置分类和标签。

###常用组合
``` hexo n title```
####
``` hexo c && hexo g && hexo d ```
