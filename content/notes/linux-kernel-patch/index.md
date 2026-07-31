---
title: 给 Linux Kernel 提了一个 Patch
summary: 向 Linux 内核主线提交代码补丁并被合并——一次独立开发者的上游贡献记录
date: '2022-01-01T00:00:00Z'
---

这不是什么大改动。但它是 Linux Kernel——世界上运行在最多设备上的操作系统内核——而且它被 Linus Torvalds 的内核主线接受了。

## 做了什么

给 Linux 内核的 USB 子系统提交了一个修复补丁。具体来说，是 `usb: gadget: f_midi` 模块中的一个问题。

- **Commit**: [`40a17923367118e32e5e413a952736dd83635b32`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=40a17923367118e32e5e413a952736dd83635b32)
- **仓库**: [git.kernel.org](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/)
- **维护者**: Linus Torvalds

## 意义

Linux Kernel 不接受"差不多就行"的代码。每一个 patch 都要经过子系统维护者的 Review，通过严格的代码风格检查（`checkpatch.pl`），并符合内核的提交规范。

这是一张入场券——证明你有能力阅读、理解、修改世界上最大的开源项目之一的源代码。

## 相关内容

- 对形式化验证语言 [TLA⁺ 的 PR 贡献](https://github.com/donghao1393)也属于同一类——在顶级开源项目中留下痕迹
- 这种"不必是核心维护者，但能精准定位问题并提交修复"的能力，是独立研究者的核心资产
