# 一头扎进猪里

> 原文：<https://www.edureka.co/blog/a-deep-dive-into-pig/>

Hadoop 最近人气飙升的最大原因之一是，Pig 和 Hive 等功能在它上面运行，允许非程序员使用以前只有 Java 程序员才能使用的功能。这些功能是对 Hadoop 专业人员需求增长的结果。非 Java 背景的 Hadoop 专业人员使用的其他功能有 Flume、Sqoop、HBase 和 Oozie。

要理解为什么你不需要 Java 来学习 Hadoop，一定要看看这个博客。

![1Pig History](img/2384a3642441384017c20ea84200bd6b.png)

让我们了解一下这些特性是如何工作的。

![2 features](img/7d95ef3e688056f5f3fb6185af12b340.png)

我们都知道编程知识是写 MapReduce 代码的必备。但是，如果我有一个工具，可以做编码，如果我只提供细节呢？那是猪展示肌肉力量的地方。Pig 使用一个名为 Pig Latin 的平台，该平台将 Java MapReduce 习语中的编程抽象为一种符号，这种符号使 MapReduce 编程更高级，类似于 RDBMS 系统中的 SQL。用 Pig Latin MapReduce 编写的代码自动转换成等价的 MapReduce 函数。是不是很牛逼？另一个令人震惊的事实是，只需要 10 行 Pig 就可以替换 200 行 Java。

**10 行 Pig = 200 行 Java**

这不仅意味着非 Java 专业人员使用 Hadoop，还证明了一个潜在的事实，即同等数量的技术开发人员也使用 Pig。

![3Pig](img/f089c8e94c78b18c26a085479c53054f.png)

此外，如果您想编写自己的 MapReduce 代码，可以使用 Perl、Python、Ruby 或 c 等任何语言。我们可以使用 Pig 对任何数据集执行的一些基本操作包括分组、连接、过滤和排序。这些操作可以在结构化、非结构化以及半结构化数据上执行。它们为在非常大的数据集上创建和执行 MapReduce 作业提供了一种特别的方式。

接下来，我们来了解一下 Hive。它是一个开源的、基于 Hadoop 的 Pb 级数据仓库框架，用于数据汇总、查询和分析。Hive 为 Hadoop 提供了类似 SQL 的接口。您可以使用 Hive 在 Hadoop 上读写文件，并从 BI 工具中运行您的报告。Hadoop 的一些典型功能包括:

![4HIVE-applications](img/e786c074b03f413199483534f9660aa7.png)

让我向您展示一个在点击流数据集上使用 Pig 的演示我们将使用此点击流数据并执行转换、连接和分组。

**![5Clickstream dataset](img/177473d3a475079d7b60bb0cf781d7bb.png)**

点击流是用户在访问互联网时进行的一系列鼠标点击，特别是在出于营销目的评估个人兴趣时进行监控。它主要由 Flipkart 和 Amazon 等在线零售网站使用，这些网站跟踪您的活动以生成推荐。我们使用的点击流数据集包含以下字段:

1.web 应用程序支持的语言类型

2.浏览器类型

3.连接类型

4.国家 ID

5.时间戳

6.统一资源定位器

7.用户状态

8.用户类型

![6dataset fields](img/99356bcfb5a5cbe9a0a13c009c0a3896.png)

有了适当的字段，它看起来就像这样。

![7dataset fields](img/b49b6dc91086c92e7effd24a20d59160.png)

以下是各种人在浏览特定网站时使用的浏览器类型列表。列表中有浏览器，如 Internet Explorer、Google Chrome、Lynx 等。

![8browser types](img/4878ce700917e5cd18e13d2632d3a637.png)

互联网连接类型可以是局域网/调制解调器/Wifi。完整列表见下图:

![9internet connection type](img/46115a2ef679acb4f2b1143bd85a8d2b.png)

在下一张图中，您将会看到网站吸引受众的国家列表及其 id。

![10website countries](img/a4621a7d32884958818dcc137312877d.png)

一旦我们收集了所有的数据集，我们必须启动 Pig 的 Grunt shell，启动它是为了运行 Pig 命令。

在启动 Grunt shell 时，我们要做的第一件事是将点击流数据加载到 Pig 的关系中。关系只不过是一张表。下面是我们用来将位于 HDFS 的文件加载到 Pig 的关系中的命令。

![11command](img/a8ce9066ea53e103ee7d8f0206df5222.png)

我们可以通过命令 describe click_stream 来验证关系的模式。****

![12click_stream](img/6632be005a6dce60fb4223269a6e8ed0.png)

我们现在需要添加参考文件，这些文件将包含关于国家列表及其 id 和不同浏览器类型及其 id 的详细信息。

![13IDs](img/0bff1765b6c5fb076b88f5af8b582ecc.png)

我们现在有两个参考文件，但是它们需要连接起来形成一个关系。我们运行一个 connection_ref 命令来指示连接的类型。

现在我们已经有了一个工作连接和一个已建立的关系，我们将向您展示如何转换这些数据。对于点击流中的每条记录，我们将生成一条不同格式的新记录，即转换后的数据。新格式将包括时间戳、浏览器类型、国家 id 等字段。

![14fields](img/37c9429a85ee68ba1446ad742c520788.png)

我们可以执行过滤操作来减少大数据。不同类型的用户是管理员、访客或机器人。在我们的演示中，我已经为客人筛选了列表。

![15guests](img/ef5fce46191312600860cfead54481af.png)如果您还记得，点击流中有国家 ID，我们加载了一个 country_ref 文件，其中包含国家名称及其 ID。因此，我们可以在两个文件之间执行连接操作，并合并数据以获得洞察力。

![16join operation](img/d5a17aff9504dadeacffece8f773eba7.png)

如果我们已经加入了数据，那么我们可以通过分组找出用户所在的不同国家。一旦我们有了这些数据，我们就可以执行计数操作来识别来自某个特定国家的用户数量。

![17count operation](img/202dae4342a24e28e3d64dbb28e846f1.png)

从大数据中获得洞察力并不是什么火箭科学。这些只是我实现的许多功能中的一部分，使用 Hive、Hbase、Oozie、Sqoop 和 Flume 等工具，还有大量数据有待探索。所以那些阻碍自己学习 Hadoop 的人，是时候改变了。

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop "get started with big data and hadoop")

[R 和 Hadoop 一起使用的 4 种方式](https://www.edureka.co/blog/4-ways-to-use-R-and-Hadoop-together/ "4 Ways To Use R And Hadoop Together")

[关于 Cloudera 的一切 Apache Hadoop 认证开发者](https://www.edureka.co/blog/questions-answers-about-cloudera-certified-developer-for-hadoop-ccdh/ "everything about cloudera certified developer for apache hadoop")