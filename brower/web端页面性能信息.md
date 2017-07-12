# web端页面性能信息

* ## 接口

/send/api/browser

* ## 属性说明

| **名称** | **指标含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | pf |  |
| ip | 主机IP | 探针发送时为\#~\#~\#~，由云端接收时替换 |
| **content** |  |  |
| jid | 唯一标识码 |  |
| url | 访问地址 |  |
| ts | 时间戳 |  |
| jt |  |  |
| bv | 浏览器版本 |  |
| je |  |  |
| ttc | dom事件（keypress、click、scroll）首次触发时间 |  |
| tn | navigationStart |  |
| tes | redirectStart |  |
| tee | redirectEnd |  |
| tus | unloadEventStart |  |
| tue | unloadEventEnd |  |
| tds | domainLookupStart |  |
| tde | domainLookupEnd |  |
| tsl | secureConnectionStart |  |
| tcs | connectionStart |  |
| tce | connectionEnd |  |
| tf | fetchStart |  |
| tqs | requestStart |  |
| trs | responseStart |  |
| tre | responseEnd |  |
| tol | domLoading |  |
| toi | domInteractive |  |
| tos | domContentLoadedEventStart |  |
| toe | domContentLoadedEventEnd |  |
| toc | domComplete |  |
| tls | loadEventStart |  |
| tle | loadEventEnd |  |
| tfp | firstPaintTime |  |
| tll | 页面总耗时 |  |
| pfcont |  |  |
| o | startTime |  |
| rt | initiatorType |  |
| n | name |  |
| f | fetchStart |  |
| ds | domainLookupStart |  |
| de | domainLookupEnd |  |
| cs | connectStart |  |
| ce | connectEnd |  |
| sl | secureConnectionStart |  |
| qs | requestStart |  |
| rs | responseStart |  |
| re | responseEnd |  |
| tfs | transferSize，资源大小。    通过document.\*\*获取的资源大小为0。正常情况下的0可能从缓存中读取的缘故 |  |
| sat | status 资源加载状态 200：成功； 0：不可用（表示无法判断的状态） |  |

* ## 样例

```json
[

{

    "header": {

        "tid": "RitGmoBwfw0151671866",

        "appid": "ztRUFZRPDK0151963951",

        "ip": "#~#~#~",

        "pt": "pf"

    },

    "content": [

        {

            "tn": 1490333165366,

            "tds": 1,

            "tde": 1,

            "tcs": 1,

            "tce": 1,

            "tf": 1,

            "tqs": 85,

            "trs": 2401,

            "tre": 2404,

            "tol": 2411,

            "toi": 3523,

            "tos": 3524,

            "toe": 3524,

            "toc": 4726,

            "tls": 4726,

            "tle": 4727,

            "je": 0,

            "jid": "24aa\_7a7cf62f1490333170101",

            "url": "http://221.228.101.161:5796/portal/app/taskcenterApp?nodecode=11110101&$portletWind=pint\_task\_pint\_TaskCenterPortlet&\_h3ra=221.228.101.161:5796/portal&$langcode=simpchn&$themeid=webclassic&lrid=2219864255&$portletWind=pint\_task\_pint\_TaskCenterPortlet&\_h3ra=221.228.101.161:5796/portal&$langcode=simpchn&$themeid=webclassic",

            "ts": 1490333170101,

            "jt": "web",

            "bv": "Chrome55.0.2883.87",

            "pfcont": [

                {

                    "o": 2414.66,

                    "rt": "script",

                    "n": "http://221.228.101.161:5796/portal/yonyou-yyy.js",

                    "f": 2414.66,

                    "ds": 2414.66,

                    "de": 2414.66,

                    "cs": 2414.66,

                    "ce": 2414.66,

                    "sl": 0,

                    "qs": 2420.2250000000004,

                    "rs": 2586.815,

                    "re": 3460.135,

                    "tfs": 8125,

                    "sat": 200

                },

                {

                    "o": 2415.11,

                    "rt": "link",

                    "n": "http://221.228.101.161:5796/lfw/frame/device\_pc/themes/webclassic/ui/ctrl/button/button.css",

                    "f": 2415.11,

                    "ds": 2415.11,

                    "de": 2415.11,

                    "cs": 2415.11,

                    "ce": 2415.11,

                    "sl": 0,

                    "qs": 2420.875,

                    "rs": 2579.4,

                    "re": 2586.46,

                    "tfs": 1205,

                    "sat": 200

                }

            ]

        }

    ]

}
]
```



