# 版本说明

本文为您介绍监控代理（UboltAgent）的版本发布信息。

## 1.0.2

| 分类     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| 发布时间 | 2025-11-6                                                    |
| 新特性   | 1. 增加对内存ECC错误数指标的监控<br/>  a. cloudwatch_uphost_memory_ecc_errors（内存ECC错误数）<br/>  b. cloudwatch_uphost_memory_noinfo_ecc_errors（无法定位的内存ECC错误） |
| 问题修复 | 1. 解决gpu掉卡时，可能导致UboltAgent崩溃的问题<br />2.   修复部分TCP状态指标采集异常问题，包括：<br />  a. cloudwatch_uphost_tcp_closed_count（TCP_CLOSED_状态数）<br/>  b. cloudwatch_uphost_tcp_syn_recv_count（TCP_SYN_RECEIVED_状态数）<br/>  c. cloudwatch_uphost_tcp_fin_wait1_count（TCP_FIN_WAIT1_状态数）<br/>  d. cloudwatch_uphost_tcp_fin_wait2_count（TCP_FIN_WAIT2_状态数） |

