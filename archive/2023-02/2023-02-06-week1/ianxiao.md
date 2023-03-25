## Algorithm

![ianxiao-2023-02-12-lc.png](../../../images/temp/ianxiao-2023-02-12-lc.png)

# Review

[Things they didn’t teach you about Software Engineering](https://vadimkravcenko.com/shorts/things-they-didnt-teach-you/)


# Tips

Redis设置过期时间的Key，需要注意的一些问题：
1. DEL/SET/GETSET等命令**会**清除过期时间；
2. INCR/LPUSH/HSET等命令**不会**清除过期时间；
3. PERSIST命令会清除过期时间；
4. 使用RENAME命令，老key的过期时间将会转到新key上；
5. 使用EXPIRE/PEXPIRE设置的过期时间为负数或使用EXPIREAT/PEXPIREAT设置过期时间戳为过去时间会导致key被删除；
6. EXPIRE命令可以更新过期时间。

# Share
