# 官方动态

编辑： 张汉东

---

## Rust 1.55 stable版本已经发布

可以通过以下命令安装：

```
$ rustup update stable
```

具体可见[Rust 1.55特性介绍](https://blog.rust-lang.org/2021/09/09/Rust-1.55.0.html)。概括而言，新的特性包括：

- Cargo
  - 不再重复展示cargo test中显示的重复编译错误
- 标准库
  - 使用[Eisel-Lemire algorithm](https://github.com/rust-lang/rust/pull/86761)算法来解析浮点数
  - std::io::ErrorKind类型更新：原先未分类错误的类型为ErrorKind::Other，避免和常用自定义错误类别冲突，1.55中将此类错误的类别改为ErrorKind::Uncategorized
  - range在match中可以不写上限或下限了，支持类同 1.. 的写法，详情见https://github.com/rust-lang/rust/pull/83918
  - 确定一些方法和trait的实现

Rust 官方发布 1.55 的时候在博客里还特意纪念了最近刚去世的 Anna Harren。

Anna Harren 是第一个将 Rust 的 `::<>` 语法命名为 Turbofish 的人。

[https://twitter.com/garblefart/status/627886036211900416](https://twitter.com/garblefart/status/627886036211900416)


## 构建安全的 I/O

最近Rust官方合并了一个[ RFC ](https://github.com/rust-lang/rfcs/blob/master/text/3128-io-safety.md)，通过引入I/O安全的概念和一套新的类型和特征，为AsRawFd和相关特质的用户提供关于其原始资源句柄的保证，从而弥补Rust中封装边界的漏洞。

相关资源：

- [https://github.com/smiller123/bento](https://github.com/smiller123/bento)
- [https://github.com/bytecodealliance/rsix](https://github.com/bytecodealliance/rsix)
- [https://github.com/rust-lang/rfcs/blob/master/text/3128-io-safety.md](https://github.com/rust-lang/rfcs/blob/master/text/3128-io-safety.md)

## GitHub Advisory Database（安全咨询数据库）现在已经支持 Rust 了

下一步将支持  dependabot ， dependabot是 GitHub 推出的一个提醒依赖更新机器人，当你项目的依赖有更新的时候就会自动推送一个 Pull requests。

GitHub Advisory Database 官方写道：

这一覆盖范围确保了Rust社区的任何成员都可以在他们的代码所在的同一个地方检查安全问题：GitHub上。这仅仅是第一步! 请查看我们的公共路线图，我们正在努力实现Rust对依赖关系图和Dependabot警报的支持。

谢谢你，RustSec和Rust社区!
在我们努力将Rust生态系统加入咨询数据库的过程中，我们得到了RustSec和Rust社区的大量支持。

我们非常感谢RustSec，这是一个独立的组织，负责收集、规范和发布与Rust库相关的安全建议。它的免费公共数据库是我们自己的Rust漏洞数据集的起点。

我们计划继续与RustSec和更广泛的Rust社区合作，使我们自己的GitHub安全咨询数据可用并易于使用，以进一步补充他们的数据。通过合作，我们可以为减少漏洞的可见性问题做更多的工作，而不是单独行动。

[https://github.blog/2021-09-23-github-advisory-database-now-supports-rust/](https://github.blog/2021-09-23-github-advisory-database-now-supports-rust/)

## Rust 1.56 beta1 (2021版)现已发布！!

你现在可以用rustup安装2021测试版了。

使用`rustup default beta`切换到最新的测试版，然后你可以将你的toml文件迁移到 `edition="2021"` 或者用`cargo new`启动一个使用21版的新项目。

关于现有项目的迁移过程的一些信息:

[https://doc.rust-lang.org/cargo/commands/cargo-fix.html](https://doc.rust-lang.org/cargo/commands/cargo-fix.html)

## Rustaceans 准则

Niko 发布了一篇博客，总结出 Rustaceans 的准则，比如其中提到：

Rust 赋予系统以下能力：

- ⚙️  可靠性: "如果它能编译，它就能工作"
- 🐎 高效性："惯用代码高效运行"
- 🥰 支持性："语言、工具和社区都在这里提供帮助"
- 🧩 生产性："事半功倍"。
- 🔧 透明性："你可以预测和控制低级别的细节"
- 🤸 通用性："你可以用Rust做任何事情"

如何使用Rustacean

- 💖 善良和体贴
- ✨ 给用户带来快乐
- 👋 展现出来
- 🔭 认可他人的知识
- 🔁 从某处开始
- ✅ 贯彻执行
- 🤝 付诸行动
- 🎁 信任和授权

[https://smallcultfollowing.com/babysteps//blog/2021/09/08/rustacean-principles/](https://smallcultfollowing.com/babysteps//blog/2021/09/08/rustacean-principles/)

## GCC 代码生成后端现已加入 rust-lang 大家庭

`rustc_codegen_gcc` 是为 Rustc 设计的 GCC 代码生成后端，目前已经加入 rust-lang 官方大家庭。

它不仅可以复用现有的 Rustc 前端，还能够获取来自 GCC 的增益，比如支持更多架构以及应用 GCC 的独门优化。

尽管该项目采用 `libgccjit` 进行实现，但其实并不是利用 JIT 技术，而是采用 AOT 方案，可不要被名字迷惑哦。

[https://github.com/rust-lang/rustc_codegen_gcc](https://github.com/rust-lang/rustc_codegen_gcc)

## LLVM13 的最新的 pass manager 进展让 Rust 的编译速度整体提高 5~20%

微软的 Ryan Levick 大神提到，LLVM13 的最新的 pass manager 进展让 Rust 的编译速度整体提高 5~20%。目前 LLVM13 还在 nightly 状态。很快估计能惠及到 Rust 这边来。

[https://twitter.com/ryan_levick/status/1443202538099073027](https://twitter.com/ryan_levick/status/1443202538099073027)

