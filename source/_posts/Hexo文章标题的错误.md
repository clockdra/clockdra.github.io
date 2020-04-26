---
title: Hexo文章标题的错误
mathjax: true
tags:
  - 错误
  - 错误记录
  - Hexo
categories:
  - 错误记录
  - Hexo
preview: 300
summary_img: 'https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/nh-pluto-atmosphere-infrared.png'
date: 2020-03-27 14:11:44
---
![插图](https://www.nasa.gov/sites/default/files/styles/full_width_feature/public/thumbnails/image/nh-pluto-atmosphere-infrared.png)


## 问题

我写了一篇新博客 [Linux更新错误](https://clockdra.github.io/2020/03/26/Linux%E6%9B%B4%E6%96%B0%E9%94%99%E8%AF%AF/) 。但是自己在创建博客的时候打的标题不是这个，在写完了之后自己打算改一个标题。于是我修改了新博客的文章对应的文件的名字。但是在自己重新生成提交博客之后发现文章还是不对，文章的标题还是之前的错误标题。  

```bash 自己使用的命令记录
hexo new "Linux的更新问题"  #这里是在创建新文章
hexo g                     #这里是生成新博客
hexo d                     #这里是提交文章
mv source/_posts/Linux的更新问题.md source/_posts/Linux更新错误.md  #重命名
hexo g                     #生成
hexo d                     #提交
```












## 解决

`Hexo` 的博客文章标题不是由文件名决定的，而是由文章的 `title` 标签决定的。所以应该修改完文件的名字之后再修改文件的 `title` 标签元素。  
之后再运行一下  

```bash
hexo clean                 #清除之前的错误文件
hexo g                     #生成
hexo d                     #提交
```




















</br>
</br>
</br>
</br>
</br>
</br>
封面图片来源 https://apod.nasa.gov/apod/image/2003/SaturnMoon_Sojuel_960.jpg
