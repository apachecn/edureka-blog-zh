# Spark 流中带窗口的状态转换

> 原文：<https://www.edureka.co/blog/stateful-transformations-with-windowing-in-spark-streaming/>

*供稿:Prithviraj Bose*

在这篇博客中，我们将讨论 Apache Spark 有状态转换的窗口概念。

**什么是有状态转换？**

Spark streaming 使用微批处理架构，其中传入的数据被分组到称为离散化流(d Streams)的微批处理中，这也是基本的编程抽象。数据流内部具有弹性分布式数据集(RDD ),因此可以进行标准 RDD 变换和操作。

在流式传输中，如果我们有跨批跟踪数据的用例，那么我们需要全状态数据流。

例如，我们可能会在用户会话期间跟踪用户在网站上的互动，或者我们可能会随着时间的推移跟踪特定的 twitter 标签，并查看全球哪些用户正在谈论它。

**状态转换的类型。**

全状态数据流有两种类型——基于窗口的跟踪和全会话跟踪。

对于有状态跟踪，所有传入的数据都应该转换为键值对，以便可以跨批跟踪键状态。这是前提条件。

此外，我们还应该启用检查点，这个概念我们将在后面的博客中讨论。

***>窗口跟踪***

在基于窗口的跟踪中，输入批次按时间间隔分组，即每“x”秒对批次进行分组。使用滑动间隔对这些批次进行进一步计算。

例如，如果窗口间隔= 3 秒，滑动间隔= 2 秒，则所有传入的数据将每 3 秒被分组为一批，对这些批的计算将每 2 秒发生一次。或者，我们可以说，每隔 2 秒对最后 3 秒到达的批处理进行计算。

![spark-streaming-dstream-window](img/55c340441e1b9493720f335c97146b92.png)

在上图中，我们看到每 3 个时间单位(窗口间隔)对传入批次进行分组，每 2 个时间单位(滑动间隔)进行一次计算。注:与 Apache Flink 不同，Apache Spark 没有翻滚窗口的概念，所有的窗口都是滑动的。

**API**

基于窗口的转换的一个流行的 API 是

*pairdstreamfunctions . reducebykeyandwindow*。

这个 API 有几个重载版本，让我们看看参数数量最多的版本。在这个解释之后，这个 API 的其他重载版本应该是不言自明的。

![API-spark-streaming](img/5b01d5b0ba5003063c99f9ddb1c69dc3.png)

返回:转换后的数据流[(K，V)]

*reduceFunc* :关联归约函数。

*invReduceFunc* :上述 reduce 函数的逆函数。这是有效计算进出批次所必需的。在此功能的帮助下，从上述 reduce 功能的累计值中扣除输出批次的值。例如，如果我们正在计算各个键的传入值的总和，那么对于传出批次，我们将减去各个键的值(假设它们存在于当前批次中，否则忽略)。

*windowDuration* :批次分组的时间单位，应该是批次间隔的倍数。

*slideDuration* :计算的时间单位，应该是批量间隔的倍数。*分割器*:用来存储结果数据流的分割器。关于分区的更多信息，请阅读 [this](http://prithvibose.blogspot.in/2016/03/demystifying-partitioning-in-spark.html) 。

*filterFunc* :过滤掉过期的键-值对的函数，例如，如果我们有一段时间没有更新某个键，我们可能希望删除它。

这里有一个 [程序](https://github.com/prithvirajbose/spark-dev/blob/master/src/main/scala/examples/streaming/TestReduceByKeyAndWindow.scala) 来计算来自套接字流的单词。我们使用了上述函数的重载版本，窗口间隔为 4 秒，滑动间隔为 2 秒。

在我的下一篇博客中，我将写关于完整会话跟踪和检查点的内容。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[Apache Spark 入门&Scala](https://www.edureka.co/apache-spark-scala-training)

[带广播变量的分布式缓存](https://www.edureka.co/blog/broadcast-variables/)