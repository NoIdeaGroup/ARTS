## Algorithm

![算法](../../images/temp/sisyphus-2023-07-30-lc.png)
* mysql 8.0 开窗函数，over pration by 

## Review

[介绍工具](https://medium.com/python-in-plain-english/top-11-tools-for-microservices-backend-development-in-2023-3d9cdd61ef10)

## Tip
Kill脚本练习
需要写Shell脚本，但是对于自动化for循环等不太熟悉，Shell脚本练习
* 实现服务状态应用。
```shell
SERVER_NAME=$2
function status() {
PIDS=`ps -ef | grep java | grep $SERVER_NAME | awk '{print $2}'`
if [ -n "$PIDS" ]; then
echo -e "\033[32m The $SERVER_NAME is running...! \033[0m"
echo -e "\033[32m PID: $PIDS \033[0m"
 exit 0
else
 echo -e "\033[33m $SERVER_NAME is not running... \033[0m"
 exit 0
fi
}

case $1 in
 start)
 start;;
 stop)
 stop;;
 restart)
 restart;;
 status)
 status;;
 *)
echo -e "\033[0;31m Usage: \033[0m  \033[0;34m sh  $0  {start|stop|restart|status} \033[0m"
echo -e "\033[0;31m Example: \033[0m \033[0;33m sh  $0  start \033[0m"
esac
```

## Share
