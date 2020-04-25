---
title: Hexo搭建时遇到的坑(1)
mathjax: true
tags:
  - 问题
  - 错误记录
  - 错误
  - Hexo
categories:
  - 错误记录
  - Hexo
preview: 300
summary_img: 'https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/20190301_as09-21-3206.jpg'
date: 2020-03-19 21:49:48
---
![插图](https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/esgs8xfwsaippf-.jpg)

## 问题

设置好了主题、安装好了博客。但是在浏览的时候发现 `日志` 这个内容无法打开。  

#### 环境

使用的 `Node.js` 版本为 v10.16.1  
使用的 `Hexo` 版本为

```bash      
hexo-cli: 3.1.0
os: Windows_NT 10.0.18362 win32 x64
http_parser: 2.8.0
node: 10.16.1
v8: 6.8.275.32-node.54
uv: 1.28.0
zlib: 1.2.11
brotli: 1.0.7
ares: 1.15.0
modules: 64
nghttp2: 1.34.0
napi: 4
openssl: 1.1.1c
icu: 64.2
unicode: 12.1
cldr: 35.1
tz: 2019a


```

`Hexo` 安装的主题 `NexT` ， `NexT` 的版本 v6.0.0

#### 发现问题的经过

设置好了博客网站，预览的时候打算把每一个部分都测试一下看有没有问题。我点击主页的首页图标的时候，浏览器跳转到了 `locallhost:4000/home/%20home` 。我点击了日志这个图标之后，浏览器跳转到了 `locallhost:4000/archives/%20archives` 。而这些URL都没有对应的页面。

## 解决

我一开始对此毫无头绪。毕竟自己完全不懂前端，也不会网站的运营。
不过在使用了一段时间，看了很多博客的教程之后还是勉强学会了一点点。我分析后发现， 博客网站主页上面的这些图标全是来自于 `NexT` 的配置文件。 文件路径应该是 `blog/themes/next/_config.yml` 。而且这些主页图标的配置都是在 `menu` 这一部分。  
我的 `NexT` 的配置文件设置如下

```yml
menu:
  home: / || home
  about: /about/ || user
  tags: /tags/ || tags
  categories: /categories/ || th
  archives: /archives/ || archive
#  schedule: /schedule/ || calendar
#  sitemap: /sitemap.xml/ || sitemap
  #commonweal: /404/ || heartbeat

# Enable/Disable menu icons.
menu_icons:
  enable: true
  home: home
  about: user
  categories: th
  tags: tags
  archives: archive
  #commonweal: heartbeat


```

很明显的一点是，点击主页的图标的时候都会跳转到不存在的页面。而且 跳转后的URL中都是一样的包含 `%20` 。URL中的 `%20` 表示空格的意思。我去看了 NexT 的官方文档([文档](https://theme-next.iissnan.com/))。官方说我的配置文件应该将 `menu` 的后面部分注释掉。将上面的内容改为下面这样  

```yml
menu:
  home: / #|| home
  about: /about/ #|| user
  tags: /tags/ #|| tags
  categories: /categories/ #|| th
  archives: /archives/ #|| archive
#  schedule: /schedule/ || calendar
#  sitemap: /sitemap.xml/ || sitemap
  #commonweal: /404/ || heartbeat

```

这样注释掉了后面的内容。但是我再预览的时候发现，虽然可以跳转到正确的页面了可是对应的图标没有了。 NexT 的官方文档介绍，没有图标是因为我使用了未定义的内容。但是我这个明明是根据官方改的啊(lll￢ω￢)  突然发现官方文档靠不住啊。  
看了很久之后我认为可能是因为配置文件中的内容改错了。因为下面的 `menu_icons` 应该对应上面的 `|| home` 这些内容。所以这里是不应该注释掉的。于是我就随便试了一下，把中间的注释去掉并且去掉空格。如下  

```yml
menu:
  home: /|| home
  about: /about/|| user
  tags: /tags/ #|| tags
  categories: /categories/|| th
  archives: /archives/|| archive
#  schedule: /schedule/ || calendar
#  sitemap: /sitemap.xml/ || sitemap
  #commonweal: /404/ || heartbeat

```

这样修改之后 `home` `about` `tags` `categories` 都正常了。既有图标也可以正常跳转到正确的页面。但是 `archives` 却还是存在问题。在网站上面既有一个 `日志` 也有一个 `归档` 的图标。其中点击 `规档` 是可以正常跳转到正确页面的。但是点击 `日志` 就还是存在跳转到 `locallhost:4000/archives/%20archives` 的情况。这里之所以有两个图标指向同一个内容，是因为主题的配置文件和博客的配置文件重复了。于是我决定改掉一个，将主题配置文件里面的 `archives` 注释掉。如下  

```yml
menu:
  home: /|| home
  about: /about/|| user
  tags: /tags/ #|| tags
  categories: /categories/|| th
#  archives: /archives/|| archive
#  schedule: /schedule/ || calendar
#  sitemap: /sitemap.xml/ || sitemap
  #commonweal: /404/ || heartbeat

```

这样就基本解决了问题。


















<br><br><br><br><br><br>
封面来自 https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/20190301_as09-21-3206.jpg
