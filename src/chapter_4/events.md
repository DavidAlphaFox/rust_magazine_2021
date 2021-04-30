# 活动回顾

## Rust 唠嗑室本月汇总

- 来源：[Rust 唠嗑室](https://space.bilibili.com/25566598/video)
- 主持人：MikeTang
- 后期编辑：高宪凤

---

### 《Rust 唠嗑室》第 21 期 - Local Native 分布式应用开发

**时间**: 2021/03/30 20:30-21:30

**主讲人**：Yi Wang

**内容**：详解 Rust 实现的跨平台去中心的应用 Local Native

- demo 网络书签信息管理工具 Local Native
- 技术讲解
- 未来的目标
- demo 姐妹项目 Fastxt
- Q&A

[查看回放](https://www.bilibili.com/video/BV1wi4y1N7Ez)

**扩展资料**：

- 官方网站 [https://yilab.com/](https://yilab.com/)

---

### 《Rust 唠嗑室》第 22 期 - 关于 Rust io_uring 异步接口实现的思考

**时间**: 2021/04/13 20:30-21:30

**主讲人**：施继成

**内容**：关于 Rust io_uring 异步接口实现的思考

io_uring 接口在 Linux 中被用于高效的异步 I/O 操作，但是使用 liburing 的简单封装十分不友好，我们探索了一种实现方法，一方面能够简化接口的使用，另外一方面避免不必要的内存拷贝保证效率。借此机会和大家分享一下实现过程中的思考，也聆听大家的建议，不断改进优化实现方法。

[查看回放](https://www.bilibili.com/video/BV1VA411L7tt)

**扩展资料**：

- Liburing 库的简单封装 [https://github.com/ringbahn/uring-sys](https://github.com/ringbahn/uring-sys)
- 队列、注册器等数据结构抽象 [https://github.com/datenlord/ring-io](https://github.com/datenlord/ring-io)
- 基于 Rust 重写 io_uring 接口 [https://github.com/tokio-rs/io-uring](https://github.com/tokio-rs/io-uring)

---

### 《Rust 唠嗑室》第 23 期 - Rust From A Haskeller's View

**时间**: 2021/04/27 20:30-21:30

**主讲人**：火锅 boy 大冬冬

**内容**：Rust From A Haskller's view

从资深 Haskell 程序员的视角，试图了解 Rust 这门年轻的语言，除了从技术的角度和 Haskell 进行对比之外，也分享了关于两个语言社区发展的思考和展望

[查看回放](https://www.bilibili.com/video/BV18h411m7Gf)

---

<center> 🔥🔥🔥🔥 <strong>Rust MeetUp</strong> 🔥🔥🔥🔥 </center>

## Rust MeetUp 本月汇总

- 来源：[Rust 活动](https://space.bilibili.com/25566598/video)
- 上传者：MikeTang
- 后期编辑：高宪凤

---

### Rust Meetup 北京站

**时间**: 2021/04/10

**地点**：北京中关村创业大街

#### 【P1】 构建安全高性能的网络应用

**嘉宾**：陈天

安全共有三个维度，即：Integrity, Confidentiality, Availability。当我们谈网络安全的时候，人们首先想到的是加密、解密，其实加密、解密只是属于安全的 Confidentiality 范畴。Rust 下 TLS 支持包括：openssl, rustls(基于 ring), tokio-tls-helper。更说详情可查看视频回放。

[查看回放](https://www.bilibili.com/video/BV1R54y1b7qo?p=1)
