# JVM运行指标

* ## 接口

/send/api/metric

* ## 属性说明

| **名称** | **指标含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| appid | 应用ID |  |
| ep | host名称 |  |
| tid | 租户码 |  |
| srid | 服务ID |  |
| **content** |  |  |
| memory.used | 已使用内存大小 |  |
| memory.physical | 自身内存大小 |  |
| memory.heap.used | 已使用堆内存大小 |  |
| memory.heap.max | 堆的最大值 |  |
| memory.heap.utilization | 堆内存的利用率 |  |
| memory.heap.committed | 为堆分配的内存大小 |  |
| memorypool.heap.survivorspace.committed | 为幸存区分配内存大小 |  |
| memorypool.heap.survivorspace.used | 已使用幸存区大小 |  |
| memorypool.heap.survivorspace.max | 幸存区的最大值 |  |
| memorypool.heap.edenspace.committed | 为伊甸园区分配的内存大小 |  |
| memorypool.heap.edenspace.used | 伊甸园区使用堆内存大小 |  |
| memorypool.heap.edenspace.max | 伊甸园区使用堆内存的最大值 |  |
| memorypool.heap.tenuredgen.max | 老年代的最大值 |  |
| memorypool.heap.tenuredgen.committed | 为老年代区分配内存大小 |  |
| memorypool.heap.tenuredgen.used | 老年代已使用堆内存大小 |  |
| memory.nonheap.used | 已使用的非堆大小 |  |
| memory.nonheap.max | 非堆的最大值 |  |
| memory.nonheap.committed | 为非堆分配内存大小 |  |
| memorypool.nonheap.codecache.committed | 为非堆代码缓存区分配内存大小 |  |
| memorypool.nonheap.codecache.used | 非堆代码缓存使用大小 |  |
| memorypool.nonheap.codecache.max | 非堆代码缓存区的最大值 |  |
| memorypool.nonheap.permgen.used | 非堆永久区的使用大小 |  |
| memorypool.nonheap.permgen.max | 非堆永久区的最大值 |  |
| memorypool.nonheap.permgen.committed | 非堆永久区分配内存大小 |  |
| gc.marksweepcompact.count | 标记-清理算法调用次数 |  |
| gc.marksweepcompact.maxtime | 标记-清理算法执行最大时间 |  |
| gc.marksweepcompact.mintime | 标记-清理算法执行最小时间 |  |
| gc.marksweepcompact.sumofsquares | 标记-清理算法执行时间的平方和 |  |
| gc.marksweepcompact.total | 标记-清理算法执行总计时间 |  |
| gc.marksweepcompact.totalexclusivetime | 标记-清理算法总计执行该方法之外的时间 |  |
| gc.copy.count | 拷贝算法次数 |  |
| gc.copy.maxtime | 拷贝算法执行最大时间 |  |
| gc.copy.mintime | 拷贝算法执行最小时间 |  |
| gc.copy.sumofsquares | 拷贝算法执行时间的平方和 |  |
| gc.copy.total | 拷贝算法执行总计时间 |  |
| gc.copy.totalexclusivetime | 拷贝算法总计执行该方法之外 |  |
| gc.all.count | gc次数 |  |
| gc.all.maxtime | gc执行最大时间 |  |
| gc.all.mintime | gc执行最小时间 |  |
| gc.all.sumofsquares | gc执行时间的平方和 |  |
| gc.all.total | gc执行总计时间 |  |
| gc.all.totalexclusivetime | gc总计执行该方法之外 |  |
| threads.count | 线程数 |  |
| threads.deadlocks.count | 死锁线程数 |  |
| cpu.user.utilization | cpu使用的利用率 |  |
| cpu.usertime | cpu使用时间 |  |

* ## 样例

\[

    {

        "content": \[

            {

                "timestamp": "1490329051890",

                "metric": "gc.copy.count",

                "value": "4"

            },

            {

                "timestamp": "1490329051890",

                "metric": "gc.copy.maxtime",

                "value": "26000"

            },

            {

                "timestamp": "1490329051890",

                "metric": "gc.copy.mintime",

                "value": "26000"

            },

            {

                "timestamp": "1490329051890",

                "metric": "gc.copy.sumofsquares",

                "value": "676000000"

            },

            {

                "timestamp": "1490329051890",

                "metric": "gc.copy.total",

                "value": "26000"

            },

            {

                "timestamp": "1490329051890",

                "metric": "gc.copy.totalexclusivetime",

                "value": "26000"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memory.nonheap.used",

                "value": "143"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memorypool.heap.survivorspace.max",

                "value": "6"

            },

            {

                "timestamp": "1490329051890",

                "metric": "cpu.usertime",

                "value": "54"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memorypool.nonheap.codecache.committed",

                "value": "13"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memorypool.heap.edenspace.committed",

                "value": "43"

            },

            {

                "timestamp": "1490329051890",

                "metric": "cpu.user.utilization",

                "value": "13"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memory.heap.committed",

                "value": "688"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memory.used",

                "value": "578"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memorypool.nonheap.permgen.used",

                "value": "130"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memory.nonheap.max",

                "value": "544"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memorypool.nonheap.codecache.used",

                "value": "13"

            },

            {

                "timestamp": "1490329051890",

                "metric": "memorypool.heap.tenuredgen.committed",

                "value": "640"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.heap.edenspace.used",

                "value": "31"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memory.physical",

                "value": "831"

            },

            {

                "timestamp": "1490329051891",

                "metric": "jvm.probe.switch",

                "value": "1"

            },

            {

                "timestamp": "1490329051891",

                "metric": "threads.count",

                "value": "53"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.nonheap.codecache.max",

                "value": "32"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memory.nonheap.committed",

                "value": "143"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.heap.survivorspace.used",

                "value": "0"

            },

            {

                "timestamp": "1490329051891",

                "metric": "threads.deadlocks.count",

                "value": "0"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.heap.edenspace.max",

                "value": "47"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.heap.survivorspace.committed",

                "value": "5"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.heap.tenuredgen.max",

                "value": "709"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memory.heap.max",

                "value": "762"

            },

            {

                "timestamp": "1490329051891",

                "metric": "gc.all.count",

                "value": "4"

            },

            {

                "timestamp": "1490329051891",

                "metric": "gc.all.maxtime",

                "value": "26000"

            },

            {

                "timestamp": "1490329051891",

                "metric": "gc.all.mintime",

                "value": "26000"

            },

            {

                "timestamp": "1490329051891",

                "metric": "gc.all.sumofsquares",

                "value": "676000000"

            },

            {

                "timestamp": "1490329051891",

                "metric": "gc.all.total",

                "value": "26000"

            },

            {

                "timestamp": "1490329051891",

                "metric": "gc.all.totalexclusivetime",

                "value": "26000"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.nonheap.permgen.max",

                "value": "512"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.nonheap.permgen.committed",

                "value": "130"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memory.heap.used",

                "value": "435"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memorypool.heap.tenuredgen.used",

                "value": "403"

            },

            {

                "timestamp": "1490329051891",

                "metric": "memory.heap.utilization",

                "value": "57"

            }

        \],

        "header": {

            "srid": "YtWELYpvZc0164342496",

            "ep": "MFTEST",

            "appid": "ztRUFZRPDK0151963951",

            "tid": "RitGmoBwfw0151671866"

        }

    }

\]

