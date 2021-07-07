# Hackintosh-联想 XiaoXin 700-15ISK-EFI

## 提示
  **！** 该EFI版本较老，已不适用，请转诗书陌大佬的OC引导：[github.com/ShiShuMo](https://github.com/ShiShuMo/Hackintosh-LENOVO-xiaoxin700-ideapad700-Opencore-OC)

## 电脑信息

- 电脑型号	联想 80SH 笔记本电脑
- 操作系统	Windows 10 64位 ( DirectX 12 )
- 处理器	英特尔 Core i5-6300HQ @ 2.30GHz 四核
- 主板	联想 XiaoXin 700-15ISK ( 100 Series/C230 Series 芯片组 Family - A14E )
- 内存	8 GB ( 三星 DDR4 2133MHz / 金士顿 DDR4 2133MHz )
- 主硬盘	三星 MZVLB256HAHQ-00000 ( 256 GB / 固态硬盘 )
- 显卡	Nvidia GeForce GTX 950M ( 2 GB / 联想 )
- 显示器	IPS2480 R240A ( 23.6 英寸  )
- 声卡	瑞昱  @ 英特尔 High Definition Audio 控制器
- 网卡	英特尔 Dual Band Wireless-AC 3165

## 使用方法

- 将根目录处的EFI文件放入安装盘的EFI分区中即可。

## 注意

- 本EFI仅适用于10.14版本。
- 系统镜像和相关教程均可在[黑果小兵的博客](https://blog.daliansky.net/)中查找。
- 开始安装前要将BIOS中的安全启动模式关闭。

## 相关工具

镜像和软件补丁下载：[百度云](https://pan.baidu.com/s/19aCykiVi4nMQJaNzd61HZg)  提取码：ab61 

**1.软件**

- Kext Utility：在安装好系统进入桌面后，打开此软件，输入系统用户密码，开始自动建立缓存；每次新安装.Kext文件后都使用一次该软件。
- Clover Configurator：使用它可以对Clover内的文件进行编辑，使用方法参考黑果小兵。
- Hackintool：用于MacOS10.14及以后版本打声卡和显卡补丁，具体步骤参考黑果小兵。需配合.kext内核补丁文件使用。
- Etcher：Windows下使用的软件，用于制作安装镜像。

**2.Kext文件**

- Kext补丁使用方法： 将其放入黑苹果系统的EFI\CLOVER\kexts\Other文件夹内，通过CLOVER启动系统时会自动安装。
- Lilu.kext：内核扩展程序,黑果小兵的镜像内自带，已安装。配合Hackintool软件使用。
- WhatEverGreen:显卡综合修复，整合了核显、AMD、NVIDIA的综合修复，包括 （单卡启动黑屏，唤醒黑屏 等等）(依赖于Lilu)。黑果小兵的镜像内自带，已安装。
- AppleALC：动态对系统注入必要的文件/打补丁以驱动声卡(依赖于Lilu)，配合Hackintool使用。黑果小兵的镜像内自带，EFI中已安装。
- ACPIBatteryManager：笔记本电源管理补丁，没有它无法检测电池带能量信息。已安装。
- IntelGraphicsDVMTFixup：修正 Broadwell/Skylake 平台核显因 DVMT 不足而导致的死机(依赖于Lilu)。已安装。

