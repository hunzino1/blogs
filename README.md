Sunhaojie's Blog
===================

Hello, 这里是孙豪杰的[技术hunzino1](https://hunzino1.github.io/hunzino1s/)源码. 在此特别感谢邓擎铧的帮助,[邓擎铧hunzino1](https://hunzino1.github.io/).

该源码基于[Rails Guides](https://github.com/rails/rails/tree/master/guides), 主要记录了自己所学时的笔记, 总结和经验, 包括下面这些内容:

* 知识树和技术栈: 如何从0开始理解和学习一门语言.
* 一些随想笔记.

--------------------------------------------------------------------------------

Usage
-----
### 安装环境
```shell
git clone https://github.com/dengqinghua/roses.git
cd roses
bundle install
```

### 编写markdown风格的文档
请参考[markdown格式实例](https://hunzino1.github.io/example.html)
将写好的文件放在 `source` 目录下

并在`source/documents.yaml`文件下编写目录.

### 生成html文件
执行脚本

```
./generate_guides

```

即可在`docs`文件夹中生成对应的html代码, 其中docs/index.html为入口文件.

源码内容简介
--------------
### 知识树
希望通过总结知识树, 可以让自己或他人更快地了解工作中需要的20%的技术知识点, 快速地根据原有自己的技术知识转化为新知识的生产力.

### 技术栈
希望通过总结技术栈, 可以了解计算机语言, 数据结构和算法的细节和本质.

### 随想笔记
这里什么都有

文章列表
--------
### 推荐
#### [业务流引擎系统](https://hunzino1.github.io/witness_flow.html)

随着系统的日益演进, 系统的业务逻辑非常复杂, 尤其是在产品需求频繁变动的情况下, 研发需要不断地进行改动代码, 最终逻辑无人知晓. 为了让核心业务逻辑更清晰, 更快速地响应业务的变更, 我们研发了业务流引擎系统. 通过 代码 + 流程图配置 的方式, 将业务的复杂度变为引擎实现的技术难度.

### Ruby
#### [Ruby知识树](https://hunzino1.github.io/blogs/ruby_knowledge_tree.html)

开发Ruby和Rails需要了解的20%内容.

#### [Ruby数据模型](https://hunzino1.github.io/blogs/ruby_knowledge_tree.html)

Ruby的数据模型, 包括方法查找, 变(常)量查找, 作用域.

#### [业务流引擎系统](https://hunzino1.github.io/blogs/witness_flow.html)

随着系统的日益演进, 系统的业务逻辑非常复杂, 尤其是在产品需求频繁变动的情况下, 研发需要不断地进行改动代码, 最终逻辑无人知晓. 为了让核心业务逻辑更清晰, 更快速地响应业务的变更, 我们研发了业务流引擎系统. 通过 代码 + 流程图配置 的方式, 将业务的复杂度变为引擎实现的技术难度.

#### [基于Sidekiq的异步任务管理引擎](https://hunzino1.github.io/blogs/sidekiq_task_event.html)

在系统中有一类常见的问题可抽象为: 批量处理n个任务, 每个任务都比较耗时, 希望可以快速地处理这些任务, 并且能知道每一个任务的执行结果情况. 基于这类问题模型, 我们研发了基于Sidekiq的异步任务管理引擎.

### Java

#### [Java知识树](https://hunzino1.github.io/blogs/java_knowledge_tree.html)

开发Java需要了解的20%内容


### MySQL
#### [MySQL知识树](https://hunzino1.github.io/blogs/mysql_knowledge_tree.html)

### 杂记
#### [markdown格式实例](https://hunzino1.github.io/blogs/example_markdown.html)

Rails Guides风格的markdown模板.

#### [注释规范](https://hunzino1.github.io/blogs/comments.html)

我们在项目中使用的注释规范.

#### [零bug落地方案](https://hunzino1.github.io/blogs/best_programming.html)

可执行的软件开发实践的零bug落地方案.

#### [Memorize My Mentor](https://hunzino1.github.io/blogs/memorize_my_mentor.html)

纪念一位Mentor,摘自擎铧博客，深有感触，自感幸运，最初步入社会就遇到一群可爱的人。

Issues
------
如果您觉得有文章对您有启发, 或者有任何问题, 可以通过邮箱联系我: coding_sun@163.com.

License
-------
- [![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
- 自由转载-非商用-非衍生-保持署名([创意共享3.0许可证](https://creativecommons.org/licenses/by-nc-nd/3.0/deed.zh))
