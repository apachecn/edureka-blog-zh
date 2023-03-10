# 2023 年阿帕奇卡夫卡面试要准备的顶级问题

> 原文：<https://www.edureka.co/blog/interview-questions/top-apache-kafka-interview-questions-for-beginners/>

多年来，由 Apache Software Foundation 开发的开源消息代理项目 Kafka 已经赢得了首选数据处理工具的声誉。对拥有阿帕奇卡夫卡 认证专长的 ***[工作专业人员的需求呈指数级增长，这是其在技术领域日益增长的价值的明显证明。Kafka 使用 Scala 语言编写，提供了一个统一的、高吞吐量、低延迟的平台来处理实时数据馈送。Kafka 的流行可以归功于其独特的属性，这些属性使其成为数据集成的一个极具吸引力的选项。可伸缩性、数据分区、低延迟以及处理大量不同消费者的能力等特性使其非常适合与数据集成相关的用例。](https://www.edureka.co/apache-kafka)***

卡夫卡的流行带来了一系列的工作机会和职业前景。简历上有卡夫卡是成长的捷径。如果你想在不久的将来参加一个 Apache Kafka 的面试，请看看下面的 Apache Kafka 面试问题和答案，这些问题和答案是专门为帮助你成功完成面试而策划的。如果你最近参加了 Kafka 访谈，我们鼓励你在评论标签中添加问题。

万事如意！

## 1。卡夫卡是什么？

维基百科对 Kafka 的定义是“由 Scala 编写的[Apache Software Foundation](https://en.wikipedia.org/wiki/Apache_Software_Foundation "Apache Software Foundation")开发的开源消息代理项目，是一个分布式的发布-订阅消息系统。

 <caption>#### **卡夫卡的显著特征**</caption> 
| **特色** | **描述** |
| ***高吞吐量*** | 用适中的硬件支持数百万条消息 |
| ***扩展性*** | 高度可扩展的分布式系统，无需停机 |
| ***复制*** | 消息在集群中复制，为多个订阅者提供支持，并在出现故障时平衡消费者 |
|  | 为消息到磁盘的持久性提供支持 |
| ***流处理*** | 用于实时流应用程序，如 Apache Spark & Storm |
| ***数据丢失*** | 适当配置的 Kafka 可以确保零数据丢失 |

## 2。列出卡夫卡作品的各个组成部分。

卡夫卡的四个主要组成部分是:

*   主题–属于同一类型的消息流
*   生产者——可以向主题发布消息
*   代理–存储发布消息的一组服务器
*   消费者——订阅各种主题并从经纪人那里获取数据。

## 3。解释偏移的作用。

包含在分区中的消息被分配一个唯一的 ID 号，称为偏移量。偏移量的作用是唯一地标识分区内的每条消息。

## 4。什么是消费群体？

消费群体是卡夫卡独有的概念。每个 Kafka 消费群都由一个或多个共同消费一组订阅主题的消费者组成。

## 5。动物园管理员的角色是什么？

Kafka 使用 Zookeeper 来存储特定主题和特定消费群分区所消费的消息的偏移量。

## 6。没有《动物园管理员》有可能用卡夫卡吗？

不，不可能绕过 Zookeeper 直接连接到 Kafka 服务器。如果由于某种原因，ZooKeeper 关闭了，您就不能为任何客户端请求提供服务。

## 7。解释领导者和追随者的概念。

Kafka 中的每个分区都有一个充当领导者角色的服务器，没有或多个充当跟随者的服务器。领导者执行对分区的所有读写请求的任务，而从者的角色是被动地复制领导者。在领导者失败的情况下，追随者之一将承担领导者的角色。这确保了服务器的负载平衡。

## 8。复制品和 ISR 扮演什么角色？

副本本质上是复制特定分区的日志的节点列表，而不管它们是否扮演领导者的角色。另一方面，ISR 代表同步副本。它本质上是一组与领导者同步的消息副本。

## 9。为什么复制在卡夫卡中至关重要？

复制可以确保发布的消息不会丢失，并且可以在出现任何机器错误、程序错误或频繁的软件升级时使用。

## 10。如果一个副本长时间不在 ISR 中，这意味着什么？

这意味着跟随者获取数据的速度赶不上领导者积累数据的速度。

## 11。启动 Kafka 服务器的流程是什么？

因为 Kafka 使用 ZooKeeper，所以有必要初始化 ZooKeeper 服务器，然后启动 Kafka 服务器。

*   启动 ZooKeeper 服务器:> bin/ZooKeeper-server-start . sh config/ZooKeeper . properties
*   接下来，要启动 Kafka 服务器:> bin/Kafka-server-start . sh config/server . properties

## 12。如何定义分区键？

在生产者内部，分区键的作用是指示消息的目的分区。默认情况下，使用基于哈希的分区器来确定给定密钥的分区 ID。或者，用户也可以使用定制的分区。

## 13。在生产者中，QueueFullException 什么时候发生？

当生产者试图以代理无法处理的速度发送消息时，通常会发生 QueueFullException。由于生产者不阻塞，用户将需要添加足够的代理来协作处理增加的负载。

## 14。解释 Kafka 生产者 API 的作用。

Kafka 的生产者 API 的作用是包装两个生产者——Kafka . Producer . sync Producer 和 Kafka . Producer . async . async Producer。目标是通过单个 API 向客户端公开所有生产者功能。

## 15。卡夫卡和《水槽》的主要区别是什么？

即使两者都用于实时处理，Kafka 也是可伸缩的，并确保消息的持久性。

以上是一些常见的阿帕奇卡夫卡面试问题及答案。你可以用 [这些](https://www.edureka.co/blog/category/big-data-analytics/ "Apache Kafka training") 的博客来温习一下阿帕奇卡夫卡的知识。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[阿帕奇卡夫卡](https://www.edureka.co/apache-kafka "Get started with Apache Kafka")

[阿帕奇卡夫卡:实时分析职业所需](https://www.edureka.co/blog/apache-kafka-career "Career in real-time analytics")