---
layout: post
category: "tech"
title:  "并行与分布处理技术总结"
tags: [并行处理,分布式处理,云计算,高性能计算,大数据分析]
---
为了对并行与分布处理具有更加全面的理解，并持续跟踪相关技术的发展，本文总结
并行与分布处理相关技术。

### 1.体系结构

### 2.云计算生态
* IaaS: [OpenStack](https://www.openstack.org/)
* PaaS: 
* SaaS: 
* FaaS: 

### 3.Hadoop生态圈

#### 3.1 调度系统
* [Hadoop YARN](http://hadoop.apache.org/): 调度系统
* [Mesos](http://mesos.apache.org/): 资源统一管理和调度的平台

#### 3.2 数据存储
* [Hadoop HDFS](http://hadoop.apache.org/): 分布存储系统
* [Hbase](http://hbase.apache.org/): Hadoop 数据库
* [Tachyon](tachyon-project.org): 分布式内存文件系统
* [Phoenix](http://phoenix.apache.org/): Hbase的SQL接口

#### 3.3 处理框架
* [Hadoop MapReduce](http://hadoop.apache.org/): MapReduce计算引擎
* [Spark](http://spark.apache.org/): 通用计算引擎
* [Flink](http://flink.apache.org/): 通用计算引擎
* [Tez](http://tez.apache.org/): DAG计算框架
* [Storm](http://storm.apache.org/): 流处理框架
* [Pig](http://pig.apache.org/): 支持脚本计算
* [Hive](https://hive.apache.org/): 支持SQL计算
* [Giraph](http://giraph.apache.org/): 图处理系统
* [Mahout](http://mahout.apache.org/): 数据挖掘算法库
* [Oozie](http://oozie.apache.org/): 工作流调度器

#### 3.4 服务
* [ZooKeeper](http://zookeeper.apache.org/): 分布应用协调
* [Kafka](http://kafka.apache.org/): 分布式发布订阅消息系统
* [Sqoop](http://sqoop.apache.org/): Sqoop是SQL-to-Hadoop的缩写，主要用于
传统数据库和Hadoop之间传输数据
* [Flume](http://flume.apache.org/): 日志收集工具
* [Ranger](http://ranger.apache.org/): Hadoop集群的权限管理工具
* [Knox](http://knox.apache.org/): Hadoop安全网关
* [Falcon](http://falcon.apache.org/): 数据生命周期管理工具
* [Ambari](http://ambari.apache.org/): 安装部署配置管理工具

### 4 HPC生态圈

#### 4.1 文件存储
* [Lustre](http://lustre.org/): 并行文件系统

#### 4.2 资源调度
* [Slurm](https://slurm.schedmd.com/): 任务调度系统

#### 4.3 编程模型与接口
* [MPI](https://www.mpi-forum.org/): 消息通信编程，常用开源实现[MPICH](http://www.mpich.org/)和[OpenMPI](https://www.open-mpi.org/)
* [OpenMP](http://www.openmp.org/): 多线程编程

#### 4.4 数学库
* [LAPACK](http://www.netlib.org/lapack/): 线性代数库
* [PETSc/Tao](http://www.mcs.anl.gov/petsc/): 可移植与可扩展的科学计算库

### 5 云计算或高性能计算提供商

#### 5.1 国家超级计算广州中心
#### 5.2 国家超级计算天津中心
#### 5.3 国家超级计算长沙中心
#### 5.4 阿里云

### 6 应用
* Indiana University的Geoffrey C.Fox研究组，分析大数据应用的特点 [网站](http://www.spidal.org/)

### 7 总结

### 8 问题

