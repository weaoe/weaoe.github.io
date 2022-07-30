---
title: xshell连接Windows乱码和退格键无效
date: 2022-05-17 22:10:21
category: Windows
tags: 
    - OpenSSH
    - System
---

xshell连接Windows服务器后界面乱码和退格键无效的解决方法。

<img src="https://s2.loli.net/2022/06/06/WF6A7pkqbnIdUlC.jpg" alt="xshell" style="zoom:80%;" />

### 1、xshell连接Windows服务器OpenSSH中文乱码

解决方法：当前连接会话属性界面，选择终端，编码设置为Unicode(UTF-8)

<img src="https://s2.loli.net/2022/06/06/oZDBecCPmsW75Ej.png" alt="xshell001" style="zoom:80%;" />

### 2、xshell连接Windows服务器OpenSSH退格键无效

解决方法：当前连接会话属性界面，选择终端-键盘，将BACKSPACE键序列修改为“ASCII 127(Ctrl+?)(I)”

<img src="https://s2.loli.net/2022/06/06/VmdxUG25grRz9hc.png" alt="xshell002" style="zoom:80%;" />



<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)