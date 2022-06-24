---
title: Windows操作系统远程管理IIS
date: 2022-04-07 22:13:34
category: Windows
tags: 
    - IIS
    - System
---

远程管理Windows服务器的iis系统服务，在无需远程服务器的情况下启动、停止、查询IIS服务。

<img src="https://s2.loli.net/2022/06/06/AwjHuEGDgPKLNb7.jpg" alt="IIS" style="zoom: 80%;" />

### 1、启动IIS

```
iisreset -start或者iisreset /start
```

### 2、停止IIS

```
iisreset -stop或者iisreset /stop
```

### 3、重启IIS

```
iisreset -restart或者iisreset /restart
```

### 4、重启服务器

```
iisreset -reboot或者iisreset /reboot
```

### 5、停止IIS服务失败重启电脑

```
iisreset -rebootonerror或者iisreset /rebootonerror
```

### 6、无需强制停止IIS服务

```
iisreset -noforce或者iisreset /noforce
```

### 7、X秒后,强制停止IIS服务,除非添加/NOFORCE 参数

```
iisreset -timeout:x或者iisreset /timeout:x
```

![](https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif)

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
