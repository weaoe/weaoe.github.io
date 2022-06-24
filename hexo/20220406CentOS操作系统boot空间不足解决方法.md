---
title: CentOS操作系统boot空间不足的解决方法
date: 2022-04-06 22:12:11
category: Linux
tags: 
    - CentOS
    - System
---

​		boot目录主要是存放一些系统的内核的配置文件，以及启动管理程序GRUB的目录，在分区的时候分了200M,结果在升级几次内核之后就发现boot空间满了，更新时提示“9 MB 以上的空间至少需要在文件系统 /boot 上”，解决方法如下：

<img src="https://s2.loli.net/2022/06/06/AqmpcIWK7VnsbF2.png" style="zoom: 50%;" />

### 1、查看正在使用的内核

```
//显示内容简洁
uname -r
//显示内容详细
uname -a
```

### 2、查看系统的其他内核

```
//显示内容简洁
rpm -q kernel
//显示内容详细
rpm -qa | grep kernel
```

### 3、删除不必要的内核

```
//通过yum或rpm删除不必要的内核
yum remove kernel-3.10.0-229.14.1.el7
rpm -e kernel-3.10.0-229.14.1.el7.x86_64
//删除后查看空间使用情况
df -lh
```

<img src="https://s2.loli.net/2022/06/07/lZYw8sgxpPcV7WO.png" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
