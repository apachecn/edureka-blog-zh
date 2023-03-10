# Apache Spark 架构–Spark 集群架构说明

> 原文：<https://www.edureka.co/blog/spark-architecture/>

Apache Spark 是一个开源集群计算框架，它正在点燃大数据世界。根据 ***[Spark 认证专家](https://www.edureka.co/apache-spark-scala-training)*** 的说法，与 Hadoop 相比，Sparks 的内存性能快 100 倍，磁盘性能快 10 倍。 在这篇博客中，我将简要介绍 Spark 架构以及 Spark 架构的基础。

在这篇 Spark 架构文章中，我将涉及以下主题:

*   [星火&其特色](#Spark)
*   [星火架构概述](#Overview)
*   [星火生态系统](#SparkE)
*   [](#rdds)
*   [星火架构](#Working)
*   [Spark Shell 中使用 Scala 的例子](#Scala)

## **星火&其特色**

Apache Spark 是一个用于实时数据处理的开源集群计算框架。Apache Spark 的主要特点是它的 ***内存集群计算*** 提高了应用程序的处理速度。Spark 提供了一个接口，通过隐式 ***数据并行和容错*** 对整个集群进行编程。它旨在涵盖广泛的工作负载，如批处理应用程序、迭代算法、交互式查询和流。

### **阿帕奇 Spark 的特点:**

![Spark Features- Spark Architecture-Edureka](img/9dad46e15f13a6e114742631cfbd709c.png)

                                                           Fig: Features of Spark



1.  **速度** Spark 运行速度比 Hadoop MapReduce 大规模数据处理快 100 倍。它还能够通过受控分区来实现这一速度。
2.  **强大的缓存** 简单的编程层提供了强大的缓存和磁盘持久化能力。
3.  **部署** 可以通过 ***Mesos，Hadoop via YARN，或者 Spark 自带的集群管理器进行部署。***
4.  **实时** 它提供实时计算&低延迟，因为 ***内存计算。***
5.  **Polyglot**Spark 提供 Java、Scala、Python、r 的高级 API，Spark 代码可以用这四种语言中的任意一种编写。它还提供了 Scala 和 Python 中的 shell。

## **星火架构概述**

Apache Spark 有一个定义良好的分层架构，其中所有 Spark 组件和层都是松散耦合的。这个架构进一步集成了各种扩展和库。 Apache Spark 架构基于两个主要的抽象:

*   *【弹性分布式数据集(RDD)*
*   *【有向无环图】*

![Spark Architecture _ Edureka](img/7b15fb75baab5d4e2b5453fc1454e80e.png)

                                                        Fig: Spark Architecture



但是在深入 Spark 架构之前，让我解释一下 Spark 的几个基本概念，比如 Spark 生态系统和 RDD。这将有助于你获得更好的见解。

我先解释一下什么是星火生态系统。

## **星火生态系统**

从下图可以看出，spark 生态系统由各种组件组成，如 Spark SQL、Spark Streaming、MLlib、GraphX 和核心 API 组件。

![Spark Eco-system- Spark Architecture - edureka](img/f4ad1fda23e9ce2d83af4c99bfa48ee9.png)

                                                              Fig: Spark Eco-System



1.  **Spark Core**Spark Core 是大规模并行和分布式数据处理的基础引擎。此外，构建在内核顶部的附加库允许流、SQL 和机器学习的不同工作负载。它负责内存管理和故障恢复，调度、分发和监控与存储系统交互的集群&上的作业。
2.  **Spark Streaming**Spark Streaming 是 Spark 的组件，用于处理实时流数据。因此，它是对核心 Spark API 的有益补充。它支持实时数据流的高吞吐量和容错流处理。
3.  **Spark SQL**Spark SQL 是 Spark 中的一个新模块，它将关系处理与 Spark 的函数式编程 API 集成在一起。它支持通过 SQL 或 Hive 查询语言查询数据。对于那些熟悉 RDBMS 的人来说，Spark SQL 将是从早期工具的简单过渡，在早期工具中，您可以扩展传统关系数据处理的边界。
4.  **GraphX** GraphX 是图形和图形并行计算的 Spark API。因此，它用弹性分布式属性图扩展了火花 RDD。在高层次上，GraphX 通过引入弹性分布式属性图(每个顶点和边都有属性的有向多图)扩展了 Spark RDD 抽象。
5.  **MLlib(机器学习)** MLlib 代表机器学习库。Spark MLlib 用于在 Apache Spark 中执行机器学习。
6.  ***SparkR*** 它是一个提供分布式数据帧实现的 R 包。它还支持选择、过滤、聚合等操作，但是是在大型数据集上。

如你所见，Spark 附带了高级库，包括对 R、SQL、Python、Scala、Java 等的支持。这些标准库增加了复杂工作流程中的无缝集成。此外，它还允许各种服务与其集成，如 MLlib、GraphX、SQL +数据帧、流服务等。来增强它的能力。通过 [蔚蓝数据工程认证](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 可以更好的了解。

现在，让我们讨论 Spark 的基本数据结构，即 RDD。

#### 订阅我们的 YouTube 频道获取新的更新...