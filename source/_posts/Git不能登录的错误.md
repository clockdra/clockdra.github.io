---
title: Git不能登录的错误
mathjax: true
tags:
  - 错误
  - 错误记录
  - GitHub
  - SSH
categories:
  - 错误记录
  - Git
preview: 300
summary_img: 'https://www.nasa.gov/sites/default/files/styles/side_image/public/thumbnails/image/sorce_pre.00002_print.jpg?itok=os-kx9mZ'
date: 2020-03-25 13:45:59
---
![插图](https://www.nasa.gov/sites/default/files/styles/ubernode_alt_horiz/public/thumbnails/image/jhelioviewer_march_5_flare_still_2.png)


## 问题

之前在弄 `Hexo` 博客的时候遇到了 `Git` 登录一直失败的问题.  
每一次自己使用 `Git Bash` 提交或者克隆的时候 `GitHub` 都会要求登录.比如在命令行输入 `git clone https://github.com/clockdra/clockdra.git` 之后会弹出登录的弹窗.但是我在输入了用户名和密码之后却提示下面这些信息  

```bash
fatal: unable to access 'https://github.com/clockdra/clockdra.github.io/': SSL certificate problem: self signed certificate in certificate chain
FATAL Something's wrong. Maybe you can find the solution here: https://hexo.io/docs/troubleshooting.html
Error: Spawn failed
    at ChildProcess.task.on.code (**\node_modules\hexo-util\lib\spawn.js:51:21)
    at ChildProcess.emit (events.js:198:13)
    at ChildProcess.cp.emit (**\node_modules\cross-spawn\lib\enoent.js:34:29)
    at Process.ChildProcess._handle.onexit (internal/child_process.js:248:12)
```

反复输入用户名和密码之后还是会这样。









## 解决

在查看了很久之后才知道，是因为自己的网站文件设置出错了。自己按照网上的教程设置了网站文件设置，但是网上的教程说 `_confid.yml` 里面的 `display` 应该设置成自己的GitHub仓库网址。于是我设置成了这样  

```yml 错误的文件
## 错误的设置
deploy:
  type: git
  repository: https://github.com/clockdra/clockdra.github.io
  branch: master
```

但是这是错误的设置。  
正确的设置应该是这样的  

```diff
## 正确的设置
deploy:
  type: git
-  repository: https://github.com/clockdra/clockdra.github.io
+  repository: git@github.com:clockdra/clockdra.github.io.git
  branch: master
```

然后在 Git 中输入如下命令配置一下 Git   

```bash
git config --golbal user.name "yourname" #yourname这里输入你的账号名字
git config --golbal user.email "youremail" #youremail这里输入你的邮箱的地址
```

接着生成 `SSH` 的密钥

```bash
ssh-keygen -t rsa -C "youremail@example.com" #这里输入你自己的电子邮箱
```

生成密钥的时候会有一些提示，可以不用管直接 `Enter` 就好。  
查看生成的公钥  

```bash
cat ~/.ssh/id_rsa.pub
```

复制公钥的内容，然后打开 GitHub ，进入 ` Setting -> SSH and GPG keys ` ，选择 ` New SSH key` 。给新的密钥取一个名字就好，然后把公钥粘贴进去就好。  
在 Git 里面输入下面的程序来测试一下  

```bash
ssh -T git@github.com
```

之后再在博客文件夹里面输入 ` hexo d ` ，提交就成功了。

## 总结

出现之前无法提交的问题，其实是我没有正确设置仓库相关的配置文件。还有就是现在 GitHub 的clone的选择有 Git 协议和 Http 协议两种。使用 Http 协议每次都要输入用户名和密码，所以还是建议大家使用 Git 协议。













</br>
</br>
</br>
</br>
</br>
</br>
封面图片来源 https://www.nasa.gov/sites/default/files/styles/side_image/public/thumbnails/image/sorce_pre.00002_print.jpg?itok=os-kx9mZ
