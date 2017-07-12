# JVM事务概要信息

* ## 接口

/send/api/transaction

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| srid | 服务ID |  |
| pt | txg |  |
| **content** |  |  |
| txid | 事务id |  |
| tp | 服务调用名称 |  |
| ts | 时间戳 |  |
| rtime | responseTime |  |
| time |  | 多个线程属于同一事务 |
| ttfb |  |  |
| ttlb |  |  |
| sid | guid，分布式服务调用ID | 分布式事务ID |
| sn | "none"或CallServer，分布式服务的名称 |  |
| bo | 业务操作，BusiAction或requestUri |  |
| user | user\_ssc或UserId+UserCode或user |  |
| ep | "empty\_ep"或request.headers.host |  |
| psid | 父调用的sid，默认为psid |  |
| pmid | 上游事务方法ID |  |
| uri | request\_uri |  |
| thid | jvm.thread\_name |  |
| nccid | 远程调用ID | 来自NC的数据 |
| ncds | 数据源 | 来自NC的数据 |
| ncbcc | 例：nc65demo | 来自NC的数据 |
| ba | 业务名称 | 来自NC的数据 |
| ncbdt |  | 来自NC的数据 |
| nccp | 例：/\_client | 来自NC的数据 |
| ncmd | 模块 | 来自NC的数据 |
| ncch | 客户端IP | 来自NC的数据 |
| ncdid |  | 来自NC的数据 |
| ncgid | 集团ID | 来自NC的数据 |
| ncgno | 集团编码 | 来自NC的数据 |
| ncuid | 用户ID | 来自NC的数据 |
| ncucd | 用户code | 来自NC的数据 |
| nccs |  | 来自NC的数据 |
| nchc |  | 来自NC的数据 |
| nclc | 语言 | 来自NC的数据 |
| ncser | 服务名 | 来自NC的数据 |
| ncra |  | 来自NC的数据 |
| ncmn | 方法名 | 来自NC的数据 |
| ncsysid |  | 来自NC的数据 |
| ncpara | 参数 | 来自NC的数据 |
| ncparat | 参数类型 | 来自NC的数据 |
| busiid | 业务关联ID | 来自NC的数据 |
| hdn |  |  |
| pin |  |  |
| gctime | gc花费时间 |  |
| ctime | 占用cpu的时间 |  |
| tripid |  |  |
| path |  |  |
| resid | 合成资源的id |  |
| monid | 合成监控的id |  |
| jodid | 合成工作的id |  |
| rtxid | 关系到事务的id |  |
| sc |  |  |
| sizel | 极限大小参数名 |  |
| stc | 异常的栈轨迹 |  |
| epc | 执行计划 |  |
| ccpid | 和客户端相关联的程序id |  |
| rph | 针对hash的路径 |  |
| aph | 交替hash路径 |  |
| port | 服务端口 |  |
| qtime | 队列时间 |  |
| etime | 额外的时间 |  |
| ecnt | 额外执行次数 |  |
| dbtime | 数据库总耗时 |  |
| dbcnt | 数据库访问次数 |  |
| gctime | gc累积时间 |  |
| error | 是否发生错误 |  |
* ## 样例

[http://pan.baidu.com/s/1eSEJB02](http://pan.baidu.com/s/1eSEJB02)

