# ASRock-B560M-ITX-AC-Hackintsh

我的配置信息

|  CPU | Intel i5 10400 |
|---|---|
|  GPU | 盈通 5600xt 萌宠 6g  |
|  主板 | ASRock B560M-ITX/AC |
|  内存 |  镁光 铂胜 3200 8G * 2   |
| 机型  |  iMac 20,1 |
|  以太网 | Intel I219V|
| 无线网卡 | AC3168 |

# 非正常工作
* 麦克风输入
* 自带蓝牙 可以连接蓝牙耳机音响等 但手动关闭后无法打开
* 核显无法输出(B560芯片组目前无解)
* 除此之外 我目前的功能使用 一切正常

# Bios 设置
* Advanced • CPU Configuration • CFG Lock = Disabled
* Advanced • Chipset Configuration • Above 4G Decoding = Disabled | or Enabled
* Advanced • Chipset Configuration • IGPU Multi-Monitor = Disabled
* Advanced • USB Configuration • XHCI Hand-off = Enabled
* Security • Secure Boot = Disabled

# 一些小建议
* 如果您需要使用板载Wi-Fi的话可以看看 [itlwm](https://github.com/OpenIntelWireless/itlwm) 这边要求根据自己系统来选择 然后拖入kext和config即可
* 如果需要用到 隔空投送 接力 等Apple原生功能建议搭配 拆机免驱卡 使用
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
* 去除 -v 啰嗦模式
* <img width="586" alt="8E3C0FFF-9042-4844-BF89-C5492F67B3BE" src="https://user-images.githubusercontent.com/53895501/135744045-31dc9a0e-5fff-4ebd-b52b-cf401a3ee36f.png">

