# JVM启动指标

* ## 接口

/send/api/vmst

* ## 属性说明

| **名称** | **指标含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| appid | 应用ID |  |
| tid | 租户码 |  |
| srid | 服务ID |  |
| pt | vmst |  |
| **content** |  |  |
| avs | 探针版本 |  |
| jvd | java供应商 |  |
| jvt | java虚拟机类型 |  |
| vmvs | 虚拟机版本 |  |
| jvs | java版本 |  |
| lp | jvm探针日志路径 |  |
| hint | 堆内存初始大小 |  |
| hmax | 堆内存最大限制 |  |
| pid | JVM进程pid |  |
| arg | jvm启动参数 |  |
| dy | 容器类型 |  |
| dyvs | 容器版本 |  |
| fwk | 框架所使用的编程语言 |  |
| ast | jvm最后一次启动时间 |  |

* ## 样例

```json
[
{

    "content": [

        {

            "fwk": "java",

            "dy": "Apache Tomcat",

            "lp": "D:\\ExmobiATP\\yonyou-yyy-agent\\probes\\logs\\ztRUFZRPDK0151963951\\5796\\yonyou-yyy.log",

            "ast": 1490328846894,

            "hint": 512,

            "pid": 4592,

            "jvs": "1.6.0\_12",

            "hmax": 762.125,

            "jvd": "Sun Microsystems Inc.",

            "avs": "3.31.1",

            "arg": "-Xms512m,-Xmx768m,-XX:PermSize=128m,-XX:MaxPermSize=512m,-Djava.awt.headless=true,-Dsun.reflect.inflationThreshold=0,-Dfile.encoding=GBK,-javaagent:D:/ExmobiATP/yonyou-yyy-agent/probes/yonyou-yyy.jar=appId=ztRUFZRPDK0151963951,serverPort=5796,-Duser.timezone=GMT+8,-Dnc.server.name=ncServer,-Dnc.server.startCount=0,-DNC\_JAVA\_HOME=./ufjdk,-Dnc.bs.logging.format=text,-Dnc.server.location=D:\\ExmobiATP,-Drun.side=server,-Dnc.run.side=server",

            "dyvs": "@VERSION@",

            "vmvs": "11.2-b01"

        }

    ],

    "header": {

        "srid": "YtWELYpvZc0164342496",

        "serverPort": "5796",

        "pt": "vmst",

        "tid": "ysjJEcEcIo3237427125",

        "appid": "ztRUFZRPDK0151963951"

    }

}
]
```



