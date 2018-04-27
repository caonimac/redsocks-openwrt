RedSocks for OpenWrt
===

简介
---

 <p>本项目是 <a href="https://github.com/darkk/redsocks">RedSocks</a> 在 OpenWrt 上的移植<br>  
 当前版本: 0.5
  

编译
---

 - 从 OpenWrt 的 [SDK][S] 编译  

   ```bash
   # 以 ar71xx 平台为例
   tar xjf OpenWrt-SDK-ar71xx-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
   cd OpenWrt-SDK-ar71xx-*
   # 获取 Makefile
   git clone https://github.com/caonimac/redsocks-openwrt.git package/redsocks
   # 选择要编译的包 Network -> redsocks
   make menuconfig
   # 开始编译
   make package/redsocks-dev/compile V=9
   # 修改redsocks.conf
   vi /etc/redsocks.conf
   # 运行
   redsocks -c /etc/redsocks.conf
   
   
   ```


  
