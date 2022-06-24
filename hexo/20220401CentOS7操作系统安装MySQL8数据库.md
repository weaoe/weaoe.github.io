---
title: CentOS7安装MySQL8数据库
date: 2022-04-01 22:16:27
category: Linux
tags: 
     - MySQL
     - CentOS
---

CentOS7操作系统安装MySQL8数据库步骤：

<img src="https://s2.loli.net/2022/06/06/wYmoFPV5Cb67fEs.png" alt="mysql" style="zoom:33%;" />

### 1、上传MySQL文件到服务器；

### 2、删除服务器的MariaDB

```
查看命令：rpm -qa|grep mariadb
删除命令：rpm -e --nodeps mariadb-libs
```

### 3、解压缩MySQL安装包

### 4、安装MySQL安装包

```
//必须安装
rpm -ivh mysql-community-common-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-client-plugins-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-libs-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-client-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-server-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-libs-compat-8.0.26-1.el7.x86_64.rpm
//非必须安装
rpm -ivh mysql-community-embedded-compat-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-devel-8.0.26-1.el7.x86_64.rpm
rpm -ivh mysql-community-test-8.0.26-1.el7.x86_64.rpm
```

### 5、MySQL服务启动停止

```
//查看状态
systemctl status mysqld
//停止服务
service mysqld stop
//初始化数据库
mysqld --initialize --console
//目录授权
chown -R mysql:mysql /var/lib/mysql/
//启动服务
systemctl start mysqld
systemctl status mysqld
```

<!--more-->

### 6、数据库操作

```
//查看临时密码
cat /var/log/mysqld.log
//使用临时密码登录，录入命令后按回车键，然后录入临时密码
mysql -u root -p
//修改MySQL数据库root用户密码
alter USER 'root'@'localhost' IDENTIFIED BY 'nitdDHpassword6***';
//授权远程登录
show databases;
use mysql;
select host, user, authentication_string, plugin from user;
update user set host = "%" where user='root';
select host, user, authentication_string, plugin from user;
flush privileges;
```

### 7、使用工具连接MySQL数据库


---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
