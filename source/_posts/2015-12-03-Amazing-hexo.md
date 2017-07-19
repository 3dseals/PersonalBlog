title: Amazing hexo
date: 2015-12-03 14:57:41
tags: hexo github nodjs 
categories: hexo
---

## Foreword

I have been looking for such a blog, strong self-confidence like WordPress.
And Spending dollars to buy the domain name and server space is prerequisite.
I never thought that a free and almost unlimited freedom blog exist.
Hexo just like this. A fast, simple & powerful blog. I did not hesitate to try it.
So far so amazing.

## Quick Start

### First
Let's introduce how to set up hexo.
Please Download nodejs from http://nodejs.org.
I get [node-v4.2.2-x64.msi](https://nodejs.org/dist/v4.2.2/node-v4.2.2-x64.msi). 
then double click to install nodejs.
Keep the default configuration to direct the installation.

``` bash
$ npm install -g hexo-cli
```

### Setup your blog.
make a name in the computer called "YOU NAME" folder (for example, I make dir in  D:\workspace\OSGDreamWorks\ibunnyteam.github.io).
then open this folder, run the following command.

``` bash
$ hexo init
[info] Copying data
[info] You are almost done! Don't forget to run `npm install` before you start b
logging with Hexo!
```

Hexo will automatically create a file in the target folder that website require. 
Then follow the prompts to run npm install (in "YOU NAME" folder).

``` bash
$ npm install
```

then you can get the node_modules.
All work will be done automatically by nodejs.

### Start the server

Run the following command (in "YOU NAME" folder).

``` bash
$ hexo server
[info] Hexo is running at http://localhost:4000/. Press Ctrl+C to stop.
```

Then you can open the local blog. easy, all right!

### Create a new post

Open a new command-line window, execute the following command

``` bash
$ hexo new "My New Post"
[info] File created at d:\Hexo\source\_posts\My-New-Post.md
```

Refresh http://localhost:4000/，you can see the "My New Post"。

### Generate static files

执行下面的命令，将markdown文件生成静态网页。

``` bash
$ hexo generate
```

After this command is executed, it will be generating a series of html, css and other documents in public directory.

## Upload the blog

Now you only have established a local blog.
How others see your blog.
You need github. Also amazing project.
your can know every thing in github.comhttps://github.com/

### continue

Deployed to the former Github need to configure _config.yml file, first locate the following content.

``` txt
# Deployment
## Docs: http://hexo.io/docs/deployment.html
deploy:
  type:
```

Changed to:

``` txt
# Deployment
## Docs: http://hexo.io/docs/deployment.html
deploy:
  type: git
  repository: git@github.com:ibunnyteam/ibunnyteam.github.io.git
  branch: master
```

##### NOTE1:

Repository: SSH form must be url (git@github.com: ibunnyteam / ibunnyteam.github.io.git), but can not be HTTPS form url (https://github.com/ibunnyteam/ibunnyteam.github.io. git), otherwise an error:
You need named the repository YOU_GITHUB_ACCOUNT.github.io then you can open the [github static web](https://ibunnyteam.github.io/ibunnyteam.github.io).
``` bash
$ hexo deploy
[info] Start deploying: github
```

Use SSH url, if the computer is not an open SSH port will cause the deployment to fail.

``` bash
[error] https://github.com/ibunnyteam/ibunnyteam.github.io is not a valid repositor URL!
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

##### NOTE2：

If you are making a project website, then you need to branch to gh-pages.

## Last

you can make a domain name with the [github static web](https://ibunnyteam.github.io/ibunnyteam.github.io).

The short command for hexo:

new blog
``` bash
$ hexo n
```
generate
``` bash
$ hexo g
```
upload
``` bash
$ hexo d
```

## Have fun

