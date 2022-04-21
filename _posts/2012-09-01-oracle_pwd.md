---
layout: post
title: "Oracle改密码"
date:   2012-09-01
tags: [VPS]
comments: true
author: Chu


---

Oracle

<!-- more -->

```
SSH登录服务器
```

```
#登录root给权限
sudo -i
```

```
#打开文件修改
vi /root/.ssh/authorized_keys
把ssh-rsa之前的文件都删除掉.
```

```
#打开文件修改
vim /etc/ssh/sshd_config
PermitRootLogin yes  #允许root登录
PasswordAuthentication yes #开启密码登录
```

```
#重启服务器
reboot
```

```
#等待重连后输入
passwd #按提示设置密码
```

```
在ssh工具中
输入
账号：root
密码：上面设置的密码
```