<!--一下子提供一种思路，欢迎大家发挥 -->

# 概览
云监控（CloudWatch）是一项专为UCloud云平台中产品及资源进行监控的服务，旨在帮助云上用户实时掌握云上资源的使用情况和运行状态，并及时对故障资源进行处理，保证业务正常运行。

云监控服务默认开通，借助云监控服务，您可以全面掌控UCloud云平台上的资源使用和业务运行状况。通过告警通知管理及灵活的监控模板配置，您能够及时发现云资源异常并迅速响应，保证您的服务及应用的良性运行。


## 了解

   * [什么是云监控](/cloudwatch/introduction/intro.md)
   * [功能特性](/cloudwatch/introduction/function.md)
   * [产品优势](/cloudwatch/introduction/advantage.md)
   * [应用场景](/cloudwatch/introduction/use.md)


## 使用

   * 快速入门
        * [查看监控看图](/cloudwatch/use/start/pictures.md)
        * [创建资源分组](/cloudwatch/use/start/groups.md)
        * [查看告警记录](/cloudwatch/use/start/records.md)
        * [新建告警策略](/cloudwatch/use/start/policy.md)
        * [新建告警屏蔽](/cloudwatch/use/start/shield.md)
   * 操作指南
        * [监控查询](/cloudwatch/use/guide/monitoring.md)
        * [资源管理](/cloudwatch/use/guide/resource.md)
        * [告警管理](/cloudwatch/use/guide/alarm.md)
        * [通知人管理](/cloudwatch/use/guide/notify.md)
   * 监控指标索引
        * [云主机](/cloudwatch/metric/uhost.md)
        * [云硬盘](/cloudwatch/metric/udisk.md)
        * [共享带宽](/cloudwatch/metric/sharebandwidth.md)
        * [云数据库](/cloudwatch/metric/udb.md)
        * [云分发](/cloudwatch/metric/ucdn.md)
        * [外网弹性IP](/cloudwatch/metric/eip.md)
        * [负载均衡](/cloudwatch/metric/ulb.md)
        * [云内存存储](/cloudwatch/metric/umem.md)
        * [物理云主机](/cloudwatch/metric/uphost.md)
        * [对象存储](/cloudwatch/metric/us3.md)
        * [云内存Redis](/cloudwatch/metric/uredis.md)
        * [混合云-交换机端口](/cloudwatch/metric/hybridcloudport.md)
        * [托管云-交换机端口总流量](/cloudwatch/metric/hybridcloudportsum.md)
        * [托管Hadoop集群](/cloudwatch/metric/uhadoop.md)
        * [托管Hadoop集群节点](/cloudwatch/metric/uhadoophost.md)
        * [Kafka消息队列](/cloudwatch/metric/ukafka.md)
        * [高速通道](/cloudwatch/metric/udpn.md)
        * [负载均衡监听器](/cloudwatch/metric/ulbvserver.md)
        * [Kafka消息队列节点](/cloudwatch/metric/ukafkahost.md)
        * [堡垒机](/cloudwatch/metric/uaudithost.md)
        * [数据库审计](/cloudwatch/metric/udbaudit.md)
        * [混合云-外网-带宽](/cloudwatch/metric/hybridcloudportsum2.md)
        * [私有专区](/cloudwatch/metric/udset.md)
        * [私有专区节点](/cloudwatch/metric/udsetuhost.md)
        * [UDisk系统盘](/cloudwatch/metric/udisksystem.md)
        * [文件存储](/cloudwatch/metric/ufs.md)
        * [ES集群](/cloudwatch/metric/ues.md)
        * [ES集群节点](/cloudwatch/metric/uesnode.md)
        * [混合云专线](/cloudwatch/metric/connect.md)
        * [云内存Memcache](/cloudwatch/metric/umemcache.md)
        * [VPN隧道](/cloudwatch/metric/vpntunnel.md)
        * [分布式NewSQL数据库TiDB](/cloudwatch/metric/tidb.md)
        * [全球动态加速](/cloudwatch/metric/pathx.md)
        * [SSD云盘](/cloudwatch/metric/udiskssd.md)
        * [RocketMQ消息队列](/cloudwatch/metric/urocketmq.md)
        * [IPv6转换](/cloudwatch/metric/nat64.md)
        * [RSSD云盘](/cloudwatch/metric/udiskrssd.md)
        * [AnycastEIP](/cloudwatch/metric/anycasteip.md)
        * [数据传输服务](/cloudwatch/metric/udts.md)
        * [IPv6地址](/cloudwatch/metric/ipv6address.md)
        * [Kafka连接器](/cloudwatch/metric/ukafkasinker.md)
        * [共享流量包](/cloudwatch/metric/utrafficpack.md)
        * [SMB文件系统](/cloudwatch/metric/ufssmb.md)
        * [云数据仓库Uclickhouse](/cloudwatch/metric/uclickhouse.md)
        * [云数据仓库UClickhouse节点](/cloudwatch/metric/uclickhousenode.md)
        * [云极高性能计算](/cloudwatch/metric/epc.md)
        * [Kafka消费组](/cloudwatch/metric/kafkagroup.md)
        * [云数据库 UDB MongoDB](/cloudwatch/metric/umongodbmember.md)
        * [云数据库读写分离中间件](/cloudwatch/metric/udbproxymember.md)
        * [云数据库 UDB PostgreSQL](/cloudwatch/metric/upgsql.md)
        * [云联网带宽包](/cloudwatch/metric/ugnbw.md)
        * [数据传输服务-数据集成子任务](/cloudwatch/metric/udtsdis.md)
        * [ALB监听器](/cloudwatch/metric/als.md)
        * [轻量应用云主机](/cloudwatch/metric/ulhost.md)
        * [负载均衡内网IP](/cloudwatch/metric/lbip.md)
        * [UWAN智联接入带宽包](/cloudwatch/metric/uwscbw.md)
        * [UWAN智联VPN隧道](/cloudwatch/metric/uwsctunnel.md)
        * [CPE智能网关](/cloudwatch/metric/uwcpe.md)
        * [CPE隧道](/cloudwatch/metric/uwcpetunnel.md)
        * [弹性伸缩](/cloudwatch/metric/uas.md)
        * [高性能文件存储系统](/cloudwatch/metric/upfs.md)
        * [优睿达](/cloudwatch/metric/ureach.md)
        * [网络型负载均衡](/cloudwatch/metric/nlb.md)
        * [NLB监听器](/cloudwatch/metric/nls.md)
        * [云数据仓库 MAXIR](/cloudwatch/metric/maxir.md)
        * [云数据仓库向量版 MAXIR Vector](/cloudwatch/metric/maxirvector.md)
        * [云数据仓库 MAXIR DPS](/cloudwatch/metric/maxirdps.md)
        * [应用仓库加速](/cloudwatch/metric/uaaa.md)
        * [分布式数据库 TiDB Cluster](/cloudwatch/metric/tidbcluster.md)

[FAQ](/cloudwatch/FAQ.md)

[词汇表](/cloudwatch/_glossary.md)

