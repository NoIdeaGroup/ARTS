## **Algorithm**

![leetcode](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/20149c89-7518-4557-b97c-d23d3df306c2/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221204T155106Z&X-Amz-Expires=86400&X-Amz-Signature=c7bad0ddce998275ab50f80dc816ae73b17efaae59fdda5713dd8ec10fde205b&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## Review

### ****[Modern Best Practices for Testing in Java](https://phauer.com/2019/modern-best-practices-testing-java/)****

这篇文章提到了很多编写 Java Test 的准则，其中有几条比较有意思，可以参照自己的情况做适当的调整 or 践行：

- Write self-contained tests
    - 类似自己实现一个类似 insertIntoDatabase 的方法，来存储 mock 的数据
- Don’t Overuse Variables
    - 实际上我自己为了减少多个分支代码的数据 mock 代码，经常 reuse
- Use Fixed Data Instead of Randomized Data
    - 以后类似`new Date()`的代码也要注意下
- KISS > DRY
    - KISS - Keep It Simple & Stupid
    - DRY - Don’t Repeat Yourself
    - 补充下，三原则的另外一个是：****YAGNI - You Ain’t Gonna Need It****

## Tip

ideaVim 的操作模式下，如果某个参数是通过调用工具类 or 方法来获取的，此时对参数列表的操作往往会变的更麻烦，可能需要多次按键才能解决。对于这种情况，可以使用 vim-argtextobj 来简化。

脚本简介：[https://www.vim.org/scripts/script.php?script_id=2699](https://www.vim.org/scripts/script.php?script_id=2699)

通过 via, cia, daa 等等操作即可自动识别单个参数，并执行相应的操作。

```bash
# 例如删除一个参数
     当光标在 arg2 范围内，按下 daa 即可删除该参数
                     ↓
function(int arg1, char* arg2="a,b,c(d,e)")

     当光标在 arg1 范围内，按下 daa 即删除所有的参数
               ↓
function(int arg1)
function(<cursor>)
```

## Share

起因是在刷到了讲[「为什么有 HTTP 协议还需要 RPC 协议」](https://v.douyin.com/hdmu7cu/)的视频，大致上的原因大家都很清楚，虽然本质上都是对 TCP 的封装，但是 RPC 相关的协议更加精简，并且针对自家的框架做了定制优化。所以用在 RPC 上更加合适。

但是里面提到了两个点，比较有意思：

- RPC 相关协议比 HTTP 协议更早出现
- HTTP 2.0 目前做的同样很优秀，有很多框架就是基于 HTTP 2.0 来实现了自己的 RPC 协议