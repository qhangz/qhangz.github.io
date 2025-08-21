---
title: Hello Hexo
date: 2025-08-20 21:08:49
tags: 
- hexo
categories: 
- hexo
cover: https://hexo.io/icon/favicon-196x196.png
---
### 关于Hexo的一些基本操作
>创建标签页：hexo new page ***
>创建文章：hexo new post ***

### Butterfly主题
>可查看https://butterfly.js.org/

### 关于submodule
什么是submodule
>有种情况我们经常会遇到：某个工作中的项目需要包含并使用另一个项目。 也许是第三方库，或者你独立开发的，用于多个父项目的库。 现在问题来了：你想要把它们当做两个独立的项目，同时又想在一个项目中使用另一个。
Git 通过子模块来解决这个问题。 子模块允许你将一个 Git 仓库作为另一个 Git 仓库的子目录。 它能让你将另一个仓库克隆到自己的项目中，同时还保持提交的独立。

添加子模块的格式如下：
>git submodule add   &lt;URL to submodule&gt;    &lt;local path&gt;
其中，&lt;URL to submodule&gt;是指子模块的远程仓库地址， &lt;local path&gt;是指子模块在本地的路径。

1、在你的 Hexo 博客根目录下执行以下命令，添加 Butterfly 主题的 Git 仓库为子模块：
```[git]
git submodule add https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
```
2、接着，在博客根目录下会出现一个名为 .gitmodules 的文件，打开该文件，将以下内容粘贴进去：
```[git]
[submodule "themes/butterfly"]
	path = themes/butterfly
	url = https://github.com/jerryc127/hexo-theme-butterfly.git
```
