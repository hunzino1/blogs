零bug落地方案
=============

DATE: 2017-03-01

该文档涵盖了减少bug量，提高代码质量的方案.

阅读完该文档后，您将会了解到:

* 开发流程各个流程设计.
* 如何有效地降低bug率.

--------------------------------------------------------------------------------

NOTE: 提高代码质量的主要途径:
1. 优化现有开发流程
2. 对现有bug进行分析
3. 解决原有的逻辑错误(补充spec测试)

开发流程设计
------------
INFO: 开发过程中，参与者应包括：架构师，开发者，reviewer. 架构师确定需求的方向; 开发者解决需求的细节和逻辑, 并进行正确地设计；reviewer保证开发者设计的可行性和合理性

WARNING: 需求分析，方案设计 也属于开发过程的一部分，而且是最重要的一部分

![best_programming](https://raw.githubusercontent.com/dengqinghua/roses/master/assets/images/best_programming.png)

### 需求分析, 方案设计
#### 需求分析
##### 需求中的每个词语的是否理解?
  + 是否存在歧义？
  + 代码中原来是如何获取该值的？现有的设计是否能够很方便地取到这个值？

##### 需求中的每个逻辑是否合理?
  + 是否逻辑自然？
  + 是否各种状态考虑到了？
  + 从用户角度，是否存在设计问题？
  + 是否会影响历史数据?

#### 方案设计
开发者需要根据需求出一份设计文档，文档主要包括下面几部分：

- 模块划分(业务逻辑)
- 数据块字段设计
- 业务解决方案(队列, 同步机制, 接口传输等)

INFO: 一个工单是否需要出具一个设计文档，这一点由`架构师`决定

### 设计review
INFO: 设计review是指 `设计reviewer` 对 `开发者` 的设计文档进行设计审核

review的点主要包括:

- 模块划分是够有遗漏的部分
- 数据库设计是否合理
- 技术方案是否可行
- 是否需要处理历史数据

WARNING: 在开发者提交给reviewer之前，需要检查一下需要review的几个点是否都考虑到.

INFO: 对于复杂的工单，需要进行设计评审会议, 共同讨论设计方案的合理性.

INFO: 对于有多种设计方案的情况，而且`开发者`和`设计reviewer`各执一词, 则需要找到另外一位reivewer来共同评定

### 估时，实现业务逻辑
- 开发根据业务review后的结果，确认最后的估时。
- 所有的需求点，业务逻辑点，表间关系确认后，才能开始进行业务逻辑开发.

### 代码review
INFO: 代码review是指 `代码reviewer` 对 `开发者` 代码的审核

NOTE: 实现方式: 开发者需要根据`设计文档`, 与reviewer 按照模块进行`face-to-face`的代码review, 开发者需要跟 reviewer 讲一下基本的业务逻辑.

review的点主要包括:

- 各个模块业务逻辑
- 是否处理了历史数据
- 是否依赖前置条件(服务，或者有前置工单)
- 部署步骤是否填写正确
- 是否补充了重要逻辑的spec测试

WARNING: 为避免给reviewer造成很大的时间负担，开发者需要提前查看一下需要review的点。要求review的时间控制在半小时之内.

对现有bug进行分析
-----------------
将所有的bug进行分类, 可选的分类有

- 粗心，PRD未阅读仔细
- 业务逻辑不清晰
- 未考虑历史数据
- 技术上的不足

解决原有的逻辑错误
------------------
- 架构师将现有的业务线进行整理和分类，并补充各个业务块的Rspec测试
- 添加页面访问量统计，去掉不常用的页面

其他
----
### 卡片模板(各个review部分的checklist)
#### 提交设计review前`开发`的checklist

|       CheckList         |
|        --------         |
|        模块划分         |
|     数据块字段设计      |
|      业务解决方案       |
|    历史数据处理方案     |
| 新增功能对原有功能的影响 |
|       前置依赖         |

#### 设计reviewer的checklist

|   CheckList     | 一次review | 二次review | 三次review | 评分 |
|    --------     |   ------   |   ------   |   ------   | ---  |
|    模块划分     |            |            |            |      |
|  数据块字段设计  |            |            |            |      |
|    技术方案     |            |            |            |      |
| 历史数据处理方案 |            |            |            |      |
|    前置依赖     |            |            |            |      |

#### 提交代码review前`开发`的checklist

|    CheckList        |
|     --------        |
|   模块逻辑整理      |
| 数据查询优化(从库)   |
|   历史数据处理      |
|     前置条件        |
| PRD文案(以PRD文字为准) |
|    部署步骤        |
|    Rspec测试        |
|      注释          |

#### 代码reviewer的checklist

| CheckList      | 一次review | 二次review | 三次review | 评分 |
|  --------      |   ------   |   ------   |   ------   | ---- |
| 模块逻辑整理    |            |            |            |      |
| 数据查询优化(从库) |            |            |            |      |
| 历史数据处理    |            |            |            |      |
|  部署步骤      |            |            |            |      |
|  Rspec测试      |            |            |            |      |
|     注释        |            |            |            |      |
