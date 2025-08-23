---
title: Linux上安装微信
date: 2025-08-23 22:00:36
tags: 
- ubuntu
- WeChat
categories: 
- linux
cover: https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdzh4eGJiNGFmbDNwMWw0N3V3emJiMm5qeGZnZDd3dmdlM2c0bGMwNiZlcD12MV9naWZzX3NlYXJjaCZjdD1n/3og0ICG4WxdKSRzE3K/giphy.gif
top_img: false
---
# Ubuntu上安装微信

原先需要下载安装Wine环境包和微信包，以此实现在linux上使用微信。不过目前腾讯推出了linux下官方版的微信，使用下来与windows版本相差不大，也有朋友圈等功能。

## 下载

打开官网<https://weixin.qq.com/，选择linux版本。>

![wechat官网](/imgs/posts/ubuntu-wechat/1.webp)

根据自己处理器架构选择对于格式版本。

![微信Linux版](/imgs/posts/ubuntu-wechat/2.webp)

下载完成后得到下述文件。

![压缩包](/imgs/posts/ubuntu-wechat/3.webp)

## 安装

可以通过软件安装程序进行安装
![软件安装程序](/imgs/posts/ubuntu-wechat/4.webp)
或者在终端中输入下述命令进行安装。

```sh
sudo dpkg -i WeChatLinux_x86_64.deb
```

## 使用

安装好后在应用程序中会出现微信的图标，正常使用即可。若想要在桌面添加快捷图标，可参考：http://localhost:4000/2025/08/23/ubuntu-desktop-icon/

## 总结

微信终于推出了Linux原生版本，整体使用体验相比之前的wine版本有了很大的提升！虽然目前还存在一些小问题，但相信开发团队在后续版本迭代中会逐步优化完善。总之，终于可以告别wine版本的各种兼容性问题了，强烈推荐日常需要使用微信的小伙伴们安装体验！

