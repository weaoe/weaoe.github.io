---
title: CentOS安装cockpit管理工具
date: 2022-05-22 22:10:02
category: Linux
tags: 
    - CentOS
    - System
---

通过cockpit管理Linux服务器。

<img src="https://s2.loli.net/2022/06/06/AqmpcIWK7VnsbF2.png" style="zoom:33%;" />

### 1、安装cockpit软件包

```
sudo yum install cockpit
sudo systemctl enable cockpit.service
sudo systemctl start cockpit.service
sudo systemctl status cockpit.service
sudo yum install cockpit-storaged
sudo yum install cockpit-dashboard
```

### 2、示例访问地址

```
http://192.168.0.1:9090
```



---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
