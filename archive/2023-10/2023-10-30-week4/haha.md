## Algorithm

[code](/images/temp/haha-2023-11-05.png)

## Review

[Node.js - Buffer](https://weread.qq.com/web/reader/d1b32290718ff65fd1befcck283328802332838023a7529)

- 真正的内存是在 Node 的 C++层面提供的，JavaScript 层面只是使用它。
- 当进行小而频繁的 Buffer 操作时，采用 slab 的机制进行预先申请和事后分配，使得 JavaScript 到操作系统之间不必有过多的内存申请方面的系统调用。
- 对于大块的 Buffer 而言，则直接使用 C++层面提供的内存，而无需细腻的分配操作。

## Tip

## Share
