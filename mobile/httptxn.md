# httptxn信息

* ## 接口

/send/api/mobile

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | httptxn |  |
| srid | 服务ID | 默认-1 |
| platform | 平台类型 | 默认Android |
| **content** |  |  |
| url | 请求url |  |
| carrier | 网络服务提供商 |  |
| total | 总耗时 |  |
| status | 状态码 |  |
| error | 错误码 |  |
| bytesent | 发送数据长度 |  |
| bytercv | 接收到的字段长度标记 |  |
| appdata | yyy与agent通信时的数据-头部 |  |
| wan | 网络接入方式 |  |
| method | http请求方法类型 |  |
| deviceid | 设备id |  |
| busiid | 业务id |  |
| txid | 事务id |  |

* ## 样例

\[

```
{
    "header":{
    
        "tid":"JsVkXHdqTG1878285484",
    
        "appid":"TZbafrPAmp1880722139",
    
        "pt":"httptxn",
    
        "srid":"-1",
    
        "platform":"Android"
    
    },

    "content":\[
    
        {
    
            "appdata": "null",
    
            "busiid": "15cce61545c0000d3ba102d1f13ffc450d2",
    
            "bytercv": 370,
    
            "bytesent": 50,
    
            "carrier": "wifi",
    
            "deviceid": "cde336a7-6921-4d07-9a92-d37f8d915dd7",
    
            "error": 0,
    
            "method": "POST",
    
            "status": 200,
    
            "total": 193.0,
    
            "txid": "null",
    
            "url": "http://10.2.112.58/xinhu/api.php",
    
            "wan": "wifi"
    
        }
    
    \]
}
```

\]

