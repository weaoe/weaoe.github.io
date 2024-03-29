---
title: Visual Studio发布.NET Core项目的方法
date: 2022-06-25 22:20:03
category: Windows
tags: 
    - DotNet
---

**Visual Studio**是一款专为程序开发人员设计，支持 Windows 和 Mac系统，适用范围广，操作简单的专业IDE开发环境，调试器功能更加丰富，更快的负载解决方案，以及更快的编译。

<img src="https://s2.loli.net/2022/06/25/VG1X5Qx3whl6yAp.jpg" alt="VS" style="zoom:80%;" />

Visual Studio的.NET Core跨平台开发功能，帮助用户实现一次开发多平台部署，下面主要介绍关于.NET Core项目发布的一些设置。

### 第一步

项目上点击右键，选择发布；

<img src="https://s2.loli.net/2022/06/25/Ws8cbKNuXR2a3LP.png" alt="image001" style="zoom:80%;" />

### 第二步

发布类型选择“文件夹”方式，根据情况也可以选择发布到FTP、Web服务器等方式，主要涉及到一些实际环境系统配置参数的区别，此处使用文件夹方式发布，然后手动更新服务。

对于大型互联网公司是有专门的发布以及更新线上环境的流程，可以保证显示系统的不间断运行的。

<img src="https://s2.loli.net/2022/06/25/b42K9EgvzhUFj7S.png" alt="image002" style="zoom:80%;" />

### 第三步

选择文件夹的存储位置，一般为本地计算机路径，对于网络位置，局域网内也很方便，如果是外部网络就和网络带宽有较大关系；

<img src="https://s2.loli.net/2022/06/25/2NWuK1qenwHMsUo.png" alt="image003" style="zoom:80%;" />

<!--more-->

### 第四步

以上设置完成后，可以对分项目发布进行编辑、重命名、删除等；

<img src="https://s2.loli.net/2022/06/25/zfuWqrGFxCoS7i8.png" alt="image004" style="zoom:80%;" />

### 第五步

重命名发布配置名称，方便区分管理多个项目，也可以通过名称来标识各个各个配置的主要用途等；

<img src="https://s2.loli.net/2022/06/25/emnJT2lCPfyrRNL.png" alt="image005" style="zoom:80%;" />

### 第六步

编辑发布配置，直接点击下一步跳转到设置选项；

配置包含“Debug”和“Release”，一般正式发布使用Release选项，可以减少项目文件的大小（也不会减少提多），而是用Debug选项，主要用在测试环境，出现问题时可以分析更多的错误异常；

<img src="https://s2.loli.net/2022/06/25/xUKMTtLDgH9NaJn.png" alt="image006" style="zoom:80%;" />

### 第七步

目标框架，是项目创建时已经确定了的，如果升级过项目，存在多个项目框架的情况，根据项目选择；

### 第八步

部署模式和目标运行时关联的，不同的部署模式适用于不同的目标运行时；

框架依赖模式，此模式发布的项目，目标服务器只需安装一次运行时环境，各个项目共用，这样发布的项目包小一些，但是各个项目的运行时环境必须一致才可以；

独立模式，此模式发布的项目，项目包内包含运行时环境，每个项目的运行环境单独引用，避免了互相冲突等异常问题，这样发布的项目包占用空间大，而且更新方便，不影响其他项目运行时的环境，不过以目前多数服务器的空间，可以忽略运行时文件占用的空间；

框架依赖和独立模式对目标运行时的影响，主要是选择独立部署时没有“可移植”选项，其它的都一致，可以部署在Windows、Linux以及苹果的OSX平台。

<img src="https://s2.loli.net/2022/06/25/pyuON7if4DU2aRG.png" alt="image007" style="zoom:80%;" />



<img src="https://s2.loli.net/2022/06/25/osrRDwtQhCZqHJi.png" alt="image008" style="zoom:80%;" />

### 第九步

文件夹发布选项：

生成单个文件，在发布后会将项目程序集包含在一个文件中，简化文件夹内的目录结构；

启用Ready Run选项，启用后能提升系统的启动运行速度，会稍微增加文件的大小（增量可以会儿不计）；

裁剪未使用的程序集，可以减小项目发布后的总体大小；

发布前删除所有现有文件，建议启用，保证每次发布后文件夹内都为最新文件；

设置完成后保存，点击发布按钮即可成功发布项目。

<img src="https://s2.loli.net/2022/06/25/pNPMcGtQgwUIi7X.png" alt="image009" style="zoom:80%;" />



<img src="https://s2.loli.net/2022/06/25/cqzj5xbPTmNitpr.png" alt="image010" style="zoom:80%;" />



---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
