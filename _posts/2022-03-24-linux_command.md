# Linux命令总结

---
## 端口相关
- 用于显示 tcp，udp 的端口和进程等相关情况。
>netstat -tunlp

- 查看当前所有tcp端口
>netstat -ntlp   

- 查看80端口占用情况
>fuser -n tcp 80

- 查看所有80端口使用情况
>netstat -ntulp | grep 80   

- 查看所有3306端口使用情况
>netstat -ntulp | grep 3306  

---

## 系统相关
- 查看系统版本
>cat /etc/os-release