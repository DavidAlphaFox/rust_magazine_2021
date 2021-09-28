# 活动回顾

后期编辑：张汉东

> 编者按：
>
> 总结了本月的活动，包括线上和线下。
>
> 线上： 《Rust 唠嗑室》和 《RustFriday 飞书群线上沙龙》

---

# 【线上】Rust 唠嗑室本月汇总

- 来源：[Rust 唠嗑室](https://space.bilibili.com/25566598/video)
- 主持人：MikeTang
- 后期编辑：高宪凤

### 《Rust 唠嗑室》第 32 期 - `delicate` 分布式调度系统

**时间**: 2021/08/31 20:30-21:30

**主讲人**：槟橙炮炮

**题目**：`delicate` 分布式调度系统

**内容**： Rust 社区之前没有活跃的分布式调度系统项目，为了填补这个空白我开始调研实现项目，目前已经快要发布 V1.1 了。

在项目设计与底层库的实现从 smol 套件中获得了很多灵感，也会简单跟大家介绍下 smol & tokio 一些各自的设计哲学，async-process async-io async-task 一些漂亮的代码片段。

参考资料：

1. 文档地址：https://delicate-rs.github.io/
2. 源码：https://github.com/BinChengZhao/delicate

【回放】

- [https://www.bilibili.com/video/BV1av411A7RC](https://www.bilibili.com/video/BV1av411A7RC)

---

### 《Rust 唠嗑室》第 33 期 - Web3.0 与 Rust

**时间**: 2021/09/14 20:30-21:30

**主讲人**：Mike Tang

**题目**：Web3.0 与 Rust

**内容**：Mike 带你了解 Web3.0，用逻辑梳理脉络，以及 Rust 在这个潮流中的机会。

参考资料：

1. Web3.0 导论系列索引：https://rustcc.cn/article?id=632e4ecb-1b8a-477b-af4c-3e41981c7315
2. https://mp.weixin.qq.com/s/TIy9DrvxetqvCEpCiivPsg
3. https://mp.weixin.qq.com/s/vJM6TIZT2f-tnQ49cpMnrw
4. https://mp.weixin.qq.com/s/h76lTnFWlvpXs72aBVs3FA

【回放】

- [https://www.bilibili.com/video/BV1W341127BR](https://www.bilibili.com/video/BV1W341127BR)

---

<center> 🔥🔥🔥🔥 <strong>RustFriday 飞书群线上沙龙</strong> 🔥🔥🔥🔥 </center>

# 【线上】RustFriday 飞书群线上沙龙

每周五晚八点，限定两个主题：语言特性和开源项目，在线讨论。

Rust 中文社群 飞书群 邀请你加入：

对话群： [https://applink.feishu.cn/TeLAcbDR](https://applink.feishu.cn/TeLAcbDR)

话题群：[https://applink.feishu.cn/TeLD868w](https://applink.feishu.cn/TeLD868w)

视频来源：[https://space.bilibili.com/24917186](https://space.bilibili.com/24917186)

## 第十九期 | Rust 与架构

分享者：张汉东

【讨论主题】

1. 架构的终极目标是用最小的人力成本来构建可维护的系统。但是 开发者的过度自信 始终阻碍着达成这个目标。
2. 「先快速上线，后面再重构」，但实际上，永远没有重构的机会。
3. 系统的行为价值（软件正常工作）和架构价值（软件的可修改能力）对你来说，哪个更重要？
4. 在编程范式、设计原则、组件原则、架构模型上依次对 Rust 语言的表现进行了探讨。
5. 嵌入式 Rust 生态正在遵循 嵌入式整洁架构 而构建

【参考资料】

1. [https://zhuanlan.zhihu.com/p/378085465](https://zhuanlan.zhihu.com/p/378085465)
2. [https://github.com/tomaka/rouille](https://github.com/tomaka/rouille)

【回放】

- [https://www.bilibili.com/video/BV1m3411i7vk](https://www.bilibili.com/video/BV1m3411i7vk)
