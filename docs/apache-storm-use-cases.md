# Apache Storm 用例

> 原文：<https://www.edureka.co/blog/apache-storm-use-cases/>

Apache Storm 因其实时处理特性而广受欢迎，正因为如此，许多组织已经将它作为其系统的一部分。让我们看看组织是如何集成 Apache Storm 的。

## **阿帕奇风暴用例:**

## **推特**

Storm 用于支持各种 Twitter 系统，如实时分析、个性化、搜索、收入优化等等。Apache Storm 与 Twitter 的其他基础设施相融合，包括 Cassandra、Memcached 等数据库系统、消息基础设施、Mesos 以及监控和警报系统。Storm 的隔离调度程序使生产应用程序和开发中的应用程序使用同一个集群变得可行。它为容量规划提供了一种有效的方法。

雅虎！ 雅虎！正在开发下一代平台，该平台支持大数据和低延迟处理的融合。虽然 Hadoop 是这里用于批处理的主要技术，但是 Apache Storm 允许对用户事件、内容提要和应用程序日志进行流处理。

Infochimps Infochimps 使用 Apache Storm 作为其三种云服务之一——数据交付服务(DDS)的来源，该服务采用 Storm 来提供容错和线性可扩展的企业数据收集、传输和复杂的流内处理云服务。与提供批量 ETL 和大规模批量分析处理的 Hadoop 类似，DDS 也提供实时 ETL 和大规模实时处理。

Flipboard 是一个探索、收集和分享你感兴趣的新闻的地方。Flipboard 将 storm 用于多种服务，如内容搜索、实时分析、定制杂志订阅等。Apache Storm 与包括 ElasticSearch、Hadoop、HBase 和 HDFS 等系统在内的基础设施相集成，以创建高度可扩展的数据平台。

Ooyala Ooyala 是一家由风险投资支持的私营公司，为一些世界上最大的网络、品牌和媒体公司提供在线视频技术产品和服务。Ooyala 拥有一个分析引擎，每天处理超过 20 亿次分析事件，这些事件来自全球近 2 亿名在 Ooyala 播放器上观看视频的观众。Ooyala 使用 Apache Storm 为他们的客户提供关于消费者观看行为和数字内容趋势的实时流分析。Storm 允许快速挖掘他们的在线视频数据集，以提供当前的商业智能，如实时模式观看、个性化内容建议、节目指南和关于如何增加收入的宝贵见解。

**淘宝** 淘宝借助 Apache Storm，创建日志统计，实时从统计中提取有用信息。日志从持久消息队列读入到 spouts 中，进行处理，然后传递给拓扑，以计算所需的结果。淘宝每天的输入日志数量在 200 万到 15 亿之间。

**Klout** Klout 使用 Apache Storm 的内置 Trident 抽象来创建复杂的拓扑结构，通过 Kafka 从网络收集器传输数据，然后处理并写入 HDFS。

Wega 是全球综合旅游元搜索引擎，在全球范围内运营，被无数旅行者用来获得更多选择，以更少的费用和更多的旅行。Wego 比较和显示实时航班时刻表、酒店可用性、价格，并显示全球其他旅游网站。在这里，Apache Storm 从分支机构向最终用户传输实时元搜索数据。Storm 中的拓扑概念解决了并发问题，同时帮助他们无情地集成、剖析和清理数据。此外，Storm 中提供的工具支持增量更新来增强他们的数据。

**Rocket Fuel**Rocket Fuel 提供大数据规模的领先媒体购买平台，利用人工智能(AI)的力量来扩大数字媒体的营销投资回报率。他们正在 Storm 上构建一个实时平台，模拟基于 Hadoop 的 ETL 管道中已经存在的时间关键型工作流。这个平台跟踪印象，点击，转换，投标请求等。实时地。

Navsite Navsite 使用 Apache Storm 作为其服务器事件日志监控&审计系统的一部分。来自数千个服务器的日志消息被发送到 RabbitMQ 集群，Storm 用于将每个消息与一组正则表达式进行比较。如果匹配，那么消息被发送到一个在 MongoDB 中存储数据的 bolt。目前，每秒处理 5-10k 条消息，但是现有的 RabbitMQ + Storm 集群已经被测试到每秒大约 50k。

有更多的组织正在实施 Apache Storm，预计会有更多的组织加入这场游戏，因为 Apache Storm 将继续成为实时分析领域的领导者。

查看我们的 **[视频和关于](https://www.edureka.co/blog/videos/aboutapachestorm/)阿帕奇风暴的演示。**