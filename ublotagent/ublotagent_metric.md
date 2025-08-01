# UBlotAgent采集指标说明

## UHost(云主机)

|指标ID|监控名称|单位|维度|采集方式(Linux)|采集方式(Windows)|
|:--|:--|:--|:--|:--|:--|
|cloudwatch_loadavg1m|LoadAverage 1min|无|-|系统过去1分钟的平均负载。<br>通过读取/proc/loadavg中的值得到|不支持|
|cloudwatch_loadavg5m|LoadAverage 5min|无|-|系统过去5分钟的平均负载。<br>通过读取/proc/loadavg中的值得到|不支持|
|cloudwatch_loadavg15m|LoadAverage 15min|无|-|系统过去15分钟的平均负载。<br>通过读取/proc/loadavg中的值得到|不支持|
|cloudwatch_memory_usage|内存使用率|%|-|系统内存使用百分比。<br>通过读取/proc/meminfo中的数据并计算得到：(Total - Free - Buffers - Cached - Sreclaimable) / Total * 100|系统内存使用百分比。。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结构中取dwMemoryLoad字段值得到|
|cloudwatch_memory_free_space|空闲内存量|MB|-|空闲的物理内存大小。<br>通过读取/proc/meminfo中的MemFree值得到|空闲的物理内存大小。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结果取ullAvailPhys值得到。|
|cloudwatch_memory_available_space|可用内存量|MB|-|可用的物理内存大小。<br>通过读取/proc/meminfo中的MemAvailable值得到(kernel3.14+)|可用的物理内存大小。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结果取ullAvailPhys值得到。|
|cloudwatch_memory_actualused_space|已用内存量|MB|-|实际使用的物理内存大小。<br>通过读取/proc/meminfo中数据并计算得到：Total - Free - Buffers - Cached - Sreclaimable|实际使用的物理内存大小。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结果取ullTotalPhys - ullAvailPhys值得到。|
|cloudwatch_process_count|进程总数|counts|-|系统当前运行的进程总数。<br>通过统计/proc/下存在的进程个数统计|系统当前运行的进程总数。<br>通过调用Widdows API: EnumProcesses列出所有进程列表，再统计存活的进程个数得到。|
|cloudwatch_runnable_process_count|运行进程数|counts|-|处于运行中或可运行状态的进程数量。<br>通过统计/proc/{{pid}}/status的State状态(R状态)得到|不支持|
|cloudwatch_block_process_count|阻塞进程数|counts|-|处于不可中断睡眠状态的进程数量。。<br>通过统计/proc/{{pid}}/status的State状态(D状态)得到|不支持|
|cloudwatch_tcp_establish_count|TCP ESTABLISHED 状态数|counts|-|处于 ESTABLISHED 状态的TCP连接数量。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 ESTABLISHED 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_close_wait_count|TCP CLOSE_WAIT 状态数|counts|-|处于 CLOSE_WAIT 状态的TCP连接数量。。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 CLOSE_WAIT 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_fin_wait1_count|TCP FIN_WAIT1 状态数|counts|-|处于 FIN_WAIT1 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 FIN_WAIT1 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_fin_wait2_count|TCP FIN_WAIT2 状态数|counts|-|处于 FIN_WAIT2 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 FIN_WAIT2 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_time_wait_count|TCP TIME_WAIT 状态数|counts|-|处于 TIME_WAIT 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于TIME_WAIT状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_listen_count|TCP LISTEN 状态数|counts|-|处于 LISTEN 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 LISTEN 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_closed_count|TCP CLOSED 状态数|counts|-|处于 CLOSED 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 CLOSED 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_syn_recv_count|TCP SYN_RECV 状态数|counts|-|处于 SYN_RECV 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 SYN_RECV 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_syn_sent_count|TCP SYN_SENT 状态数|counts|-|处于 SYN_SENT 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 SYN_SENT 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_last_ack_count|TCP LAST_ACK 状态数|counts|-|处于 LAST_ACK 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 LAST_ACK 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_closing_count|TCP CLOSING 状态数|counts|-|处于 CLOSING 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 CLOSING 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_tcp_connection_count|TCP连接数|counts|-|所有状态的TCP连接总数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于所有状态的个数|所有状态的TCP连接总数|
|cloudwatch_disk_read_only|只读磁盘数量|counts|-|处于只读模式的磁盘/分区数量。|处于只读模式的分区数量。|
|cloudwatch_sys_disk_used_per|系统盘使用率|%|key:disk<br />value:磁盘名称<br />key:mount<br />value:挂载点|系统盘空间使用百分比。<br>通过得到挂载点为/的磁盘/分区的空间使用率得到。|系统盘空间使用百分比。<br>盘符为C:的的分区空间使用率。|
|cloudwatch_data_disk_used_per|数据盘使用率|%|key:disk<br />value:磁盘名称<br />key:mount<br />value:挂载点|数据磁盘/分区空间使用百分比。<br>所有挂载点不是/的，类型为磁盘/分区的物理块设备的空间使用率。|数据磁盘/分区空间使用百分比。<br>所有盘符不是C:的分区的空间使用率。|
|cloudwatch_diskpart_inode_usage|磁盘分区inode使用率|%|key:disk<br />value:磁盘名称<br />key:mount<br />value:挂载点|文件系统inode使用百分比。<br>通过系统调用statfs或statvfs得到文件系统inode使用率（空闲inode节点数/总inode节点数*100%）。|不支持|
|cloudwatch_available_gpu_num_by_driver|驱动识别的GPU卡数量|counts|-|驱动程序识别的可用GPU数量|不支持|
|cloudwatch_available_gpu_num_by_pcie|硬件识别的GPU卡数量|counts|-|通过PCIe总线识别的可用GPU数量|不支持|
|cloudwatch_gpu_memory_used|GPU卡显存使用量|MB|key:gpu_bus_id<br/>value:GPU总线ID|显卡显存当前使用量|不支持|
|cloudwatch_gpu_driver_detectable|GPU卡驱动可识别性|无|key:gpu_bus_id<br/>value:GPU总线ID|显卡驱动是否正常加载(0/1布尔值)|不支持|
|cloudwatch_gpu_util|GPU卡使用率|%|key:gpu_bus_id<br/>value:GPU总线ID|显卡计算核心利用率|不支持|
|cloudwatch_gpu_memory_usage|GPU卡显存使用率|%|key:gpu_bus_id<br/>value:GPU总线ID|显存使用占总显存的百分比|不支持|
|cloudwatch_gpu_card_down|GPU掉卡|无|-|GPU是否处于故障状态(0=正常,1=故障)|不支持|
|cloudwatch_gpu_power_usage|GPU功耗使用率|%|key:gpu_bus_id<br/>value:GPU总线ID|当前功耗占功率上限的百分比|不支持|
|cloudwatch_gpu_memory_free|GPU显存空闲量|MB|key:gpu_bus_id<br/>value:GPU总线ID|显卡可用显存大小|不支持|
|cloudwatch_gpu_memory_total|GPU显存总量|MB|key:gpu_bus_id<br/>value:GPU总线ID|显卡物理显存总大小|不支持|
|cloudwatch_gpu_uncorr_ecc|GPU卡ecc纠错|times|key:gpu_bus_id<br/>value:GPU总线ID|显存不可纠正的ECC错误数量|不支持|
|cloudwatch_gpu_utilization_encoder|编码器使用率|%|key:gpu_bus_id<br/>value:GPU总线ID|视频编码硬件单元使用率|不支持|
|cloudwatch_gpu_utilization_decoder|解码器使用率|%|key:gpu_bus_id<br/>value:GPU总线ID|视频解码硬件单元使用率|不支持|
|cloudwatch_gpu_power_draw|GPU功耗使用量|W|key:gpu_bus_id<br/>value:GPU总线ID|显卡当前实际消耗功率|不支持|
|cloudwatch_gpu_power_limit|GPU功耗总量|W|key:gpu_bus_id<br/>value:GPU总线ID|显卡设置的功率上限|不支持|
|cloudwatch_pcie_link_gen_gpucurrent|PCI-E当前链路版本|无|key:gpu_bus_id<br/>value:GPU总线ID|GPU当前使用的PCIe代数(如3.0/4.0)|不支持|
|cloudwatch_pcie_link_gen_gpumax|GPU和PCI-E的最大链路版本|无|key:gpu_bus_id<br/>value:GPU总线ID|GPU支持的最高PCIe代数|不支持|
|cloudwatch_pcie_link_width_current|PCI-E当前链路带宽|无|key:gpu_bus_id<br/>value:GPU总线ID|GPU当前PCIe通道宽度(如x16)|不支持|
|cloudwatch_pcie_link_width_max|PCI-E最大链路带宽|无|key:gpu_bus_id<br/>value:GPU总线ID|GPU支持的最大PCIe通道宽度|不支持|
|cloudwatch_pcie_util_tx|PCI-E发送量|MB/s|key:gpu_bus_id<br/>value:GPU总线ID|PCIe总线发送方向带宽利用率|不支持|
|cloudwatch_pcie_util_rx|PCI-E接受量|MB/s|key:gpu_bus_id<br/>value:GPU总线ID|PCIe总线接收方向带宽利用率|不支持|
|cloudwatch_nvlink_link_state|NVLink链路激活状态|无|key:gpu_bus_id<br/>value:GPU总线ID|多GPU间NVLink连接状态(0=断开,1=连接)|不支持|
|cloudwatch_nvlink_throughput_raw_tx|NVLink当前发送（TX）速率|MB/s|key:gpu_bus_id<br/>value:GPU总线ID|NVLink发送方向的原始数据传输速率|不支持|
|cloudwatch_nvlink_throughput_raw_rx|NVLink当前接收（RX）速率|MB/s|key:gpu_bus_id<br/>value:GPU总线ID|NVLink接收方向的原始数据传输速率|不支持|

## UPhost(裸金属云主机)

|指标ID|监控名称|单位|维度|采集方式(Linux)|采集方式(Windows)|
|:--|:--|:--|:--|:--|:--|
|cloudwatch_uphost_load_avg1m|LoadAverage 1min|无|-|系统过去1分钟的平均负载。<br>通过读取/proc/loadavg中的值得到|不支持|
|cloudwatch_uphost_load_avg5m|LoadAverage 5min|无|-|系统过去5分钟的平均负载。<br>通过读取/proc/loadavg中的值得到|不支持|
|cloudwatch_uphost_load_avg15m|LoadAverage 15min|无|-|系统过去15分钟的平均负载。<br>通过读取/proc/loadavg中的值得到|不支持|
|cloudwatch_uphost_mem_usage|内存使用率|%|-|系统内存使用百分比。<br>通过读取/proc/meminfo中的数据并计算得到：(Total - Free - Buffers - Cached - Sreclaimable) / Total * 100|系统内存使用百分比。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结构中取dwMemoryLoad字段值得到|
|cloudwatch_uphost_mem_free|空闲内存量|MB|-|空闲的物理内存大小。<br>通过读取/proc/meminfo中的MemFree值得到|空闲的物理内存大小。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结果取ullAvailPhys值得到。|
|cloudwatch_uphost_mem_available_space|可用内存量|MB|-|可用的物理内存大小。<br>通过读取/proc/meminfo中的MemAvailable值得到(kernel3.14+)|空闲的物理内存大小。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结果取ullAvailPhys值得到。|
|cloudwatch_uphost_mem_actualused_space|已用内存量|MB|-|实际使用的物理内存大小。<br>通过读取/proc/meminfo中数据并计算得到：Total - Free - Buffers - Cached - Sreclaimable|实际使用的物理内存大小。<br>通过调用Windows API：GlobalMemoryStatusEx，从返回结果取ullTotalPhys - ullAvailPhys值得到。|
|cloudwatch_uphost_process_count|进程总数|counts|-|系统当前运行的进程总数。<br>通过统计/proc/下存在的进程个数统计|系统当前运行的进程总数。<br>通过调用Widdows API: EnumProcesses列出所有进程列表，再统计存活的进程个数得到。|
|cloudwatch_uphost_runnable_process_count|运行进程数|counts|-|处于运行中或可运行状态的进程数量。<br>通过统计/proc/{{pid}}/status的State状态(R状态)得到|不支持|
|cloudwatch_uphost_block_process_count|阻塞进程数|counts|-|处于不可中断睡眠状态的进程数量。。<br>通过统计/proc/{{pid}}/status的State状态(D状态)得到|不支持|
|cloudwatch_uphost_tcp_establish_count|TCP ESTABLISHED 状态数|counts|-|处于 ESTABLISHED 状态的TCP连接数量。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 ESTABLISHED 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_close_wait_count|TCP CLOSE_WAIT 状态数|counts|-|处于 CLOSE_WAIT 状态的TCP连接数量。。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 CLOSE_WAIT 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_fin_wait1_count|TCP FIN_WAIT1 状态数|counts|-|处于 FIN_WAIT1 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 FIN_WAIT1 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_fin_wait2_count|TCP FIN_WAIT2 状态数|counts|-|处于 FIN_WAIT2 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 FIN_WAIT2 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_time_wait_count|TCP TIME_WAIT 状态数|counts|-|处于 TIME_WAIT 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于TIME_WAIT状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_listen_count|TCP LISTEN 状态数|counts|-|处于 LISTEN 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 LISTEN 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_closed_count|TCP CLOSED 状态数|counts|-|处于 CLOSED 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 CLOSED 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_syn_recv_count|TCP SYN_RECV 状态数|counts|-|处于 SYN_RECV 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 SYN_RECV 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_syn_sent_count|TCP SYN_SENT 状态数|counts|-|处于 SYN_SENT 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 SYN_SENT 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_last_ack_count|TCP LAST_ACK 状态数|counts|-|处于 LAST_ACK 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 LAST_ACK 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_closing_count|TCP CLOSING 状态数|counts|-|处于 CLOSING 状态的TCP连接数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于该状态的连接数量得到。|处于 CLOSING 状态的TCP连接数量。<br>通过调用Windows API：GetTcpTable2、GetTcp6Table2得到ipv4、ipv6的tcp连接表，解析并统计该状态的tcp连接数量。|
|cloudwatch_uphost_tcp_connection_count|TCP连接数|counts|-|所有状态的TCP连接总数。<br>通过统计/proc/net/tcp、/proc/net/tcp6中处于所有状态的个数|所有状态的TCP连接总数|
|cloudwatch_uphost_readonly_disk_count|只读磁盘数量|counts|-|处于只读模式的磁盘/分区数量。|处于只读模式的分区数量。|
|cloudwatch_uphost_root_space_usage|系统盘使用率|%|key:disk<br />value:磁盘名称<br />key:mount<br />value:挂载点|系统盘空间使用百分比。<br>通过得到挂载点为/的磁盘/分区的空间使用率得到。|系统盘空间使用百分比。<br>盘符为C:的的分区空间使用率。|
|cloudwatch_uphost_data_space_usage|数据盘使用率|%|key:disk<br />value:磁盘名称<br />key:mount<br />value:挂载点|数据盘/分区空间使用百分比。<br>所有挂载点不是/的，类型为磁盘/分区的物理块设备的空间使用率。|数据盘/分区空间使用百分比。<br>所有盘符不是C:的分区的空间使用率。|
|cloudwatch_uphost_available_gpu_num_by_driver|驱动识别的GPU卡数量|counts|-|驱动程序识别的可用GPU数量|不支持|
|cloudwatch_uphost_available_gpu_num_by_pcie|硬件识别的GPU卡数量|counts|-|通过PCIe总线识别的可用GPU数量|不支持|
|cloudwatch_uphost_gpu_memory_used|GPU卡显存使用量|MB| key:gpu_bus_id value:GPU总线ID                               |显卡显存当前使用量|不支持|
|cloudwatch_uphost_gpu_driver_detectable|GPU卡驱动可识别性|无|key:gpu_bus_id value:GPU总线ID|显卡驱动是否正常加载(0/1布尔值)|不支持|
|cloudwatch_uphost_gpu_util|GPU卡使用率|%|key:gpu_bus_id value:GPU总线ID|显卡计算核心利用率|不支持|
|cloudwatch_uphost_gpu_memory_usage|GPU卡显存使用率|%|key:gpu_bus_id value:GPU总线ID|显存使用占总显存的百分比|不支持|
|cloudwatch_uphost_gpu_card_down|GPU掉卡|无|-|GPU是否处于故障状态(0=正常,1=故障)|不支持|
|cloudwatch_uphost_gpu_power_usage|GPU功耗使用率|%|key:gpu_bus_id value:GPU总线ID|当前功耗占功率上限的百分比|不支持|
|cloudwatch_uphost_gpu_memory_free|GPU显存空闲量|MB|key:gpu_bus_id value:GPU总线ID|显卡可用显存大小|不支持|
|cloudwatch_uphost_gpu_memory_total|GPU显存总量|MB|key:gpu_bus_id value:GPU总线ID|显卡物理显存总大小|不支持|
|cloudwatch_uphost_gpu_uncorr_ecc|GPU卡ecc纠错|times|key:gpu_bus_id value:GPU总线ID|显存不可纠正的ECC错误数量|不支持|
|cloudwatch_uphost_gpu_utilization_encoder|编码器使用率|%|key:gpu_bus_id value:GPU总线ID|视频编码硬件单元使用率|不支持|
|cloudwatch_uphost_gpu_utilization_decoder|解码器使用率|%|key:gpu_bus_id value:GPU总线ID|视频解码硬件单元使用率|不支持|
|cloudwatch_uphost_gpu_power_draw|GPU功耗使用量|W| key:gpu_bus_id value:GPU总线ID                               |显卡当前实际消耗功率|不支持|
|cloudwatch_uphost_gpu_power_limit|GPU功耗总量|W|key:gpu_bus_id value:GPU总线ID|显卡设置的功率上限|不支持|
|cloudwatch_uphost_pcie_link_gen_gpucurrent|PCI-E当前链路版本|无|key:gpu_bus_id value:GPU总线ID|GPU当前使用的PCIe代数(如3.0/4.0)|不支持|
|cloudwatch_uphost_pcie_link_gen_gpumax|GPU和PCI-E的最大链路版本|无|key:gpu_bus_id value:GPU总线ID|GPU支持的最高PCIe代数|不支持|
|cloudwatch_uphost_pcie_link_width_current|PCI-E当前链路带宽|无|key:gpu_bus_id value:GPU总线ID|GPU当前PCIe通道宽度(如x16)|不支持|
|cloudwatch_uphost_pcie_link_width_max|PCI-E最大链路带宽|无|key:gpu_bus_id value:GPU总线ID|GPU支持的最大PCIe通道宽度|不支持|
|cloudwatch_uphost_pcie_util_tx|PCI-E发送量|MB/s|key:gpu_bus_id value:GPU总线ID|PCIe总线发送方向带宽利用率|不支持|
|cloudwatch_uphost_pcie_util_rx|PCI-E接受量|MB/s|key:gpu_bus_id value:GPU总线ID|PCIe总线接收方向带宽利用率|不支持|
|cloudwatch_uphost_nvlink_link_state|NVLink链路激活状态|无|key:gpu_bus_id value:GPU总线ID|多GPU间NVLink连接状态(0=断开,1=连接)|不支持|
|cloudwatch_uphost_nvlink_throughput_raw_tx|NVLink当前发送（TX）速率|MB/s|key:gpu_bus_id value:GPU总线ID|NVLink发送方向的原始数据传输速率|不支持|
|cloudwatch_uphost_nvlink_throughput_raw_rx|NVLink当前接收（RX）速率|MB/s|key:gpu_bus_id value:GPU总线ID|NVLink接收方向的原始数据传输速率|不支持|
