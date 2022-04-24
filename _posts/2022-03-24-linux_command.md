---
layout: post
title: "Linux命令总结"
date:   2022-03-24
tags: [Learning]
comments: true
author: Chu
---

Linux常用命令总结

<!-- more -->


---
## 端口相关

- **`ps aux |grep 进程名`**

  > 如：`ps aux |grep sillyGirl`
  >
  > ps是显示当前状态处于running的进程，grep表示在这些里搜索，而ps aux是显示所有进程和其状态

- **`netstat -tunlp`**

  > 用于显示 tcp，udp 的端口和进程等相关情况。

- **`netstat -ntlp`**   

  > 查看当前所有tcp端口

- **`fuser -n tcp 80`**

  > 查看80端口占用情况

- **`netstat -ntulp | grep 80`**

  > 查看所有80端口使用情况  

- **`netstat -ntulp | grep 3306`**

  > 查看所有3306端口使用情况 

---

## 系统相关
- **`cat `命令**

  1.cat命令的全称是 **`concatenate`**，主要用于显示文件内容。

  2.查看centos系统版本

  > `cat /etc/os-release`



- **`yum` 命令**

  1.YUM全称为 Yellow dog Updater Modified，它是一个在线的软件安装命令。



- **`tar` 命令**

  1.解压缩:

  > `tar -zxvf 1filename.tar.gz`
  >
  > > z ：表示 tar 包是被 gzip 压缩过的 (后缀是.tar.gz)，所以解压时需要用 gunzip 解压 (.tar不需要) 
  > >
  > > x ：表示 从 tar 包中把文件提取出来
  > >
  > > v ：表示 显示打包过程详细信息 
  > >
  > > f ：指定被处理的文件是什么 ：适用于参数分开使用的情况，连续无分隔参数不应该再使用（所以上面的命令不标准） 
  > >
  > > 由此分析，v 是可以省去的（v属于辅助参数） 直接用 zxf 即可， 上面命令默认解压到当前目录，如果我们想要直接解压到指定目录并切换过去



- **`nohup`命令**

  1.`nohup`：放在命令的开头，表示不挂起（no hang up），也即，关闭终端或者退出某个账号，进程也继续保持运行状态，一般配合&符号一起使用。如`nohup command &`

  1.语法：`nohup Command [ Arg … ] [　& ]`

  > `&` 用途：在后台运行
