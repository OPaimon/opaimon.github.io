---
title: 使用Astro来构建自己的博客
# Title of the post
description: "本着对折腾的喜爱，以及希望有一个地方记录自己的学习生活，外带对之前用Vuepress构建博客却连文件结构都没搞明白的不满，尝试用Astro来构建自己的博客"
# Description of the post.
pubDatetime: 2023-09-29T01:00:05+08:00
# Published datetime in ISO 8601 format.
#author: ""
# default = SITE.author
postSlug: "how-to-take-blog-by-astro"
# Slug for the post. Will automatically be slugified.
# default = slugified title
featured: true
draft: false
tags:
  - post
---

### 为什么要建立这么一个博客呢

老实说，建立一个博客的原动力大概是在一些奇怪的文章里看见的「输出倒逼输入」之类的观点。希望能够通过这么一个方式来倒逼自己能够更好的学习之类的想法。

其次则在于一直以来折腾过程中查资料会看到的各种个人博客，自我开始接触这些个人博客时，便想着也要有一个自己的小网站，姑且算作完成过去自己的小小愿望吧。

最后便也是因为自己一直以来一直喜欢折腾各种事的缘故(VPS，域名等该有的都有了，为什么不做一个博客呢?

### 曾今做过的尝试

其实之前便已经使用 VuePress+hope 主题做过一个博客(还在上面分享了在洛谷上做的题，但是老实说，当时其实根本什么都没做，仅仅只是用预设好的模板，除此之外便什么也没做了，因此对此也觉得不太满意(

于此同时，近日我不知从哪得知了 Astro 这么一个可以称的上「新」的东西，恰巧，通过阅读文档我们发现其非常适合做内容网站!(当然也包括个人博客！甚至文档里给出的教程也是教我们如何搭建一个博客！)

那么，用这么一个新的东西来重新制作我们的博客便成了一个自然而然的主意了！

### 让我们开始吧！

现在，打开我们的电脑，安装好`pnpm` `git` `code-OSS`等工具，开始我们的探索旅程吧！旅途中的每一步都将被我记录在这篇博文里~

```shell
$> paru -S pnpm git code
$> echo "Adventure Start!"
```

## Table of contents

## 在本地构建自己的博客

### 建立自己的项目！

参照[ Astro 的文档](https://docs.astro.build/zh-cn/)我们可以用 `pnpm create astro@latest` 来创建一个本地的 Astro 项目

```sh
$> pnpm create astro@latest
```

当然你也可以用社区的主题模板作为开始来建立自己的项目，例如`npm create astro@latest -- --template satnaing/astro-paper`来用 Astro Paper 主题来建立一个项目

```sh
$> npm create astro@latest -- --template satnaing/astro-paper
```

接下来的步骤引用一下[文档](https://docs.astro.build/zh-cn/tutorial/1-setup/2/)中的步骤

> 确认后安装 create-astro

> 当提示 Where would you like to create your new project?（你想要在哪里创建你的新项目？）时输入文件夹的名称来为你的项目创建一个新目录，例如: ./tutorial

> 你将看到一个简短的入门模板列表可供选择。使用方向键（上和下）导航至模板，然后按回车键（回车）选择对应模板。

> 当提示询问 Would you like to install dependencies?（你想现在安装依赖吗？）时输入 y（现在安装）。

> 当提示询问你是否打算编写 TypeScript 时，输入 n（不打算）。

> 当提示询问 Would you like to initialize a new git repository?（你想要初始化一个新的 Git 仓库吗？）时输入 y（要初始化）。

当然，是否启用TypeScript还是要取决于你用的模板，同时记住**新的Astro项目只能在空文件夹建立**

关于 Astro 项目的具体结构，本文不多做赘述，建议大家还是可以多多参照[文档](https://docs.astro.build/zh-cn/core-concepts/project-structure/)来做理解。

而我自己对于 Astro 的一些理解(目前还不存在的东西，将会在后续的章节中进行讲述。

也推荐大家先跟着文档中给的[Tutorial](https://docs.astro.build/zh-cn/tutorial/0-introduction/)先过一遍，这样对于 Astro 的一些基本理念也能有所了解

在建立完自己的项目以后，来到项目文件夹，运行:

```sh
$> pnpm run dev
```

即可启动本地的开发服务器！

此时你在本地做出的任何修改都会如实的反应到 [localhost:4321](localhost:4321) 里(如果你没改一些奇怪的东西的话
