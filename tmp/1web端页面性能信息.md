|指标名称|指标含义|注释|
|:--|:--|:--|
|header|||
|tid|租户码||
|appid|应用ID||
|pt|pf||
|ip|主机IP|探针发送时为#~#~#~，由云端接收时替换|
|content|||
|jid|唯一标识码||
|url|访问地址||
|ts|时间戳||
|jt|||
|bv|浏览器版本||
|je|||
|ttc|dom事件（keypress、click、scroll）首次触发时间||
|tn|navigationStart||
|tes|redirectStart||
|tee|redirectEnd||
|tus|unloadEventStart||
|tue|unloadEventEnd||
|tds|domainLookupStart||
|tde|domainLookupEnd||
|tsl|secureConnectionStart||
|tcs|connectionStart||
|tce|connectionEnd||
|tf|fetchStart||
|tqs|requestStart||
|trs|responseStart||
|tre|responseEnd||
|tol|domLoading||
|toi|domInteractive||
|tos|domContentLoadedEventStart||
|toe|domContentLoadedEventEnd||
|toc|domComplete||
|tls|loadEventStart||
|tle|loadEventEnd||
|tfp|firstPaintTime||
|tll|页面总耗时||
|pfcont|||
| o|startTime||
| rt|initiatorType||
| n|name||
| f|fetchStart||
| ds|domainLookupStart||
| de|domainLookupEnd||
| cs|connectStart||
| ce|connectEnd||
| sl|secureConnectionStart||
| qs|requestStart||
| rs|responseStart||
| re|responseEnd||
| tfs|transferSize，资源大小。    通过document.**获取的资源大小为0。正常情况下的0可能从缓存中读取的缘故||
| sat|status 资源加载状态 200：成功； 0：不可用（表示无法判断的状态）||
