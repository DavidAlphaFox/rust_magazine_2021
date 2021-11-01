# 社区热点

聚焦 Rust 生态热点新闻

---

## Linus Torvalds : Rust 为 Linux 的发展带来更多乐趣，乐趣是Linux 长青的基石

> 原文： [Linus Torvalds on Community, Rust and Linux’s Longevity](https://thenewstack.io/linus-torvalds-on-community-rust-and-linuxs-longevity/)

本周，Linux创建者Linus Torvalds在北美开源峰会上进行了一年一度（[去年也做过相同主题的报告](https://thenewstack.io/linus-torvalds-on-diversity-longevity-rust-and-arm-chips/)）的报告，今年的峰会在西雅图举行（同时也包括线上）。

Torvalds周二在西雅图凯悦酒店的宴会厅登台，在下午的主题会议上接受了Linux早期贡献者Dirk Hohndel（现在也是VMware的首席开源官和副总裁）的惯例半小时提问。

仪式一开始就确认了一个特殊的时间点，将一个生日蛋糕隆重地送给了 Linus Torvalds，以纪念Linux的30周年，引来了观众的阵阵掌声。Hohndel补充说，他向 "所有的内核开发者 "致以30岁生日的祝福，它确实也是一个社区。

之后，Torvalds 开始回忆 Linux 的发展过程，包括他从 Linux 社区学到了什么。

Torvalds 认为 Linux 之所以如此长青，其中一个重要的基石就是 乐趣（Fun），并且 乐趣也是他一直追求的东西。当人们讨论 使用Rust编写一些Linux内核模块的可能性时，乐趣就出现了。

"从技术角度来看，Rust 进 Linux 内核 有意义吗？" 

当  Torvalds 被问道这个问题，他如是说：“谁知道呢。这不是问题的关键。重点是为了使一个项目保持有趣--保持乐趣--你必须玩它。”

即使现在有数十亿的设备依赖于Linux，该项目仍然强调要找到有趣的新方向来探索。"这是我非常自豪的一件事，仍然如此。"

在用C语言开发了三十年的操作系统之后，Hohndel承认他 "非常惊讶地看到 linux 对在新系统中引入Rust模块这个想法是如此开放"。

"我真的很喜欢C，"Torvalds承认。"我认为C语言是一种伟大的语言，对我来说，C语言确实是一种在相当低的水平上控制硬件的方法。因此，当我看到C语言代码时，我可以非常接近地猜测编译器的工作。它是如此接近硬件，以至于你可以用它来做任何事情"。

然而，Torvalds也看到了Hohndel的比喻，即它可能像玩电锯一样。

作为C语言的长期观察者，Torvalds知道C语言微妙的类型交互 "并不总是合乎逻辑的"，"对几乎所有人来说都是陷阱。它们很容易被忽视，而在内核中，这并不总是一件好事"。

Torvalds称Rust是 "我看到的第一种看起来像是真的可以解决问题的语言"

还有其他C语言程序员看重的考虑因素--比如高性能和易于调试--但对Rust的实验仍有一些开放性。"人们现在已经谈论Rust在内核中的应用很久了--它还没有完成，"这位Linux创建者说。"所以我们将拭目以待。

"可能在明年，我们会开始看到一些首次用Rust编写的无畏的模块，也许会被整合到主线内核中。"

主题谈话结束时，Hohndel问他们应该为Linux的50周年做什么，在2041年，他们两个都将是70多岁的人。

Torvalds的回答很有特色，就像对Linux内核一样，他不做超过6个月的计划。但这个问题确实引起了一些思考。"我做了30年的内核，非常高兴，" ，Torvalds开始思考。

"不知何故，我不认为自己在70岁时还能做内核编程。但另一方面，几年前，我也没有看到自己在50岁时做内核编程。所以......我们会看到的。"

## Linkerd 2.11 发布：更多组件向 Rust 迁移

Linkerd 之前只有 proxy 部分是 Rust 实现，在昨天发布的2.11.0版本中，Linkerd采用了一个用Rust编写的新策略控制器组件！它使用 kube-rs 进行通信。它使用 kube-rs 与Kubernetes API进行通信，并暴露了一个用Tonic实现的gRPC API。

虽然 Linkerd 在数据面有丰富的Rust经验，但他们选择Go作为控制面组件，因为Kubernetes生态系统（以及它的API客户端等）是如此严重地倾向于Go。然而，由于u/clux在kube-rs上的出色工作，现在用Rust实现控制器已经变得可行。这对Linkerd项目来说是一大进步，他们计划在整个项目中更多地使用Rust。

他们希望Linkerd的这个新方向将有助于欢迎更多希望增长Rust实践经验的贡献者。

- [policy-controller](https://github.com/linkerd/linkerd2/tree/main/policy-controller)
- [https://linkerd.io/2021/09/30/announcing-linkerd-2.11/](https://linkerd.io/2021/09/30/announcing-linkerd-2.11/)



## 【Rust 生态观察】 Rust 实现的事件处理引擎 tremor-runtime 已经在 美国最大家具电商公司 Wayfair 生产环境跑了三年

深挖了一下 tremor-runtime 项目背后的公司，原来是 Wayfair 。

Wayfair 是美国最大的家具电商，2017 年市值就达58亿美元，前身是早在2002年就成立的CNSStores。亚马逊都吃不下它。

Tremor 应该是 Wayfair 公司旗下的开源项目，已经进入 CNCF 。今年九月份还召开了一次小型的线上的 [Tremor Conf](https://community.cncf.io/events/details/cncf-tremor-community-presents-tremor-con-2021)

去年（2020）3月份的一次分享：Rust 如何为 Wayfair 省掉数千个核心和TB级的内存的成本 ：[2020-03-31-RustAndTellBerlin-functions](https://www.tremor.rs/slides/2020-03-31-RustAndTellBerlin-functions.pdf)

从2018年开始， tremor 就是跑在了 wayfair生产环境中，每天处理10兆字节的数据，或每分钟100亿条消息，每秒1000万个指标。tremor 降低了成本，减少了复杂性，巩固和简化了操作环境，以激发SRE的乐趣，减少NOC的工作量，并降低运营成本。

最近有一个 Rust 插件开发系列文章，也是出自 tremor 项目的 GSoC 挑战：[rust-plugins](https://nullderef.com/series/rust-plugins/) ，已经发布了四篇。

[tremor-runtime](https://github.com/tremor-rs/tremor-runtime)

## 使用Rust进行内核开发

在2021年的Linux Plumbers大会上，Linux的Rust开发者们都在那里进行了许多富有成效的讨论。在维护者峰会上，Miguel Ojeda从Plumbers中走出来，在一个不同的场合谈论Rust。要怎样才能让Rust补丁被合并？他得到的答案是令人鼓舞的，即使不是完全承诺的。

[https://lwn.net/Articles/870555/](https://lwn.net/Articles/870555/)

### 【官方】安卓团队正式介绍 Android Rust

Android平台提供了对用Rust开发本地操作系统组件的支持。

- Android Rust 模块 ： [https://source.android.com/setup/build/rust/building-rust-modules/android-rust-modules](https://source.android.com/setup/build/rust/building-rust-modules/android-rust-modules)
- hello Rust example: [https://source.android.com/setup/build/rust/building-rust-modules/hello-rust-example](https://source.android.com/setup/build/rust/building-rust-modules/hello-rust-example)
- Android Rust 模式: [https://source.android.com/setup/build/rust/building-rust-modules/android-rust-patterns](https://source.android.com/setup/build/rust/building-rust-modules/android-rust-patterns)

还有其他模块介绍，详细请看：[https://source.android.com/setup/build/rust/building-rust-modules/overview](https://source.android.com/setup/build/rust/building-rust-modules/overview)

## OpenSUSE 2021 Rust Survey的结果

从9月8日到10月7日，OpenSUSE帮助我主持了一个关于开发人员如何在他们的环境中使用Rust的调查。作为SUSE和OpenSUSE中Rust包的维护者，对我来说，更好地了解人们如何使用Rust是很重要的，这样我们才能做出符合社区工作方式的决定。

所有的数据都可以在这里找到: [https://fy.blackhats.net.au/blog/html/2021/10/08/results_from_the_opensuse_2021_rust_survey.html](https://fy.blackhats.net.au/blog/html/2021/10/08/results_from_the_opensuse_2021_rust_survey.html)

## Pest 项目找维护人

pest 是著名的 Rust 解析器框架，现在作者好像停止维护了。需要有人接手。有意者请参与讨论：

[https://github.com/pest-parser/pest/discussions/547](https://github.com/pest-parser/pest/discussions/547)

## 嵌入式异步的现在与未来

该文作者写过三篇嵌入式下Rust异步的系列文章：

- [Async and asleep: designing our future embedded applications](https://tweedegolf.nl/blog/58/async-and-asleep-designing-our-future-embedded-applications)
- [Measuring power consumption: sync vs. async](https://tweedegolf.nl/blog/62/measuring-power-consumption-sync-vs-async)
- [Async on Embedded: Present & Future](https://tweedegolf.nl/blog/63/async-on-embedded-present-and-future)

 在前面的两篇中，作者介绍了 嵌入式下使用 Rust 异步的好处：更好的任务管理和节省能耗。

但是实际的测试结果发现，同步和异步的能耗其实没差多少。使用 embassy 嵌入式异步运行时库可以工作的更好。

但是目前异步还有限制，比如 trait 不能包含 async 方法。幸运的是，Rust 的 泛型关联类型 （GAT）可能在今年稳定，届时可以解决这个限制。

Rust Nightly 已经实现了 trait 中支持异步方法的特性。作者试用了这个Nightly特性。

```rust
pub trait I2c<A: AddressMode = SevenBitAddress> {
    /// Error type
    type Error;
    // 这里用到了生命周期参数，需要 Nightly 下 GAT 的支持
    type ReadFuture<'a>: Future<Output = Result<(), Self::Error>> + 'a
    where
        Self: 'a;

    fn read<'a>(&'a mut self, addr: A, bs: &'a mut [u8]) -> Self::ReadFuture<'a>;
}
```

trait 里虽然不让出现异步函数，但是可以在函数实现中使用 异步块来解决：

```rust
fn read<'a>(&'a mut self, addr: u8, bs: &'a mut [u8]) -> Self::ReadFuture<'a> {
    async move {
        // implementation
    }
}
```

总之，对于嵌入式需求来说，稳定目前存在于 nightly 上的GAT 就足以为编写 async驱动 crate 提供基础，有效地推动了生态系统的发展。有了这些，嵌入式上的异步将成为一种非常有效的技术。

在准备过程中，现在可能是一个很好的时机，可以开始在夜间玩玩异步特性。一旦GAT 稳定下来，我们就可以一起建立 Rust Embedded 异步生态系统🦀❤️🦀。

