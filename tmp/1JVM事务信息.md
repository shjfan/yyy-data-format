|新名称|含义|注释|
|:--|:--|:--|
|header|||
|tid|租户码||
|appid|应用ID||
|srid|服务ID||
|pt|tx||
|content|||
|txid|事务ID|取newrelic的tripid|
|tp|服务调用名称||
|ts|时间戳||
|rtime|responseTime||
|time||多个线程属于同一事务|
|ttfb|||
|ttlb|||
|sid|事务的guid|分布式事务ID|
|sn|"none"或CallServer，分布式服务的名称||
|bo|业务操作，BusiAction或requestUri||
|user|user_ssc或UserId+UserCode或user||
|ep|"empty_ep"或request.headers.host||
|psid|父调用的sid，目前为psid|取newrelic的rtxid|
|uri|request_uri||
|thid|jvm.thread_name||
|pmid|上游事务方法ID||
|  cont|||
|  mtd|类.方法||
|  mid|方法ID||
|  time|执行时间||
|  ac|线程名||
|  cnt|次数||
|  mtp|metricname/类/方法||
|  pthid|||
|  st|||
|  thid|||
|  stk|堆栈信息，是字符串数组||
|  depth|深度||
|  sqls|sql列表||
|    sqlstr|sql语句||
|    sqltime|sql执行时间||
|    sqlcnt|sql执行次数||
|  stime|自执行时间||
|  nst|开始时间（纳秒）|目前后台使用|
|  net|结束时间（纳秒）|目前后台使用|
|nccid|远程调用ID|来自NC的数据|
|ncds|数据源||
|ncbcc|例：nc65demo||
|ba|业务名称||
|ncbdt|||
|nccp|例：/_client||
|ncmd|模块||
|ncch|客户端IP||
|ncdid|||
|ncgid|集团ID||
|ncgno|集团编码||
|ncuid|用户ID||
|ncucd|用户code||
|nccs|||
|nchc|||
|nclc|语言||
|ncser|服务名||
|ncra|||
|ncmn|方法名||
|ncsysid|||
|ncpara|参数||
|ncparat|参数类型||
|busiid|业务关联ID||
|hdn|||
|pin|||
|gctime|gc花费时间||
|ctime|占用cpu的时间||
|tripid|跟踪事务ID，newrelic本身带的分布式事务ID||
|path|||
|resid|合成资源的id||
|monid|合成监控的id||
|jodid|合成工作的id||
|rtxid|关联的事务id，即父事务的ID||
|sc|||
|sizel|极限大小参数名||
|stc|异常的栈轨迹||
|epc|执行计划||
|ccpid|和客户端相关联的程序id||
|rph|针对hash的路径||
|aph|交替hash路径||
|port|服务端口||
|qtime|队列时间||
|etime|额外的时间||
|ecnt|额外执行次数||
|dbtime|数据库总耗时||
|dbcnt|数据库访问次数||
|gctime|gc累积时间||
|error|是否发生错误||
