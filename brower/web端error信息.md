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

\[

    {

        "header": {

            "tid": "fUJiOvmThW1856091935",

            "appid": "CpbHQfunCj3212410448",

            "ip": "\#~\#~\#~",

            "pt": "err"

        },

        "content": \[

            {

                "jid": "1c8nr1xv1490333932630",

                "url": "http://ycm.yonyou.com/ycm-appmonitor/\#/appview/",

                "ts": 1490333932630,

                "jt": "web",

                "bv": "Chrome55.0.2883.87",

                "fu": 0,

                "os": 40,

                "msg": "Uncaught Error: Load timeout for modules: directive,webconstant\nhttp://requirejs.org/docs/errors.html\#timeout",

                "lno": 168,

                "cno": 17,

                "ref": "http://ycm.yonyou.com/ycm-appmonitor/components/bower/requirejs/require.js",

                "cnt": 1,

                "stk": "Error: Load timeout for modules: directive,webconstant\nhttp://requirejs.org/docs/errors.html\#timeout\n    at makeError \(http://ycm.yonyou.com/ycm-appmonitor/components/bower/requirejs/require.js:168:17\)\n    at checkLoaded \(http://ycm.yonyou.com/ycm-appmonitor/components/bower/requirejs/require.js:696:23\)\n    at http://ycm.yonyou.com/ycm-appmonitor/components/bower/requirejs/require.js:717:25",

                "module": "undefined",

                "rc": 1

            }

        \]

    }

\]

