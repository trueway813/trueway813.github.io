---
layout: post
title: "Docker镜像备份"
date:   2012-09-03
tags: [Docker]
comments: true
author: Chu

---

Docker

<!-- more -->



### 1.首先注册一个DockerHub账号 注册地址:DockerHub

### 2.登录帐号 使用docker login -u 你注册的账号，输入密码显示Login Succeeded表示登录成功

```
docker login -u 你注册的账号
```

### 3.我们可以通过运行 docker images 命令来查看Docker镜像，如下。

```
docker images
或者
docker iamge ls
```

### 4.镜像构建及提交

- 使命使用docker tag 镜像id 新名称:版本号命令修改镜像名称与版本信息

```
docker tag 镜像id 你的账号/新名称:版本号
```

- 使用docker push 你的账号/镜像名称:版本号 提交镜像

```
docker push 你的账号/镜像名称:版本号 

#就是你刚才构建的名称版本
```

### 5.然后你就成功提交到了DockerHub上，可以登录WEB端查看及修改。