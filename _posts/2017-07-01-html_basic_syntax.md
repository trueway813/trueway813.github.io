---
layout: post
title: "HTML基本语法"
date:   2017-07-01
tags: [HTML]
comments: true
author: Chu
---

HTML(Hyper Text Mark-up Language超文本标记语言)：不是编程语言，而是一种描述性的标记语言，用于描述网页中内容的显示方式，比如文字以什么颜色、大小来显示等，这些都是利用Html标记来实现。

<!-- more -->

# HTML的文档结构
```
<!doctype html>
<html>
    <head>
        <!-- 声明当前页面的编码集：charset=gbk,gb2312(中文编码) , utf-8(国际编码) -->
        <meta http-equiv='Content-Type' content='text/html; charset=utf-8'>
        <!-- 声明当前页面的三元素 -->
        <title>helloWorld--zxk</title>
        <meta name='keywords' content='关键词,关键词'>
        <meta name='description' content=''>
        <!-- js/css -->
		<link rel="stylesheet" type="text/css" href="asset/all.less" />
		<script src="common/css/less-1.3.3.min.js"></script>
            
		<style type="text/css">
			/* 重置浏览器默认样式 */
			body, dl, dt, dd, ul, ol, li, pre, form, fieldset, input, p, blockquote, th, td {
			    margin: 0;
			    padding: 0;
			}

			img {
			    border: 0;
			    vertical-align: top;
			}
		</style>
            
    </head>
 <body>
精于勤<br />荒于嬉
 </body>
</html>
```
> 小结：
- `<html>…</html>` 标识网页文件的开始与结束，所有的Html元素，都要放在这对标记中。
- `<head>…</head>` 标识网页文件的头部信息，如标题、搜索引擎关键字等
- `<title>…</title>` 标识网页文件的标题
- `<body>…</body>` 标识网页文件的主体部分

---

# 常见的HTML的标记语法

1.常见的单标记(由一个标签组成的)
- 例如 `<br>、<hr>、<img>、<input>、<param>、<meta>、<link>`

1.1 单标记(单一型，无属性值)
- `<标记名称>`
- 如：`<br>` —— 表示换行符

1.2 单标记(单一型，有属性值)
- `<标记名称属性=”属性值”>`
- 如：`<hr width=”80%”/>`

2.常见的双标记（由“开始标签”和“结束标签”两部分构成）
- 例如 `<html>、<head>、<title>、<body>、<table>、<tr>、<td>、<span>、<p>、<form>、<h1>、<h2>、<h3>、<h4>、<h5>、<h6>、<object>、<style>、<b>、<u>、<strong>、<i>、<div>、<a>、<script>、<center>（双标签的一部分）`

2.1 双标记(没有属性值)
- `<标记名称>…</标记名称>`
- 如：`<title>…<title>`

2.2 双标记(有属性值)
- `<标记名称属性=”属性值”>…</标记名称>`
- 如：`<body bgcolor=”red”>…</body>`
  
# 注释
- 格式：
- `<!—注释内容-->`
  
# Body属性
`<body bgcolor=”背景颜色” background=”背景图像” text=”文本颜色” link=”链接文本颜色” vlink=”访问过的文本颜色” alink=”激活的连接文本颜色” leftmargin=”左边界”>`

# `<font>`标记
- 语法：
- `<font color=”文本颜色” size=“字号”>文本</font>`
  
# 字符格式

|功能|标记|
|:--:|:--:|
|加粗    |`<b>文本</b>`|
|倾斜    |`<i>文本</i>`|
|加强语气 |`<strong>文本</strong>`|
|下划线|`<u>文本</u>`|
|删除线|`<s>文本</s>`|
|上标|`<sup>文本</sup>`|
|下标|`<sub>文本<sub>`|


# 段落标记
- 格式：
- `<p align=“对齐方式”>…</p>`

align|Left|左对齐
:--:|:--:|:--:
align|Center|居中
align|Right|右对齐


# HTML中的特殊字符

特殊字符|转义码
:--:|:--:|
空格|`&nbsp;`
版权号|`&copy;`
注册商标|`&reg;`
`“`|`&quot；`
`&`|`&amp;`
`<`|`&it;`
`>`|`&gt;`


# 修饰标记

## 水平直线 `<hr/>`

属性名称|属性值|说明
:--:|:--:|:--:
Size|像素绝对值|越大，线越粗
Width|宽度|随着值得变化


# 总结：
## 以上就是我们在学习html中经常用到的语法





## jQuery 语法

jQuery 语法是通过选取 HTML 元素，并对选取的元素执行某些操作。

基础语法： **$(\*selector\*).\*action\*()**

- 美元符号定义 jQuery
- 选择符（selector）"查询"和"查找" HTML 元素
- jQuery 的 action() 执行对元素的操作

实例:

`$(this).hide() `- 隐藏当前元素

`$("p").hide()` - 隐藏所有段落

`$("p .test").hide()` - 隐藏所有 class="test" 的段落

`$("#test").hide()` - 隐藏所有 id="test" 的元素
