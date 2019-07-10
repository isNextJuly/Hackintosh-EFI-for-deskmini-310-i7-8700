# 目前自用稳定的EFI

### os
Mac os 10.14.5

### 设备

###### cpu:i7-8700
###### 内存：8Gx2
###### 风扇：猫扇L9i
###### 硬盘：固态Intel 760p  256G + 希捷机械 1T
###### 无线网卡：拆机卡 BCM94360CS2 
###### 显示器： 某c 4k 显示器（自动开启retina效果）

### 工作状态

- [x] 1.cpu 变频Ok 开启HWP ok
- [x] 2.核显加速 Ok
- [x] 3.声卡  Ok
- [x] 4.airdrop app store handoff ok
- [x] 5.睡眠 ok


### 可能存在不足
> 用   [BruceX Test  - 5K]()  测试Final Cut Pro 之后 ，导致 睡眠，关机，重启都失效。只能强制关机解决。

> 测试步骤： 导入xml，导出母版，观察核显加速。结束。关机屏幕变一直亮黑，机器不停电。
 



### 注意
安装前bios 设置

> * Load UEFI Defaults
> * Advanced
> * Onboard HD Audio: Enabled
> * USB Configuration, XHCI Hand-off, Enabled
> * Super IO Configuration, Serial Port, Disabled（必须）
> * Security Secure Boot, Disabled(by default)
> * CSM打开 ，仅UEFI

开启HWP（bios）设置
> * cpu 芯片组 -> CPU C STATE SUPPORT  ENABLED
> * CFG Lock   Disabled

安装后

> * 需自己生成3码

### EFI 包含文件
> * EFI
> * nvram.plist(模拟nvram需要)


### 感谢
QQ群：580456695 以及群内各位高手


