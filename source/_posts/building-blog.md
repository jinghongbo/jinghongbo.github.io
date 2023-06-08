---
title: 使用Hexo搭建个人博客并通过GitHub Pages和Cloudflare加速
date: 2023-06-08 16:17:11
tags:
---

## 简介
在本文中，我们将介绍如何使用Hexo框架搭建个人博客，并利用GitHub Pages进行静态页面托管，同时结合Cloudflare提供的CDN加速服务，提升博客的访问速度和稳定性。

## 步骤1：安装Node.js和Git
首先，确保你的计算机上安装了最新版本的Node.js和Git。你可以从官方网站下载并按照相应的安装指南进行安装。

## 步骤2：安装Hexo
在命令行中执行以下命令安装Hexo：

```shell
npm install -g hexo-cli
```

## 步骤3：初始化Hexo
选择一个适合你的文件夹作为博客项目的根目录，在命令行中进入该目录并执行以下命令：

```shell
hexo init myblog
cd myblog
npm install
```

以上命令将创建一个名为myblog的文件夹，并在其中初始化Hexo项目。

## 步骤4：配置Hexo
打开myblog文件夹中的`_config.yml`文件，根据你的需要进行以下配置：

```yaml
# Site
title: My Blog
subtitle: Welcome to my blog!
description: A simple and elegant blog powered by Hexo.
author: Your Name
language: en
timezone: # Your timezone
```

## 步骤5：创建新文章
在命令行中执行以下命令创建一篇新文章：

```shell
hexo new "Hello World"
```

这将在`source/_posts`目录下创建一个名为`hello-world.md`的Markdown文件，其中包含了文章的初始内容。

## 步骤6：编辑文章
使用你喜欢的文本编辑器打开`hello-world.md`文件，撰写你的博客内容。可以使用Markdown语法进行格式化。

## 步骤7：生成静态页面
在命令行中执行以下命令，生成静态页面：

```shell
hexo generate
```

执行完毕后，你将在`public`目录下看到生成的静态页面文件。

## 步骤8：配置GitHub Pages
首先，创建一个新的GitHub仓库，仓库名为`yourusername.github.io`（将`yourusername`替换为你的GitHub用户名）。确保仓库是公开的。

在Hexo项目根目录的`_config.yml`文件中，进行以下配置：

```yaml
deploy:
  type: git
  repo: git@github.com:yourusername/yourusername.github.io.git
  branch: master
```

将上述命令中的`yourusername`替换为你的GitHub用户名。

## 步骤9：部署到GitHub Pages
在命令行中执行以下命令，将生成的静态页面部署到GitHub Pages：

```shell
hexo deploy
```

## 步

骤10：配置Cloudflare CDN
创建一个Cloudflare账户，并添加你的域名到Cloudflare进行管理。在Cloudflare中，设置合适的DNS记录和SSL选项，以确保你的博客可以通过域名进行访问。

## 结论
恭喜你！现在你已经成功地搭建了个人博客并通过GitHub Pages和Cloudflare加速。你可以使用Hexo框架创建新的文章，然后使用`hexo generate`生成静态页面，并通过`hexo deploy`部署到GitHub Pages上。Cloudflare将为你提供CDN加速服务，提升你的博客访问速度和稳定性。

开始写作吧，与世界分享你的知识和见解吧！