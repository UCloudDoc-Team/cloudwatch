# ulbvserver负载均衡监听器

| 产品中文名称  | 产品唯一标识     | 指标唯一标识                             | 指标中文名称                 | 单位  | 备注 |
|---------|------------|------------------------------------|------------------------|-----|----|
| 负载均衡监听器 | ulbvserver | ulbvserver_ulb_current_connections | VServer连接数             | 个   |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb4_vserver_pps_in            | ulb4的vserver 网卡入包量     | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb4_vserver_pps_out           | ulb4的vserver 网卡出包量     | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb4_vserver_bps_in            | ulb4的vserver 网络入口      | bps |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb4_vserver_bps_out           | ulb4的vserver 网络出口      | bps |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb7_vs_new_connections        | 新建连接数                  | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulbvserver_hrsp_2xx                | ulb7的vserver HTTP 2XX  | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulbvserver_hrsp_3xx                | ulb7的vserver HTTP 3XX  | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulbvserver_hrsp_4xx                | ulb7的vserver HTTP 4XX  | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulbvserver_hrsp_5xx                | ulb7的vserver HTTP 5XX  | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulbvserver_hrsp_other              | ulb7的vserver HTTP其他返回码 | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb7_vs_qps                    | ulb7的vserver 每秒请求数     | 个/s |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb7_rs_down_percent           | 节点失效百分比                | %   |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb7_vs_rt                     | ulb7的vserver 平均请求时间    | ms  |    |
| 负载均衡监听器 | ulbvserver | ulb_ulb7_vs_upstream_rt            | ulb7的vserver 后端平均响应时间  | ms  |    |
