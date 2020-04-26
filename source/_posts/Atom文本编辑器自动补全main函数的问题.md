---
title: Atom文本编辑器自动补全main函数的问题
mathjax: true
tags:
  - 错误
  - 错误记录
  - Atom
  - C语言
  - C++
  - main
categories:
  - 错误记录
  - 程序语言
preview: 300
summary_img: 'https://www.nasa.gov/sites/default/files/styles/image_card_4x3_ratio/public/thumbnails/image/pluto_color_mapmosaic.jpg'
date: 2020-04-05 10:32:00
---
![插图](https://www.nasa.gov/sites/default/files/styles/full_width_feature/public/thumbnails/image/pluto_color_mapmosaic.jpg)


## 问题

`Atom` 文本编辑器一直是我最爱的文本编辑器。Atom上面开源的扩展很多，很适合用来写各种程序代码。而且语法高亮和代码补全功能体验也非常好。所以一直以来我都是用 Atom 写各种程序、记笔记、制作网页的。但是我遇到一个很麻烦的地方，我在写 `C语言` 和 `C++` 程序的主函数的时候 Atom 的代码补全都是这样的


```cpp
int main(int argc, char const *argv[]) {
  /* code */
  return 0;
}
```


每次输入 `main` 敲回车之后就会出现这个。不仅要我去删除 `main` 里面的参数，还要把 `int` 改成 `void` ，删去 `return 0;` 这些内容。









## 解决

解决这个问题其实要讲到一个很常见的错误。
在很多教程上面 `C语言` 和 `C++` 的主函数都是 `void` 型函数。但是，这种写法是错误的。无论是 `C语言` 还是 `C++` 主函数都是 `int` 型函数，并且返回值为0。当你把主函数写成 `void` 型函数时，现在的编译器都会在程序中加入一句 `return 0;` 。所以之所以你的错误写法可以正常编译，这是因为编译器的处理。但是不是所有的编译器都可以处理这些错误的写法。如果，你用特别古老的编译器时就有可能遇到不能正确编译的情况。所以建议大家使用标准的写法。





## 总结

关于为什么标准的 `C语言` 主函数是下面这种格式的原因很多人可能不能很好的理解。其实如果你经常用Linux系统的话就可以比较容易理解了。
在Linux系统的操作中，大多数时候是使用命令。而命令的格式通常是 `程序名 操作参数` 。这里程序后面接的操作参数就是传递给 `main` 函数的参数。所以 `main` 函数是可以有参数的，参数来自操作系统。第一个参数传递给了 `argc` ，也就是了命令的第一个词，后面的参数传递给了 `argv` 字符串。而在Linux系统中每次正常执行完程序之后，程序就会给操作系统返回一个值，这个值为0。通过在执行完程序之后输入 `echo $` 可以查看。如果程序正常执行并退出，输入 `echo $` 会得到 `0` 。这就是为什么 `main` 函数有返回值，而且返回值为 `0` 的原因。

```c
int main(int argc, char const *argv[]) {
  /* code */
  return 0;
}
```













</br>
</br>
</br>
</br>
</br>
</br>
封面图片来源 https://apod.nasa.gov/apod/image/2003/SaturnMoon_Sojuel_960.jpg
