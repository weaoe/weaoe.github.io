---
title: 常用软件收藏和下载
date: 2022-04-27 22:08:36
category: Software
tags: 
    - Software
---

微软 PowerToys 是免费的系统实用工具套件，从 Windows XP 时代复活，并于 2019 年 5 月引入Windows10系统。可以用于高级用户调整和简化 Windows 操作，以提高效率。通过与 Windows 10/11搭配使用，同时让用户可以自定义各种高效快捷操作。

<img src="https://s2.loli.net/2022/08/03/LdUJPyAbRKwk346.webp" alt="PowerToys" style="zoom:80%;" />
今天PowerToys 迎来 **0.61.1 版本**，包含始终置顶、FancyZones 和 PowerToys Run 等方面的多项错误修复，详细内容详见官方说明，具体如下：

### 常规

- 已将 Windows 应用 SDK 运行时升级到 1.1.2。
- 新的 Windows 11 上下文菜单项现已正确添加到 Windows 11 开发人员频道内部版本。（这是 0.60 的修补程序）
- 旧的上下文菜单项与新的 Windows 11 上下文菜单项一起显示，以便与覆盖 Windows 11 上下文菜单行为的软件兼容。（这是 0.60 的修补程序）
- 跨解决方案的合并 C# 语言版本。谢谢[@davidegiacometti]！
- 删除了已弃用的 Segoe 图标字形代码，并将其替换为正确的代码。谢谢[@niels9001]和[@Jay-o-way]！
- 修复了在启用某些模块时导致在某些键盘布局上随机按下重音键的问题。

### 始终处于顶部

- 修复了激活时边框闪烁的问题。谢谢[@davidegiacometti]！
- 修复了导致 Always on Top 在退出 PowerToys 时激活并挂起的错误。谢谢[@davidegiacometti]！
- 修复了圆角上出现的黑边。
- 修复了导致 100% CPU 消耗的错误。

### 花式地带

- 修复了当许多显示器报告具有相同的序列号时导致布局无法正确应用的错误。（这是 0.60 的修补程序）
- 修复了导致布局无法在某些虚拟监视器设置上正确应用的错误（这是 0.60 的修补程序）
- “行”默认布局现在应用于垂直监视器，而不是“列”布局。谢谢[@augustkarlstedt]！

### 图像调整器

- 屏幕阅读器现在宣布大小名称而不是类名称。

### 文件资源管理器加载项

- 修复了为使用 Inkscape 创建的 SVG 文件创建缩略图时出现的问题。

### 键盘管理器

- 调整了当键被孤立时编辑器上的措辞。

### 鼠标实用程序

- 修复了导致当前“查找我的鼠标”聚光灯在屏幕左上角激活时挂起的错误。（这是 0.60 的修补程序）

### PowerRename

- “PowerRename”窗口在创建时会对当前 dpi 做出反应。

### PowerToys Run

- 修复了WindowWalker插件UI中的拼写错误。谢谢[@rohanrdy]！
- 通过在退出时仅保存搜索历史记录文件提高了性能。谢谢[@davidegiacometti]！
- PowerToys Run 在全局查询中查询空格时不再显示某些插件的结果。谢谢[@davidegiacometti]！
- 添加了对在程序插件中显示某些 win32 程序的本地化名称的支持。谢谢[@htcfreek]！
- 程序插件现在将考虑直接在ProgramPluginSettings.json中更改的设置。谢谢[@bezgumption]！

### 设置

- PowerToys 运行设置页面会在插件不是全局时将分数调整设置正确显示为灰色。谢谢[@jefflord]！
- PowerToys Run 插件分数调整字段仅接受数字字符。谢谢[@jefflord]
- 如果直接从其可执行文件启动，则不会运行，就像 WinUI 3 升级之前一样。
- 修复了 PowerToys Run 设置页面描述中的拼写错误。谢谢[@eltociear]！

### 安装

- 删除了死代码以制作 msix 安装程序。
- 将 .NET 依赖项更新到了 6.0.7。
- 如果用户已手动删除 PowerToys 快捷方式，则不会在更新时创建新的 PowerToys 快捷方式。

### 发展

- 更新了 Windows 应用商店包提交脚本，以便在安装 PowerToys 时显示较少的 UI。（这是 0.60 的修补程序）
- 向监视器报告工具添加了更多功能。
- 发布 CI 现在在符号工件中包含版本号。
- GitHub 现在应该将 .vsconfig 显示为 JSON 文件。谢谢[@osfanbuff63]！
- 集中了 NetAnalyzers 和 StyleCop 的配置。谢谢[@davidegiacometti]！
- 拼写检查已升级到版本 0.0.20。谢谢[@jsoref]！

下载地址：[Releases · microsoft/PowerToys · GitHub](https://github.com/microsoft/PowerToys/releases)

原文地址：[Release Release v0.61.0 · microsoft/PowerToys · GitHub](https://github.com/microsoft/PowerToys/releases/tag/v0.61.0)

---

## <center>欢迎关注公众号收藏小程序</center>

![河洛先生](https://s2.loli.net/2022/06/23/bYdtKDC2U5J7iWr.jpg)![河洛先生](https://s2.loli.net/2022/06/23/PlUgz5KSHm7OBke.jpg)
