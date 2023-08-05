## Algorithm

![算法](../../../images/temp/sisyphus-2023-07-02-lc.png)

* 日期计算日期函数DATE_SUB

## Review

[设计模式](https://medium.com/@kalkidant/your-code-architecture-sucks-if-3e65683693ab)
* 常见设计问题，每层职责分离
* 日志设计
* 数据库迁移设计
* 静态文件存储分离
* 消息队列分离

## Tip

Gauss db

docker 安装gauss
### search

docker search opengauss

docker pull enmotech/opengauss

### run
docter run --name opengauss --privileged=true -d -e GS_PASSWORD=openGauss@123
-p 5432:5432 enmotech/opengauss:latest

### 进入容器验证
docker exec -it opengauss bash
openGauss=> CREATE USER zjutuser WITH PASSWORD "Bigdata@123";

## Share
