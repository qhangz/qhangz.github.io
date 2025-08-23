---
title: 添加看板娘
date: 2025-08-21 18:47:14
tags: 
- hexo
- 看板娘
categories: 
- beautify
cover: ../imgs/posts/poster-girl/cover.png
top_img: false
---
为站点加入可爱的看板娘。

## 使用

{% tabs 主题, 1 %}

<!-- tab 通用 -->

将以下 `.css` 与 `.js` 文件链接插入到你的网页中即可调加入可爱的 Live2D 看板娘了！

```html
<link rel="stylesheet" href="https://registry.npmmirror.com/weblive2d/latest/files/waifu.css">
<script async src="https://registry.npmmirror.com/weblive2d/latest/files/js/autoload.js"></script>
```

<!-- endtab -->

<!-- tab NexT -->

进入 `NexT` 主题的配置文件 `_config.next.yml`，释放 `head` 的注释以启动自定义文件配置项

```yaml
# Define custom file paths.
# Create your custom files in site directory `source/_data` and uncomment needed files below.
custom_file_path:
  #head: source/_data/head.njk
  #header: source/_data/header.njk
  #sidebar: source/_data/sidebar.njk
  #postMeta: source/_data/post-meta.njk
  #postBodyStart: source/_data/post-body-start.njk
  #postBodyEnd: source/_data/post-body-end.njk
  #footer: source/_data/footer.njk
  #bodyEnd: source/_data/body-end.njk
  #variable: source/_data/variables.styl
  #mixin: source/_data/mixins.styl
  #style: source/_data/styles.styl
  head: source/_data/head.njk
```

新建文件 `siteroot/source/_data/head.njk`

进入 `siteroot/source/_data/head.njk` 文件内，将以下代码粘贴进去

```html
<link rel="stylesheet" href="https://registry.npmmirror.com/weblive2d/latest/files/waifu.css">
<script async src="https://registry.npmmirror.com/weblive2d/latest/files/js/autoload.js"></script>
```

执行 `Hexo` 二连即可查看效果！

```sh
hexo cl; hexo s
```

<!-- endtab -->

<!-- tab Butterfly -->

进入 `Butterfly` 主题的配置文件 `_config.butterfly.yml`，搜索 `Insert the code to head` 然后参照以下配置更改自己的配置项即可

```yaml
# Inject
# Insert the code to head (before '</head>' tag) and the bottom (before '</body>' tag)
# 插入代码到头部 </head> 之前 和 底部 </body> 之前
inject:
  head:
    # - <link rel="stylesheet" href="/xxx.css">
    - <link rel="stylesheet" href="https://registry.npmmirror.com/weblive2d/latest/files/waifu.css">

  bottom:
    # - <script src="xxxx"></script>
    - <script async src="https://registry.npmmirror.com/weblive2d/latest/files/js/autoload.js"></script>
```

执行 `Hexo` 二连即可查看效果！

```sh
hexo cl; hexo s
```

<!-- endtab -->

{% endtabs %}

## 源码

本文章所用到的 `CDN` 服务其源码来源于此处..

> GitHub：[nova1751/live2d-api](https://github.com/nova1751/live2d-api)