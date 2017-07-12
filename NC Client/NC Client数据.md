# NC Client数据

* ## 接口

/send/api/transaction

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| srid | 服务ID |  |
| ip | ip地址 |  |
| pt | busi |  |
| **content** |  |  |
| ba | 业务操作名称 |  |
| nodecode | 节点编码 |  |
| nodename | 节点名称 |  |
| btnname | 按钮名称 |  |
| usercode | 用户编码 |  |
| nodebtn | 节点编码-按钮名称 |  |
| bsid | 业务标识 |  |
| bstotal | 业务总耗时 |  |
| nettotal | 网络总耗时 |  |
| txtotal | 服务器事务总耗时 |  |
| type | 类型，默认为busi |  |
| ts | 时间戳 |  |
| txs |  |  |
| total | 事务耗时 |  |
| txid | 事务ID |  |

* ## 样例

```json
[

{

    "content":[

        {

            "ba":"打开节点-管控范围",

            "bsid":"15b70d034f1000028d244a4096000daf0a0",

            "bstotal":219,

            "nettotal":15,

            "ts":1492246345164,

            "txs":[

                {

                    "total":61,

                    "txid":"1492246316820a390af9"

                },

                {

                    "total":17,

                    "txid":"14922463170766ddef87"

                },

                {

                    "total":19,

                    "txid":"1492246311205f04b507"

                },

                {

                    "total":37,

                    "txid":"1492246317018f74e744"

                }

            ],

            "txtotal":119,

            "type":"busi"

        }

    ],

    "header":{

        "appid":"UsrQECBWnj0346199601",

        "pt":"busi",

        "srid":"TygVRsxzMV1485091813",

        "tid":"fUJiOvmThW1856091935"

    }

}
]
```



