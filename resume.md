
## 基础信息



<table width="100%" style="border: none; border-collapse: collapse;"> <tr> <td style="border: none;">姓    名： 李兵</td> <td style="border: none;">专        业： 计算机科学与技术（本科）</td> </tr> <tr> <td style="border: none;">电    话： 185 7434 9690</td> <td style="border: none;">邮        箱： abing22333@163.com</td> </tr> <tr> <td style="border: none;">性    别： 男</td> <td style="border: none;">工作经验： 4年</td> </tr> <tr> <td style="border: none;">Github: <a href="https://github.com/abing22333" target="_blank">https://github.com/abing22333</a></td> <td style="border: none;">工作岗位： Java研发</td> </tr> </table>


## 相关技能

- 了解Java多线程，**实现过基于原子操作的锁**, 了解Jvm原理，熟悉常用垃圾回收器。
- 掌握常用的数据结构与算法、设计模式，有实际使用经验
- 熟练掌握MySQL，了解索引、事务的底层原理
- 熟练使用Redis，了解主从、哨兵的底层原理
- 熟悉使用Kafka，了解底层原理和架构
- 熟悉Raft分布式一致性共识算法，**实现过基于Raft的分布式key/value数据库**
- 熟练使用Spring Boot框架、Spring Cloud Alibaba微服务框架
- 熟练使用Git, Maven项目管理构建工具，了解Docker、Linux常用命令，学习k8s中
- 有较强的文档编写能力 (设计方案，需求分析，概要设计，详细设计)
## 项目经历



### **SDN家庭网关管理平台 （2023-07~2023-11）**

能够为**百万数量级家庭网关设备**提供升级版本、查看网关信息和业务下发等功能。  

**技术栈：** Java 17，Spring Cloud Alibaba 2022, Kafka, Redis，MySQL, Quartz

**工作职责：**

1. 负责确定开发规范（项目结构， 接口文档，Git工作流等），详细文档设计
2. 使用批量数据插入方式，降低百万级数据落库时间
3. 设备调度和设备执行模块执行效率相差悬殊，使用Kafka消息队列来进行流量削峰、模块解耦
4. 使用Quartz框架，实现时间调度功能
5. 负责设备调度模块的核心代码，重启恢复机制

### **MetaBrother服务云（2021-01~2023-06）**

是一款数字化运维管理的SaaS产品，满足全行业工单/运维/售后服务场景。对接了公众号、小程序、企业微信等外部系统。由服务管理系统，配置管理系统，库存管理系统，知识库系统，二维码系统构成。

**技术栈：**Java 8, Spring Cloud Alibaba, kafka, Redis，MySQL

**项目官网：**[https://www.metaitsaas.com/](https://www.metaitsaas.com/)

### **MetaBrother服务云-消息中心**

为上层应用提供发送消息能力，提供了发送短信、邮箱、系统消息、公众号消息、企业微信消息的能力。

**工作职责：**

1. 参与需求评审，设计技术方案
2. 引入消息模板，向上层应用屏蔽不同消息的具体细节
3. 对接了短信服务商，企业微信消息
4. 使用Redis缓存系统消息阅读情况，减轻数据库压力

### **MetaBrother服务云-知识库系统**

MetaBrother服务云产品栈的核心产品。拥有标题模糊搜索，热门知识推荐，评论、点赞等功能

**工作职责：**

1. 参与需求评审，设计技术方案，设计核心表结构
2. 开发树型评论接口，方便前端同事展示
3. 使用Redis缓存知识浏览、点赞等操作，数据定时落库
4. 对知识标题进行分词，手动维护倒排索引，实现标题模糊搜索

### **MetaBrother服务云-服务管理系统**

MetaBrother服务云产品栈的支撑产品。是一个支持工单快速查询、工单池抢单、工单挂起、指派、转派、回撤、退回、关注、催办工单系统，可以自定义表单、工作流、规则。

**工作职责：**

1. 参与需求评审，设计技术方案，设计表结构
2. 开发、维护用户、部门、工作组等基础模块，对接企业微信开放平台
3. 开发、维护工单核心参数权限校验接口（涉及接口众多，逻辑复杂）
4. 使用SpEL，开发轻量级规则引擎，实现自定义规则功能
5. 使用创建高效索引，减少无关字段查询等方法优化慢SQL

## 工作经历

* 2023-12~ 至今：深圳市图元科技有限公司（Java研发）
* 2021-06 ~ 2023-11：北京直真科技有限公司 （Java研发）
