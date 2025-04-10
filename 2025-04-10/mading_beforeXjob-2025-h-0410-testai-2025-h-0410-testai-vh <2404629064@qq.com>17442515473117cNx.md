变更，以下是对各个
根据您提供的代码项目的主要更新：

**distribution 项目**：

* **新增 UserCouponDO 实体类**： 用于存储用户优惠券信息，包括用户ID、优惠券模板ID、领取时间、有效期等。
* **新增 CouponTaskFailMapper 接口**： 用于操作优惠券任务失败记录表。
* **新增 CouponTaskMapper 接口**： 用于操作优惠券推送任务表。
* **新增 CouponTemplateMapper 接口**： 用于操作优惠券模板表，并新增 decrementCouponTemplateStock 方法用于扣减优惠券模板库存。
* **新增 UserCouponMapper 接口**： 用于操作用户优惠券表。
* **新增 DBHashModShardingAlgorithm 类**： 自定义分库算法，基于 HashMod 方式。
* **新增 TableHashModShardingAlgorithm 类**： 自定义分表算法，基于 HashMod 方式。
* **新增 BaseSendExtendDTO 类**： 定义消息发送事件基础扩充属性实体。
* **新增 MessageWrapper 类**： 定义消息体包装器。
* **新增 CouponExecuteDistributionConsumer 类**： 消费优惠券推送任务消息，并处理用户优惠券分发逻辑。
* **新增 CouponTaskExecuteConsumer 类**： 消费优惠券推送任务执行消息，并读取 Excel 文件进行用户优惠券分发。
* **新增 CouponTemplateDistributionEvent 类**： 定义优惠券模板分发事件。
* **新增 CouponTaskExecuteEvent 类**： 定义优惠券推送任务执行事件。
* **新增 AbstractCommonSendProduceTemplate 类**： 定义抽象公共发送消息组件。
* **新增 CouponExecuteDistributionProducer 类**： 优惠券推送任务执行生产者。
* **新增 CouponTaskExcelObject 类**： 定义优惠券推送任务 Excel 元数据实体。
* **新增 ReadExcelDistributionListener 类**： Excel 文件读取监听器，用于处理用户优惠券分发逻辑。
* **新增 UserCouponTaskFailExcelObject 类**： 定义用户优惠券分发失败记录写入 Excel 的实体类。
* **新增 StockDecrementReturnCombinedUtil 类**： 用于将两个字段组合成一个 int，并提取字段值。

**engine 项目**：

* **新增 EngineRedisConstant 类**： 定义分布式 Redis 缓存引擎层常量类。
* **新增 UserContext 类**： 用于存储用户登录信息。
* **新增 UserInfoDTO 类**： 定义登录用户信息实体。
* **新增 CouponRemindTypeEnum 类**： 定义优惠券提醒类型枚举。
* **新增 CouponTemplateStatusEnum 类**： 定义优惠券模板状态枚举。
* **新增 RedisStockDecrementErrorEnum 类**： 定义 Redis 扣减优惠券库存错误枚举。
* **新增 UserCouponStatusEnum 类**： 定义用户优惠券状态枚举。
* **新增 DataBaseConfiguration 类**： 数据库持久层配置类，配置 MyBatis-Plus 相关分页插件等。
* **新增 RBloomFilterConfiguration 类**： 布隆过滤器配置类。
* **新增 SwaggerConfiguration 类**： 设置文档 API Swagger 配置信息。
* **新增 UserConfiguration 类**： 用户相关配置类，用于设置用户信息拦截器。
* **新增 CouponTemplateController 类**： 优惠券模板控制层，提供查询优惠券模板接口。
* **新增 CouponTemplateRemindController 类**： 优惠券预约提醒控制层，提供创建、查询、取消预约提醒接口。
* **新增 UserCouponController 类**： 用户优惠券管理控制层，提供兑换优惠券、创建订单、核销订单、退款订单接口。
* **新增 CouponSettlementDO 类**： 定义优惠券结算单数据库持久层实体。
* **新增 CouponTemplateDO 类**： 定义优惠券模板数据库持久层实体。
* **新增 CouponTemplateRemindDO 类**： 定义优惠券预约提醒数据库持久层实体。
* **新增 UserCouponDO 类**： 定义用户优惠券数据库持久层实体。
* **新增 CouponSettlementMapper 接口**： 用于操作优惠券结算单表。
* **新增 CouponTemplateMapper 接口**： 用于操作优惠券模板表，并新增 decrementCouponTemplateStock 方法用于扣减优惠券模板库存。
* **新增 CouponTemplateRemindMapper 接口**： 用于操作优惠券预约提醒表。
* **新增 UserCouponMapper 接口**： 用于操作用户优惠券表。
* **新增 DBHashModShardingAlgorithm 类**： 自定义分库算法，基于 HashMod 方式。
* **新增 TableHashModShardingAlgorithm 类**： 自定义分表算法，基于 HashMod 方式。
* **新增 CouponTemplateService 接口**： 优惠券模板业务逻辑层，提供查询优惠券模板接口。
* **新增 CouponTemplateServiceImpl 类**： 优惠券模板业务逻辑实现层。
* **新增 CouponTemplateServiceRemindImpl 类**： 优惠券预约提醒业务逻辑实现层。
* **新增 UserCouponServiceImpl 类**： 用户优惠券业务逻辑实现层。
* **新增 DBShardingUtil 类**： 用于获取数据库分片