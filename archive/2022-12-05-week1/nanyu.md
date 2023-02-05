## **Algorithm**

![leetcode](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/75ec2ec0-7e18-49ce-8d5c-388cce22f54b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221211%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221211T150046Z&X-Amz-Expires=86400&X-Amz-Signature=aa44e8e14856107ece2165bc77095add7e6bb0c176722200bb333fd866638d1f&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## Review

### **[State machines are wonderful tools](https://nullprogram.com/blog/2020/12/31/)**

状态机可能是个耳熟能详的东西，但是这篇文章中使用了一种特别的状态机思路的代码，实现了摩斯电码、UTF-8 解码、单词统计等能力。和平时使用传统 Spring State Machine 的思路略有不同，可以参考，也许对业务代码有所启发。

## Tip

MacOS 上虽然有原生 OCR 的支持，但是需要保存到本地才能通过「预览」来使用。一些使用较少，但是复杂的 OCR 场景（如：表格、列表等）推荐直接用「白描」，不过日常答疑中，对方经常将一些编号、ID 截图给你，这个时候可以使用 UTools 的插件来解决：

- 先按照 UTools（本质上也是一个类 Alfred、Raycast 的效率启动器）

  - PS：虽然感觉有点奇怪，但是我自己电脑上现在就是 UTools + RayCast 两个启动器混用

- 在插件市场安装「OCR-图片转文字」

即可轻松实现，截图 + 粘贴直接 OCR，并根据 OCR 结果自行编辑，做一些识别错误的微调，非常方便！

## Share

一个有意思的前端实现：[「为什么B站的弹幕可以不挡人物」](https://juejin.cn/post/7141012605535010823)

本质上是一个「人物识别 + 蒙板」实现的，不过由于 webkit-mask-image 对低版本并不支持，所以老浏览器就享受不到这个功能了。