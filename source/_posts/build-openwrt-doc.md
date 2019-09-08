---
title: Openwrt编译指导文档
date: 2019-09-03 22:19:00
categories: 
- 驱动开发
tags:
- Openwrt
---

#### 1. 官方指导文档

https://openwrt.org/zh-cn/doc/howto/build

#### 2. 查看板卡支持情况

https://openwrt.org/toh/start

​	之前openwrt是不支持树莓派3B+版本编译的，所以，对应的支持版本需要通过官方查询。通过查找到的结果，也可以点击查看详细的板卡信息及CPU信息。

https://openwrt.org/toh/hwdata/raspberry_pi_foundation/raspberry_pi_3_bplus

#### 3. 编译

编译过程非常消耗时间，时间主要消耗在下载各种源码包。

这里提供几个可以手动下载到源码包的网址

1.  http://sources.openwrt.org/   这个网址上比较齐全，基本都能找到对应的源码包。
2. http://openwrt.bjbook.net/download/
3. https://gitee.com/ziguayungui/Openwrt_18.06_dl 我将自己用到的源码包上传到了码云上面，国内下载的速度比github快很多。