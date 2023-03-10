# OLTP 与 OLAP

> 原文：<https://www.edureka.co/blog/oltp-vs-olap/>

[//www.youtube.com/embed/SaxtCeONG80](//www.youtube.com/embed/SaxtCeONG80)

## **OLTP vs OLAP**

OLTP 更像是一个在线事务系统或数据存储系统，用户使用数据存储进行大量在线事务处理。据说它还有更多实时的随机读/写操作。

OLAP 更像是一个离线数据商店。它以离线方式被访问次。例如，读取大容量日志文件，然后将其写回数据文件。使用 OLAP 的一些常见领域是日志作业、数据挖掘作业等。

据说 Cassandra 更像 OLTP，因为它是实时的，而 Hadoop 更像 OLAP，因为它用于分析和批量写入。

## **为什么要整合 OLAP & OLTP？**

如果您正在寻找未来 365 天内最便宜的酒店预订价格，这里有一个巨大的 Cassandra 数据集，并希望在实时数据库中获得推荐，一个促销活动将根据价格进行。

在这种情况下，我们必须迭代所有记录，并在其上保持分析，这是一项巨大的离线工作，必须经常启动。在这里，Hadoop 在批量数据处理中发挥了作用。

另一个好处是，我们可以运行一个集群，中止运行另一个 Hadoop 集群。

第三个好处是还可以减少很多运营成本。

给定一个场景，如果用户精通各种 Hadoop 生态系统，如 Hive、Pig Latin，并需要将数据集成到其中，那么必须在 Cassandra 中插入一些数据源，并尝试运行 Map Reduce 作业。

OLTP 和 OLAP 之间有一个明显的模式。在 OLTP 中，写入次数较少，例如酒店信息。假设价格变化每秒发生 5000 次，这里的读数可能更多。在这种情况下，每秒可以有 1 次写入，但读取可能会达到成百上千次。所以这里的比例是 1:1000 左右。

这是一个有趣的观察，Cassandra 可以很容易地适应这个模型，其中包括读/写相等的模型。此外，当谈到 OLTP 时，即使进入可调和强一致性模型，也可以看到最终一致性模型和最强一致性模型之间的毫秒级差距。因此，Cassandra 可以适合 OLTP。

来到 OLAP，可以看到不同的 OLAP 模式，这意味着有几个写入同时发生。在 OLAP，我们一次性转储数据，即所有日志文件都放入数据存储，然后开始处理。数据模式或访问模式与 OLTP 类型的应用程序完全相反。在这里，Hadoop 或 MapReduce 将是有用的。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[卡珊德拉用例](https://www.edureka.co/blog/cassandra-use-cases/)

[学习卡珊德拉的 5 大理由](https://www.edureka.co/blog/top-5-reasons-to-learn-cassandra-decoded/)

[阿帕奇卡珊德拉在线课程](https://www.edureka.co/cassandra)