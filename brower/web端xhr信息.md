# web端xhr信息

* ## 接口

/send/api/browser

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | xhr |  |
| ip | 主机IP | 探针发送时为\#~\#~\#~，由云端接收时替换 |
| **content** |  |  |
| jid | 唯一标识码 |  |
| ref | 访问地址 |  |
| ts | 时间戳 |  |
| jt |  |  |
| bv | 浏览器版本 |  |
| m | 请求方式 |  |
| url | 资源地址 |  |
| es | 总耗时 |  |
| d |  |  |
| sat | status 资源加载状态 200：成功； 0：不可用（表示无法判断的状态） |  |
| t |  |  |
| res |  |  |
| req |  |  |
| txid | 事务ID |  |
| txtime |  |  |
| mark |  |  |
| bid | 业务操作标识 |  |
| dtxt | 发起业务请求的元素文本信息 |  |
| ba | 业务操作名称，ref+dtxt |  |
| uc | 用户编码usercode |  |
| nodeflag | 节点标识 |  |

* ## 样例

```json
[

{

    "header": {

        "tid": "RitGmoBwfw0151671866",

        "appid": "ztRUFZRPDK0151963951",

        "ip": "#~#~#~",

        "pt": "xhr"

    },

    "content": [

        {

            "jid": "s895rf9v1490333457291",

            "ref": "http://221.228.101.161:5796/portal/app/salesfunnelCAApp/salesfunnelWin?nodecode=CA211040&$portletWind=pmng\_adminforuser\_pmng\_MgrContentPortlet&\_h3ra=221.228.101.161:5796/portal&$langcode=simpchn&$themeid=webclassic&lrid=1684348072",

            "ts": 1490333457291,

            "jt": "web",

            "bv": "Chrome55.0.2883.87",

            "m": "POST",

            "url": "/portal/core",

            "es": 220,

            "d": 28,

            "sat": 200,

            "t": 0,

            "res": 1317,

            "req": 3306,

            "txid": "1490333456253dd637d0",

            "txtime": "45818889",

            "bid": "hyee7huommq9dx2n",

            "dtxt": "other",

            "ba": "CA211040\#other"

        },

        {

            "jid": "ftngxqvd1490333457759",

            "ref": "http://221.228.101.161:5796/portal/app/salesfunnelCAApp/salesfunnelWin?nodecode=CA211040&$portletWind=pmng\_adminforuser\_pmng\_MgrContentPortlet&\_h3ra=221.228.101.161:5796/portal&$langcode=simpchn&$themeid=webclassic&lrid=1684348072",

            "ts": 1490333457759,

            "jt": "web",

            "bv": "Chrome55.0.2883.87",

            "m": "POST",

            "url": "/portal/core",

            "es": 449,

            "d": 3,

            "sat": 200,

            "t": 0,

            "res": 659,

            "req": 4385,

            "txid": "1490333456521fd45708",

            "txtime": "383455386",

            "bid": "hyee7huommq9dx2n",

            "dtxt": "other",

            "ba": "CA211040\#other"

        }

    ]

}
]
```



