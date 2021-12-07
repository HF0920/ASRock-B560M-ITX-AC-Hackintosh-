# ASRock-B560M-ITX-AC-Hackintsh

| ITX| 配置单 |
|---|---|
|  CPU | Intel i5 10400 |
|  主板 | ASRock B560M-ITX/AC |
|  GPU | 盈通 5600xt 萌宠 6g  |
|  内存 |  镁光 铂胜 3200 8G * 2   |
|  以太网 | Intel I219V|
| 无线网卡 | BCM94360CS2 |
| 机箱及延长线 | 超频三蜂鸟2 自带延长线 |

# <p align="right">[EFI下载地址](https://github.com/HF0920/ASRock-B560M-ITX-AC-Hackintosh-/releases)</p>

# 非正常工作
* 麦克风输入
* 核显无法输出(B560芯片组目前无解)
* 除此之外 我目前的功能使用 一切正常

# Bios 设置 （高级模式F6）
* <h2>高级</h2>

* <h3>CPU配置</h3>
* CFG LOCK  关闭

* <h3>芯片组配置</h3>
* Above 4G Decoding  启用
* VT-D  禁用
* 共享内存  64M
* IGPU 多监视器  开启
 
* <h3>USB配置</h3>
* XHCI Hand-off  开启
 
* <h3>可信赖运算</h3>
* Security Device Support  关闭
* Disable Block Sid  关闭
 
* <h2>安全</h2>
* 安全启动  关闭

* <h2>引导</h2>
* 闪速启动  关闭
* CSM  关闭

# 一些小建议
* 在V1.4版本后 我移除了对Intel网卡的支持以达到更快的启动 如果有板载无线网卡需要 可以自己加入[Wi-Fi驱动](https://github.com/OpenIntelWireless/itlwm)、[蓝牙驱动](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)以及[BlueToolFixup驱动](https://github.com/acidanthera/BrcmPatchRAM/) 等后续可能更新的驱动程序
* 如果需要用到 隔空投送 接力 等Apple原生功能建议搭配 拆机免驱卡 使用 我目前使用的BCM94360CS2+延长线 体验十分完美
* 建议开机点亮后第一件事就是重新使用OpenCore Configurator工具 生成三码 以获得更好的使用体验
* 如果你使用了显卡延长线接显卡的话 可能遇到设置完BIOS无法点亮的问题 建议先拔下独显设置BIOS后 进入install流程前再安装独立显卡
* 请勿使用单核显安装 目前B560主板的板载核显输出可能没有办法使用 我在系统层已经驱动了核显 并且实现了双显卡的硬件加速 但核显仍无法输出

# 预览
<img width="2560" alt="截屏2021-10-02 11 27 56" src="https://user-images.githubusercontent.com/53895501/135702232-6f585c70-a13b-4090-b098-4f7a81e61b13.png">



# 更新日志

v1.1 2021.10.2 
* 更新OC引导至7.3 
* 更改机型为iMac 20,1 
* 替换 UHD 630 缓冲帧 以实现更好的硬件加速

v1.2 2021.10.3 
* 更新OC引导至7.4
* 替换intel蓝牙驱动为BlueToolFixup 使在 Monterey 能够正常工作
* 添加 macOS Monterey Beta(21A5534d) 支持
* 添加图形化引导菜单
* <img width="586" alt="8E3C0FFF-9042-4844-BF89-C5492F67B3BE" src="https://user-images.githubusercontent.com/53895501/135744045-31dc9a0e-5fff-4ebd-b52b-cf401a3ee36f.png">

v1.3 2021.11.19 
* 更新OC引导至0.75
* 更新Lilu、AppleALC、WhateverGreen、RestrictEvents驱动为当前最新

v1.4 2021.12.7 
* 更新OC引导至0.76
* 因本人更换BCM94360CS2免驱网卡 现已在此版本上移除对 Intel AC3168 支持
