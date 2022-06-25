---
title: Windows服务占用磁盘和CPU
date: 2022-03-25 22:20:42
category: Windows
tags: 
    - System
---

### 问题描述：

电脑在使用过程中占用磁盘和CPU过高，导致电脑反应缓慢，查看任务管理器是Microsoft Compatibility Telemetry服务占用磁盘和CPU。

<img src="https://s2.loli.net/2022/06/25/hcEz27AZsote6xy.png" alt="image001" style="zoom:80%;" />

Microsoft Compatibility Telemetry是微软下的一个监测数据收集服务，如果加入Microsoft客户反馈改善计划，该服务就会在监测系统异常并收集反馈到微软，禁用Microsoft Compatibility Telemetry任务计划即可解决问题。

### 解决方法：

1、打开开始菜单，找到Windows管理工具下的任务计划程序；

<img src="https://s2.loli.net/2022/06/25/KERjnfBUW6azoJZ.png" alt="image002" style="zoom:80%;" />

2、展开任务程序左侧导航，任务计划程序库-Microsoft-Windows-Application Experience，然后在右面的任务计划中找到Microsoft Compatibility Telemetry计划；

<img src="https://s2.loli.net/2022/06/25/O87EuZwx4LksHhz.png" alt="image003" style="zoom:80%;" />

3、在该任务计划上点击右键禁用该任务计划；

<img src="https://s2.loli.net/2022/06/25/GAmEFXK5OyeisVY.png" alt="image004" style="zoom:80%;" />

<!--more-->

4、任务计划改为禁用状态后，以后计划任务不会再执行，如果想立刻降低硬盘和CPU的，可以通过任务管理器结束任务；

<img src="https://s2.loli.net/2022/06/25/tvSkXn5rMWuVRey.png" alt="image005" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/25/hacvbUXC3nxqNLK.png" alt="image006" style="zoom:80%;" />

<img src="https://s2.loli.net/2022/06/24/cxZCrmoFPD5JSuv.gif" style="zoom:80%;" />

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
