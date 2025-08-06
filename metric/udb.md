# udb云数据库

| 产品中文名称 | 产品唯一标识 | 指标唯一标识                            | 指标中文名                   | 单位    | 备注 |
| ------------ | ------------ | --------------------------------------- | ---------------------------- | ------- | ---- |
| 云数据库     | udb          | udb_db_cpu                              | CPU使用率                    | %       |      |
| 云数据库     | udb          | udb_db_mem                              | 内存大小                     | MB      |      |
| 云数据库     | udb          | udb_db_conns                            | 连接数                       | 个      |      |
| 云数据库     | udb          | udb_db_qps                              | QPS                          | 次/s    |      |
| 云数据库     | udb          | udb_db_qps_delete                       | 删除QPS                      | 次/s    |      |
| 云数据库     | udb          | udb_db_qps_insert                       | 插入QPS                      | 次/s    |      |
| 云数据库     | udb          | udb_db_qps_select                       | 查询QPS                      | 次/s    |      |
| 云数据库     | udb          | udb_db_qps_update                       | 更新QPS                      | 次/s    |      |
| 云数据库     | udb          | udb_db_slave_delay                      | 从库同步延迟                 | 秒      |      |
| 云数据库     | udb          | udb_db_mem_usage                        | 内存使用率                   | %       |      |
| 云数据库     | udb          | udb_db_slowlog_count                    | 慢查询                       | 个      |      |
| 云数据库     | udb          | udb_db_slave_error_count                | 主从同步失败监控             | 个      |      |
| 云数据库     | udb          | udb_db_backup_error_count               | 备份失败                     | 次      |      |
| 云数据库     | udb          | udb_db_ping_error_count                 | 存活探测失败次数             | 个      |      |
| 云数据库     | udb          | udb_db_qps_replace                      | 替换QPS                      | 次/s    |      |
| 云数据库     | udb          | udb_io_count_avg                        | IO次数                       | 次/s    |      |
| 云数据库     | udb          | udb_io_transfer_avg                     | IO平均读写字节数             | Bps     |      |
| 云数据库     | udb          | udb_id_db_reboot                        | 异常重启                     | 次      |      |
| 云数据库     | udb          | udb_id_ucloudbackup_invalid             | 核心管理功能失效             | 次      |      |
| 云数据库     | udb          | udb_cpu_total_used                      | CPU使用量(核数)              | 个      |      |
| 云数据库     | udb          | udb_backup_dump_error                   | dump失败                     |         |      |
| 云数据库     | udb          | udb_id_ha_slave_error                   | 高可用主从是否异常           |         |      |
| 云数据库     | udb          | udb_db_sandbox_memory                   | DB系统总内存                 | MB      |      |
| 云数据库     | udb          | udb_db_sandbox_cache                    | DB系统总缓存                 | MB      |      |
| 云数据库     | udb          | udb_db_service_available                | 服务不可用                   |         |      |
| 云数据库     | udb          | udb_tps                                 | 事务数每秒                   | 次/s    |      |
| 云数据库     | udb          | udb_connection_max_flag                 | 连接数是否打满               |         |      |
| 云数据库     | udb          | udb_ha_slave_disk_usage                 | 高可用备库磁盘使用率         | %       |      |
| 云数据库     | udb          | udb_rwproxy_qps                         | 读写分离QPS                  | 次/s    |      |
| 云数据库     | udb          | udb_rwproxy_connection_count            | 读写分离连接数               | 个/min  |      |
| 云数据库     | udb          | udb_rwproxy_memory                      | 读写分离内存使用率           | %       |      |
| 云数据库     | udb          | udb_rwproxy_cpu                         | 读写分离CPU使用率            | %       |      |
| 云数据库     | udb          | udb_ha_health_state                     | 高可用状态                   |         |      |
| 云数据库     | udb          | udb_ha_sync_delay                       | 高可用主备数据同步延时       | 秒      |      |
| 云数据库     | udb          | udb_db_active_memory_ratio              | 活跃内存占比                 | %       |      |
| 云数据库     | udb          | udb_disk_io_await                       | 磁盘的IO响应时间             | 毫秒    |      |
| 云数据库     | udb          | udb_mongodb_active_client_readers       | 正在读的客户端数             | 个      |      |
| 云数据库     | udb          | udb_mongodb_active_client_writers       | 正在写的客户端数             | 个      |      |
| 云数据库     | udb          | udb_mongodb_insert_op_counts_total      | 累计插入操作数               | 个      |      |
| 云数据库     | udb          | udb_mongodb_query_op_counts_total       | 累计查询操作数               | 个      |      |
| 云数据库     | udb          | udb_mongodb_update_op_counts_total      | 累计更新操作数               | 个      |      |
| 云数据库     | udb          | udb_mongodb_delete_op_counts_total      | 累计删除操作数               | 个      |      |
| 云数据库     | udb          | udb_mongodb_getmore_op_counts_total     | 累计getMore操作数            | 个      |      |
| 云数据库     | udb          | udb_mongodb_command_op_counts_total     | 累计执行管控命令操作数       | 个      |      |
| 云数据库     | udb          | udb_mongodb_current_queue_total         | 读写等待队列总长度           | 个      |      |
| 云数据库     | udb          | udb_mongodb_active_conns                | 活跃连接数                   | 个      |      |
| 云数据库     | udb          | udb_mongodb_wt_cache_read_size_total    | WT缓存读入累计数据量         | Byte    |      |
| 云数据库     | udb          | udb_mongodb_wt_cache_written_size_total | WT缓存落盘累计数据量         | Byte    |      |
| 云数据库     | udb          | udb_mongodb_wt_maximum_size             | WT缓存配置的最大值           | Byte    |      |
| 云数据库     | udb          | udb_mongodb_wt_cache_usage              | WT缓存使用率                 | %       |      |
| 云数据库     | udb          | udb_mongodb_wt_cache_dirty_usage        | WT脏页的占用率               | %       |      |
| 云数据库     | udb          | udb_mongodb_wt_read_size_total          | WT磁盘读取的累计数据量       | Byte    |      |
| 云数据库     | udb          | udb_mongodb_wt_written_size_total       | WT磁盘写入的累计数据量       | Byte    |      |
| 云数据库     | udb          | udb_mongodb_current_queue_readers       | globalLock当前等待读队列长度 | 个      |      |
| 云数据库     | udb          | udb_mongodb_current_queue_writers       | globalLock当前等待写队列长度 | 个      |      |
| 云数据库     | udb          | udb_mysql_bytes_received_total          | MySQL接收数据总量            | Byte    |      |
| 云数据库     | udb          | udb_bytes_received_rate                 | MySQL接收数据速率            | bytes/s |      |
| 云数据库     | udb          | udb_mysql_bytes_sent_total              | MySQL发送数据总量            | Byte    |      |
| 云数据库     | udb          | udb_mysql_bytes_sent_rate               | MySQL发送数据速率            | bytes/s |      |
| 云数据库     | udb          | udb_io_utilization_ratio                | IO利用率                     | %       |      |
| 云数据库     | udb          | udb_io_average_queue_size               | IO等待队列长度               |         |      |
| 云数据库     | udb          | udb_standby_cpu_usage                   | 高可用备库CPU使用率          | %       |      |
| 云数据库     | udb          | udb_standby_io_wait_queue               | 高可用备库IO等待队列长度     | 个/s    |      |
| 云数据库     | udb          | udb_standby_memory_usage                | 高可用备库内存使用率         | %       |      |
| 云数据库     | udb          | udb_standby_io_wait                     | 高可用备库磁盘IO响应时间     | 毫秒    |      |
| 云数据库     | udb          | udb_standby_io_usage                    | 高可用备库IO利用率           | %       |      |
| 云数据库     | udb          | udb_ha_failover                         | 容灾记录                     | 次      |      |
| 云数据库     | udb          | udb_ha_standby_oom                      | 高可用备库OOM                | 次      |      |
| 云数据库     | udb          | udb_oom                                 | OOM                          | 次      |      |
| 云数据库     | udb          | udb_dbspaceusage                        | 磁盘使用率                   | %       |      |
| 云数据库     | udb          | udb_mysql_active_conns                  | MySQL活跃连接数              | 个      |      |
| 云数据库     | udb          | udb_mysql_connection_usage              | MySQL连接数使用率            | %       |      |
