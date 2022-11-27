## Algorithm
![image.png](https://tva1.sinaimg.cn/large/006iGVg2ly1h8ig3c9to7j32wq1j2x1q.jpg)
计划先刷完所有的 Easy，找下手感。本周进度如下：
![image.png](https://tva1.sinaimg.cn/large/006iGVg2ly1h8ig4e1zufj32wq1j2kf3.jpg)

## Review
### **[Effective Microservices: 10 Best Practices](https://towardsdatascience.com/effective-microservices-10-best-practices-c6e4ba0c6ee2)**

My Conclusion:

Monolithic architecture: The traditional structure for software applications,
Monolithic architecture has three components:
  - Client-side user interface
  - Server-side application
  - Data interface

All three parts interact with a single database.

### Best Practice
1. DDD(Domain Driven Design)

    - The software development team should work in close co-operation with the Business department or Domain Experts.
    - Finding the Bounded Context and related Core Domain and Ubiquitous Language, Subdomains, Context Maps.
    - Decompose the Core Domain into fine-grained Building blocks: Entity, Value Object, Aggregate, Aggregate Root.

2. Database per Microservice

    - every Microservice should have its Database (or Private Tables).

3. Micro Frontends
    - Provided Micro Frontends for every backend.

4. Continuous Delivery
    - To take full advantage of this Microservice feature, one needs CI/CD and DevOps.
   
5. Observability
    - Logs, RTT, and other means are required to monitor microservices.

6. Unified Tech Stack

7. Asynchronous Communication
    - The easiest and most common way to communicate between Microservices is via Synchronous REST API which is pragmatic but a short term solution. But for a long term solution, Microservices should communicate Asynchronously. Such as MQ, CQRS

8. Microservice First
    - Start with Microservices if there is a plan to use Microservice Architecture eventually. It's difficult to transform monolith into microservices.

9. Infrastructure over Libraries
    
10. Organizational Considerations

## Tip
工作中经常需要用到将一列数字（可能是 DB 的某一列 id）转换为逗号分隔的形式，用于另外一张表的 select 查询。比如：
```text
1000001
1000002
1000003

转换为 '1000001','1000002','1000003'
如果带参数 none，则转换为 1000001,1000002,1000003
```
在 macOS 上可以利用 pbpaste + pbcopy 实现从剪贴板读取并回写，同时完成对文本的处理。代码如下：
```shell
#!/bin/bash
flag="'"
none="none"
if [ "$1"x = "$none"x ];then
 flag=""
fi

joinByChar() {
 local IFS="$1"
 shift
 echo "$*"
}

OLD_IFS="$IFS"
IFS=$'\n'
for line in `pbpaste`
do
 data[${#data[@]}]="${flag}${line}${flag}"
done;
IFS="$OLD_IFS"
joinByChar , "${data[@]}" | tr -d '\n' | pbcopy
```
如果想要全局调用，可以将该命令放置在 /usr/local/bin 下面，按照喜好自行命名。

## Share
[没有二十年功力，写不出Thread.sleep(0)这一行“看似无用”的代码！](https://juejin.cn/post/7139741080597037063?share_token=c4657c2a-9073-4edf-a02f-99d3b9369134)

讨论了 JVM SafePoint 机制，以及如何通过 Thread.sleep(0) 利用该机制。