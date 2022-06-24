---
title: Windows操作系统安装Oracle 12C
date: 2022-06-15 22:09:37
category: Windows
tags: 
    - Oracle
---

ORACLE数据库系统是美国ORACLE公司（甲骨文）提供的以分布式数据库为核心的一组软件产品，是目前最流行的客户/服务器(CLIENT/SERVER)或B/S体系结构的数据库之一。

Oracle数据库12c引入了一个新的多承租方架构，使用该架构可轻松部署和管理数据库云。

<img src="https://s2.loli.net/2022/06/15/GhMWUS6gNzHETOI.jpg" alt="img" style="zoom:90%;" />

## Oracle下载

打开Oracle官网，登录账号，选择相应版本下载即可。

网站地址：https://www.oracle.com

下载成功解压后得到一下文件，双击setup.exe即可安装。

<img src="https://s2.loli.net/2022/06/15/iTyEReJxsNlgSF2.png" alt="img" style="zoom:80%;" />

## Oracle安装

### 第一步

双击setup.exe，启动安装程序，可以取消“我希望通过……”，然后点击“下一步”，弹出“尚未提供电子邮件地址”的提示窗口，直接点击“是”即可。

<img src="https://s2.loli.net/2022/06/15/nMwCsl4tLbXIVHD.png" alt="img" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/15/NQtZJgU1ACep87x.png" alt="img" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/15/bDJtjRdkhGFymLA.png" alt="img" style="zoom:80%;" />

### 第二步

选择“创建和配置数据库”，在安装过程中会自动创建示例数据库，选择“仅安装数据库软件”，可以自定义数据库安装选项和参数，我需要自定义数据库，选择“仅安装数据库软件”，点击“下一步”。

<img src="https://s2.loli.net/2022/06/15/apf1Bg2O3Ln8vUN.png" alt="img" style="zoom:80%;" />

### 第三步

根据实际情况选择安装类型，我在服务器安装，所以选择“服务器类”，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/XDEWra3KAivGwqm.png" alt="img" style="zoom:80%;" />

<!--more-->

### 第四步

根据实际情况选择数据库安装类型，点击“下一步”

<img src="https://s2.loli.net/2022/06/15/BKPtHAfhZ4ImDnr.png" alt="img" style="zoom:80%;" />

### 第五步

建议选择“高级安装”，可以分别设置用户口令、数据库字符集、产品语言和自动备份等高级功能，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/O1WGZkbcEe5syjT.png" alt="img" style="zoom:80%;" />

### 第六步

根据需要选择数据库版本，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/FdIj6xLsGebrBzO.png" alt="img" style="zoom:80%;" />

### 第七步

根据需求选择数据库服务运行的账户，点击“下一步”，弹出提示信息直接点击“是”即可；

<img src="https://s2.loli.net/2022/06/15/5ox1aPI3nvUFemE.png" alt="img" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/15/HLazN4ToymUYKVB.png" alt="img" style="zoom:80%;" />

### 第八步

Oracle会自动选择安装在空间最大的磁盘目录，也可以自定义修改安装路径；

<img src="https://s2.loli.net/2022/06/15/Dh9rj8fvlsuzOGM.png" alt="img" style="zoom:80%;" />

### 第九步

根据需求选择数据库类型，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/5ynicpdAYsmGqux.png" alt="img" style="zoom:80%;" />

### 第十步

设置数据库的“全局数据库名”和“SID”，并根据需求选择是否“创建为容器数据库”，点击“下一步”；

容器数据库主要应用于虚拟化技术；

<img src="https://s2.loli.net/2022/06/15/KsXALiDE1I4kH6y.png" alt="img" style="zoom:80%;" />

### 第十一步

根据服务器性能和用途设置内存和字符集，点击“下一步”；

服务器完全用作数据库的话可以设置到80%；

<img src="https://s2.loli.net/2022/06/15/RzqIjf6HZCDu5sa.png" alt="img" style="zoom:80%;" />

### 第十二步

根据实际需求设置存储方式，一般为“文件系统”，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/p3eL6XgMC9uGy1A.png" alt="img" style="zoom:80%;" />

### 第十三步

按照需求选择是否“注册到……”，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/zKg6c5U1BIA8X9f.png" alt="img" style="zoom:80%;" />

### 第十四步

建议启用“文件恢复”，在数据库出现问题时可以恢复数据，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/nR43uHBoezQ5X6a.png" alt="img" style="zoom:80%;" />

### 第十五步

根据需要设置管理用户的口令，建议分开设置不同的密码，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/iejVGI5SHKCkmF8.png" alt="img" style="zoom:80%;" />

### 第十六步

自动检查是否满足产品的最低安装和配置要求，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/ZflSHquIF5rz29s.png" alt="img" style="zoom:80%;" />

### 第十七步

显示之前选择和设置的各项功能和参数，点击“安装”；

 

<img src="https://s2.loli.net/2022/06/15/bNROxHnKDre9g8M.png" alt="img" style="zoom:80%;" />

### 第十八步

数据根据配置项开始安装，安装过程根据服务器配置时间长短不定，点击“下一步”；

<img src="https://s2.loli.net/2022/06/15/hAoXVbvlzIx8T5N.png" alt="img" style="zoom:80%;" />

### 第十九步

数据库安装完成，点击“关闭”即可。

接下来可以设置监听、网络服务名等，使用自己常用的数据库管理工具进行数据库的创建、配置和使用。

<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
