---
sidebar: auto
---

# ChangeLog

## 3.21

### 新增特性
1. 项目协作能力增强
* 支持企业级别对于事项属性的自定义设置 
* 支持项目级别对于事项状态、工作流的自定义设置 
* 新增项目里程碑管理，方便项目全员成员清晰项目规划目标 
* 新增迭代版本归档 
2. 代码仓库和代码质量能力增强
* 新增代码仓库的标签管理 
* 新增代码合并请求的多人审批和评分机制 
* 新增代码质量门槛配置 
3. 运维大盘新版本发布
* 同时支持在微服务治理平台和多云管理平台配置自己的Dashboard 
* 支持折线图、面积图、饼图、漏斗图、下钻地图、指标卡片和表格 
* 对标Grafana，支持图表多维度分组，指标聚合、过滤和排序，指标展示别名和单位转换等功能的界面化配置 
* 支持自定义表达式和数十种内置的聚合、转换函数 
4. 多云管理平台中新增 Service、StatefulSet、DaemonSet、configmaps管理 
* 支持 K8S 集群下的 Service 创建、编辑、详情查看和删除管理 
* 支持 K8S 集群下的 StatefulSet 创建、编辑、详情查看和删除管理 
* 支持 K8S 集群下的 DaemonSet 创建、编辑、详情查看和删除管理 
* 支持 K8S 集群下的 configmaps 创建、编辑、详情查看和删除管理 
5. 其他新增内容
* 新增数据银行和配置单管理 
* 增加测试流程逻辑控制等功能，如判断、思考时间 

### 改善内容
1. 项目协作整体交互改善
2. 应用流水线管理移动至流水线菜单管理

## 3.20

### 新增特性
1. 自动化测试平台 - 接口自动化测试基于 pipline 图形化编排的 beta 版上线
* 解决痛点：  
主要对齐业界的差距，打造自己的自动化测试平台， 
完成研发持续集成 + 自动化测试 + 上线的整体链路
2. 基于 dice.yml 控制流量入口路由
* 解决痛点：  
主要解决目前项目每次部署的时候，都需要手动配置 API 流量入口，
没有沉淀到代码或者配置文件的痛点。
3. 企业级域名资源管理
* 解决痛点：  
主要解决现在没有统一视角查看和管理企业所配置的域名，方便域名冲突等问题的定位。
4. 新增服务网格能力 -  本迭代主要提供透明加密传输功能
* 解决痛点：  
主要是增加产品在服务网格方面的能力，会持续上线负载均衡、限流熔断等功能
5. API 管理平台 - 增加了 API 流量管理审计
* 解决痛点：  
主要是完善 API 管理平台的基本能力功能

### 改善内容
1. 微服务平台治理 - 注册中心下支持通过 IP 快速查询服务以及查看服务的部署信息
2. 企业中心 - 项目管理中支持统计数据的直观展示
3. 支持超级管理员修改用户的手机和邮箱信息
4. 移动开发平台的灰度发布改善
5. 项目协作相关功能的交互改善

## 3.19

### 新增特性
1. pipeline流水线图形化编排的重新设计编版
* 解决痛点：  
主要降低 Action 编排过程中参数填写的复杂度
编排过程中 Action 通过分类管理，减少用户选择Action的难度
通过页面信息透出改善，能够让用户更直观地理解流水线内容
2. 流水线部署阶段的日志透出
* 解决痛点：  
相比以前的部署日志，对于用户来说有日志分散、Addon日志难理解的痛点，
导致应用部署出错的时候大概率需要 Dice 答疑人员来解决，这个过程效率较低，
本次通过部署日志的梳理给出准确的错误信息的同时，还有建议排查的方法给出
3. 多流水线的支持
* 解决痛点：  
解决一个应用不同场景下需要不断去调整和修改当前的流水线 pipeline.yml 文件，
通过多流线可以满足不同场景的流水线任务，比如包含代码扫描和不包含代码扫描的两条流水线
4. API 管理-- 新增客户端和访问控制管理
* 解决痛点：  
企业或者项目团队内部 API 统一设计展示、分享和调用管理
5. 代码安全漏洞的扫描
* 解决痛点：  
目前 CICD 过程中代码和依赖包的安全扫描是缺失的，
以致产品发布到客户环境后经常被扫描出问题被动解决，本次就是要把被动化主动。
6. 支持项目各环境回滚点数的设置
* 解决痛点：  
当前除生产环境以外，没有回滚点的保留，开发同学在生产环境以外想回滚的时候无法进行回滚
7. 部署参数支持文件的挂载，并且支持文件的加密
* 解决痛点：  
用户希望用文件的形式管理部署参数的时候，不能有效进行支持
8. 针对依赖库下载速度的改善，大幅缩减编译部署的时间
* 解决痛点：  
应用流水线过程中所依赖下载的库文件进行本地缓存的优化，可以大幅缩减编译部署总体时长。

### 改善内容
1. 支持应用代码分支规则管理
主要是应用分支保护和持续集成开关下放到应用设置管理，分支命名规则还是项目侧维护
2. 审计日志的全面支持
3. 支持浏览器性能自定义监控告警配置
4. 支持 Java11 的监控
5. 支持 Trantor 多分支的 API 注册
6. 支持工单问题一键转待办事项、任务支持移出和转迭代
7. 企业管理页面支持用户角色信息的查看、用户登录方式的切换（多种登录方式的时候）
8. 企业成员邀请管理
9. 代码扫描质量页面中问题和内容联动的交互改善

## 3.18

### 新增功能

1. 研发效能大盘
2. API 管理平台- 阶段1: 企业内部 API 集市管理，覆盖 API 的发布、查阅。
3. 企业级封网以及个别项目应用临时申请解封处理流程
4. 任务缺陷预计和实际工作量跟踪管理
5. 支持告警事件处理结果追踪
6. 用户角色具体权限说明页面（添加成员页面中可以查看）
7. 项目工单管理
8. 新增reporter角色，reporter用户只有工单提工单权限
9. 微服务治理平台中应用监控追加自定义运维大盘

### 改善内容

1. 流水线和部署配置参数支持快速查找
2. 平台组件es和glusterfs增加监控指标和告警
3. 支持应用的持续集成配置
4. 自定义大盘优化
5. 告警策略配置、告警分析优化
6. 待办事项的拓展，覆盖需求、缺陷和任务
7. 多云管理平台中云账号下资源总览内容优化
8. 增加用户相关的操作日志审计
9. 应用域名的默认配置支持删除
10. 缺陷复杂度修改为严重程度
11. 制品快速部署的交互优化
12. 支持默认分支的设置


## 3.17

### 新增功能

1. 企业级日志中心
   支持对接阿里云 SLS 日志服务，同时支持云服务日志和企业内所有项目应用日志清洗，通过自定义监控大盘把清洗结果指标直观进行展示
2. 平台的操作日志审计
    已经完成项目、应用、流水线、事件管理的日志审计，后续迭代中会持续完善平台其他操作的审计
3. 各环境的 CICD 工作流中新增人工审核节点开关配置，开启后需要管理员审核确认后才能部署
4. 支持内置 ES addon 的精细化管理（监控、扩缩容、运行参数配置）
5. 支持阿里云部分服务（API、WAF）的监控

### 改善内容

1. Pipeline 优化（文件不存在报错等）

2. 自定义监控大盘的交互改善

## 3.16

### 新增功能

1. 新增外置代码仓库的配置使用。
2. 新增通过制品快速在指定的环境中部署。
3. 新增项目级代码分支管理规则配置，主要包含分支名编辑、部署环境配置、该分支代码制品能够部署到指定环境的配置。
4. 新增代码仓库保护
5. 新增待办需求（Product backlog）管理，统一管理未规划需求
6. 新增任务看板
7. 新增自定义 dashboard 在线编辑器
8. 新增阿里云 API 网关对接管理（通过云 addon 的方式）
9. 新增 log4j2 日志框架的对接

### 改善内容

1. 支持企业、项目、迭代的中文名的展示
2. 支持研发事件（需求、任务、缺陷）的导出，以及查询条件的增强（按名称模糊查询、创建人等）
3. 增加事件变更通知方式，可以通过钉钉方式进行通知
4. 多云管理平台中云资源 dashboard 内容改善
5. 系统用户角色和权限的加强（增加企业项目角色、细化各角色权限）
8. 多云管理平台中新建集群的方式改善