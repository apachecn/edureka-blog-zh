# Apache Hadoop 中 MapReduce 作业的剖析

> 原文：<https://www.edureka.co/blog/anatomy-of-a-mapreduce-job-in-apache-hadoop/>

![MapReduce - Anatomy of MapReduce -Edureka](img/df13ee1fc9c7326d4dff80e1f4a7d26c.png) Hadoop 框架由两个主要组件组成，即:

*   用于数据存储的 Hadoop 分布式文件系统(HDFS)和
*   MapReduce 进行数据处理。

在本帖中，我们将讨论 Apache Hadoop 中 MapReduce 作业的剖析。典型的 Hadoop MapReduce 作业分为一组在 Hadoop 集群上执行的 Map 和 Reduce 任务。执行流程如下所示:

*   输入数据被分割成小的数据子集。
*   地图任务处理这些数据分割。
*   来自地图任务的中间输入数据在经过一个称为“洗牌”的中间过程后被提交给 Reduce task。
*   Reduce 任务处理这些中间数据，以生成 MapReduce 作业的结果。

在这篇博客中，让我们把注意力集中在贴图和减少相位上。*(我们将在以后的博客中详细回顾输入数据拆分和洗牌过程)。 *从* [*数据工程师培训*](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) *中了解大数据及其应用。**

让我们看一个简单的 MapReduce 作业执行，使用其中一个示例，CDH3 中的[teragen](https://hadoop.apache.org/docs/r1.0.4/api/org/apache/hadoop/examples/terasort/TeraGen.html)。该程序用于生成大量数据，以便对 Cloudera CDH3 快速演示虚拟机中可用的集群进行基准测试。

[![Generating large amount of data available in Cloudera CDH3 Quick Demo VM](img/5639b55581c1036ad620dc9eb4027243.png "Generating large amount of data available in Cloudera CDH3 Quick Demo VM")](https://www.edureka.co/blog/anatomy-of-a-mapreduce-job-in-apache-hadoop/)

要生成的数据大小和输出文件位置被指定为“teragen”程序的一个参数。“teragen”类/程序运行 MapReduce 作业来生成数据。我们将分析这个 MapReduce 作业执行。

[![MapReduce job execution](img/3d92cb17a2a34d120248aefe325cd824.png "MapReduce job execution")](https://www.edureka.co/blog/anatomy-of-a-mapreduce-job-in-apache-hadoop/)

这个输出文件存储 HDFS 的输出数据。下图显示了 MapReduce 作业执行的执行过程和所有中间阶段:

[![Intermediate phases of a MapReduce Job execution](img/9deb252bf942f40e16cb89a5f888042a.png "Intermediate phases of a MapReduce Job execution")](https://www.edureka.co/blog/anatomy-of-a-mapreduce-job-in-apache-hadoop/)

让我们回顾一下执行日志，以了解作业执行流程:

从加拿大 [Azure 数据工程课程](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-canada) 了解大数据及其应用。

[![Execution log ](img/a4b2498ba978e0143bf475aea7416481.png "Execution log")](https://www.edureka.co/blog/anatomy-of-a-mapreduce-job-in-apache-hadoop/)

“teragen”计划启动了两个地图任务和三个 reduce 任务来生成所需的数据。

1.  地图任务生成记录。
2.  生成的记录作为输入进入组合器任务。“合并器”是一个中间过程。(我们将在未来的博客中详细讨论合并器。现在把它看作是减少任务之前中间过程)。
3.  合并器输出记录作为输入进入 Reduce 任务。
4.  最后，reducer 任务聚合数据并生成输出记录。

请注意，Reduce 任务在地图任务完成后开始，并且每一级的记录数都会继续减少。通过此次[大数据课程](https://www.edureka.co/big-data-hadoop-training-certification)，您将对 HDFS 和 MapReduce 有更深入的了解。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

相关帖子:

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop)

[全面上手 MapReduce](https://www.edureka.co/comprehensive-mapreduce-self-paced)

[MapReduce 设计模式入门](https://www.edureka.co/mapreduce-design-patterns-sp/)