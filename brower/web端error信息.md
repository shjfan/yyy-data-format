# web端error信息

* ## 接口

/send/api/browser

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | err |  |
| ip | 主机IP | 探针发送时为\#~\#~\#~，由云端接收时替换 |
| **content** |  |  |
| jid | 唯一标识码 |  |
| url | 访问地址 |  |
| ts | 时间戳 |  |
| jt |  |  |
| bv | 浏览器版本 |  |
| fu |  |  |
| os |  |  |
| msg | 错误信息 |  |
| lno | 行号 |  |
| cno | 列号 |  |
| ref | 访问页面 |  |
| cnt | 次数 |  |
| stk | 错误堆栈 |  |
| module |  |  |
| rc |  |  |

* ## 样例



