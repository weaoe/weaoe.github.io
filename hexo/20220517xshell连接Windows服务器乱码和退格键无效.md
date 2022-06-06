---
title: xshell连接Windows乱码和退格键无效
date: 2022-05-17 22:10:21
category: Windows
tags: 
    - OpenSSH
    - System
---

通过xshell连接Windows系统部署OpenSSH服务。

![xshell](https://s2.loli.net/2022/06/06/WF6A7pkqbnIdUlC.jpg)

### 1、xshell连接Windows服务器OpenSSH中文乱码

解决方法：当前连接会话属性界面，选择终端，编码设置为Unicode(UTF-8)

![xshell001](https://s2.loli.net/2022/06/06/oZDBecCPmsW75Ej.png)

### 2、xshell连接Windows服务器OpenSSH退格键无效

解决方法：当前连接会话属性界面，选择终端-键盘，将BACKSPACE键序列修改为“ASCII 127(Ctrl+?)(I)”

![xshell002](https://s2.loli.net/2022/06/06/VmdxUG25grRz9hc.png)