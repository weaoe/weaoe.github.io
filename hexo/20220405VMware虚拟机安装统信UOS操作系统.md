---
title: VMware安装统信UOS操作系统
date: 2022-04-05 22:15:28
category: Linux
tags: 
    - VMware
    - UOS
---

VMware虚拟机安装统信UOS操作系统后的一些设置；

<img src="https://s2.loli.net/2022/06/06/ahxdVYX52FOMpsB.jpg" alt="UOS" style="zoom:80%;" />

### 1、启用ssh连接

```
sudo apt install openssh-server  //默认已安装
systemctl enable ssh  //设置开机启动
systemctl status ssh
systemctl start ssh
systemctl stop ssh
systemctl restart ssh
systemctl reload ssh
```

### 2、启用root的ssh连接，默认root不能ssh连接

```
编辑sshd配置文件,将#PermitRootLogin prohibit-password的#删除，将prohibit-password更改为yes
vi /etc/ssh/sshd_config
重启ssh服务
systemctl restart ssh
```

<!--more-->

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
