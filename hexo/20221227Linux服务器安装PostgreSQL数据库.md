---
title: Linux服务器安装PostgreSQL数据库
date: 2022-12-27 22:13:51
category: Linux
tags: 
    - PostgreSQL
---

Linux服务器安装PostgreSQL数据库

<img src="https://weaoe.com/hexo/img/2022102900.png" alt="PostgreSQL" style="zoom: 80%;" />

## 下载

- 首先访问https://www.postgresql.org/download/
- 选择操作系统，下载自己需要的安装包版本
- 如果是在线安装，可以直接选在版本、操作系统、架构，然后复制安装命令
- 如果是离线安装，直接点击页面最下方的“direc download”进入新页面，选择版本、操作系统、架构后，直接点击Available Groups下的链接，下载安装包。以centos7为例，一般需要下载四个安装包。
- 本文使用的最新版本15.0

## 安装

### 上传文件

将下载的文件上传到服务器

- postgresql15-15.1-1PGDG.rhel7.x86_64.rpm

- postgresql15-contrib-15.1-1PGDG.rhel7.x86_64.rpm

- postgresql15-libs-15.1-1PGDG.rhel7.x86_64.rpm

- postgresql15-server-15.1-1PGDG.rhel7.x86_64.rpm

### 安装顺序

```
rpm -ivh postgresql15-libs-15.1-1PGDG.rhel7.x86_64.rpm
rpm -ivh postgresql15-15.1-1PGDG.rhel7.x86_64.rpm
rpm -ivh postgresql15-server-15.1-1PGDG.rhel7.x86_64.rpm
rpm -ivh postgresql15-contrib-15.1-1PGDG.rhel7.x86_64.rpm
```

### 初始化数据库

```
/usr/pgsql-15/bin/postgresql-15-setup initdb
```

### 设置自动启动

```
systemctl enable postgresql-15
systemctl start postgresql-15
```

### 创建用户和数据库

1、切换postgres用户登录

```
 su postgres
```

2、登录数据库

```
psql
```

3、创建用户和数据库并授权

```
create user test_user with password '123456';            // 创建用户
create database test_db owner test_user;                 // 创建数据库
grant all privileges on database test_db to test_user;   // 授权
```

如果不创建用户可以使用数据库默认的用户postgres，可以登录数据库后修改用户密码，然后创建数据库并授权；

```
alter role postgres with password 'your_pwd';
```

### 设置远程连接数据库

1、编辑文件postgresql.conf

文件路径为/var/lib/pgsql/15/data/postgresql.conf，取消 listen_addresses的注释并将值改为“*”，取消port的注释；

```
listen_addresses = '*'
port = 5432
```

2、编辑文件pg_hba.conf

文件路径为/var/lib/pgsql/12/data/pg_hba.conf，在最后添加

```
host    all    all    0.0.0.0/0    md5
```

3、重启数据库

```
systemctl restart postgresql-15
```

4、关闭防火墙

```
systemctl status firewalld.service  查看状态
systemctl stop firewalld.service  停止
systemctl start firewalld.service  启动
systemctl disable firewalld.service  禁止开机自启
```

### 连接数据库

Dbeaver

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
