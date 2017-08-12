rtl8188eu
=========

Repository for the stand-alone RTL8188EU driver.

Compiling & Building
---------
### Dependencies
To compile the driver, you need to have make and a compiler installed. In addition,
you must have the kernel headers installed. If you do not understand what this means,
consult your distro.
### Compiling

> make all

### Installing

> sudo make install

DKMS
---------
The module can also be installed with DKMS. Make sure to install the `dkms` package first.

    sudo dkms add ./rtl8188eu
    sudo dkms build 8188eu/1.0
    sudo dkms install 8188eu/1.0

Submitting Issues
---------

Frequently asked Questions
---------

### The network manager says: "Device is not ready"!
Make sure you copied the firmware (rtl8188eufw.bin) to /lib/firmware/rtlwifi/

我有一个8188eu的无线网卡，可以用来调试熟悉linux下的驱动程序。我对linux驱动了解较少，只是看代码并添加一些中文注释，希望可以学到一些有用的的东西。你也有兴趣可以一起交流。
一些名词解释：
AP access point 无线接入点
STA station 无线终端
BSS 多个STA在一定范围内(也许是AP范围内)可以互相通信，构成一个BSS
BSSID是一个BSS的标识，如果有就是AP的mac地址
ESS 多个BSS可以构成一个扩展网络ESS，扩展服务集
SSID是一个ESS的网络标识,也是网络的使用名称例如"TPLink-xxx"

