---
layout: post
title: "HTML基本语法"
date:   2022-03-22
tags: [HTML]
comments: true
author: Chu
---

HTML(Hyper Text Mark-up Language超文本标记语言)：不是编程语言，而是一种描述性的标记语言，用于描述网页中内容的显示方式，比如文字以什么颜色、大小来显示等，这些都是利用Html标记来实现。

<!-- more -->

# HTML的文档结构
```
<html>
 
      <head>
 
           <title>
 
                标题
 
           </title>
 
      </head>
 
      <body>
 
           正文
 
      </body>
 
</html>
```
## 小结：
- <html>…</html>标识网页文件的开始与结束，所有的Html元素，都要放在这对标记中。

- <head>…</head>标识网页文件的头部信息，如标题、搜索引擎关键字等

- <title>…</title>标识网页文件的标题

- <body>…</body>标识网页文件的主体部分


# 常见的HTML的标记语法

## 1.单标记

### 一．<标记名称>
```
单一型，无属性值

如：<br/>——表示换行符
```

### 二．<标记名称属性=”属性值”>
```
单一型，有属性值

如：<hr width=”80%”/>
```

## 2.双标记

### 三．<标记名称>…</标记名称>
```
没有属性值

如：<title>…<title>
```

### 四．<标记名称属性=”属性值”>…</标记名称>
```
有属性值

如：<body bgcolor=”red”>…</body>
```
  
### 注释

- 格式：
```
<!—注释内容-->
```
  
- Body属性
```
<body bgcolor=”背景颜色” background=”背景图像” text=”文本颜色” link=”链接文本颜色” vlink=”访问过的文本颜色” alink=”激活的连接文本颜色” leftmargin=”左边界”>
```

# <font>标记
语法：

`<font color=”文本颜色” size=“字号”>文本</font>`
  
# 字符格式
  
功能|标记
--|:--:
加粗|<b>文本</b>
倾斜|<i>文本</i>
加强语气|<strong>文本</strong>
下划线|<u>文本</u>
删除线|<s>文本</s>
上标|<sup>文本</sup>
下标|<sub>文本<sub>  

  
段落标记

格式：

<p align=“对齐方式”>…</p>

align

Left

左对齐

Center

居中

Right

右对齐

 

 

HTML中的特殊字符

特殊字符

转义码

空格

&nbsp;

版权号

&copy;

注册商标

&reg;

“

&quot；

&

&amp;

< 

&it;

> 

&gt;

 

      修饰标记

水平直线<hr/>

属性名称

属性值

说明

Size

像素绝对值

越大，线越粗

Width

宽度

随着值得变化

 

 

 

总结：

   以上就是我们在学习html中经常用到的语法












