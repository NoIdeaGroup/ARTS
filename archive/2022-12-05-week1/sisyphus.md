## Algorithm
![算法](../../images/temp/sisyphus-2022-12-10-lc.png)
* 减一相与
## Review
[正则匹配](http://web.mit.edu/6.031/www/sp21/classes/17-regex-grammars/)
从基础开始讲解正则：
```regex
Repetition: *
Concatenation: space
Union: y | z
* > space > |
eg: x ::= (y z | a b)*  // x matches zero or more yz or ab pairs
```
Demo:
```java
String s = " +,te    st";
// 把任意多个空格替换为一个空格
String singleSpacedString = s.replaceAll(" +", " ");
Assert.assertEquals(" +,te st", singleSpacedString);

// 捕获url
s = "http://google.com";
if (s.matches("http://([a-z]+\\.)+[a-z]+(:[0-9]+)?/")) {
    // then s is a url
    Assert.assertTrue(true);
}

```
## Tip


## Share




