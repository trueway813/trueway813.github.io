---
layout: post
title: "VPS装Docker"
date:   2012-09-02
tags: [Docker]
comments: true
author: Chu

---

Docker

<!-- more -->

```
方法一#服务器选择CentOS7/8
#一条一条地执行以下命令-安装docker

sudo yum check-update
curl -fsSL https://get.docker.com/ | sh
sudo systemctl start docker
sudo systemctl status docker
sudo systemctl enable docker
```

```
方法二#Linux系统例如Ubuntu、Debian系统都可以

#1.1 使用docker官方的一键安装脚本
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
#这里用的是阿里云的镜像源，安装过程中出现要确认的直接确认就好，安装速度视网络速度和硬件性能而定，时间一般较长，请耐心等待。

#1.2 将当前用户加入docker组
sudo groupadd docker
sudo usermod -aG docker $USER

#1.3 为docker设置镜像加速
#在这里新建一个文件
sudo nano /etc/docker/daemon.json
#填入以下内容
{    
	"registry-mirrors": [
    "https://1nj0zren.mirror.aliyuncs.com",
    "https://docker.mirrors.ustc.edu.cn",        
    "http://f1361db2.m.daocloud.io",        
    "https://registry.docker-cn.com"    ]
    }
    #保存退出
    
#1.4 重启docker应用
sudo systemctl daemon-reload
sudo systemctl restart docker

#1.5 确认安装完成
输入docker -v 显示docker的版本号，即表示成功。
```