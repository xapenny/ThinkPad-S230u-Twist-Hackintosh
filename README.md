

# ThinkPad S230u Twist Hackintosh

### 前言

> 这台机子我大概是从17年开始折腾黑果。这台机器最开始黑的是10.11，然后10.12、10.13再到现在的10.14。从一开始的一片voodoo进系统一直到后期慢慢完善，最终到现在的完美。可以说基本都是我自己折腾出来的。当然在一开始的时候群里的朋友帮了我不少。但到后期由于网络上缺少关于这台机器的资料，很多别人能成功的东西到我这就不行了，需要我自己慢慢摸索。其实我的黑果在18年的6月份左右就基本完美了，只是因为19年高考复习所以一直没时间把这些东西总结出来。希望我发出来的东西能帮到一些人吧。

### 注意

1. 无论OC还是Clover我在config里都去掉了机器序列号和UUID，如果需要iMessage的要自己写入白苹果三码
2. 本套配置默认使用OpenCore引导，使用前需要在BIOS里修改一些项目，具体细节请参考[黑果小兵的OpenCore教程](https://blog.daliansky.net/OpenCore-BootLoader.html)
3. 如果想使用Clover，请先移走`/Boot`目录下的`BOOTx64.efi`,并将`Clover_BOOTX64.efi`重命名为`BOOTx64.efi`

---

### 配置

|   硬件   | 描述                                                         |
| :------: | ------------------------------------------------------------ |
|   CPU    | Intel(R) Core(TM) i5-3317u CPU @ 1.70GHz                     |
|   RAM    | 4 GB 1333 MHz DDR3                                           |
|   硬盘   | - SATA: Samsung SSD 860 EVO mSATA 250GB <br/>- mSATA: SAMSUNG MZMPA024HMCD-000L1 24GB |
|   显卡   | Intel HD Graphics 4000 1536 MB                               |
|   声卡   | Realtek ALC269VC                                             |
| 有线网卡 | Realtek RTL8168E-VL/8111E-VL PCI Express Gigabit Ethernet    |
| 无线网卡 | Broadcom BCM94352HMB                                         |
|  显示器  | - Built-in: ThinkPad LCD (1366x768)<br/>- Display-Port: Philips 193E (1440x900) |

---

### 工作正常

- 系统启动
- 显卡
- 无线网卡 (需要更换和刷白名单)
- AppleALC声卡内建 (支持自动切换)
- USB3.0
- 键盘亮度/音量调节按钮
- 触控板/小红点
- 摄像头
- CPU/GPU变频
- 睡眠/唤醒
- 电池百分比显示
- ~~HandOff~~
- ~~个人热点~~
- AirDrop
- iCloud/iMessage/FaceTime (需要自己写白苹果三码)
- 外接显示器 (HDMI/DP)

---

### 已知问题

1. HandOff 功能部分失效
2. Instant Hotspot 功能部分失效

---

### 适用系统

- macOS 10.12 Sierra
- macOS 10.13 High Sierra 
- macOS 10.14 Mojave
- macOS 10.15 Catalina

---

### 更新日志

- 2019.11.8

> 1.更新支持macOS 10.15 Catalina
>
> 2.加入OpenCore引导
>
> 3.修复了一个导致AppleALC找不到输入设备的问题

---

### 最后的尾巴

- ~~目前我的黑果目标主要是搞定OC引导和10.15，在这两个方向我遇到了比较大的困难。我遇到的问题非常罕见，甚至我去找OC原作者都问不出原因，新一轮的折腾就这样开始了(笑)~~ **FUCK IT**
- 如果在使用我的文件当中出现了什么问题也欢迎来问我<xapenny@roselia.club>