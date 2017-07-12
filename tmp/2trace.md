|新名称|含义|注释|
|:--|:--|:--|
|header|||
|tid|租户码||
|appid|应用ID||
|pt|trace||
|srid|服务ID|默认-1|
|platform|平台类型|默认Android|
|content|||
|params|参数||
| version|trace版本||
| deviceid|设备id||
| type|trace类型||
|entryts|开始时间戳||
|exitts|结束时间戳||
|display|显示名称||
|busiid|当前activity的业务id||
|total|总耗时||
|segment|||
| env|环境信息||
|   app|应用信息||
|    name|应用名称||
|    packageid|应用包路径||
|    version|应用版本||
|   device|设备信息||
|     osname|操作系统名称||
|     osversion|操作系统版本||
|     model|编译打包模型||
|     agentname|友云音agent名称||
|     agentver|友云音agent版本||
|     deviceid|设备id||
|     country|国家编码||
|     region|地区编码||
|     manufacturer|厂商||
|     hostip|ip地址||
|     province|省份||
|     city|城市||
|    misc|镜像说明||
|      platver|镜像版本||
|      platform|平台类型||
| tracetree|trace树||
|  params|参数||
|   type|类型||
|   carrier|network类型参数：网络服务提供商||
|   method|network类型参数：http请求方法类型||
|   status|network类型参数：状态码||
|   bytercv|network类型参数：接收的数据长度标识||
|   wan|network类型参数：网络接入方式||
|   uri|network类型参数：http请求路径||
|  entryts|开始时间戳||
|  exitts|结束时间戳||
|  display|显示名称||
|  busiid|当前activity的业务id||
|  thread|线程信息||
|   id|线程id||
|   name|线程名称||
|  children|trace数组||
|  vitals|重要信息（cpu+内存）||
|   MEMORY|内存采集||
|    ts|时间戳||
|    value|数值||
|   CPU|cpu采集||
|    ts|时间戳||
|    value|数值||
| previousActivity|activity历史||
|  activity_history_type|类型||
