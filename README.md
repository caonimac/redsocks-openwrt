RedSocks for OpenWrt
===

简介
---

本项目是 <a href="https://github.com/darkk/redsocks">RedSocks</a> 在 OpenWrt 上的移植
 当前版本: 0.5
  

编译
---

 - 从 OpenWrt 的 [SDK][S] 编译  

  
   # 以 ar71xx 平台为例
   tar xjf OpenWrt-SDK-ar71xx-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
   
   cd OpenWrt-SDK-ar71xx-*
   # 获取 Makefile
   git clone https://github.com/caonimac/redsocks-openwrt.git package/redsocks
   # 安装依赖包源码
   ./scripts/feeds update base && ./scripts/feeds install -a
   # 选择要编译的包 Network -> redsocks
   make menuconfig
   # 开始编译
   make package/redsocks/compile V=99
   # 运行
   service redsocks start
