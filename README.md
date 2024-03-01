# proj306-Rust-OS-for-Box-Kernel-Architecture
# 基于框内核架构的Rust OS实践与创新

## 项目描述

> 宏内核的性能，微内核的安全

[框内核（framekernel）](https://asterinas.github.io/book/kernel/the-framekernel-architecture.html)
是一种面向Rust内核的新型OS架构，
可匹敌宏内核的性能，媲美微内核的安全。
框内核的基本思想是将一个Rust内核分为**OS框架**和**OS服务**两大部分，
其中只有OS框架部分被允许使用unsafe Rust，
而OS服务必须完全基于safe Rust编写，
使得该内核的内存安全性仅需依赖于一个极小范围内的代码（可信基），
且无需引入额外的硬件隔离和性能开销。

[星绽（Asterinas）](https://github.com/asterinas/asterinas)
是一个致力于打造生产级Rust内核的开源社区，旗下有三个主要项目：
1. [星绽Kernel](https://asterinas.github.io/book/kernel/index.html)
是一个高效、安全、通用的OS内核，基于Rust语言和框内核架构，提供Linux ABI；
2. [星绽Framework](https://asterinas.github.io/book/framework/index.html)
是第一个满足框内核架构要求的、对OS框架部分的实现，
星绽Kernel就是基于星绽Framework实现的；
3. [星绽OSDK](https://asterinas.github.io/book/osdk/index.html)
是一个适用于框内核的、Rust OS开发工具包，
可大幅OS开发者的工作效率、降低入门门槛。

本题目希望通过OS比赛的形式
向同学们分享和传递框内核架构的技术理念，
鼓励同学们加入星绽开源社区中共同探讨和进度，
帮助同学们参与到开源运动中，
共同推动Rust内核的技术进步。

## 预期目标

本项目希望参赛学生能够扩展星绽Kernel
或者利用星绽Framework开发新的OS内核。

**以下预期目标都是建议性的，学生可以选择其中一项或者多项。
选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标。**

1. 基于星绽Framework构造一个新的微内核（2.3.2 新型内核）
2. 基于星绽Framework构造一个新的实时操作系统（2.3.2 新型内核）
3. 将星绽Kernel移植到Arm或RISC-V等CPU架构上（2.3.5 内核移植）
4. 将星绽Kernel移植到AMD SEV等VM TEE环境下（2.3.7 安全操作系统/可信执行环境）
5. 给星绽Kernel增加新的文件系统（2.3.3 文件系统）
6. 给星绽Kernel增加namespace和cgroup等Linux支持（2.3.6 内核完善）
7. 给星绽Kernel实现KVM的功能（2.3.1 虚拟化）

## 参考资料

* 星绽的Github组织：https://github.com/asterinas
* 星绽的技术文档：https://asterinas.github.io/book
* 星绽的社区论坛：https://asterinas.zulipchat.com/

## 赛题分类

本题目所属的大类是：
* 操作系统内核大类

## 参赛要求

* 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生
* 允许学生参加大赛的多个不同题目，最终自己选择一个题目参与评奖
* 请遵循“2024全国大学生操作系统比赛”的章程和技术方案要求

## 额外激励

* 社区认可：如果参赛同学的代码被星绽旗下的项目接收，该同学将得到星绽社区[官方致谢页面](https://asterinas.github.io/contributors.html) 的感谢。
* 编程之夏：星绽社区将在2024年组织编程之夏，选择本题目的同学会被社区优先考虑。完成编程之夏的同学将得到实物或现金奖励。

## 难度

中等至高等

## License

Mozilla Public License (MPL), Version 2.0，或其他与MPLv2兼容的开源许可。

## 所属赛道

2024全国大学生操作系统比赛的“OS功能挑战”赛道

## 项目导师

- 姓名：田洪亮
- 单位：蚂蚁集团
- email：tate.thl AT antgroup.com
- zulip：Hongliang Tian (Tate) on [Zulip](asterinas.zulipchat.com)
