---
title: VMware虚拟机安装CentOS操作系统
date: 2022-03-30 22:15:05
category: Linux
tags: 
     - CentOS
     - VMware
---

VMware虚拟机安装CentOS操作系统，以下内容为安装注意事项和说明。

<img src="https://s2.loli.net/2022/06/06/AqmpcIWK7VnsbF2.png" alt="centos" style="zoom:50%;" />

### 1、软件选择：

带GUI的服务器（FTP服务器、Linux的远程管理）

### 2、root密码：

DH***6888

### 3、新用户：

kgdit

### 4、防火墙：

```
//查看防火墙状态
systemctl status firewalld.service
//开启防火墙
systemctl start firewalld.service
//关闭防火墙
systemctl stop firewalld.service
//永久开启防火墙
systemctl enable firewalld.service
//永久关闭防火墙
systemctl disable firewalld.service
```

### 5、设置访问端口

```
#查看防火墙状态
sudo firewall-cmd --state
#开放8081端口
sudo firewall-cmd --zone=public --add-port=8081/tcp --permanent
#开放8080-8090端口
sudo firewall-cmd --zone=public --add-port=8080-8090/tcp --permanent
#关闭8081端口
sudo firewall-cmd --zone=public --remove-port=8081/tcp --permanent
#重启防火墙
sudo firewall-cmd --reload
#查看防火墙开放的端口
sudo firewall-cmd --list-ports
```

<!--more-->

### 6、设置Windows远程连接

```
//查看是否安装桌面--忽略此命令
rpm -qa |grep -i desktop
//如果没有则安装gnome桌面--忽略此命令
yum -y groups install "GNOME Desktop"
//安装rdp软件
yum install xrdp
//提示没有xrdp请先执行以下命令
yum install  epel* -y
//开启rdp服务
systemctl start xrdp
//设置rdp服务开机自启
systemctl enable xrdp
//关闭rdp服务--忽略此命令
systemctl stop xrdp
//开放3389端口，关闭防火墙可以不执行此命令
firewall-cmd --permanent --zone=public --add-port=3389/tcp
firewall-cmd --reload
```

### 7、设置固定IP

```
#编辑本地网卡的配置文件
vi /etc/sysconfig/network-scripts/ifcfg-eth0

#参数说明
ONBOOT=yes  #第一项是确保本地网卡eth0开启
BOOTPROTO=none  #第二项表示不使用dhcp服务，如果是手动配置静态的ip地址，BOOTPROTO的值可以为none或者static。
IPADDR=192.168.0.100  第三项表示设置IP地址
NETMASK=255.255.255.0  第四项表示设置子网掩码
GATEWAY=192.168.0.1  第五项表示设置网关
DNS1=192.168.0.1  第六项表示设置首选DNS服务器，其实DNS有自己的配置文件/etc/resolv.conf，在这里设置DNS，就是把它写入了DNS的配置文件/etc/resolv.conf

#重启网络服务
service network restart 
```

### 8、安装WinRAR压缩软件

```
安装
# wget http://www.rarlab.com/rar/rarlinux-x64-5.0.0.tar.gz
# tar -zxvf rarlinux-x64-5.0.0.tar.gz
# mv rar /opt/
# cd /opt/rar/
# make && make install

使用：
1、rar命令
rar a test.rar file1 file2　　#压缩

2、unrar命令
unrar e test.rar DestPath　　#解压（会在把当前压缩包内容解压到当前目录内，容易造成解压内容和当前目录原文件混合，不容易区分，不建议使用）
unrar x test.rar DestPath　　#解压（会在当前解压目录内产生一个以压缩包名字命名的目录，目录内是解压内容，推荐使用）
```

### 提示权限不够的解决方法

方法一：命令前添加 sudo

方法二：使用命令 sudo su 切换到root用户，然后在执行命令。

![](https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif)

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
