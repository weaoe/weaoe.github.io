---
title: Linux服务器设置Oracle数据库开机启动
date: 2022-12-29 22:11:42
category: Linux
tags: 
    - Oracle
---

Linux服务器安装Oracle数据库后，通过自带的dbstart和 dbshut两个脚本进行配置自动启动

<img src="https://s2.loli.net/2022/06/06/vkiqp7ATZIMhdCK.png" alt="Oracle" style="zoom: 80%;" />

### 1、Oracle 用户修改 /etc/oratab 文件

编辑oratab，将最后一行的
DHPO:/data/oracle/product/11.2.0/db_1:N
修改为
DHPO:/data/oracle/product/11.2.0/db_1:Y
意思是将不允许自动启动改为允许自动启动
```
vim /etc/oratab
DHPO:/data/oracle/product/11.2.0/db_1:Y
```

### 2、Oracle用户修改安装目录下dbstart文件

编辑dbstart文件，将
ORACLE_HOME_LISTNER=1 
修改为 
ORACLE_HOME_LISTNER=ORACLE_HOME

```
cd $ORACLE_HOME/bin  //也可以输入绝对路径
vi dbstart
ORACLE_HOME_LISTNER=ORACLE_HOME
```

如果数据库是 19c 的话，需要修改如下两处

```
将 ORACLE_HOME_LISTNER=1 修改为 ORACLE_HOME_LISTNER=ORACLE_HOME
将 ORACLE_HOME=1 修改为 ORACLE_HOME=ORACLE_HOME
```

### 3、root用户将dbstart加入开机自启动

编辑 rc.local 文件,在最后添加如下命令，其中路径修改为服务器Oracle安装目录

```

vi /etc/rc.d/rc.local
su - oracle -lc /data/oracle/product/11.2.0/db_1/bin/dbstart
```

### 4、root用户将rd.local 文件添加可执行权限

```
//查看文件权限
ll /etc/rc.d/rc.local 
//返回结果
-rw-r--r-- 1 root root 541 Jul 19 19:01 /etc/rc.d/rc.local
//添加执行权限
chmod u+x /etc/rc.d/rc.local
//重新查看权限
ll /etc/rc.d/rc.local
//返回结果，已添加成功
-rwxr--r-- 1 root root 541 Jul 19 19:01 /etc/rc.d/rc.local
```

### 5、重启服务器验证

Oracle 数据库实例及监听均已成功启动

<!--more-->

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
