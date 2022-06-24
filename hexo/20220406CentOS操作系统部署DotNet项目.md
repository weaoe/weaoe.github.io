---
title: CentOS操作系统部署DotNet项目
date: 2022-04-06 22:10:19
category: Linux
tags: 
    - CentOS
    - DotNet
---

CentOS操作系统部署DotNet项目的两种方法，以DoeNet5项目为例

<img src="https://s2.loli.net/2022/06/06/7faubgJelkFACqx.jpg" alt="dotnet" style="zoom:50%;" />

### 方法一：项目依赖运行时环境

```
//添加签名密钥
sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
//安装.Net5 SDK
sudo yum install dotnet-sdk-5.0
//安装.Net5运行时--无需执行
sudo yum install aspnetcore-runtime-5.0
sudo yum install dotnet-runtime-5.0
//安装证书
dotnet dev-certs https
//安装证书（仅限Windows和macos）
dotnet dev-certs https --trust
//运行.Net5访问命令
dotnet Demo.Net.Core.dll --urls="http://*:8081;http://*:8082" --environment=Development
//解决验证码无法显示的问题
sudo yum install libc6-dev 
sudo yum install libgdiplus
```

### 方法二：项目集成运行环境

```
//通过工具将发布的独立运行的文件上传到Linux系统，进入项目文件夹后给项目文件添加权限
chmod 755 ./EIVApp
//运行项目
./EIVApp
//如果提示“Couldn't find a valid ICU package installed on the system...”,请安装依赖项安装包
sudo rpm -ivh libicu-50.2-4.el7_7.x86_64.rpm
```

<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
