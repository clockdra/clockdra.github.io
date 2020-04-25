---
title: Linux更新错误
mathjax: true
tags:
  - Linux
  - Ubuntu
  - apt
  - 错误
  - 错误记录
  - 问题
categories:
  - 错误记录
  - Linux
  - Ubuntu
preview: 300
summary_img: 'https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/nh-pluto-atmosphere-infrared.png'
date: 2020-03-25 13:44:22
---
![插图](https://apod.nasa.gov/apod/image/2003/S106_Mishra_960.jpg)


## 问题

最近我更新Ubuntu的时候一直出错.  每次执行完  `apt-get update` 之后还是正常的,但是执行 `apt-get upgrade` 的时候就会出错.  
错误的内容如下:  

```bash
E: 仓库 “http://ppa.***/ubuntu eoan Release” 没有 Release 文件。
N: 无法安全地用该源进行更新，所以默认禁用该源。
N: 参见 apt-secure(8) 手册以了解仓库创建和用户配置方面的细节。

```

或者这样  

```bash
错误:29 http://ppa.launchpad.net/morphis/anbox-support/ubuntu eoan Release     
404  Not Found [IP: 91.189.95.83 80]
正在读取软件包列表... 完成                                                     
E: 仓库 “http://ppa.launchpad.net/morphis/anbox-support/ubuntu eoan Release” 没有 Release 文件。
N: 无法安全地用该源进行更新，所以默认禁用该源。
N: 参见 apt-secure(8) 手册以了解仓库创建和用户配置方面的细节。
```









## 解决

一直出现这个问题,我反复使用了更新的命令也还是会因为这个错误而更新失败.  
最后我去网上Google了错误信息.发现问题是因为我安装了一些软件,安装软件的时候添加了一些源.但是添加的源后来失效了.所以每次更新的时候遇到失效的源就会中断.解决方法当然就是把失效的源删掉啦.  
先记住错误的源的名字,比如说   

```bash
E: 仓库 “https://download.sublimetext.com apt/stable/ Release” 没有 Release 文件。
N: 无法安全地用该源进行更新，所以默认禁用该源。
N: 参见 apt-secure(8) 手册以了解仓库创建和用户配置方面的细节。
```

如果错误信息是这样的话,那么错误的源就是 `sublimetext`  
打开终端输入: `cd /etc/apt/sources.list.d/`     
然后删除错误的源对应的文件(文件的名字中应该包含 `sublimetext` 这样的字样),注意别删错了.   
然后再执行 `apt-get update` 更新一下就可以了.




















</br>
</br>
</br>
</br>
</br>
</br>
封面图片来源 https://apod.nasa.gov/apod/image/2003/S106_Mishra_960.jpg
