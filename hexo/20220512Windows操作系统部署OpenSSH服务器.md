---
title: Windows操作系统部署OpenSSH服务器
date: 2022-05-12 22:17:45
category: Windows
tags: 
    - OpenSSH
    - System
---

通过OpenSSH管理Windows服务器。

### 1、下载OpenSSH

- 下载地址：https://github.com/PowerShell/Win32-OpenSSH/releases

### 2、安装OpenSSH

- 将最新版本的内容提取到C:\Program Files\OpenSSH，在目录下打开Powershell ；
- 在 Powershell 控制台中，运行以下命令

```
powershell.exe -ExecutionPolicy Bypass -File install-sshd.ps1
```

### 3、设置防火墙

- 关闭防火墙或者设置防火墙允许OpenSSH服务和22端口

### 4、设置OpenSSH自动启动并启动服务

- 通过计算机管理下服务管理功能，设置OpenSSH自动启动并启动服务；
- 通过以下命令设置OpenSSH自动启动并启动服务；

```
sc config sshd start= auto
net start sshd
```

### 5、通过工具连接OpenSSH
