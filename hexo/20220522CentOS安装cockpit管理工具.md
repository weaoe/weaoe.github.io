---
title: CentOS安装cockpit管理工具
date: 2022-05-22 22:10:02
category: Linux
tags: 
    - CentOS
    - System
---

通过cockpit管理Linux服务器。

![](https://s2.loli.net/2022/06/06/AqmpcIWK7VnsbF2.png)

### 1、安装cockpit软件包

```
sudo yum install cockpit
sudo systemctl enable cockpit.service
sudo systemctl start cockpit.service
sudo systemctl status cockpit.service
sudo yum install cockpit-storaged
sudo yum install cockpit-dashboard
```

