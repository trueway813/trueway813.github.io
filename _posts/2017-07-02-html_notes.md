---
layout: post
title: "HTML_NOTES"
date:   2017-07-02
tags: [Learning]
comments: true
author: Chu

---

HTML常用
<!-- more -->



------

## Body相关

- ### 网页自适应

```html
<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0,user-scalable=no">
```

> - `width=device-width` width为设置layout viewport 的宽度，为一个正整数，”width-device”表示宽度是设备屏幕的宽度 
> - `initial-scale=1.0` initial-scale为设置页面的初始缩放值，可以是一个带小数的数字，1.0就是占网页的100%
> - `minimum-scale=1.0` 表示最小的缩放比例
> - `maximum-scale=1.0` 表示最大的缩放比例
> - `user-scalable=no`	表示用户是否可以调整缩放比例，值为”no”或”yes”



------



## 图片相关

- ### 图片自适应

```css
img{
            background-size: contain|cover;
            height: auto;
            width: 100%
            }
```



------



## 按钮相关

- ### onclick事件

```html
<button class="btn" onclick="window.location.href = '网址'"><span>文本</span></button>
```

- ### 超链接

```html
<a id="id" href="网址">文本</a>
```



------

