---
title: CentOS操作系统设置DotNet项目自动运行
date: 2022-04-06 22:11:10
category: Linux
tags: 
    - CentOS
    - DotNet
---

CentOS操作系统部署DotNet项目并设置开机自动运行的方法：

<img src="https://s2.loli.net/2022/06/06/7faubgJelkFACqx.jpg" alt="dotnet" style="zoom:50%;" />

### 方法一：通过服务运行，项目依赖运行时环境

```
//在 /etc/systemd/system目录下创建xxx.service文件，如eivision.service
vi /etc/systemd/system/kgdit.service
//在文件中粘贴如下内容，WorkingDirectory为项目路径，ExecStart为启动指令
 [Unit]
 Description=kgdit
 [Service]
 WorkingDirectory=/home/kgdit/kgsoft/kgdit_lin64
 ExecStart=/usr/bin/dotnet kgdit.dll
 Restart=always
 RestartSec=10
 [Install]
 WantedBy=multi-user.target

//其中两种命令的区别是是否有local路径的区别，也许是dotnet版本的区别
//ExecStart=/usr/local/bin/dotnet EIVApp.dll、ExecStart=/usr/bin/dotnet EIVApp.dll

//使启动生效
systemctl enable kgdit.service
//立即启动项目服务
systemctl start kgdit.service
//重新加载服务
systemctl daemon-reload
//查看服务状态
systemctl status kgdit.service
//重启服务器看是否生效
shutdown -r now
```

### 方法二：通过服务运行，项目集成运行环境

```
//在 /etc/systemd/system目录下创建xxx.service文件，kgdit.service
vi /etc/systemd/system/kgdit.service
//在文件中粘贴如下内容，WorkingDirectory为项目路径，ExecStart为启动指令
[Unit]
Description=kgdit
After=default.target

[Service]
ExecStart=/home/kgdit/kgsoft/kgdit.sh

[Install]
WantedBy=default.target

//使启动生效
systemctl enable kgdit.service
//立即启动项目服务
systemctl start kgdit.service
//重新加载服务
systemctl daemon-reload
//查看服务状态
systemctl status kgdit.service
//重启服务器看是否生效
shutdown -r now
```

<!--more-->

### 方法三：通过命令运行，项目集成运行环境

```
//创建.sh命令执行文件,内容如下
1、第一行#!/bin/sh首先指明脚本的解释器（一定要在第一行，否则报错）
2、第二行# chkconfig:2345 60 30，chkconfig的第一个参数是指定脚本的运行等级，一般为2345即可，第二个参数是脚本的启动优先级（0-100），等级越高，优先级越低，也就启动越晚，第三个参数是关闭优先级，同理启动优先级。
3、脚本的描述信息
#!/bin/sh
# chkconfig:2345 60 30
# description:otfapi
cd /home/centos/kgsoft/otfapi_lin64
./OTFApi
//项目赋予可执行权限
chmod +x ./OTFApi
//后台执行sh命令
nohup sh otfapi.sh &
//上一步运行成功后，按任意键，最后通过exit命令退出终端
exit
//通过端口确认后台程序的进程1111
lsof -i:5000
//结束进程，例如进程ID为1111
kill -9 1111
//重新运行
nohup sh otfapi.sh &

//将以上方法设置为开机自动运行，将sh文件复制到/etc/init.d目录下；
cp /home/centos/kgsoft/otfapi.sh /etc/init.d/otfapi.sh
//给脚本增加执行权限
chmod +x /etc/init.d/otfapi.sh
//键入开机启动项
chkconfig --add otfapi.sh
chkconfig otfapi.sh on
//查看开机启动情况
chkconfig --list otfapi.sh
```



![](https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif)

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
