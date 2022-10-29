---
title: CentOS7安装Oracle11G数据库
date: 2022-04-04 22:21:03
category: Linux
tags: 
    - CentOS
    - Oracle
---

CentOS7操作系统安装Oracle11G数据库步骤：

<img src="https://s2.loli.net/2022/06/06/vkiqp7ATZIMhdCK.png" alt="oracle" style="zoom:50%;" />

### 1、创建用户和组

```
groupadd oinstall
groupadd dba
useradd -g oinstall -g dba -m oracle
passwd oracle
id oracle
```

Oracle用户密码：nitd***6888

system用户密码：nitd***6888

### 2、创建目录

```
mkdir -p /data/oracle　　#oracle数据库安装目录
mkdir -p /data/oraInventory　　#oracle数据库配置文件目录
mkdir -p /data/database　　#oracle数据库软件包解压目录
cd /data
ls　　#创建完毕检查一下
chown -R oracle:oinstall /data/oracle　　#设置目录所有者为oinstall用户组的oracle用户
chown -R oracle:oinstall /data/oraInventory
chown -R oracle:oinstall /data/database
```

### 3、修改系统信息

```
cat /proc/version
cat /etc/redhat-release		#查看redhat-release文件
vi /etc/redhat-release 		#修改redhat-release文件，将类似于 CentOS Linux release 7.2.1511 (Core) 的内容替换为redhat-7
cat /etc/redhat-release 	#看一下是不是真的保存好了
```

<!--more-->

### 4、安装依赖项

```
binutils-2.23.52.0.1-12.el7.x86_64 
compat-libcap1-1.10-3.el7.x86_64 
compat-libstdc++-33-3.2.3-71.el7.i686
compat-libstdc++-33-3.2.3-71.el7.x86_64
gcc-4.8.2-3.el7.x86_64 
gcc-c++-4.8.2-3.el7.x86_64 
glibc-2.17-36.el7.i686 
glibc-2.17-36.el7.x86_64 
glibc-devel-2.17-36.el7.i686 
glibc-devel-2.17-36.el7.x86_64
ksh
libaio-0.3.109-9.el7.i686 
libaio-0.3.109-9.el7.x86_64 
libaio-devel-0.3.109-9.el7.i686 
libaio-devel-0.3.109-9.el7.x86_64 
libgcc-4.8.2-3.el7.i686 
libgcc-4.8.2-3.el7.x86_64 
libstdc++-4.8.2-3.el7.i686 
libstdc++-4.8.2-3.el7.x86_64 
libstdc++-devel-4.8.2-3.el7.i686 
libstdc++-devel-4.8.2-3.el7.x86_64 
libXi-1.7.2-1.el7.i686 
libXi-1.7.2-1.el7.x86_64 
libXtst-1.2.2-1.el7.i686 
libXtst-1.2.2-1.el7.x86_64 
make-3.82-19.el7.x86_64 
sysstat-10.1.5-1.el7.x86_64 
示例：
yum install binutils # 安装的软件包名称可以省略后边的版本号
```

### 5、设置防火墙

```
systemctl status firewalld.service　　#查看防火墙状态，运行中
显示防火墙信息，比如包含下边，说明防火墙正在运行
Started firewalld - dynamic firewall daemon.
systemctl disable firewalld.service　　#禁止使用防火墙（重启也是禁止的）
```

### 6、未完待续

。。。



---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
