# JVM SQL信息

* ## 接口

/send/api/sql

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| srid | 服务ID |  |
| pt | sql |  |
| **content** |  | **数组** |
| bmn | 事务名 |  |
| uri | uri |  |
| mn | 指标名 |  |
| id |  |  |
| txid | 事务id |  |
| sid | 分布式事务id |  |
| sqlstr | sql语句 |  |
| max | 最大执行时间 |  |
| min | 最大执行时间 |  |
| time | 总执行时间 |  |
| cnt | 次数 |  |
| ts | 时间戳 |  |
| stk | 堆栈 |  |
| avgtime | 平均执行时间 |  |
| ba | 业务操作名称 |  |
| busiid | 业务操作ID |  |

* ## 样例

```json
[
{

    "content": [            

        {

            "min": 13,

            "mn": "Datastore/operation/Oracle/other",

            "sid": "1490331088218f346113",

            "max": 13,

            "cnt": 1,

            "ts": 1490331091868,

            "uri": "/ServiceDispatcherServlet/default",

            "stk": [

                "oracle.jdbc.driver.OraclePreparedStatement.executeQuery\(OraclePreparedStatement.java:3479\)",

                "nc.jdbc.framework.crossdb.CrossDBPreparedStatement.executeQuery\(CrossDBPreparedStatement.java:103\)",

                "nc.jdbc.framework.JdbcSession.executeQuery\(JdbcSession.java:299\)",

                "nc.md.common.MetaDataDAO.queryObjectByCond\(MetaDataDAO.java:76\)",

                "nc.mddb.manager.impl.TableColumnDAO.queryColumnsByTableID\(TableColumnDAO.java:79\)",

                "nc.mddb.manager.impl.DataModelPersistUtils.toTable\(DataModelPersistUtils.java:69\)",

                "nc.mddb.manager.impl.TableDAO.retrieveObjectFromRSDataMaps\(TableDAO.java:101\)",

                "nc.md.common.MetaDataDAO.queryObjectByCond\(MetaDataDAO.java:86\)",

                "nc.mddb.manager.impl.TableDAO.queryTableByID\(TableDAO.java:50\)",

                "nc.mddb.manager.cache.MDDBCachePoolProxy.getTableViewByID\(MDDBCachePoolProxy.java:112\)",

                "nc.mddb.manager.impl.DataModelQueryServiceImp.getTableByTableID\(DataModelQueryServiceImp.java:42\)",

                "nc.mddb.MDDBBaseQueryFacade.getTableByID\(MDDBBaseQueryFacade.java:31\)",

                "nc.mddb.model.impl.ForeignKey.getEndTable\(ForeignKey.java:59\)",

                "nc.mddb.model.impl.Table.initTableRelation\(Table.java:195\)",

                "nc.mddb.model.impl.Table.getForeignKeies\(Table.java:79\)",

                "nc.mddb.manager.impl.DataModelPersistUtils.toTable\(DataModelPersistUtils.java:71\)",

                "nc.mddb.manager.impl.TableDAO.retrieveObjectFromRSDataMaps\(TableDAO.java:101\)",

                "nc.md.common.MetaDataDAO.queryObjectByCond\(MetaDataDAO.java:86\)",

                "nc.mddb.manager.impl.TableDAO.queryTableByID\(TableDAO.java:50\)",

                "nc.mddb.manager.cache.MDDBCachePoolProxy.getTableViewByID\(MDDBCachePoolProxy.java:112\)",

                "Skipping 122 lines....\(:0\)",

                "org.apache.catalina.core.StandardHostValve.invoke\(StandardHostValve.java:168\)",

                "org.apache.catalina.valves.ErrorReportValve.invoke\(ErrorReportValve.java:98\)",

                "org.apache.catalina.core.StandardEngineValve.invoke\(StandardEngineValve.java:118\)",

                "org.apache.catalina.connector.CoyoteAdapter.service\(CoyoteAdapter.java:407\)",

                "org.apache.coyote.http11.AbstractHttp11Processor.process\(AbstractHttp11Processor.java:987\)",

                "org.apache.coyote.AbstractProtocol$AbstractConnectionHandler.process\(AbstractProtocol.java:539\)",

                "org.apache.tomcat.util.net.JIoEndpoint$SocketProcessor.run\(JIoEndpoint.java:300\)",

                "java.util.concurrent.ThreadPoolExecutor$Worker.runTask\(ThreadPoolExecutor.java:886\)",

                "java.util.concurrent.ThreadPoolExecutor$Worker.run\(ThreadPoolExecutor.java:908\)",

                "java.lang.Thread.run\(Thread.java:619\)"

            ],

            "id": 1157529897,

            "time": 13,

            "bmn": "WebTransaction/Uri/ServiceDispatcherServlet/default",

            "txid": "1490331088218f346113",

            "sqlstr": " select \* from \( select row\_number \(\) over \( partition by id order by versiontype desc \) rn, t1.columnlength, t1.columnsequence, t1.columntype, t1.defaultvalue, t1.description, t1.displayname, t1.forlocale, t1.groupid, t1.help, t1.id, t1.isactive, t1.name, t1.nullable, t1.pkey, t1.precise, t1.resid, t1.sqldatetype, t1.tableid, t1.ts, t1.versiontype FROM md\_column t1 where tableID = ? \) a where a.rn = ? order by columnsequence"

        }

    ],

    "header": {

        "srid": "YtWELYpvZc0164342496",

        "pt": "sql",

        "appid": "ztRUFZRPDK0151963951",

        "tid": "RitGmoBwfw0151671866"

    }

}
]
```



