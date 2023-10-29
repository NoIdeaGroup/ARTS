## Algorithm

[code](/images/temp/haha-2023-10-29.png)

## Review

[Node.js - 内存泄漏排查](https://weread.qq.com/web/reader/d1b32290718ff65fd1befcckd9d320f022ed9d4f495e456)

- v8-profiler。由 Danny Coates 提供，它可以用于对 V8 堆内存抓取快照和对 CPU 进行分析，但该项目已经有 3 年没有维护了。
- node-heapdump。这是 Node 核心贡献者之一 Ben Noordhuis 编写的模块，它允许对 V8 堆内存抓取快照，用于事后分析。
- node-mtrace。由 Jimb Esser 提供，它使用了 GCC 的 mtrace 工具来分析堆的使用。
- dtrace。在 Joyent 的 SmartOS 系统上，有完善的 dtrace 工具用来分析内存泄漏。
- node-memwatch。来自 Mozilla 的 Lloyd Hilaiel 贡献的模块，采用 WTFPL 许可发布。

## Tip

## Share
