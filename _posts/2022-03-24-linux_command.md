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
## 端口-进程

- **`netstat -ntulp | grep 80`**

  > 查看所有80端口使用情况  
  >
  > -n : 不进行DNS轮询，显示IP(可以加速操作)
  >
  > -t : 指明显示TCP端口 
  >
  > -u : 指明显示UDP端口 
  >
  > -l : 仅显示监听套接字(所谓套接字就是使应用程序能够读写与收发通讯协议(protocol)与资料的程序) 
  >
  > -p : 显示进程标识符和程序名称，每一个套接字/端口都属于一个程序。 

- **`ps aux | grep 进程名`**

  > 如：`ps aux |grep sillyGirl`
  >
  > `ps` (英文全称:**processstatus**)是显示当前状态处于running的进程
  >
  > `ps aux ` 是显示所有进程和其状态
  >
  > `grep` 是 **global regular expression print**（全局正则表达式输出）

- **`|`**   竖线管道命令

  > 用法： **`command 1 | command 2`** 他的功能是把第一个 命令1 执行的结果作为 命令2 的输入传给 命令2
  >
  > 常用的可以直接用于管道的命令有 `cut` `grep` `sort` `uniq` `wc` `tee` `tr` `col` `join` `paste` `expand` `xargs`

- **`-`**  减号符

  > "-"：就是代表标准输出/标准输入, 视命令而定."-"代替stdin和stdout的用法,stdin就是标准输入,stdout就是标准输出
  >
  > 1.为应用程序指定参数。
  >
  > 如`ps -aux,tar -zxf test.tar`
  >
  > 2.一个减号和两个减号
  >
  > 一个减号后面跟的参数必须是单字符参数，可以多个参数写在同一个减号后面。
  >
  > 例如：`tar -xvf ×××`
  >
  > 两个减号后面跟的参数必须是多字符参数，一个“--”只能跟一个参数。
  >
  > 例如：`tar --version`
  >
  > 3 表示上一级工作目录。如cd -
  >
  > `cd -`

---

## 系统命令
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
