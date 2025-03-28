# 监控查询
## 创建监控面板

### 背景信息
创建监控面板，满足您对云产品运行情况不同的监控需求。

### 操作步骤
1. 登录云监控控制台。
2. 在顶部导航栏选择监控看图 > 新增面板，页面增加监控面板。

![Image text](images/1.jpg.png)

3. 配置监控面板参数：
- 选择时间范围：默认为最近1小时，用户可以自定义时间范围。
- 选择资源类型：默认为云主机，单选，展示已接入监控的产品列表。
- 选择项目：默认选择一个项目，单选，展示用户可见的项目列表。
- 指标：根据所选择的资源类型，出现该类型下的指标列表，默认选择一个【单选】。
- 资源对象：根据所选择的资源类型+项目，出现其下的资源列表，支持搜索选择【多选】。（最多选择10个资源）
- 手动刷新：点击手动刷新按钮，可以刷新最新数据。
4. 完成监控面板的创建。
  
![Image text](images/1111.png)
  
## 删除监控看图

### 背景信息
当您业务发生变更或需要对监控看图页面上的监控面板进行重新规划时，您可以删除该监控面板。

### 操作步骤
1. 登录云监控控制台。
2. 在顶部导航栏选择监控看图 。
3. 选择需要删除的监控面板，单击右上角的关闭按钮。
   
![Image text](images/5.png)

## 查看监控看图
### 背景信息
云监控（CloudWatch）为客户提供了多种方式查看资源的监控数据。

入口1：监控面板添加完成后，您可以在监控看图页面查看该监控指标的监控走势图。

入口2：您可以在产品监控页面，在对应资源所属的云产品类别中，查找到对应资源，并在资源详情中查看资源的监控数据。

### 操作步骤
#### 入口1：通过监控看图查看
1. 登录云监控控制台。
2. 在顶部导航栏选择监控看图 > 新增面板，页面增加监控面板。

![Image text](images/2.jpg.png)

4. 在监控面板配置需要查看的监控指标参数：
- 选择时间范围：默认为最近1小时，用户可以自定义时间范围。
- 选择资源类型：默认为云主机，单选，展示已接入监控的产品列表。
- 选择项目：默认选择一个项目，单选，展示用户可见的项目列表。
- 指标：根据所选择的资源类型，出现该类型下的指标列表，默认选择一个【单选】。
- 资源对象：根据所选择的资源类型+项目，出现其下的资源列表，支持搜索选择【多选】。
- 手动刷新：点击手动刷新按钮，可以刷新最新数据。
4. 在监控看图页面查看该监控指标的监控走势图

#### 入口2：通过产品监控查看
1. 登录云监控控制台。
2. 在顶部导航栏，选择产品监控 。
3. 在产品监控页面，单击目标云产品。
4. 在目标云产品的监控页面，单击目标资源对应操作列的详情。
![Image text](images/3.jpg.png)

6. 在资源详情页查看该云产品中指定资源的监控看图。
![Image text](images/4.png)
