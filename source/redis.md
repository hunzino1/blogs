Redis知识树
===========

DATE: 2018-05-10

本文档总结了Redis的知识树.

阅读完该文档后，您将会了解到:

* Redis支持的数据结构.
* 基于Redis的缓存.
* 基于Redis的分布式锁.
* 基于Redis的队列.
* Redis的持久化.
* Redis的高可用.

--------------------------------------------------------------------------------

数据结构
-------
### List
#### 实现方式
#### 常用命令

### Set
#### 实现方式
#### 常用命令

### SortedSet
#### 实现方式
#### 常用命令

### Hash
#### 实现方式
#### 常用命令

缓存
----
### 使用
### 过期机制

分布式锁
-------
### 单节点
SETNX

### 多节点
RedLock

队列
----
Sidekiq

持久化
-----
### AOF
### fsync

Redis常见面试题目
----------------