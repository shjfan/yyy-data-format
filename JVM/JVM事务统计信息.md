# JVM事务统计信息

* ## 接口

/send/api/txc

* ## 属性说明
* | **名称** | **含义** | **注释** |
  | :--- | :--- | :--- |
  | **header** |  |  |
  | tid | 租户码 |  |
  | appid | 应用ID |  |
  | srid | 服务ID |  |
  | pt | txc |  |
  | **content** |  |  |
  | dtime | 统计时间区间 |  |
  | ts | 统计结束时间 |  |
  | ecnt | 错误数量 |  |
  | cnt | 总数量 |  |
  | time | 事务执行总时间 |  |
  | webcnt | web事务数 |  |
  | wtime | web事务执行时间 |  |
  | wecnt | web事务错误数 |  |
  | thp | 吞吐量 | 每分钟执行事务数 |
  | webthp | web事务吞吐量 | 每分钟执行web事务数 |
* ## 样例



