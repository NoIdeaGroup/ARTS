## Algorithm

![leetcode](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7eb52c96-064a-45a7-85c7-3edc8262ffa7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230305%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230305T082225Z&X-Amz-Expires=86400&X-Amz-Signature=194f697c520e19fc5a7c0e5edda5bef6ba4e6de7bb0e657ef99e55f5021b665e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## Review

### **[Java动态追踪技术探究](https://tech.meituan.com/2019/02/28/java-dynamic-trace.html)**

起因是本周遇到一个仿真环境的超时问题，上游打到某台机器的 RPC 请求大概 80% 左右会超时，实际执行时间远超正常水准。但是又有大概
20% 是正常的，且同样的代码在另外一台机器上是正常的。检查了对 DB 的访问日志，发现在 DB 层面请求都是正常的。最后通过机器的 CPU
负载、火焰图、arthas 终于定位到是机器上有个 agent 代码有 bug，导致某个开关类序列化异常，导致一次请求大部分时间都 hang
在这里面一直重复执行。所以本周没有找英文文档，通过这篇文章大致对类 arthas 的 Java 动态追踪技术有个大概的了解。

## Tip

arthas 的强大毋庸置疑，这次实际用到了 thread 命令定位问题。所以也对 thread 的用法做一个回顾：

官方文档：[https://arthas.aliyun.com/doc/thread.html](https://arthas.aliyun.com/doc/thread.html)

| 参数名称        | 参数说明                             |
|-------------|----------------------------------|
| id          | 线程 id                            |
| [n:]        | 指定最忙的前 N 个现成并打印堆栈                |
| [b]         | 找出当前阻塞其他线程的线程                    |
| [i <value>] | 指定 cpu 使用率统计的采样间隔，单位为毫秒，默认值为 200 |
| [-all]      | 显示所有匹配的线程                        |

在上面提到的 case 里面，就是通过多次执行 `thread -n 1` 最终捕捉到了一次超时的请求，而 arthas
也给出了该线程执行的完整堆栈，最终定位到该问题。通过卸载有问题的 agent 解决了问题。

## Share

个人感觉 canvas 是前端里面“风骚”又强大的一块内容，碰巧最近刷到了讲解 canvas 意义和基本操作的课程。分享给做后端的小伙伴，拓展下知识面。
原视频参见：https://v.douyin.com/SSVy22m/