# 版本说明

本文为您介绍监控代理（UboltAgent）的版本发布信息。

## 1.3.0

| 分类     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| 发布时间 | 2025-12-5                                                    |
| 新特性   | 1. 云主机新增指标：<br/>CPU 类指标：<br/>• cloudwatch_cpu_usage_usr（用户空间 CPU 占比）<br/>• cloudwatch_cpu_usage_sys（内核空间 CPU 占比）<br/>• cloudwatch_cpu_usage_idle（CPU 空闲时间占比）<br/>• cloudwatch_cpu_usage_iowait（I/O 等待时间占比）<br/>• cloudwatch_cpu_usage_irq（硬件中断时间占比）<br/>• cloudwatch_cpu_usage_softirq（软中断时间占比）<br/>• cloudwatch_cpu_usage_steal（CPU 抢占时间占比）<br/><br/>内存类指标：<br/>• cloudwatch_memory_system_usage（系统内存使用率）<br/><br/>进程类指标：<br/>• cloudwatch_process_cpu_usage（进程 CPU 使用率）<br/>• cloudwatch_process_mem_usage（进程内存使用率）<br/>• cloudwatch_process_open_files（进程打开文件数）<br/>• cloudwatch_process_match_count（匹配到的进程数）<br/><br/>2.裸金属云主机新增指标：<br/>CPU 类指标：<br/>• cloudwatch_uphost_cpu_usage_usr（用户空间 CPU 占比）<br/>• cloudwatch_uphost_cpu_usage_sys（内核空间 CPU 占比）<br/>• cloudwatch_uphost_cpu_usage_idle（CPU 空闲时间占比）<br/>• cloudwatch_uphost_cpu_usage_iowait（I/O 等待时间占比）<br/>• cloudwatch_uphost_cpu_usage_irq（硬件中断时间占比）<br/>• cloudwatch_uphost_cpu_usage_softirq（软中断时间占比）<br/>• cloudwatch_uphost_cpu_usage_steal（CPU 抢占时间占比）<br/><br/>内存类指标：<br/>• cloudwatch_uphost_memory_system_usage（系统内存使用率）<br/><br/>进程类指标：<br/>• cloudwatch_uphost_process_cpu_usage（进程 CPU 使用率）<br/>• cloudwatch_uphost_process_mem_usage（进程内存使用率）<br/>• cloudwatch_uphost_process_open_files（进程打开文件数）<br/>• cloudwatch_uphost_process_match_count（匹配到的进程数） |
| 问题修复 | 修复 Linux 内核 3.14 及以上版本中内存使用率计算异常的问题。  |


## 1.0.2

| 分类     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| 发布时间 | 2025-11-6                                                    |
| 新特性   | 1. 增加对内存ECC错误数指标的监控<br/>       a. cloudwatch_uphost_memory_ecc_errors（内存ECC错误数）<br/>       b. cloudwatch_uphost_memory_noinfo_ecc_errors（无法定位的内存ECC错误） |
| 问题修复 | 1. 解决gpu掉卡时，可能导致UboltAgent崩溃的问题<br />2.   修复部分TCP状态指标采集异常问题，包括：<br />      a. cloudwatch_uphost_tcp_closed_count（TCP_CLOSED_状态数）<br/>      b. cloudwatch_uphost_tcp_syn_recv_count（TCP_SYN_RECEIVED_状态数）<br/>      c. cloudwatch_uphost_tcp_fin_wait1_count（TCP_FIN_WAIT1_状态数）<br/>      d. cloudwatch_uphost_tcp_fin_wait2_count（TCP_FIN_WAIT2_状态数） |

