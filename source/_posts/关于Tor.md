---
title: 关于Tor
mathjax: true
tags:
  - Tor
  - 暗网
  - 隐私
  - 网络安全
categories:
  - 闲谈
preview: 300
summary_img: 'https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/shl_5284.jpg'
date: 2020-04-05 10:34:53
---
![插图](https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/s70-31774_orig.jpg)

`Tor` 网络是一组志愿者操作的服务器，允许人们在连接到互联网时增强个人隐私和安全性。
这里是维基百科上的介绍 https://zh.wikipedia.org/zh/Tor
简单一点的说这是一个可以让你隐藏IP地址的一个工具，利用 `Tor` 你可以隐藏自己的行踪。让别人不知道你访问过什么网站。当然， `Tor` 代理在中国有时候被用来突破中国政府的网络审查。不过我认为用 `Tor` 来突破网络审查似乎并不是很有效。
关于 `Tor` 网上有很多介绍了，在中国地区的建议就是先使用前置的 `VPN` 或者 `Shandowsocks` 等代理然后使用 `Tor` 代理。
这里要说的是，现在网上出现了很多人对 `Tor` 不了解。导致了有两种错误的观点。

1. `Tor` 网络不能保护隐私。个人无法对抗政府和企业的网络监控。没有人能够保护自己的隐私。
2. `Tor` 网络非常安全。可以肆无忌惮的使用 `Tor` 。

这两者都有各自的偏激的地方。
先来慢慢讲解一下吧。
这两种偏激的观点，其实都是有害的。而且都是源于大家的无知。

### 先讲一下第一种观点的错误。

关于无法保护网络隐私的这种观点，其实是政府这些组织刻意操作的结果。他们的目的之一是创造出这种假象，进而让普通人放弃抵抗他们对个人权利的侵害。
很多时候政府刻意营造出他们不可战胜的这种表现让普通民众不敢反抗。在网络上也是如此。比如说，经常在中国的网络(包括墙外的网站)上流传一些政府要对发布不利言论的人进行信息收集进而迫害这些人的信息。但是这种信息很明显是假的，因为中国政府一直都在攻击、拘捕、陷害、迫害异见人士。根本不会发布这种信息出来，让你先知道要开始进行信息收集。那么这种信息有什么意义呢？大概有两种意义

1. 这样可以让一些普通人害怕而噤声。
2. 这样做可以让大家误以为中国政府很全能。

但是事实上，政府也有自己的弱点。或者说世间万物都有自己的弱点。比如说中国政府，他们内部的腐败、权力的不均衡、领导者的自大都是他们的弱点。只要利用好敌我之间的强弱关系，小也可博大。在网络方面也是如此。网络是尊从与算法的，而不是服从于权力的。只要充分利用好技术，就可以让普通人也能对抗可怕的政府审查。比如使用加密技术加密文档，使用 `Tor` 隐藏网络踪迹，使用 `Tox.chat` 匿名聊天，使用 `ZeroNet` 匿名建设网站，使用 `Solid` 创建服务。
很多人认为 `Tor` 是不安全的，原因在于有很多人使用了 `Tor` 但是仍然被发现了。
其实，被发现的 `Tor` 用户通常没有做好自己的防护。从一些其它方面暴露了自己。比如偶尔的聊天中透露了自己的信息，暴露了自己的身份。或者是自己的电脑中了木马。自己访问的网站泄露了自己的电子邮箱。这些情况并不能算是 `Tor` 本身有问题。当然在Wikipedia上面也介绍了很多针对 `Tor` 的攻击，不过主要都是针对浏览器的漏洞进行的。而 `Tor` 网络本身则几乎无懈可击。
几个利用 `Tor` 网络保护自己隐私的著名例子包括 [Edward Joseph Snowden](https://zh.wikipedia.org/zh/%E7%88%B1%E5%BE%B7%E5%8D%8E%C2%B7%E6%96%AF%E8%AF%BA%E7%99%BB)、[编程随想](https://program-think.blogspot.com/2019/01/Security-Guide-for-Political-Activists.html)等。

### 第二种观点的错误

有人因为暗网等方面的消息，误以为使用了 `Tor` 就可以了但是却忘记了其它的安全注意事项。比如说在 `Tor` 网络中泄露了自己的身份，登录了某个网站的账号，浏览器上有漏洞，电脑中了病毒等等。
总之， `Tor` 并不是什么超级道具可以让你绝对安全。必须要小心使用才能保护好自己。如果你要做一个需要匿名的事情，那么 `Tor` 一定是你必备的工具。如果你打算使用 `Tor` 去做需要匿名的事情，则一定要非常小心。
使用 `Tor` 的注意事项

- https://tb-manual.torproject.org/zh-CN/security-settings/
- https://tb-manual.torproject.org/security-settings/
- https://steemit.com/crypto/@iyouport/tor


还有一点就是，很多人以为 `Tor` 就是 `暗网` 。但是这是两个概念， `暗网` 指的是使用了 `Tor` 技术以达到匿名的网站。 `Tor` 是一种实现匿名技术手段， `暗网` 则是使用了匿名手段的网站。还有很多人以为 `暗网` 就是违法网站。这也是一个明显错误的观念，毕竟 `暗网` 只是匿名的网站而已这与是否违法并没有关系。

<br>
<br><br>
<br>







相关资料：
- https://www.bilibili.com/bangumi/play/ss20849/
- https://www.iyouport.org/%e5%a6%82%e4%bd%95%e5%9c%a8android%e4%b8%8a%e8%ae%be%e7%bd%ae%e5%92%8c%e4%bd%bf%e7%94%a8tor/
- https://www.iyouport.org/%e6%96%b0%e7%89%88-onionshare-%e4%bd%bf%e4%bb%bb%e4%bd%95%e4%ba%ba%e9%83%bd%e5%8f%af%e4%bb%a5%e8%bd%bb%e6%9d%be%e5%8f%91%e5%b8%83%e5%8c%bf%e5%90%8d%e7%9a%84%e3%80%81%e6%97%a0%e6%b3%95%e5%ae%a1/
- https://www.iyouport.org/%e5%a2%9e%e5%bc%ba%e5%8c%bf%e5%90%8d%e6%80%a7%e7%9a%84%e7%ae%80%e5%8d%95%e6%96%b9%e6%b3%95/
- https://www.iyouport.org/%e5%a6%82%e4%bd%95%e6%89%be%e5%88%b0%e5%9c%a8-cloudflare-%e6%88%96-tor-%e8%83%8c%e5%90%8e%e9%9a%90%e8%97%8f%e7%9a%84%e7%9c%9f%e5%ae%9e%e6%ba%90-ip%ef%bc%9f/
- https://www.iyouport.org/%e7%bb%a7%e7%bb%ad%e6%9d%80%e6%ad%bb%e9%80%8f%e6%98%8e%e5%ba%a6%e9%9d%a9%e5%91%bd-%e5%bd%93%e5%b1%80%e5%a6%82%e4%bd%95%e5%be%97%e7%9f%a5tor%e4%bd%bf%e7%94%a8%e8%80%85%e7%9a%84/
- https://www.iyouport.org/%e5%a6%82%e4%bd%95%e5%9c%a8%e4%bd%a0%e7%9a%84%e7%bd%91%e9%a1%b5%e6%b5%8f%e8%a7%88%e5%99%a8%e4%b8%ad%e4%bd%bf%e7%94%a8tor%e7%bd%91%e7%bb%9c%ef%bc%9f/
- https://www.iyouport.org/%e6%98%af%e6%97%b6%e5%80%99%e5%93%81%e5%b0%9d%e6%b4%8b%e8%91%b1%e4%ba%86/
- https://www.iyouport.org/%e5%8f%af%e6%80%9c%e6%ad%a3%e4%b9%89%e6%b2%a1%e6%9c%89%e9%92%b1/
- https://www.iyouport.org/%e7%b3%bb%e7%bb%9f%e8%a2%ab%e6%94%bb%e5%87%bb%e3%80%81%e7%94%a8-tor-%e8%a2%ab%e9%92%93%e9%b1%bc%e3%80%81%e5%a5%bd%e5%a5%87%e5%ae%b3%e6%ad%bb%e7%8c%ab%ef%bc%8c%e6%80%8e%e4%b9%88%e5%8a%9e%ef%bc%9f/
- https://www.iyouport.org/%e5%a6%88%e5%a6%88%e8%af%b4%ef%bc%8c%e6%93%8d%e4%bd%9c%e5%ae%89%e5%85%a8%e6%b0%b8%e8%bf%9c%e4%b8%8d%e8%83%bd%e8%a2%ab%e5%bf%bd%e8%a7%86%e2%80%8a-%e2%80%8a%e5%8c%bf%e5%90%8d%e5%b7%a5%e5%85%b7%ef%bc%9a/
- https://www.iyouport.org/cia%e5%89%8d%e9%9b%87%e5%91%98%e8%a2%ab%e6%80%80%e7%96%91%e6%b3%84%e5%af%86%ef%bc%8c%e5%94%af%e4%b8%80%e8%af%81%e6%8d%ae%e6%98%af%e4%bb%96%e4%bd%bf%e7%94%a8%e4%ba%86tor%e6%b5%8f/
- https://www.iyouport.org/%e4%bd%bf%e7%94%a8-tor-%e4%bf%9d%e6%8a%a4%e8%87%aa%e5%b7%b1%e6%97%b6%e5%8d%83%e4%b8%87%e4%b8%8d%e8%a6%81%e5%81%9a%e8%bf%99%e4%b9%9d%e4%bb%b6%e4%ba%8b%ef%bc%81/
- https://www.iyouport.org/%e8%af%b7%e5%85%b3%e4%b8%8a%e8%ba%ab%e5%90%8e%e7%9a%84%e9%97%a8%ef%bc%8c%e9%99%a4%e9%9d%9e%e4%bd%a0%e6%83%b3%e6%8a%8a%e5%88%80%e9%80%92%e7%bb%99%e6%95%8c%e4%ba%ba-%e6%b4%8b%e8%91%b1/
- https://www.iyouport.org/%e7%9c%9f%e7%9a%84%e5%ae%89%e5%85%a8%e5%90%97%ef%bc%9f%e9%82%a3%e4%b9%88%e4%bb%96%e4%bb%ac%e6%98%af%e6%80%8e%e4%b9%88%e6%8a%93%e4%ba%ba%e7%9a%84%ef%bc%9f-%e6%b4%8b%e8%91%b1%e5%a4%b4/
- https://matters.news/@Luterngun/%E6%88%96%E8%AE%B8-telegram-%E6%98%AF%E6%9C%80%E4%B8%8D%E5%9D%8F%E7%9A%84%E9%80%89%E6%8B%A9-zdpuAqSCzLTLgisSHVv6QtyFAysE8j1rCrMj1HEc8hWTUiyAd
- https://matters.news/@Luterngun/%E6%95%B0%E5%AD%97%E6%9E%81%E6%9D%83%E7%9A%84%E9%93%81%E5%B9%95%E4%B8%8B-%E6%88%91%E4%BB%AC%E5%B7%B2%E9%80%80%E6%97%A0%E5%8F%AF%E9%80%80-zdpuB2rVyKBpoHLuxJCWh9BxeqmAas2XqjryFasdS2JhUQdg6
- https://www.iyouport.org/%E9%A6%99%E6%B8%AF%EF%BC%9A%E5%B9%B4%E8%BD%BB%E7%9A%84%E6%8A%97%E8%AE%AE%E8%80%85%E6%93%85%E9%95%BF%E6%8A%B5%E5%BE%A1%E6%95%B0%E5%AD%97%E7%9B%91%E6%8E%A7%EF%BC%88%E9%99%84%E5%AE%89%E5%85%A8%E9%A1%BB/
- https://www.iyouport.org/%e5%bd%93%e6%90%ac%e7%9f%b3%e5%a4%b4%e7%a0%b8%e8%84%9a%e9%81%87%e5%88%b0%e8%bf%90%e5%8a%a8%e6%ad%bb%e4%ba%a1-%e6%b4%8b%e8%91%b1%e5%a4%b4%e4%bc%9a%e8%ae%a9%e8%b0%81/



<br><br><br><br><br><br>
封面来自 https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/shl_5284.jpg
