## Algorithm
![算法](../../images/temp/sisyphus-2023-11-26-lc.png)

day1 排序+双指针 3sum
- 去除重复值
- 排序后，l与r
- 判等后，去除重复+1 -1；
- 前置重复判断，用-1。

day2 最长无重复子串
- 滑动窗口模板
- Map 缓存
- 移动指针 left+1 left 谁最大

day 3 相交链表
- 12
- 3
- 1 2 n 3 n 1
- 3 n 1 2 n 3
- 终止条件 两者不等，遍历走对方的路。O(m+n)

day 4 滑动指针

先将p中的字符全部入桶bucketP。
用left和right分别记录s中滑动窗口的左右端点，准备一个桶bucketS记录此滑动窗口中的字符及其出现次数
right不断向右移动，每移动一次都将一个新的字符加入到桶bucketS中。
当桶bucketS中元素种类或个数比桶bucketP多时，此时right再向右只会让二者差的更多，不可能找到字母异位词。因此这时应该将滑动窗口的左端向右移动，将一些字符踢出桶，直到桶bucketS和桶bucketP中元素相同为止。
当桶bucketS中元素种类或个数与桶bucketP完全相同时，只需要判断窗口的长度和p是否相同，就可判断是否找到字母异位词
- 26位int存储

## Review

[一些介绍](https://medium.com/@danielfoo/software-architecture-and-design-trend-2023-f55ecfbcfcc0)

## Tip


精益辅导实践

先试点项目，再继续推广。

## Share
