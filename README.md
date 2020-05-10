# 目前自用稳定的EFI

### 折腾往事

> 关于内存补丁驱动：OsxAptioFix3Drv.efi 和  AptioMemoryFix-64.efi 选择，多方爬帖中推荐后者，此EFI 经 试用，两者并无差异到。前者是clover 会长期支持版本。所以本次更新替换成前者。
> slide 参数大多数EFI 会选择 =0，而我的通过计算出来是 =1，其实不填发现也没什么影响。
> 核显uhd 630 虽然能 被 whatevergreen 容易驱动，但是完美还不够。 参考 文中 的可能 不足。  此处爬帖众多，不知处理方法。只知很大可能是whatevergreen的锅。



### update
> *  2020-05-10  增加opencore引导版本。
> *  2020-04-13  update to 10.15.4 and some kexts.
> *  2020-02-16  支持 原生nvram.


### os
- [x] Mac os 10.14.5
- [x] Mac os 10.15.3
- [x] Mac os 10.15.4

### 平台主板ID
###### 随机生成的，请更换一个，大家不要都用同一个，否则影响iCloud。

### BIOS version

###### p3.4(后续版本应该支持，打了bios补丁，后续版本未做测试)

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
- [x] 6.USB ok(未测试usb 扩展卡)
- [x] 7.双屏显示(网友测试，开机后HDMI需要插拔一下，网友小技巧开机完成后立马睡眠唤醒，HDMI可不用插拔，有双屏需求者注意。)


### ~~可能存在不足(其他同deskmini 310 网友的版本 试过好几个，都有这个问题。估计whatevergreen 后续升级才能解决吧)~~
### 10.15.2 和 fcpx 10.4.8 环境下，上述可能的问题已经解决。 可能fcpx 10.4.8以下版本都会有这个问题。
> 用   [BruceX Test  - 5K](https://github.com/isNextJuly/Hackintosh-EFI-for-deskmini-310-i7-8700/blob/master/BruceX%20Test%20%20-%205K.fcpxml)  测试Final Cut Pro 之后 ，导致 睡眠，关机，重启都失效。只能强制关机解决。

> 测试步骤： 导入xml，导出母版，观察核显加速。结束。关机屏幕变一直亮黑，机器不停电。
 

### Tips

> * 升级系统异常或者不成功时，可尝试清除nvram.（开机clover 界面按F11或删除EFI/CLOVER/ACPI/patched/SSDT-PMC.aml）。
> * 苹果开发用户，xcode重度用户，请远离黑苹果。
> * 此机较适合：前端，后端，安卓端。对苹果新版本系统依赖不是很强的用户。
> * 升级后维护测试时间长，请谨慎升级。


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
> * OC_EFI(用这个版本，请删除OC_)

### 感谢
QQ群：580456695 以及群内各位高手

### HWP开启意义
  [http://bbs.pcbeta.com/viewthread-1798057-1-1.html](http://bbs.pcbeta.com/viewthread-1798057-1-1.html)



