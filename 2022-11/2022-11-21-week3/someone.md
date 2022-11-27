## Algorithm
* 重建二叉树
    1. 前中和后中且没有重复元素可以重建二叉树。前序和后序是为了找根节点。中序区分左右树。
* 二叉树中序遍历的下一个节点
    1. 如果此节点有右子树，则找到右子树的中序遍历的第一个节点。
    2. 如果此节点没有右子树，则找此节点的父节点，如果此节点是其父节点的左子树，则其父节点就是一下个节点。若不是，则继续验证父节点是否是其父节点的左子树。

## Review

原文链接：https://javascript.plainenglish.io/my-20-most-useful-javascript-tips-tricks-and-best-practices-9ad8fe7f0c01

## Tip
无

## Share
浏览器线程与事件循环总结
原文链接：https://nettle-hydrofoil-55e.notion.site/85968752baa1439dbb79e6cba6f62c25