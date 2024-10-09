# tidbcluster 分布式数据库 TiDB Cluster

|产品中文名称|产品唯一标识|指标唯一标识|指标中文名称|单位|备注|
|:----|:----|:----|:----|:----|:----|
|分布式数据库 TiDB Cluster|tidbcluster|tidb_qps|QPS|次/s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_tps|TPS|次/s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_query_duration_99|sql执行时间99值|ms| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_query_duration_95|sql执行时间95值|ms| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_query_duration_80|sql执行时间80值|ms| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_binlog_execute_time|binglog写从库耗时|ms| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_write_binlog_latency_99|binglog写延时99值|ms| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_write_binlog_latency_95|binglog写延时95值|ms| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_write_binlog_qps|写binglog qps|次/s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_connection_usage|连接数使用率|%| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_connection_num|连接数|个| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_tiflash_mem_usage|TiFlash内存使用量|Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidb_tiflash_storage_size|TiFlash磁盘使用量|Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_storage_size|tidb节点磁盘使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_mem_usage|tidb节点内存使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_cpu_usage_rate|tidb节点cpu使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_storage_usage_rate|tidb节点磁盘使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_mem_usage_rate|tidb节点内存使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_storage_size|tikv节点磁盘使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_mem_usage|tikv节点内存使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_cpu_usage_rate|tikv节点cpu使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_storage_usage_rate|tikv节点磁盘使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_mem_usage_rate|tikv节点内存使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_mem_usage|pd节点内存使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_mem_usage_rate|pd节点内存使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_cpu_usage_rate|pd节点cpu使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_storage_size|ticdc节点磁盘使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_mem_usage|ticdc节点内存使用量| Byte| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_cpu_usage_rate| ticdc节点cpu使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_storage_usage_rate|ticdc节点磁盘使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_mem_usage_rate|ticdc节点内存使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_cpu_usage_rate |tiflash节点cpu使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_storage_usage_rate|tiflash节点磁盘使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_mem_usage_rate|tiflash节点内存使用率 | %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_node_restart |tidb集群节点重启| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_node_restart|tikv集群节点重启| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_node_restart|pd集群节点重启| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_node_restart|tiflash集群节点重启| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_node_restart|ticdc集群节点重启| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_server_is_down|TiDB 服务端口探测失败| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_server_is_down|TiFlash 服务端口探测失败| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tikv_server_is_down|TiKV 服务端口探测失败| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_server_is_down|PD 服务端口探测失败| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_server_is_down|TiCDC服务端口探测失败| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tps_usage|IO吞吐量使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_iops_usage | OPS使用率| %| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_read_tps|读吞吐量MB/s|MB/s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_write_tps|写吞吐量MB/s|MB/s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tidb_ddl_waiting_jobs|tidb集群ddl等待任务数| 个| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_cluster_down_store_nums| PD 长时间没有收到 TiKV/TiFlash 心跳| 个| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_cluster_low_space|TiKV/TiFlash 节点空间不足| 个| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_cluster_unhealthy_tikv_nums|异常状态的 Store数| 个| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_etcd_write_disk_latency|Pd节点ETCD写磁盘延迟| s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_pd_cluster_slow_tikv_nums|TiKV 慢节点数| 个| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_raft_wait_index_duration|TiFlash wait index 延迟| s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_tiflash_raft_read_index_duration|TiFlash read index 延迟| s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_cdc_checkpoint_high_delay |TiCDC 同步任务延迟| s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_cdc_resolvedts_high_delay|TiCDC 同步任务的 resolved ts 延迟| s| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_changefeed_failed|TiCDC 同步任务遇到无法自动恢复的错误| 次| |
|分布式数据库 TiDB Cluster|tidbcluster|tidbcluster_ticdc_processor_exit_with_error_count|TiCDC 同步任务报错数| 次| |
