---
title: Windows server 2019安装Hyper-V教程
date: 2022-03-25 22:13:51
category: Windows
tags: 
    - System
---

Hyper-V是微软的虚拟化产品，是采用类似Vmware ESXi的基于hypervisor的技术，能够实现桌面虚拟化。

<img src="https://s2.loli.net/2022/06/25/8GlZ9rgwjULaMW7.jpg" alt="lYnZedwGQRcpV45" style="zoom:80%;" />

**软件硬件要求：**

1、[Intel](https://baike.baidu.com/item/Intel/125450)或者[AMD](https://baike.baidu.com/item/AMD/5905)64位处理器；

2、Windows Server 2008 R2或Windows 7及以上操作系统；

3、硬件虚拟化，[Intel vt](https://baike.baidu.com/item/Intel vt/2091588)或AMD-v；

4、[CPU](https://baike.baidu.com/item/CPU/120556)必须具备[数据执行保护](https://baike.baidu.com/item/数据执行保护)（ DEP ）功能并且启动；

5、内存最低限度为2GB。

Windows server 2019 安装Hyper-V具体图文说明如下

### 第一步

通过开始菜单，启动服务器管理；

<img src="https://s2.loli.net/2022/06/25/V2Z1GICuFR8Mrxn.png" alt="image001" style="zoom:80%;" />

### 第二步

点击“添加角色和功能”，弹出添加功能向导，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/dWUHYli6o5bmgst.png" alt="image002" style="zoom:80%;" />

### 第三步

根据需求选择“安装类型”，由于我是本地安装，所以选择“基于角色或基于功能安装”，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/4NoUGqCs8wzEa16.png" alt="image003" style="zoom:80%;" />

<!--more-->

### 第四步

选择服务器，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/zpJM7smVYItNDfL.png" alt="image004" style="zoom:80%;" />

### 第五步

选中“Hyper-V”功能，在弹出的窗口中点击“添加功能”；

<img src="https://s2.loli.net/2022/06/25/ELbpCIa2XfjTB1k.png" alt="image005" style="zoom:80%;" />

### 第六步

如果需要添加其他角色请继续选择，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/pD1PCiZmoWKS3kO.png" alt="image006" style="zoom:80%;" />

### 第七步

如果需要添加其他功能请选择，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/me4zt2rQkgsPfYl.png" alt="image007" style="zoom:80%;" />

### 第八步

直接点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/ZlnsM2aYQFAS3dh.png" alt="image008" style="zoom:80%;" />

### 第九步

选择网卡，创建虚拟交换机；

建议此步骤不选择，安装好Hyper-V后单独创建虚拟交换机；

<img src="https://s2.loli.net/2022/06/25/dBq2MruKC9GxHja.png" alt="image009" style="zoom:80%;" />

### 第十步

根据实际需求选择“…发送和接收虚拟机的实时迁移”，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/1CczGPZ8nf69QYK.png" alt="image010" style="zoom:80%;" />

### 第十一步

选择虚拟硬盘和虚拟机配置文件的存储位置，点击“下一步”；

<img src="https://s2.loli.net/2022/06/25/A8pFtoWqMRz5rfB.png" alt="image011" style="zoom:80%;" />

### 第十二步

点击“安装”按钮开始安装功能；

<img src="https://s2.loli.net/2022/06/25/BqIhlaRScwJAdPL.png" alt="image012" style="zoom:80%;" />

功能正在安装中；

<img src="https://s2.loli.net/2022/06/25/HqWBE3Vz89waPg6.png" alt="image013" style="zoom:80%;" />

安装完成后点击“关闭”即可，但需要重启服务器；

<img src="https://s2.loli.net/2022/06/25/gQV8IcOhFyDRM34.png" alt="image014" style="zoom:80%;" />

### 第十三步

安装完成后，启动Hyper-V管理器，点击“虚拟交换机管理器”进行新建交换机；

<img src="https://s2.loli.net/2022/06/25/zHt6MuRQyFeYVgj.png" alt="image015" style="zoom:80%;" />

### 第十四步

输入虚拟交换机名称、说明，然后选择连接类型，如果需要其他人访问，请选择外部网络，点击“确定”完成创建；

<img src="https://s2.loli.net/2022/06/25/YKEng1U4qJBcdZN.png" alt="image016" style="zoom:80%;" />

 

### 第十五步

Hyper-V的功能到此已经安装完成，接下来可以创建虚拟机、安装操作系统、连接网络并使用虚拟机。

<img src="https://s2.loli.net/2022/06/25/Wu6UdmFerPRIDC9.png" alt="image017" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
