# 具有仲裁日志管理器的 NameNode 高可用性

> 原文：<https://www.edureka.co/blog/namenode-high-availability-with-quorum-journal-manager-qjm/>

[//www.youtube.com/embed/nu16zSDw0BA](//www.youtube.com/embed/nu16zSDw0BA)

这是 Hadoop 2.0 最重要的特性之一。在讨论 Namenode 高可用性特性之前，有必要了解什么是仲裁。Quorum 是在集群中使用的一个通用术语，我们称之为稳定的集群。Quorum 提供了计算机列表，有助于确定群集的健康状况。有两种类型的法定人数:预期法定人数和计算法定人数。

## **带仲裁日志管理器的 NameNode 高可用性(QJM)**

在 Hadoop 2.0 之前，NameNode 是 HDFS 集群中的单点故障(SPOF)。每个集群都有一个 NameNode，如果该机器不可用，那么整个集群都不可用，直到该 NameNode 在另一台机器上重新启动。在传统的 HA 群集中，两台独立的机器被配置为 NameNodes。在任何时候，其中一个 NameNodes 将处于活动状态，而另一个将处于备用状态。活动 NameNode 负责集群中的所有客户端操作，而备用 NameNode 只是充当从节点，维护足够的状态以提供快速故障转移。

为了让备用节点保持其状态与活动节点相协调，两个节点都与一组称为“journal nodes”(JNs)的独立守护进程进行通信。当活动节点执行任何命名空间修改时，它会在 JournalNodes 中记录所做的更改。备用节点能够从 JNs 读取修改后的信息，并定期监视它们的变化。当备用节点看到这些更改时，它会将它们应用到自己的名称空间。在故障转移的情况下，备用服务器将确保在将其状态更改为“活动状态”之前，已经从 JounalNodes 中读取了所有更改。这保证了名称空间状态在故障转移发生之前完全同步。

为了提供快速故障切换，备用节点必须拥有关于块在群集中的位置的最新信息。为此，DataNodes 配置了两个 NameNodes 的位置，并向两者发送块位置信息和心跳。

一次只能有一个 NameNodes 是活动的，这一点很重要。否则，命名空间状态会在两者之间偏离，并导致数据丢失或错误的结果。为了避免这种情况，JournalNodes 一次只允许一个写者有一个 NameNode。在故障转移期间，将成为活动状态的 NameNode 将接管向 JournalNodes 写入的责任。

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[大数据和 Hadoop 培训](https://www.edureka.co/big-data-and-hadoop)

[Hadoop 2.0 简介](https://www.edureka.co/blog/introduction-to-hadoop-2-0-and-advantages-of-hadoop-2-0/ "Introduction to Hadoop 2.0 and Advantages of Hadoop 2.0 over 1.0")

[Hadoop 2.0 集群架构联盟概述](https://www.edureka.co/blog/overview-of-hadoop-2-0-cluster-architecture-federation/ "Overview of Hadoop 2.0 Cluster Architecture Federation")

[学习 Hadoop 的 5 个理由](https://www.edureka.co/blog/5-reasons-to-learn-hadoop "5 Reasons to Learn Hadoop")