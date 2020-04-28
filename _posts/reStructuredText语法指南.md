---
layout: post
title: "reStructuredText语法指南"
author: "wts"
header-style: text
tags:
  - tutorial
---
> reStructuredText（可简写为RST、ReST或reST）是一种用于文本数据的文件格式，主要用于 Python 编程语言社区的技术文档。 它是Python Doc-SIG（Documentation Special Interest Group）的 Docutils 项目的一部分，旨在为 Python 创建一组类似于 Java 的 Javadoc 或 Perl 的 Plain Old Documentation（pod）的工具。Docutils 可以从 Python 程序中提取注释和信息，并将它们格式化为各种形式的程序文档。  

> reStructuredText 是一种轻量级标记语言，其设计目的是  
>>1. 文档处理软件（如Docutils）可以处理它  
>>2. 读和写 Python 源代码的程序员很容易读它。Sphinx，也是从 reStructuredText 文档生成 HTML/PDF 的工具。

> 学习本章 reStructuredText 语法，首先要理解两种标记元素：指令（Directives）和角色（Role）。区别在于指令是块级元素，像段落一样使用。角色是行内元素，可以写在普通文本之中。