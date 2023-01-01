# 大数据分析:BigQuery、Impala 和 Drill

> 原文：<https://www.edureka.co/blog/big-data-analytics-bigquery-impala-and-drill/>

在之前的帖子中，我们讨论了 [Apache Hive](https://haifengl.wordpress.com/2014/09/02/big-data-analytics-hive/ "Big Data Analytics: Hive") ，它首次将 SQL 引入 Hadoop。实际上有几个 Hadoop 解决方案上的 SQL 与 Hive 正面竞争。今天，我们将了解一下[Google big query](https://developers.google.com/bigquery/)[Cloudera Impala](http://www.cloudera.com/content/cloudera/en/products-and-services/cdh/impala.html)和 [Apache Drill](http://incubator.apache.org/drill/) ，它们都源自于 [Google Dremel](http://research.google.com/pubs/pub36632.html) ，后者是为 web 级数据集的交互分析而设计的。简而言之，它们是对只读数据的本地大规模并行处理查询引擎。

Google BigQuery 是 Dremel 的公共实现。BigQuery 通过 REST API 向第三方开发者提供了 Dremel 中可用的核心特性集。Impala 是 Cloudera 的开源 SQL 查询引擎，运行在 Hadoop 上。它是仿照 Dremel 和阿帕奇许可的。Impala 于 2013 年 5 月正式上市。Drill 是另一个受 Dremel 启发的开源项目，目前仍在 Apache 孵化。Impala 和 Drill 都可以直接查询 Hive 表。Impala 其实用的是 Hive 的 metastore。

Hive 基本上是一个前端，用于解析 SQL 语句，生成和优化逻辑计划，将它们转换为最终由 MapReduce 或 Tez 等后端执行的物理计划。Dremel 及其衍生产品是不同的，因为它们在本地执行查询，而不需要将它们转换为 MapReduce 作业。例如，核心 Impala 组件是一个守护进程，作为查询规划器、协调器和执行引擎在集群的每个节点上运行。每个节点都可以接受查询。计划员将请求转化为并行计划片段的集合。协调器在集群中的远程节点上启动执行。执行引擎读取和写入数据文件，并将中间查询结果传输回协调器节点。

Dremel 的两个核心技术是嵌套数据的列存储和查询执行的树架构:

## 柱状存储

数据以列存储方式存储，以实现非常高的压缩率和扫描吞吐量。

## 树形架构

该体系结构形成大规模并行分布式多级服务树，用于将查询下推到该树，然后聚集来自叶子的结果。

这些都是很好的想法，已经被其他系统采用。例如，Hive 0.13 具有用于列存储的 ORC 文件，并且可以使用 Tez 作为执行引擎，将计算结构化为有向非循环图。这两者(以及其他创新)对提高 Hive 的性能帮助很大。然而，来自 Cloudera(黑斑羚的供应商)的 [基准](http://blog.cloudera.com/blog/2014/05/new-sql-choices-in-the-apache-hadoop-ecosystem-why-impala-continues-to-lead/) 和 AMPLab 的 [基准测试表明，黑斑羚仍然具有超过 Hive 的性能领先优势。众所周知，由于硬件设置、软件调整、测试中的查询等原因，基准测试经常会有偏差。但是找出导致这种性能差异的可能的设计选择和实现细节仍然是有意义的。这可能有助于两个社区在未来改进产品。下面列出了一些可能的原因:](https://amplab.cs.berkeley.edu/benchmark/)

*   作为原生查询引擎，Impala 避免了 MapReduce/Tez 作业的启动开销。众所周知，MapReduce 程序在所有节点满负荷运行之前需要一些时间。在 Hive 中，每个查询都会遇到这个“冷启动”问题。相比之下，Impala 守护进程在引导时启动，因此总是准备好执行查询。
*   Hadoop 重用 JVM 实例来部分减少启动开销。然而，它也引入了另一个问题。Cloudera 基准测试中的节点拥有 384 GB 内存。如此大的堆实际上对重用的 JVM 实例的垃圾收集系统是一个很大的挑战。世界末日的 GC 暂停可能会增加查询的延迟。另一方面，黑斑羚更喜欢这样的大内存。
*   Impala 进程是多线程的。重要的是，计划片段的扫描部分在 SSD 上是多线程的，并利用 SSE4.2 指令。I/O 和网络系统也是高度多线程的。因此，每个单个 Impala 节点通过高水平的本地并行性更高效地运行。
*   Impala 的查询执行尽可能流水线化。在聚合的情况下，只要预聚合片段已经开始返回结果，协调器就开始最终聚合。相比之下，只有当 MapReduce 中的所有映射器都完成后，sort 和 reduce 才能启动。Tez 目前还不支持 [流水线执行](https://issues.apache.org/jira/browse/TEZ-1166) 。
*   MapReduce 将所有中间结果具体化。这个特性支持更好的可伸缩性和容错性。然而，这也大大降低了数据处理的速度。相比之下，Impala 在执行者之间传输中间结果(当然，是以可伸缩性为代价的)。Tez 允许不同类型的输入/输出，包括文件、TCP 等。但是似乎 Hive 还没有使用这个特性来避免不必要的磁盘写入。
*   MapReduce 的 reducer 采用拉模型来获得地图输出分区。对于排序后的输出，Tez 使用 MapReduce ShuffleHandler，它需要下游输入通过 HTTP 拉取数据。在多个 reducerss(或下游输入)同时运行的情况下，其中一些 reducer 很可能会尝试同时从同一个 map 节点读取数据，从而导致大量磁盘寻道，降低有效磁盘传输速率。
*   Hive 的查询表达式在编译时生成，而 Impala 使用 llvm 为“大循环”生成运行时代码，可以实现更优化的代码。
*   Tez 可以完全控制加工过程，例如，当达到限值时停止加工。对于 top-k 计算和散兵游勇处理非常有用。遗憾的是，Hive 目前没有使用该功能。顺便说一下，Dremel 使用一遍算法计算 top-k 和 count-distinct 的近似结果。尚不清楚 Impala 是否也是如此。
*   在查询执行期间，Dremel 计算药片处理时间的直方图。如果平板电脑的处理时间过长，它会被重新安排到另一台服务器上。如果速度和准确性之间的权衡是可以接受的，Dremel 可以在扫描所有数据之前返回结果，这可能会大大减少响应时间，因为一小部分表通常会花费更长的时间。虽然路线图中提到了散兵游勇的处理方式，但不清楚 Impala 是否实现了类似的机制。

如您所见，其中一些原因实际上与 MapReduce 或 Tez 有关。随着 MapReduce 和 Tez 的不断改进，Hive 未来可能会避免这些问题。此外，最后两个是 Dremel 的特性，不清楚 Impala 是否实现了它们。

总之，Dremel 及其衍生产品为我们提供了一种进行交互式大数据分析的廉价方式。Hadoop 生态系统现在对传统的关系型 MPP 数据仓库系统构成了真正的威胁。AMPLab 的基准测试表明，亚马逊红移(基于 Actian 的 ParAccel)仍然领先于 Impala，但差距很小。随着不断的改进(例如，Hive 和 Impala 都在研究基于成本的计划优化器)，我们可以期待 Hadoop/HDFS 上的 SQL 在 near 特性中处于更高的水平。

**本博客最初发表于 haifengl.wordpress.com/2015/01/06/big-data-analytics-tez/**

*Edureka 有一个由行业专家共同创建的关于大数据& Hadoop 的特别策划课程。 [点击了解更多](https://www.edureka.co/big-data-and-hadoop)*

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[2016 年十大热门科技技能掌握](https://www.edureka.co/blog/10-hottest-tech-skills-in-2016/)