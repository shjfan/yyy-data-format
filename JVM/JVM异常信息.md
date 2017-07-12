# JVM异常信息

* ## 接口

/send/api/exception

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| srid | 服务ID |  |
| pt | excp |  |
| content |  |  |
| class | 发生的异常 |  |
| rqref | 请求来自哪个页面，例如在百度上点击链接到了这里，那么Referer:[http://www.baidu.com](http://www.baidu.com); 如果你是在浏览器的地址栏里输入，那么就没有这个Referer请求头了 |  |
| rqacc | 告诉服务器客户端可以接收的文档类型 |  |
| rqua | 与浏览器和操作系统有关的信息，有些网站会显示用户的系统版本和浏览器的版本信息，就是从这得到 |  |
| rqmeth | post/get |  |
| type | 错误类型 |  |
| txname | 事务名称 |  |
| txid | 事务ID |  |
| sid | 分布式事务ID |  |
| rquri | 请求的uri |  |
| ssc | session中的用户编码 |  |
| rqhost | 请求方的ip端口 |  |
| time | 耗时 |  |
| thread | 线程名称 |  |
| msg | 错误信息 |  |
| stk | 堆栈信息 |  |
| ts | 时间戳 |  |
| rphc | 表单的数据类型，说明会使用url编码。url编码的数据都是以“%”为前缀，后面跟随两位的16进制 |  |
| rqconl | 请求体的长度 |  |
| dbcnt | 请求数据库的次数 |  |

**注：rp和rq开头的字段分别对应http协议中的POST请求和GET请求，具体可参考http协议相关资料**

* ## 样例



