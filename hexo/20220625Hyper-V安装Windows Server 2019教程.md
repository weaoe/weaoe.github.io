---
title: Hyper-V安装Windows server 2019教程
date: 2022-06-25 22:14:13
category: Windows
tags: 
    - System
---

Hyper-V是微软的虚拟化产品，是采用类似Vmware ESXi的基于hypervisor的技术，能够实现桌面虚拟化。

![image022](https://s2.loli.net/2022/06/25/S4hP7za9ceuLktR.jpg)

**软件硬件要求：**

1、[Intel](https://baike.baidu.com/item/Intel/125450)或者[AMD](https://baike.baidu.com/item/AMD/5905)64位处理器；

2、Windows Server 2008 R2或Windows 7及以上操作系统；

3、硬件虚拟化，[Intel vt](https://baike.baidu.com/item/Intel vt/2091588)或AMD-v；

4、[CPU](https://baike.baidu.com/item/CPU/120556)必须具备[数据执行保护](https://baike.baidu.com/item/数据执行保护)（ DEP ）功能并且启动；

5、内存最低限度为2GB。

Windows server 2019 安装Hyper-V具体图文说明如下

## 第一步

运行Hyper-V管理器，在服务器名称点击右键，选择“新建-虚拟机”。

![image001](https://s2.loli.net/2022/06/25/Wu6UdmFerPRIDC9.png)

 

## 第二步

点击“下一步”按照流程创建虚拟机，也可以直接点击“完成”创建默认配置虚拟机，此处自定义设置；

 ![image002](https://s2.loli.net/2022/06/25/PIJUn4WisqylKtg.png)



## 第三步

录入虚拟机的名称，默认保存在Hyper-V管理器安装时设置的存储目录，可以选择“将虚拟机存储在…”更改存储目录，点击“下一步”继续；

  ![image003](https://s2.loli.net/2022/06/25/NRJPI8oAQ74bE3m.png)

<!--more-->

## 第四步

选择虚拟机的代数，建议选择第二代，支持最新的操作系统和功能；

  ![image004](https://s2.loli.net/2022/06/25/32bSg9AtXiqhaML.png)



## 第五步

分配虚拟机内存，设置动态调整会稍微影响性能；

![image005](https://s2.loli.net/2022/06/25/1MabEVzv7cIeNUi.png)

## 第六步

选择已经创建的虚拟交换机，上一篇安装Hyper-V教程有虚拟机创建图文说明；

![image006](https://s2.loli.net/2022/06/25/WCSxJv5DYf29gpy.png)

## 第七步

选择虚拟硬盘的使用方式，每个虚拟机使用单独的虚拟硬盘可以提升虚拟机性能，设置虚拟机硬盘的名称和位置，点击“下一步”；

 ![image007](https://s2.loli.net/2022/06/25/E4vbkABW7NLHz5X.png)

## 第八步

选择操作系统的安装方式，如果已经下载好镜像文件的话可以直接选择系统镜像；

 ![image008](https://s2.loli.net/2022/06/25/ZlMv1y2VXISRqBj.png)



## 第九步

本次选择“以后安装操作系统”，点击“完成”开始创建虚拟；

![image009](https://s2.loli.net/2022/06/25/Pu9wWbogscrDv6i.png)

 

![image010](https://s2.loli.net/2022/06/25/VPWrCFNJa7mHgcI.png)

## 第十步

安装完成后，启动虚拟机开始安装操作系统；

![image011](https://s2.loli.net/2022/06/25/RdzvDhrF1pWfUJQ.png)

## 第十一步

安装完成后，启动虚拟机开始安装操作系统，点击“下一步”；

![image012](https://s2.loli.net/2022/06/25/T4znFfKsHRciAVm.jpg)

## 第十二步

点击“现在安装”按钮；

![image013](https://s2.loli.net/2022/06/25/3reuCYf7zb62mEB.jpg)

## 第十三步

可以先选择“我没有产品秘钥”选项继续安装；

![image014](https://s2.loli.net/2022/06/25/sIyBR4OEKHQdqcX.jpg)

## 第十四步

选择系统各版本，数据中心版本功能最全，“桌面体验”是指包含操作界面；

![image015](https://s2.loli.net/2022/06/25/w2bTaDEPcfMmpjt.jpg)

## 第十五步

选择“我接受许可条款”，点击“下一步”；

![image016](https://s2.loli.net/2022/06/25/z7FIXo54nTQSPUJ.jpg)

## 第十六步

选择安装类型，建议选择“自定义：……”；

![image017](https://s2.loli.net/2022/06/25/l6LfAKqNQzhMRoW.jpg)

## 第十七步

选择自定义需要新建分区并格式，点击“下一步”；

![image018](https://s2.loli.net/2022/06/25/c4xZ6wCAljU9LIk.jpg)

## 第十八步

等待安装操作系统，一般十分钟左右；

![image019](https://s2.loli.net/2022/06/25/sdVytxLQwGj4UnS.jpg)

## 第十九步

安装完成后，操作系统会自动重新启动；

![image020](https://s2.loli.net/2022/06/25/npHVTJ2dArkj4Eq.jpg)

## 第二十步

操作系统启动后，首次登录需要设置用户名密码，并且需要符合密码校验规则；

 ![image021](https://s2.loli.net/2022/06/25/RDtnubGi7AVkM51.jpg)

设置完成后，即可登录操作系统进行使用；

![image022](https://s2.loli.net/2022/06/25/XFdE7L2x8HaNjCr.jpg)



<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
