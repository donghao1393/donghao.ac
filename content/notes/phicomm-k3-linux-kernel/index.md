---
title: 我给 Linux Kernel 写了一段代码
summary: 斐讯暴雷后，用三个月把一台变砖的路由器写进了 Linux 内核——72 行代码，最终进入了全球数十亿台设备
date: '2019-10-28T00:00:00Z'
---

2018 年冬天，我坐在老家安徽安庆的公寓里，面前摆着一台电烙铁、一管助焊剂，和一台花了近两千元买来的路由器——斐讯 K3。

斐讯暴雷了。它用"零元购"的模式吸引了大量用户购买高端路由器，承诺全额返现，然后资金链断裂。成千上万的人血本无归。我手里这台 K3——BCM4709C0 处理器、512MB 内存、双频 WiFi、甚至还有一块 LCD 小屏幕——一夜之间变成了一堆电子垃圾。

## 决定

我决定让它活过来。

具体来说：把斐讯 K3 的硬件描述写进 Linux 内核主线。这样，任何运行 Linux 的系统——包括 OpenWrt 开源路由器固件——都能原生识别并支持这台设备。不用再依赖斐讯（已经消失）的官方固件更新。

这意味着我要写一个**设备树源文件**（Device Tree Source, DTS）——一份描述硬件组成的结构化数据，告诉 Linux 内核"这台设备有什么芯片、多少内存、WiFi 模块怎么接线"。

## 三个月

我不知道怎么做。所以我把能学的都学了：

1. **焊接**。K3 主板上有些硬件信息需要直接读取。我买了电烙铁和助焊剂，对着网上找来的焊接教程视频，自己摸索着完成了第一次硬件操作。
2. **"文档"**。没有现成的。Linux 内核的设备树规范写得抽象，Broadcom BCM5301X 系列的硬件细节不在任何官方文档里。我用的是最笨的办法——在 OpenWrt 源码里找参数相近的其他路由器固件，一个文件一个文件地比对，一个参数一个参数地试，把 K3 的硬件规律从零总结出来。
3. **`git send-email`**。Linux 内核不用 GitHub PR。它用邮件列表。我花了整整一个周末学习如何用 `git format-patch` 生成补丁，用 `git send-email` 通过 SMTP 发给内核邮件列表。

## 提交

2019 年 1 月 20 日 23:33（北京时间 1 月 21 日凌晨），我的补丁出现在 Linux 内核邮件列表中。

```c
// SPDX-License-Identifier: GPL-2.0-or-later OR MIT
/*
 * Copyright (C) 2017 Hamster Tian <haotia@gmail.com>
 * Copyright (C) 2019 Hao Dong <halbertdong@gmail.com>
 */

#include "bcm47094.dtsi"

/ {
    compatible = "phicomm,k3", "brcm,bcm47094", "brcm,bcm4708";
    model = "Phicomm K3";

    memory@0 {
        device_type = "memory";
        reg = <0x00000000 0x08000000>,
              <0x88000000 0x18000000>;
    };
    // ...
};
```

这个文件不长。但每一行参数都是我从零散的固件代码中比对出来的——没有用万用表逐个测量，靠的是从一堆看似不相关的信息里抽象出正确的硬件模型。

OpenWrt 开发者 **Rafał Miłecki** 帮我清理了代码格式，Broadcom 子系统维护者 **Florian Fainelli** 在 1 月 31 日合并了补丁。

## 它去了哪里

大约十个月后——2019 年 10 月——我收到一封 GitLab 的自动通知。镜像仓库出了问题，我点进去一看……等等，这封通知说的是我的代码已经不在我的仓库里了。它**在上游**。

Linux Kernel mainline。Linus Torvalds 的仓库。

后来我意识到：**全球每一台安卓手机都运行着 Linux 内核。** 我的 72 行代码——在这个世界上运行次数最多的软件项目里——是其中的一部分。

我不是内核的核心贡献者。我没写调度器，没修安全漏洞，没优化内存管理。我只是让一台被资本游戏抛弃的路由器，重新获得了自由。

---

[在 kernel.org 查看这个 commit](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=40a17923367118e32e5e413a952736dd83635b32)
