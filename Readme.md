# Hexo 博客搭建指南

Hexo的简洁、神秘让我跃跃欲试，在使用过程中遇到了很多问题，整理此文，一是方便其他技术人搭建自己的博客，二是给自己的学习之旅做个总结。
我搭建的博客地址：[**limedroid.github.io**](https://limedroid.github.io)
## Hexo介绍

[Hexo](https://hexo.io/zh-cn/)是基于NodeJs的静态博客框架，简单、轻量，其生成的静态网页可以托管在Github和Heroku上。

* 超快速度
* 支持MarkDown
* 一键部署
* 丰富的插件

> 下面以我的博客为例，limedroid.github.io

## 环境准备

### 安装node.js

去[nodejs官网](https://nodejs.org/en/download/)下载对应系统的安装包，按提示安装。

检验安装成功：
```
$ node -v
```

### 安装hexo

```
$ npm install hexo-cli -g
```

注意：Mac系统，则需要  
```
$ sudo npm install hexo-cli -g
```

## 利用Hexo搭建一个博客

### 创建博客目录limedroid.github.io

```
$ hexo init limedroid.github.io
$ cd limedroid.github.io
$ npm install
```

### 生成静态页面

```
$ hexo clean
$ hexo g
```
> g 即generate

### 运行

```
$ hexo s
```

> s 即server

然后打开浏览器，输入地址 **localhost:4000** 即可看到效果

## 发一篇文章试试

### 命令方式

```
$ hexo new test
```

此时会在source/_posts目录下生成test.md文件，输入些许内容，然后保存.

生成下，看看效果

```
$ hexo clean
$ hexo g
$ hexo s
```

访问 **localhost:4000** 即可

### 直接方式

在 source/_posts/下新建一个.md文件也可

## 配置

网站的设置大部分都在_config.yml文件中，详细配置可以查看[官方文档](https://hexo.io/zh-cn/docs/configuration.html)

下面只列出简单常用配置

* **title** -> 网站标题
* **subtitle** -> 网站副标题
* **description** -> 网站描述
* **author** -> 您的名字
* **language** -> 网站使用的语言

坑：**进行配置时，需要在冒号:后加一个英文空格**

```
title: Droidlover
```

## 换一个好看的主题

Hexo 中有很多主题，可以在[官网](https://hexo.io/themes/)查看。
这里我推荐[hexo-theme-next](https://github.com/iissnan/hexo-theme-next)，下面列举更换主题的一般套路：

### 下载主题资源

```
$ cd theme/
$ git clone git clone https://github.com/iissnan/hexo-theme-next themes/next
```

### 应用下载的主题

在网站配置文件_config.yml中，配置theme

```
theme: next
```

> next是主题名称，具体的可查看主题的文档

### 主题其他配置

可在/theme/{theme}/_config.yml 主题的配置文件下进行主题的配置。

接下来，可以执行万能的调试命令看看效果

```
$ hexo clean
$ hexo g
$ hexo s
```

## 部署到Github

### 有个github账号xxx

### 创建一个xxx.github.io的public仓库
如果您的账户名是limedroid,则需要创建一个limedroid.github.io的public仓库.

### 安装 [hexo-deployer-git](https://github.com/hexojs/hexo-deployer-git)

```
$ npm install hexo-deployer-git --save
```

### 网站配置git
在网站的_config.yml中配置deploy

```
deploy:
  type: git
  repo: <repository url>
  branch: [branch]
```

> branch为分支，默认为master,可以不配置
> repo为仓库地址，在github上新建仓库后，可复制此地址

### 部署

```
$ hexo d
```

> d 即deploy


## 贴标签，方便搜索

## 分类，给文章归档

## 添加评论功能

## 加介绍页面，让全世界认识你










