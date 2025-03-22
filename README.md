# thread
构建一个支持动态任务分配、资源隔离、实时监控的高并发任务处理系统
项目目标
构建一个支持动态任务分配、资源隔离、实时监控的高并发任务处理系统

应用场景：电商库存预扣减、金融交易订单批量处理、日志异步分析

技术焦点：线程池定制化、锁优化、并发容器、CompletableFuture、性能压测

技术选型
组件	技术方案	对应并发知识点
任务调度	自定义线程池（拒绝策略动态扩展）	ThreadPoolExecutor源码扩展
资源隔离	分组线程池+Semaphore配额控制	信号量/资源限制
任务状态管理	ConcurrentHashMap + Version字段	CAS乐观锁
任务依赖	CompletableFuture链式编排	异步编程/回调机制
监控	AtomicLong统计指标 + JMX暴露	原子类/线程安全计数器
