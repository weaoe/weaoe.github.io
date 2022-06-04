---
title: xshell连接Windows乱码和退格键无效
date: 2022-05-17 22:10:21
category: Windows
tags: 
    - OpenSSH
    - System
---

通过xshell连接Windows系统部署OpenSSH服务。

### 1、xshell连接Windows服务器OpenSSH中文乱码

解决方法：当前连接会话属性界面，选择终端，编码设置为Unicode(UTF-8)

![202205171001](https://s2.loli.net/2022/05/21/2wqdpJKXIy7Dsi9.png)

### 2、xshell连接Windows服务器OpenSSH退格键无效

解决方法：当前连接会话属性界面，选择终端-键盘，将BACKSPACE键序列修改为“ASCII 127(Ctrl+?)(I)”

![202205171002](https://s2.loli.net/2022/05/21/3tinBpgOuC5UehI.png)