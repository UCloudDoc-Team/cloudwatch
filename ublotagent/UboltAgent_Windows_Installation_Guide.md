
# UboltAgent Windows 安装手册

UboltAgent Windows 版本支持 Windows 镜像的监控信息采集和上报。

---

## Windows 安装

### 准备工作

- 安装和卸载时，都需要使用具有“管理员”权限的账户（如 Administrator 用户）登录 Windows 云主机。
> **注意：**  
> 安装新版本 UboltAgent，会卸载历史安装的版本。   
> 不同操作系统支持版本请参考 [支持的CPU 云主机镜像列表](cloudwatch\ublotagent\CPUHostImageList.md)。
---

### 安装步骤

#### 登录云主机

登录云主机后，使用内网浏览器访问安装包下载路径：下载并保存安装包。注意由于浏览器安全设置，可能会有文件安全提示，请信任并下载保存。

```
http://umon.api.service.ucloud.cn/static/cloudwatch/uboltagent-v1.0.0-windows-amd64.exe
```
> **注意：**  
> 使用内网下载监控组件前，请登录 Windows 实例执行命令，并且确保云服务器为内网DNS，否则将无法解析监控组件的下载地址
#### 执行安装

进入安装包存放目录，找到下载的安装包：  `uboltagent-v1.0.0-windows-amd64.exe`，双击该文件开始安装过程，按照安装向导提示完成安装。

![](images\Windows安装向导-1.PNG)

![](images\Windows安装向导-2.PNG)

![](images\Windows安装向导-3.PNG)

![](images\Windows安装向导-4.PNG)

#### 确认安装状态

##### 方法一：使用服务管理器

1. 使用快捷键 `Win + R` 打开“运行”对话框，输入 `services.msc` 并回车。

   ![](images\打开服务管理器1.png)

2. 或通过：开始菜单 -> Windows 管理工具 -> 服务，打开服务管理器。

   ![](images\打开服务管理器2.png)

3. 找到名为 `UCloudUboltAgent`  的服务，确认其状态为“正在运行”。

   ![](images\服务管理器找到服务.png)

##### 方法二：查看日志文件

进入 Agent 的安装目录，查看 `log` 目录下的日志文件，以获取更详细的运行状态信息。

![](images\Windows查看log日志文件.png)

##### 方法三：查看云监控状态

等待约 5 分钟，进入 控制台：资源监控-> 产品监控 -> 点击资源详情，确认监控数据是否上报。

![](images\控制台确认Windows数据上报.png)

---

## Windows 卸载

1. 打开控制面板，点击“卸载程序”。

   ![](images\Windows卸载步骤1.png)

2. 找到 **UCloudBoltAgent** 程序，点击“卸载”，完成卸载操作。

   ![](images\Windows卸载步骤2.png)

   ![](images\Windows卸载步骤3.png)

   ![](images\Windows卸载步骤4.png)

---

## 注意事项
1. 在执行任何安装或卸载操作之前，请确保已备份重要数据。
2. 如遇问题或错误消息，请参考官方文档或联系技术支持。

