## Algorithm

![供暖器](../../images/ianxiao-2022-11-27-lc.png)
排序 + 二分

## Review

[How to do distributed locking](https://martin.kleppmann.com/2016/02/08/how-to-do-distributed-locking.html)

关于基于Redis的分布式锁算法Redlock是否安全的争议，有一些观点比较有意思：

1. 分布式锁的使用一般有两种目的：效率和正确性。效率：有一些资源不希望被访问多次，但访问多次了也不会有太严重后果，比如AWS一些资源的冗余使用，最多造成多付一些钱；正确性：需要保证强互斥，如果不满足互斥则会造成严重的后果，比如像资金之类的修改。文章的作者Martin认为如果是需要效率，没必要使用5个Redis实例来做Redlock，使用单个最多加一些主从复制实例即可。如果为了正确性，Redlock可能在一些情况下并不安全（存在争议）。
2. 在一些比较极端的情况（分布式系统需要考虑的三种极端问题：NPC，Network Delay、Processor Pause、Clock Drift），会造成互斥的失效（多个客户端持有同一个锁）。
3. Redlock假设面对的分布式系统是同步的（有限的网络延时、有限的进程暂停、有限的时钟漂移），但实际的分布式系统应当更类似异步的。

## Tip

[一些工作常用的命令](https://ianxiao2.github.io/2022/11/27/useful-command/)

## Share

[基于Redis的分布式锁](https://ianxiao2.github.io/2022/11/27/redlock/)
