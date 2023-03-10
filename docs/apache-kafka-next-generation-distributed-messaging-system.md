# Apache Kafka:下一代分布式消息系统

> 原文：<https://www.edureka.co/blog/apache-kafka-next-generation-distributed-messaging-system>

在当今世界，**数据是互联网应用的主要成分**，通常包括以下内容:

*   页面访问量和点击量
*   用户活动
*   与登录对应的事件
*   社交网络活动，如赞、分享和评论
*   特定于应用的指标(如日志、页面加载时间、性能等。)

此**数据可用于实时运行分析**服务于各种目的，其中包括:

*   投放广告
*   跟踪异常用户行为
*   基于相关性显示搜索
*   显示基于以前活动的建议

**问题:**收集所有数据并不容易，因为数据是从各种来源以不同格式生成的

**解决方案:**解决这个问题的方法之一就是使用消息传递系统。消息传递系统在消息的帮助下提供了分布式应用程序之间的无缝集成。

[![apache-kafka-next-generation-distributed-messaging-system](img/5ac0df95ee43a8ded149ccfa61ec73fd.png "apache-kafka-next-generation-distributed-messaging-system")](https://www.edureka.co/apache-kafka)

Apache Kaka:t1]

Apache Kafka 是一个分布式发布/订阅消息系统，最初由 LinkedIn 开发，后来成为 Apache 项目的一部分。Kafka 的设计是快速、敏捷、可扩展和分布式的。

**卡夫卡建筑与术语:**

[![kafka-cluster](img/e1fb44ba2a62e44a3eb6074f7d029949.png "kafka-cluster")](https://www.edureka.co/apache-kafka)

**主题:**属于特定类别的消息流称为主题

**生产者:**生产者可以是能够向主题发布消息的任何应用程序

**消费者:**消费者可以是订阅主题和消费消息的任何应用程序

**代理:** Kafka 集群是一组服务器，每个服务器称为一个代理

Kafka 是可扩展的，允许创建多种类型的集群。

*   **单节点单代理集群**
*   **单节点多代理集群**
*   **多节点多代理集群**

[![single-node-single-broker](img/f328b185dc3cb6a5f6984aaa984f15e5.png "single-node-single-broker-") ](https://www.edureka.co/apache-kafka) **单节点单经纪人**

动物园管理员的角色是什么？

每个 Kafka 经纪人使用 ZooKeeper 与其他 Kafka 经纪人协调。ZooKeeper 服务会通知生产者和消费者 Kafka 系统中新代理的出现或代理的失败。

[![single-node-multiple-brokers](img/2d36d3ff63dea9aa984ed676e626410c.png)](https://www.edureka.co/blog/wp-content/uploads/2015/11/single-node-multiple-brokers.jpg)

**单节点多经纪人**

[![multiple-node-multiple-broker](img/fbbf10869119f1fdec8a53406cb4a7fa.png "multiple-node-multiple-broker")](https://www.edureka.co/apache-kafka)

**多个节点多个经纪人**

**Kafka @ LinkedIn**

![lnewsfeed-kafka-linkedin](img/c9bcf4405f0586f2a51c45a5a827270c.png "kafka-linkedin")

**LinkedIn Newsfeed 由 Kafka 提供支持**

[![lrecommendations](img/215ffb48315bc79d1f4a8865ad68e313.png) ](https://www.edureka.co/blog/wp-content/uploads/2015/11/lrecommendations.png) ** LinkedIn 推荐由卡夫卡**

[![lnotifications](img/3342f3b03845769b63715381d00b990c.png)](https://www.edureka.co/blog/wp-content/uploads/2015/11/lnotifications.png)

**LinkedIn 通知由 Kafka 提供支持**

**注意:**除此之外，LinkedIn 还使用 Kafka 完成许多其他任务，如日志监控、性能指标、搜索改进等等。

**还有谁用卡夫卡？**

**DataSift:** DataSift 使用 Kafka 作为监控事件的收集器，并实时跟踪用户对数据流的消费

Wooga: Wooga 使用 Kafka 在一个中心位置聚集和处理所有脸书游戏(由不同的提供商托管)的跟踪数据

**海绵细胞:**海绵细胞使用 Kafka 运行其整个分析和监控管道，驱动实时和 ETL 应用程序

**Loggly :** Loggly 是世界上最流行的基于云的日志管理。它使用 Kafka 进行日志收集。

**对比研究:Kafka vs. ActiveMQ vs. RabbitMQ**

卡夫卡有更高效的存储格式。平均来说，每条消息在 Kafka 中有 9 字节的开销，而在 ActiveMQ 中有 144 字节

[![kafka-storage-cmp1](img/5f322bb70cdbbf1aacd80b9b33b7e10f.png)](https://www.edureka.co/apache-kafka) 在 ActiveMQ 和 RabbitMQ 中，代理通过写入磁盘来维护每个消息的交付状态，但在 Kafka 中，没有磁盘写入，因此速度更快。

[![kafka-storage-cmp2](img/7a0c0017e5fc11ac3d339c657401e7df.png)](https://www.edureka.co/apache-kafka)

随着卡夫卡在生产中的广泛采用，它看起来是解决现实世界问题的一个有前途的解决方案。Apache Kafka 培训可以帮助您在实时分析职业生涯中领先于同行。阿帕奇卡夫卡入门教程 [这里](https://www.youtube.com/watch?v=BGhlHsFBhLE&%20link& "here") 。

有问题要问我们吗？请在评论区提到它，我们会回复你或者今天就加入我们的[卡夫卡培训](https://www.edureka.co/kafka-certification-training)。

**相关帖子:**

[【阿帕奇】卡夫卡](https://www.edureka.co/blog/videos/apache-kafka-with-spark-streaming-real-time-analytics-redefined/ "apache kafka with spark streaming")

[实时分析事业所需](https://www.edureka.co/blog/apache-kafka-career "what you need for a career in real time analytics")