# 产品公告

## 公告：云监控产品重大版本迭代更新
尊敬的用户：您好！

我们很高兴地宣布，我们即将对云监控产品进行一次重大版本迭代更新。此次更新不仅在产品设计、功能增强和用户易用性上均带来了显著的改进，更是我们对产品理念与用户需求的深度理解与回应。

一、产品形态的新变化

新版本中，云监控产品的整体形态发生了显著的变化。我们针对用户反馈和市场趋势，对界面设计、操作流程、功能布局等方面进行了全面优化。新版本的产品将呈现出更加直观、简洁、易用的特点，同时增加了资源更精细维度的指标监控和告警能力，以满足用户精准告警和高效运维的诉求。

二、功能亮点与差异

1. 全新界面设计：新版本重新定义了告警配置相关的概念，优化了操作流程，降低了用户的使用成本。同时采用最新的设计框架，使得整个界面与控制台一体性更强，更加简洁、直观。
2. 告警功能升级：新版本支持告警分级，支持不同阈值配置不同的告警等级；支持将告警推送至企微、飞书、钉钉或多个回调地址，更多渠道保障您及时接收告警通知。
3. 高效运维：新版本支持资源分组和条件模版功能；资源分组支持将跨地域资源统一管理，设置告警策略，提升运维效率；条件模版可以一键复用在不同策略上，简化设置。
4. 多维度数据监控告警：新版本支持多维度数据的监控和告警能力，如容器云资源监控，支持namespace、workload_kind级别的监控数据展示和告警能力。

三、提醒与帮助

请注意，在您完成从老版本到新版本CloudWatch的升级后，您之前在老版本UMon中设置的告警模板将会有所调整：
- 在老版本中已经绑定了具体资源的告警模板，将会作为告警策略直接导入到新版CloudWatch中。
- 在老版本中未绑定具体资源的告警模板，将会转换为告警条件模板，并展示在新版CloudWatch的“条件模板”页面中。
如果您有调用BindAlarmTemplate接口进行资源和告警模板绑定的使用场景：
- 如果传入的是默认模板ID，系统将正常处理。
- 如果传入的是自定义模板ID，则绑定操作失败，系统返回错误码提醒。
为了确保顺利迁移，请您在进行相关操作前仔细检查所使用的模板ID类型。

同时，为提供更好的服务，迁移完成后为保障您子账号的正常使用，将为您进行过变更操作的子账号添加对应的IAM权限。

此外，若在迁移后您有使用Pathx产品或福建泉州机房资源后出现接口不兼容的情况，请及时联系我们的技术支持团队获取帮助。

四、更新时间与方式

新版本将于10月25日正式上线，并将按批次逐步进行客户迁移。在升级过程中，若您有任何疑问或需要帮助，或者希望立即升级到新版本，请随时联系我们的客服团队。

五、感谢与期待

感谢广大用户一直以来对云监控产品的支持与信任。正是您们的反馈与建议，推动我们不断进步。在未来的日子里，期待听到更多用户的声音和建议，让我们共同打造更加优秀的云监控产品！
再次感谢您的关注与支持！让我们共同期待新版本的到来！
祝好！

## 公告：云监控新老版本差异项

| 对比点 / 产品                             | CloudWatch                                                                                                                                            | UMon                                                                                                                          |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 产品定位                                 | 提供对UCloud云平台产品资源的监控信息。通过监控模板设置及告警通知管理，使用户能够实时掌握资源及应用的运行状态，保证服务及应用稳定运行。                                                                                | 提供对UCloud云平台产品资源的监控信息。通过监控模板设置及告警通知管理，使用户能够实时掌握资源及应用的运行状态，保证服务及应用稳定运行。                                                        |
| 产品功能清单                               | 监控看图<br>产品监控（资源监控查询）<br>资源分组<br>告警记录<br>告警策略<br>告警屏蔽<br>通知人管理                                                                                         | 资源监控查询<br>告警模版<br>告警记录<br>告警屏蔽<br>通知人管理                                                                                       |
| 产品属性1<br>（影响各个模块的业务数据是全局级别，还是属于某个地域） | 全局级别，不区分地域                                                                                                                                            | 资源监控查询（地域级别，部分产品全局级别）<br>告警模版（地域级别）<br>告警记录（全局级别）<br>告警屏蔽（地域级别）<br>通知人管理（全局级别）<br>消息订阅（全局级别）                                  |
| 产品属性2<br>（影响各个模块的业务数据是全局级别，还是属于某个项目） | 监控看图（项目单选）<br>产品监控（项目单选）<br>资源分组（项目级别）<br>告警策略（项目级别）<br>告警记录（项目级别）<br>告警屏蔽（项目级别）<br>通知人管理（全局级别）                                                       | 资源监控查询（项目级别）<br>告警模版（项目级别）<br>告警记录（项目级别）<br>告警屏蔽（项目级别）<br>通知人管理（项目级别）<br>消息订阅（项目级别）                                           |
| 监控看图                                 | 跨地域多资源单指标对比看图<br>支持查看各个指标对比图<br>快捷查询资源指标监控数据<br>监控数据展示支持按数据维度过滤                                                                                       | 同地域多资源单指标对比看图                                                                                                                 |
| 拉取长时间监控数据点处理                         | 获取聚合周期内的最近的一个点                                                                                                                                        | 按照聚合策略（max\avg\sum）显示对应的值                                                                                                     |
| 产品监控                                 | 展示资源指标最新数据<br>展示所选产品+项目下的资源列表<br>资源监控详情支持对指标进行分组展示<br>支持展示资源产生的告警历史                                                                                   | 展示资源指标最新数据<br>展示所选产品+项目+地域+可用区下的资源列表                                                                                          |
| 资源分组                                 | 用户能够对同一云产品中同项目、跨地域的实例进行分组。当用户创建大量资源时，可以按需求建立资源分组，通过管理资源分组从而更便捷的管理资源、设置告警策略，提升运维效率。                                                                    | 不支持                                                                                                                           |
| 告警策略                                 | 支持将项目下的告警策略绑定到同项目下的资源或资源组<br>告警规则与资源的绑定在策略中统一配置完成<br>资源支持绑定多个告警策略<br>资源支持匹配多个告警规则<br>策略可以配置通知人或组<br>策略可以配置通知方式<br>告警规则支持匹配数据维度，精确匹配告警<br>告警规则支持告警定级配置 | 支持将项目+地域下的告警模版绑定到同项目+地域下的资源<br>资源与告警模版的绑定需要在资源列表进行绑定操作<br>资源仅支持绑定一个告警模版<br>资源仅支持匹配一个告警规则<br>策略可以配置通知组<br>由通知组的通知方式决定告警最终的通知方式 |
| 告警记录                                 | 展示某个项目+时间段下的告警记录信息                                                                                                                                    | 展示某个项目+时间段下的告警记录信息（告警恢复前，列表上只会显示第一条告警记录）                                                                                      |
| 告警屏蔽                                 | 展示某个项目下的屏蔽策略信息                                                                                                                                        | 展示某个项目+地域下的屏蔽策略信息                                                                                                             |
| 通知对象管理                               | 通知人全局级别，任何告警策略都可以绑定<br>通知组全局级别，任何告警策略都可以绑定                                                                                                            | 通知人项目级别，仅可被添加到同项目下的通知组里<br>通知组项目级别名，仅可被同项目下的告警策略绑定                                                                            |
| 主机代理uma                              | 支持                                                                                                                                                    | 支持                                                                                                                            |
