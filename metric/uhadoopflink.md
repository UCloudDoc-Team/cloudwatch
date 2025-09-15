# UHadoop Flink 组件

| 产品中文名称       | 产品唯一标识 | 指标唯一标识                                      | 指标中文名                            | 单位    | 备注 |
| ------------------ | ------------ | ------------------------------------------------- | ------------------------------------- | ------- | ---- |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_checkpoints_completed_per_min | 每分钟完成的检查点数目                | 个/min  |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_job_uptime                           | Job已运行的时间                       | 秒      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_jm_heap_memory_used_ratio            | JM的堆内存使用率                      | %       |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_last_checkpoint_restore_timestamp    | 协调器上恢复最后一个检查点的时间戳    |         |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_running_jobs                  | 正在运行的job数量                     | 个      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_available_task_slots          | 当前空闲的任务槽数量                  | 个      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_tm                            | 已注册的taskmanager数量               | 个      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_checkpoints_total_per_min     | 每分钟检查点数量总数                  | 个/min  |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_checkpoints_failed_per_min    | 每分钟失败的检查点数目                | 个/min  |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_of_checkpoints_inprocess_per_min | 每分钟正在进行的检查点数目            | 个/min  |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_last_checkpoint_duration             | 完成最新一个checkpoint所花费的时间    | 毫秒    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_last_checkpoint_size                 | 最新一个checkpoint大小                | MB      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_bytes_in_local_per_second        | 每秒本地文件读取字节数                | bytes/s |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_buffers_in_local_per_second      | 每秒本地读取网络缓冲区数量            | 个/s    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_bytes_in_remote_per_second       | 每秒远端数据读取字节数                | bytes/s |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_bytes_out_per_second             | 每秒发出字节数                        | bytes/s |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_buffers_out_per_second           | 每秒发出网络缓冲区数量                | 个/s    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_records_in_per_second            | 每秒接收记录数                        | 个/s    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_records_out_per_second           | 每秒发出记录数                        | 个/s    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_operator_current_send_time           | 最后一个请求批次的1次往返所花费的时间 | 毫秒    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_jm_cpu_load                          | JMCPULoad                             | %       |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_jm_heap_memory_max                   | JM可使用的最大堆内存                  | MB      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_tm_cpu_load                          | TMCPULoad                             | %       |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_tm_heap_memory_max                   | TM的可使用的最大堆内存                | MB      |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_tm_heap_memory_used_ratio            | TM的堆内存使用率                      | %       |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_num_buffers_in_remote_per_second     | 每秒远端读取网络缓冲区数量            | 个/s    |      |
| UHadoop Flink 组件 | uhadoopflink | uhadoopflink_taskslots_total                      | 任务槽总数                            | 个      |      |