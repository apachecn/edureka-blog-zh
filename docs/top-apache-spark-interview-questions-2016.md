# 2023 年你应该准备的 Apache Spark 面试问题

> 原文：<https://www.edureka.co/blog/interview-questions/top-apache-spark-interview-questions-2016/>

2018 年是大数据年，这一年，大数据和分析通过创新技术、数据驱动的决策和以结果为中心的分析取得了巨大进展。大数据和商业分析(BDA)的全球收入将从 2016 年的 1301 亿美元增长到 2021 年的 2030 亿美元以上(来源 IDC)。准备好这些顶级的 **Apache Spark 面试问题**，在蓬勃发展的大数据市场中获得优势，全球和本地企业，无论大小，都在寻找高质量的 ***大数据和 Hadoop 专家*。**

想提升自己的技能，在职业生涯中获得成功吗？查看 ***[热门科技](https://www.edureka.co/blog/top-10-trending-technologies/)** 文章**。***

作为一名大数据专业人员，了解正确的流行语、学习正确的技术并为常见的 Spark 面试问题准备正确的答案至关重要。围绕 *Spark Core* 、 *Spark Streaming* 、 *Spark SQL* 、 *GraphX* 、 *MLlib* 等问题和答案，这个博客是你下一份 Spark 工作的门户。

## **阿帕奇星火面试问答**

### **1。比较 Hadoop 和 Spark。**

我们将基于以下几个方面比较 Hadoop MapReduce 和 Spark】

 <caption>#### **阿帕奇 Spark vs Hadoop**</caption> 
| **特征标准** | **阿帕奇星火** | **Hadoop** |
| **速度** | 比 Hadoop 快 100 倍 | 像样的速度 |
| **处理** | 实时&批处理 | 仅批处理 |
| **难度** | 因为高级模块而简单 | 难学 |
| **恢复** | 允许恢复分区 | 容错 |
| **交互性** | 有交互模式 | 除了 猪&蜂巢之外没有其他互动模式 |

**表:***Apache Spark vs Hadoop*

*让我们用一个有趣的比喻来理解同样的道理。*

*“单个厨师烹饪一道主菜是有规律的计算。Hadoop 是多个厨师将一道主菜烹饪成几块，并让每个厨师烹饪自己的那一块。* *每个厨师都有单独的炉子和食物架。第一个厨师做肉，第二个厨师做调味汁。这个阶段叫做“地图”。最后，主厨组装完整的主菜。这就是所谓的“减少”。* *对于 Hadoop，厨师不允许在操作之间把东西放在炉子上。每次你做一个特别的手术，厨师都会把结果放在架子上。这会减慢速度。* *对于火花，炊事员在操作之间不准把东西放在炉子上。这加快了速度。* *最后，对于 Hadoop 来说，配方是用一种不合逻辑且难以理解的语言编写的。* *对于星火来说，菜谱写得很好看。”–斯坦克拉德科 ，银河交易所. io*

### **2。什么是阿帕奇火花？**

*   ***[Apache Spark](https://www.edureka.co/blog/spark-tutorial/)***是一个用于实时处理的开源集群计算框架。
*   它有一个繁荣的开源社区，是目前最活跃的 Apache 项目。
*   Spark 提供了一个接口，通过隐式数据并行和容错对整个集群进行编程。

![Apache Spark - Spark Interview Questions - Edureka](img/250d1412d6710fea5fbbb24b8cb1703b.png)  Spark 是 Apache 软件基金会中最成功的项目之一。Spark 显然已经发展成为大数据处理的市场领导者。许多组织在具有数千个节点的集群上运行 Spark。今天，Spark 正在被亚马逊、易贝和雅虎等主要公司采用。

### **3。解释 Apache Spark 的主要特性。**

以下是 Apache Spark 的主要特性:

2.  **速度**
3.  **多种格式支持**
4.  **懒评**
5.  **实时计算**
6.  **Hadoop 集成**
7.  **机器学习**

让我们详细看看这些特性:

1.  **Polyglot**:Spark 提供 Java、Scala、Python 和 r 的高级 API，Spark 代码可以用这四种语言中的任意一种编写。它用 Scala 和 Python 提供了一个 shell。Scala shell 可以通过**访问。/bin/spark-shell** 和 Python shell 到**。安装目录中的/bin/pyspark** 。

2.  **速度** : Spark 运行速度比 Hadoop MapReduce 大规模数据处理快 100 倍。Spark 能够通过受控分区实现这一速度。它使用分区管理数据，有助于以最小的网络流量并行处理分布式数据。

3.  **多种格式** : Spark 支持 Parquet、JSON、Hive、Cassandra 等多种数据源。数据源 API 提供了通过 Spark SQL 访问结构化数据的可插拔机制。数据源不仅仅是简单的转换数据并将其导入 Spark 的管道。

4.  **懒评测** : Apache Spark 将其评测延迟到绝对必要的时候。这是促成其速度的关键因素之一。对于转换，Spark 将它们添加到 DAG 计算中，只有当驱动程序请求一些数据时，DAG 才会真正执行。

5.  **实时计算** : Spark 的计算是实时的，因为是内存计算，所以延迟更小。Spark 旨在实现巨大的可扩展性，Spark 团队记录了运行具有数千个节点的生产集群的系统用户，并支持多种计算模型。

6.  **Hadoop 集成** : Apache Spark 提供了与 Hadoop 的流畅兼容。这对于所有以 Hadoop 开始职业生涯的大数据工程师来说是一大福音。Spark 是 Hadoop MapReduce 功能的潜在替代品，而 Spark 能够在现有 Hadoop 集群之上运行，使用 YARN 进行资源调度。

7.  **机器学习** : Spark 的 MLlib 是机器学习组件，在大数据处理时得心应手。它消除了使用多个工具的需要，一个用于处理，一个用于机器学习。Spark 为数据工程师和数据科学家提供了一个强大的统一引擎，既快速又易于使用。

### **4。Apache Spark 支持哪些语言，哪种语言最受欢迎？**

Apache Spark 支持以下四种语言:Scala、Java、Python 和 r，在这些语言中，Scala 和 Python 都有 Spark 的交互外壳。Scala shell 可以通过**访问。/bin/spark-shell** 和 Python shell 通过**。/bin/pyspark** 。Scala 是其中使用最多的，因为 Spark 是用 Scala 编写的，也是 Spark 最常用的。

### **5。Spark over MapReduce 有什么好处？**

Spark 相比 MapReduce 有以下优势:

1.  由于内存处理的可用性，Spark 实现处理的速度比 Hadoop MapReduce 快 10 到 100 倍，而 MapReduce 利用持久存储来完成任何数据处理任务。
2.  与 Hadoop 不同，Spark 提供了内置的库来从同一个内核执行多项任务，如批处理、流、机器学习、交互式 SQL 查询。但是，Hadoop 只支持批处理。
3.  Hadoop 高度依赖磁盘，而 Spark 则促进缓存和内存数据存储。
4.  Spark 能够在同一个数据集上执行多次计算。这被称为迭代计算，而 Hadoop 没有实现迭代计算。

### **6。什么是纱线？**

与 Hadoop 类似，YARN 是 Spark 的关键特性之一，它提供了一个集中的资源管理平台，可在集群中提供可扩展的操作。YARN 是一个分布式容器管理器，比如 Mesos，而 Spark 是一个数据处理工具。Spark 可以在 YARN 上运行，就像 Hadoop Map Reduce 可以在 YARN 上运行一样。在纱线上运行火花需要建立在纱线支撑上的火花的二元分布。

### **7。纱簇的所有节点都需要安装 Spark 吗？**

不，因为火花在纱线上运行。Spark 独立于其安装运行。Spark 有一些选项可以在向集群分派作业时使用 YARN，而不是它自己的内置管理器或 Mesos。此外，还有一些运行纱线的配置。它们包括*主*、*部署模式*、*驱动-内存*、*执行-内存*、*执行-内核*和*队列*。

### **8。如果 Spark 比 MapReduce 好，学 MapReduce 有什么好处吗？**

是的，MapReduce 是包括 Spark 在内的许多大数据工具使用的范例。当数据变得越来越大时，使用 MapReduce 是非常重要的。大多数工具，如 Pig 和 Hive，将它们的查询转换成 MapReduce 阶段，以便更好地优化它们。从伦敦 [Azure 数据工程认证](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-london) 了解更多大数据及其应用。

### **9。解释弹性分布式数据集(RDD)的概念。**

RDD 代表弹性分布数据集。RDD 是并行运行的操作元素的容错集合。RDD 中的分区数据在本质上是不可变的和分布式的。主要有两种类型的 RDD:

1.  并行收集:在这里，现有的 rdd 彼此并行运行。
2.  Hadoop 数据集:它们对 HDFS 或其他存储系统中的每个文件记录执行功能。

rdd 基本上是存储在分布在许多节点上的内存中的数据的一部分。rdd 在 Spark 中被延迟评估。这种懒惰的评估有助于 Spark 的速度。

### **10。我们如何在 Spark 中创建 rdd？**

Spark 提供了两种创建 RDD 的方法:

1。通过在驱动程序中并行化一个集合。

2。这利用了 SparkContext 的“并行化”

```

method val DataArray = Array(2,4,6,8,10)

val DataRDD = sc.parallelize(DataArray)

```

3。通过从外部存储(如 HDFS、HBase、共享文件系统)加载外部数据集。

### **11。Spark 应用程序中的执行器内存是什么？**

对于一个 spark 执行器，每个 spark 应用程序都有相同的固定堆大小和固定数量的内核。堆大小就是所谓的 Spark executor 内存，它由***–executor-memory***标志的 spark.executor.memory 属性控制。每个 spark 应用程序在每个 worker 节点上都有一个执行器。执行器内存基本上是应用程序将利用多少工作节点内存的度量。

### **12。在 Apache Spark 中定义分区。**

顾名思义，分区是一种更小的数据逻辑划分，类似于 MapReduce 中的“split”。它是大型分布式数据集的逻辑块。分区是导出数据逻辑单元以加速处理过程的过程。Spark 使用分区来管理数据，这有助于并行化分布式数据处理，并以最少的网络流量在执行器之间发送数据。默认情况下，Spark 会尝试从靠近它的节点将数据读入 RDD。由于 Spark 通常访问分布式分区数据，为了优化转换操作，它创建分区来保存数据块。Spark 中的一切都是被分割的 RDD。

### **13。RDD 支持哪些行动？**

RDD 是 Spark 中主要的逻辑数据单元。一个 RDD 人分发了一批物品。分布式意味着每个 RDD 被分成多个分区。这些分区中的每一个都可以驻留在内存中，或者存储在集群中不同机器的磁盘上。rdd 是不可变(只读)数据结构。你不能改变原来的 RDD，但你可以用任何你想要的改变把它变成不同的 RDD。

rdd 支持两种类型的操作:转换和动作。

*转换*:转换从现有的 RDD 创建新的 RDD，就像我们刚刚看到的 map、reduceByKey 和 filter。转换是按需执行的。这意味着它们是延迟计算的。

*动作*:动作返回 RDD 计算的最终结果。动作使用沿袭图触发执行，以将数据加载到原始 RDD，执行所有中间转换，并将最终结果返回到驱动程序或将其写出到文件系统。

### **14。你对 Spark 中的转换有什么理解？**

变换是应用于 RDD 的函数，产生另一个 RDD。它不会执行，直到一个动作发生。map()和 filter()是转换的示例，前者将传递给它的函数应用于 RDD 的每个元素，并生成另一个 RDD。filter()通过从当前 RDD 中选择传递函数参数的元素来创建新的 RDD。

```

val rawData=sc.textFile("path to/movies.txt")

val moviesData=rawData.map(x=&gt;x.split("	"))

```

正如我们在这里看到的，*原始数据* RDD 被转换成*电影数据* RDD。转换是延迟计算的。

### **15。在 Spark 中定义操作。**

一个动作帮助将数据从 RDD 带回本地机器。动作的执行是所有先前创建的转换的结果。动作使用沿袭图触发执行，以将数据加载到原始 RDD，执行所有中间转换，并将最终结果返回到驱动程序或将其写出到文件系统。

*【reduce()】*是一个动作，它执行一次又一次传递的函数，直到剩下一个值为止。 *take()* 动作将 RDD 的所有值取至一个本地节点。

```
moviesData.saveAsTextFile(“MoviesData.txt”)

```

正如我们在这里看到的，*电影数据* RDD 被保存到一个名为*电影数据. txt* 的文本文件中。

### **16。定义 SparkCore 的功能。**

*Spark Core* 是大规模并行和分布式数据处理的基础引擎。核心是分布式执行引擎，Java、Scala 和 Python APIs 为分布式 ETL 应用程序开发提供了一个平台。SparkCore 执行各种重要功能，如内存管理、监控作业、容错、作业调度以及与存储系统的交互。此外，构建在核心之上的额外库允许流、SQL 和机器学习的不同工作负载。 它负责:

1.  内存管理和故障恢复
2.  在集群上调度、分发和监控作业
3.  与存储系统交互

### **17。你对 RDD 的理解是什么？**

Apache 将 PairRDD 函数类定义为

```
class PairRDDFunctions[K, V] extends Logging with HadoopMapReduceUtil with Serializable

```

使用键/值对可以在 Spark 中的 rdd 上执行特殊操作，这种 rdd 被称为对 rdd。成对 rdd 允许用户并行访问每个密钥。它们有一个基于每个键收集数据的 *reduceByKey()* 方法和一个基于具有相同键的元素将不同 rdd 组合在一起的 *join()* 方法。

### **18。说出 Spark 生态系统的组成部分。**

1.  **Spark Core** :大规模并行分布式数据处理的基础引擎
2.  **火花流**:用于处理实时流数据
3.  **Spark SQL** :将关系处理与 Spark 的函数式编程 API 集成
4.  **GraphX** :图和图并行计算
5.  **MLlib** :在 Apache Spark 中执行机器学习

### **19。Spark 中的流是如何实现的？举例说明。**

*火花流*用于处理实时流数据。因此，它是对核心 Spark API 的有益补充。它支持实时数据流的高吞吐量和容错流处理。基本流单元是数据流，它基本上是一系列用于处理实时数据的弹性分布式数据集。来自不同来源(如 Flume、HDFS)的数据经过流式传输，最终处理到文件系统、实时仪表盘和数据库中。它类似于批处理，因为输入数据被分成类似批处理的流。

**![Spark Streaming - Spark Tutorial - Edureka](img/d1e7bdd440dc83f44985d677fb78cb1a.png)**

**图:** *星火面试问题——星火分流*

### **20。Spark 中有实现图形的 API 吗？**

*GraphX* 是用于图形和图形并行计算的 Spark API。因此，它用弹性分布式属性图扩展了火花 RDD。

属性图是一个有向多图，它可以有多条平行的边。每个边和顶点都有用户定义的相关属性。这里，平行边允许相同顶点之间的多种关系。在高层次上，GraphX 通过引入弹性分布式属性图扩展了 Spark RDD 抽象:一个每个顶点和边都有属性的有向多图。

为了支持图形计算，GraphX 公开了一组基本操作符(例如，子图、joinVertices 和 mapReduceTriplets)以及 Pregel API 的优化变体。此外，GraphX 还包含了越来越多的图形算法和构建器来简化图形分析任务。

### **21。GraphX 中的 PageRank 是什么？**

PageRank 衡量图中每个顶点的重要性，假设从 *u* 到 *v* 的一条边代表 *v* 的重要性被 *u* 认可。例如，如果一个 Twitter 用户被许多其他人关注，该用户将被排名很高。

GraphX 附带了 PageRank 的静态和动态实现，作为 PageRank 对象上的方法。静态 PageRank 运行固定的迭代次数，而动态 PageRank 运行直到等级收敛(即，停止变化超过指定的容差)。GraphOps 允许直接调用这些算法作为 Graph 上的方法。

### **22。机器学习在 Spark 中是如何实现的？**

MLlib 是 Spark 提供的可扩展的机器学习库。它旨在通过常见的学习算法和用例(如聚类、回归过滤、降维等)使机器学习变得简单和可扩展。

**![Machine Learning - Spark Interview Questions - Edureka](img/0b37f45ca86e22b91c7db3c9795bb816.png)**

### **23。Spark 中有实现 SQL 的模块吗？它是如何工作的？**

*Spark SQL* 是 Spark 中的一个新模块，它将关系处理与 Spark 的函数式编程 API 集成在一起。它支持通过 SQL 或 Hive 查询语言查询数据。对于那些熟悉 RDBMS 的人来说，Spark SQL 将是从早期工具的简单过渡，在早期工具中，您可以扩展传统关系数据处理的边界。

Spark SQL 将关系处理与 Spark 的函数式编程集成在一起。此外，它提供了对各种数据源的支持，并使将 SQL 查询与代码转换结合起来成为可能，从而产生了一个非常强大的工具。

以下是 Spark SQL 的四个库。

1.  数据源 API
2.  数据框架 API
3.  解释器&优化器
4.  SQL 服务

### **![Spark SQL - Spark Interview Questions - Edureka](img/9955d97c290b4d1c246ca56144b1d7e1.png) 24。什么是拼花锉刀？** 

Parquet 是由许多其他数据处理系统支持的列格式文件。Spark SQL 对 Parquet 文件执行读写操作，并认为这是迄今为止最好的大数据分析格式之一。

Parquet 是一种柱状格式，受许多数据处理系统支持。拥有柱状存储器的优点如下:

1.  列存储限制 IO 操作。
2.  它可以获取你需要访问的特定列。
3.  柱状存储占用空间更少。
4.  它给出了更好的汇总数据，并遵循特定类型的编码。

### **25。Apache Spark 如何与 Hadoop 一起使用？**

Apache Spark 最好的部分是它与 Hadoop 的兼容性。因此，这是一个非常强大的技术组合。在这里，我们将了解 Spark 如何从 Hadoop 的优势中获益。结合使用 Spark 和 Hadoop 有助于我们利用 Spark 的处理能力，充分利用 Hadoop 的 HDFS 和 YARN。

**![](img/cf9b3577a707320e32f6e5a84820285a.png) 图:  ** *使用 Spark 和 Hadoop* 

Hadoop 组件可以通过以下方式与 Spark 一起使用:

1.  :Spark 可以在 HDFS 上运行，以利用分布式复制存储。
2.  **MapReduce** : Spark 可以在同一个 Hadoop 集群中与 MapReduce 一起使用，也可以单独作为一个处理框架使用。
3.  **YARN** : Spark 应用也可以在 YARN 上运行(Hadoop NextGen)。
4.  **批处理&实时处理** : MapReduce 和 Spark 一起使用，MapReduce 用于批处理，Spark 用于实时处理。

### **26。什么是 RDD 血统？**

Spark 不支持内存中的数据复制，因此，如果有任何数据丢失，将使用 RDD 血统重建。RDD 沿袭是重建丢失的数据分区的过程。最棒的是，RDD 总是记得如何从其他数据集构建。

### **27。什么是火花驱动器？**

Spark Driver 是在机器的主节点上运行的程序，它声明数据 rdd 上的转换和动作。简单地说，Spark 中的驱动程序创建 SparkContext，连接到给定的 Spark Master。驱动程序还将 RDD 图传递给主程序，独立集群管理器在主程序中运行。

### **28。Spark 支持哪些文件系统？**

Spark 支持以下三种文件系统:

1.  Hadoop 分布式文件系统(HDFS)。
2.  本地文件系统。
3.  亚马逊 S3

### **29。列出 Spark SQL 的函数。**

Spark SQL 能够:

1.  从各种结构化来源加载数据。
2.  使用 SQL 语句查询数据，既可以在 Spark 程序内部查询，也可以从通过标准数据库连接器(JDBC/ODBC)连接到 Spark SQL 的外部工具中查询。例如，使用 Tableau 这样的商业智能工具。
3.  在 SQL 和常规 Python/Java/Scala 代码之间提供丰富的集成，包括连接 rdd 和 SQL 表的能力，在 SQL 中公开定制函数，等等。

### **30。什么是星火执行者？**

当 SparkContext 连接到集群管理器时，它在集群中的节点上获取一个执行器。执行器是运行计算并将数据存储在工作节点上的 Spark 进程。SparkContext 的最终任务被传递给执行者执行。

### **31。Spark 中集群管理器的名称类型。**

Spark 框架支持三种主要类型的集群管理器:

1.  **单机**:设置集群的基本管理器。
2.  **Apache Mesos** :通用/常用集群管理器，也运行 Hadoop MapReduce 和其他应用。
3.  **纱**:负责 Hadoop 中的资源管理。

### **32。你所理解的工人节点是什么？**

Worker 节点指的是集群中可以运行应用程序代码的任何节点。驱动程序必须监听并接受来自其执行器的输入连接，并且必须可以从工作节点通过网络寻址。

工作者节点基本上是从节点。主节点分配工作，工作节点实际执行分配的任务。工作节点处理存储在节点上的数据，并向主节点报告资源。基于资源可用性，主计划任务。

### **33。举例说明使用 Spark 的一些缺点。**

以下是使用 Apache Spark 的一些缺点:

1.  与 Hadoop 和 MapReduce 相比，Spark 使用更多的存储空间，因此可能会出现一些问题。
2.  开发人员在 Spark 中运行他们的应用程序时需要小心。
3.  工作必须分布在多个集群上，而不是在单个节点上运行一切。
4.  在经济高效地处理大数据方面，Spark 的“内存”功能可能会成为一个瓶颈。
5.  与 Hadoop 相比，Spark 消耗大量数据。

### **34。列举一些 Spark 在处理上优于 Hadoop 的用例。**

1.  **传感器数据处理** : Apache Spark 的“内存”计算在这里工作得最好，因为数据是从不同来源检索和组合的。
2.  **实时处理** : Spark 比 Hadoop 更适合实时查询数据。如*股市分析*、*银行业*、*医疗保健*、*电信*等。
3.  **流处理**:对于处理日志和检测实时流中的欺诈以发出警报，Apache Spark 是最佳解决方案。
4.  **大数据处理**:在处理中大型数据集时，Spark 的运行速度比 Hadoop 快 100 倍。

你甚至可以通过 [Azure 数据工程师助理](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 查看大数据的细节。

### **35。什么是稀疏向量？**

一个稀疏向量有两个平行的数组；一个用于索引，另一个用于值。这些向量用于存储非零条目以节省空间。

```
Vectors.sparse(7,Array(0,1,2,3,4,5,6),Array(1650d,50000d,800d,3.0,3.0,2009,95054))

```

可以用上面的稀疏向量代替密集向量。

```
val myHouse = Vectors.dense(4450d,2600000d,4000d,4.0,4.0,1978.0,95070d,1.0,1.0,1.0,0.0)

```

### **36。你能使用 Spark 访问和分析 Cassandra 数据库中存储的数据吗？**

是的，如果你使用 Spark Cassandra 连接器，这是可能的。要将 Spark 连接到 Cassandra 集群，需要将 Cassandra 连接器添加到 Spark 项目中。在设置中，Spark 执行器将与本地 Cassandra 节点对话，并且只查询本地数据。它通过减少在 Spark 执行器(处理数据)和 Cassandra 节点(数据所在的位置)之间发送数据的网络使用，使查询更快。

### **37。有可能在 Apache Mesos 上运行 Apache Spark 吗？**

是的，Apache Spark 可以在 Mesos 管理的硬件集群上运行。在独立集群部署中，下图中的集群管理器是一个 Spark master 实例。当使用 Mesos 时，Mesos 主服务器取代 Spark 主服务器作为集群管理器。Mesos 决定什么机器处理什么任务。因为它在调度这些短期任务时考虑到了其他框架，所以多个框架可以在同一个集群上共存，而无需采用静态的资源划分。

### **38。Spark 如何连接阿帕奇 Mesos？**

连接 Spark 和 Mesos:

1.  配置火花驱动程序以连接到 Mesos。
2.  Spark 二进制包应放在 Mesos 可以接触到的位置。
3.  将 Apache Spark 安装在与 Apache Mesos 相同的位置，并将属性' spark.mesos.executor.home '配置为指向它的安装位置。

### **39。在使用 Spark 时，如何最大限度地减少数据传输？**

最小化数据传输和避免混乱有助于编写快速可靠运行的 spark 程序。使用 Apache Spark 时，可以最小化数据传输的各种方法有:

1.  使用广播变量——广播变量提高了小型和大型 rdd 之间的连接效率。
2.  使用累加器——累加器有助于在执行时并行更新变量的值。

最常见的方法是避免按键操作、重新分区或任何其他触发洗牌的操作。

### **40。什么是广播变量？**

广播变量允许程序员在每台机器上缓存一个只读变量，而不是在任务中发送一个副本。它们可用于以高效的方式为每个节点提供大型输入数据集的副本。Spark 还尝试使用高效的广播算法来分发广播变量，以降低通信成本。

### **![Broadcast Variables - Spark Interview Questions - Edureka](img/9210a056d1fbf5e1c3972e223007ee34.png) 41。解释 Apache Spark 中的累加器。** 

累加器是只通过结合和交换运算相加的变量。它们用于实现计数器或求和。在用户界面中跟踪累加器有助于了解运行阶段的进度。Spark 本身支持数字累加器。我们可以创建命名或未命名的累加器。

**![Accumulators - Spark Interview Questions - Edureka](img/0442d21af6e8df0906a1a38af5cafccc.png)**

### **42。为什么用 Apa** **che Spark 工作时需要广播变量？**

广播变量是只读变量，存在于每台机器的内存缓存中。使用 Spark 时，广播变量的使用消除了为每个任务发送变量副本的必要性，因此可以更快地处理数据。广播变量有助于在内存中存储查找表，与 RDD *lookup()* 相比，提高了检索效率。

### **43。如何在 Spark 中触发自动清理来处理累积的元数据？**

您可以通过设置参数“ *spark.cleaner.ttl* ”或通过将长时间运行的作业分成不同的批次并将中间结果写入磁盘来触发清理。

### **44。滑动窗口操作的意义是什么？**

滑动窗口控制各种计算机网络之间数据包的传输。Spark Streaming library 提供了窗口计算，其中 rdd 上的转换应用于数据的滑动窗口。每当窗口滑动时，落在特定窗口内的 rdd 被组合和操作，以产生窗口数据流的新 rdd。

### **![DStream Sliding Window - Spark Interview Questions - Edureka](img/655f3a7e33fc8faa3935ec22d8c63313.png) 45。Apache Spark 中的 DStream 是什么？** 

***离散化流*** (DStream)是 Spark Streaming 提供的基本抽象。它是一个连续的数据流。它是从数据源或从通过转换输入流而生成的已处理数据流中接收的。在内部，数据流由一系列连续的 RDD 表示，每个 RDD 包含某个区间的数据。 应用于数据流的任何操作都会转化为对底层 rdd 的操作。

数据流可以从各种来源创建，如 Apache Kafka、HDFS 和 Apache Flume。数据流有两个操作:

1.  产生新数据流的变换。
2.  将数据写入外部系统的输出操作。

在 Spark Streaming 中有许多可能的数据流转换。 让我们看看**滤镜(*****)func*****)**。 filter( *func* )通过仅选择源数据流中 *func* 返回 true 的记录来返回新的数据流。

### **![DStream Filter - Spark Interview Questions - Edureka](img/1ce97057d7a631adbd058c47a68a64c9.png) 46。解释 Spark 流中的缓存。** 

数据流允许开发者在内存中缓存/保存数据流的数据。如果数据流中的数据将被计算多次，这是很有用的。这可以使用 DStream 上的 persist()方法来完成。对于通过网络接收数据的输入流(如 Kafka、Flume、Sockets 等。)，默认的持久性级别设置为将数据复制到两个节点以实现容错。

**![Caching - Spark Interview Questions - Edureka](img/51d2612e91969f1b2f73a6d2ce220471.png)**

### **47。运行 Spark 应用时，是否需要在 YARN cluster 的所有节点上都安装 Spark？**

在 YARN 或 Mesos 下运行作业时，不需要安装 Spark，因为 Spark 可以在 YARN 或 Mesos 集群上执行，而不会影响集群的任何变化。

### **48。Spark SQL 中有哪些不同的数据源？**

Spark SQL 中可用的数据源有 Parquet 文件、JSON 数据集和 Hive 表。

### **49。Apache Spark 中持久化的各个层次是什么？**

Apache Spark 自动持久化各种混洗操作的中间数据，但是，如果用户打算重用它，通常建议用户在 RDD 上调用 persist()方法。Spark 有不同的持久性级别来将 rdd 存储在磁盘或内存中，或者以不同复制级别将两者结合起来。

Spark 中的各种存储/持续级别有:

1.  MEMORY_ONLY:将 RDD 作为反序列化的 Java 对象存储在 JVM 中。如果 RDD 不适合内存，一些分区将不会被缓存，并将在每次需要时动态地重新计算。这是默认级别。
2.  MEMORY_AND_DISK:将 RDD 作为反序列化的 Java 对象存储在 JVM 中。如果 RDD 不适合内存，存储不适合磁盘的分区，并在需要时从那里读取它们。
3.  MEMORY_ONLY_SER:将 RDD 存储为*序列化的* Java 对象(每个分区一个字节数组)。
4.  MEMORY_AND_DISK_SER:类似于 MEMORY_ONLY_SER，但是将不适合内存的分区溢出到磁盘，而不是在每次需要时动态地重新计算它们。
5.  DISK_ONLY:仅在磁盘上存储 RDD 分区。
6.  OFF_HEAP:类似 MEMORY_ONLY_SER，但是将数据存储在堆外内存中。

### **50。Apache Spark 提供检查点吗？**

*关卡*类似于游戏中的关卡。它们使它 24/7 全天候运行，并使它对与应用程序逻辑无关的故障具有弹性。

![Checkpoints - Spark Interview Questions - Edureka](img/ab9c9e9ec03e8a365df6c191575fbcf8.png) **图:** *星火面试试题——关卡* 

谱系图对于从故障中恢复 rdd 总是有用的，但是如果 rdd 具有长的谱系链，这通常是耗时的。Spark 有一个用于检查点的 API，即一个持久的复制标志。但是，对哪些数据进行检查点的决定是由用户决定的。当谱系图很长并且具有广泛的依赖性时，检查点很有用。

### **51。Spark 如何使用 Akka？**

Spark 基本使用 Akka 进行调度。所有工人注册后都要求掌握一项任务。主人只是分配任务。在这里，Spark 使用 Akka 在工人和主人之间传递信息。

### **52。你所理解的懒评是什么？**

Spark 处理数据的方式是智能的。当你告诉 Spark 对一个给定的数据集进行操作时，它会留意指令并记录下来，这样它就不会忘记——但它什么也不做，除非询问最终结果。当在 RDD 上调用类似 map *()* 的变换时，操作不会立即执行。Spark 中的转换直到您执行一个动作时才会被评估。这有助于优化整个数据处理工作流程。

### **![Lazy Evaluation - Spark Interview Questions - Edureka](img/4087d918f0437eeb8a1413be3cb00ceb.png) 53。你对《阿帕奇星火 RDD》中的 SchemaRDD 有什么理解？** 

*SchemaRDD* 是一个 RDD，它由行对象(基本字符串或整数数组的包装器)组成，带有关于每列数据类型的模式信息。

SchemaRDD 旨在让开发人员在 SparkSQL 核心模块上进行代码调试和单元测试的日常工作变得更加轻松。这个想法可以归结为使用类似于关系数据库模式的正式描述来描述 RDD 内部的数据结构。除了通用 RDD API 提供的所有基本函数之外，SchemaRDD 还提供了一些通过 SparkSQL 实现的简单的关系查询接口函数。

现在，在 Spark 最新的主干上正式更名为 *DataFrame API* 。

### **54。****Spark SQL 与 HQL 和 SQL 有何不同？**

Spark SQL 是 Spark 核心引擎上的一个特殊组件，支持 SQL 和 Hive 查询语言，不改变任何语法。可以将 SQL 表和 HQL 表连接成 Spark SQL。

### **55。解释一个您将使用 Spark Streaming 的场景。**

就 Spark 流而言，数据是实时流入我们的 Spark 程序的。

Twitter 情绪分析是 Spark 流媒体的真实用例。趋势话题可用于创建活动和吸引更多的观众。它有助于危机管理、服务调整和目标营销。

情绪是指社交媒体在线提及背后的情绪。情感分析是对与特定主题相关的推文进行分类，并使用情感自动化分析工具进行数据挖掘。

Spark Streaming 可用于将世界各地的实时推文收集到 Spark 计划中。这个流可以使用 Spark SQL 过滤，然后我们可以根据情绪过滤推文。过滤逻辑将使用 MLlib 实现，我们可以从公众的情绪中学习，并相应地改变我们的过滤尺度。

![Twitter Use Case - Spark Interview Questions - Edureka](img/b9f9868ee97720bacae3bc89676d3f3c.png)

上图显示了包含单词*‘Trump’*的推文的情绪。

在本教程中了解更多 Spark Streaming:[Spark Streaming 教程| YouTube | edu reka](https://www.youtube.com/watch?v=uD_q4Rm4i2Q&list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb)

我希望这套 Apache Spark 面试问题能帮助你准备面试。

此外，我首先推荐以下来自 Edureka 的 [Apache Spark 教程视频](https://www.youtube.com/playlist?list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb) 。

## 2023 年星火面试问答| Edureka



[//www.youtube.com/embed/LjNY3ijB2K4?rel=0&showinfo=0](//www.youtube.com/embed/LjNY3ijB2K4?rel=0&showinfo=0)

本 Edureka Apache Spark 面试问答教程帮助您了解如何在 Spark 面试中处理问题，并让您了解在 Spark 面试中可以提出的问题。

*Spark Tutorial 上的这个视频系列提供了这些组件的完整背景，以及真实生活中的用例，如 [Twitter 情绪分析](https://www.youtube.com/watch?v=uD_q4Rm4i2Q&amp;amp;amp;amp;amp;list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb)、 [NBA 游戏预测分析](https://www.youtube.com/watch?v=zeDUx_Jf154&amp;amp;amp;amp;amp;list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb)、[地震检测系统](https://www.youtube.com/watch?v=9mELEARcxJo&amp;amp;amp;amp;amp;list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb)、[飞行数据分析](https://www.youtube.com/watch?v=BQlgZaKvfac&amp;amp;amp;amp;amp;list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb)和[电影推荐系统](https://www.youtube.com/watch?v=qX1kYJ6h7j8&amp;amp;amp;amp;amp;list=PL9ooVrP1hQOGyFc60sExNX1qBWJyV5IMb)。我们亲自设计了用例，以便为运行代码的任何人提供全面的专业知识。*

*有问题吗？请在评论区提到它，我们会尽快回复您。* *如果您希望学习 Spark，并在 Spark 领域建立职业生涯，并积累使用 RDD、Spark Streaming、SparkSQL、MLlib、GraphX 和 Scala 执行大规模数据处理的专业知识，并在实际生活中使用案例，请查看我们的交互式在线直播* *[Apache Spark 认证培训](https://www.edureka.co/apache-spark-scala-training)此处，* *该培训提供 24*7 支持，可在整个学习期间为您提供指导。*