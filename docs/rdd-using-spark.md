# 使用 Spark 的 RDD:Apache Spark 的构建块

> 原文：<https://www.edureka.co/blog/rdd-using-spark/>

**[火花](https://www.edureka.co/apache-spark-scala-certification-training)、** 这个词本身就足以在每一个 Hadoop 工程师的脑海里产生火花。**一个** **n 内存**处理工具**** 在集群计算中快如闪电。与 MapReduce 相比，内存数据共享使 RDDs **比网络和磁盘共享快 10-100 倍**，这一切都是因为 RDDs(弹性分布式数据集)而成为可能。在这篇使用 Spark 的 RDD 文章中，我们今天关注的要点是:

*   [对 rdd 的需求](#need-for-rdd)
*   [rdd 是什么？](#what-are-rdds)
*   [RDDs 的特性](#features-of-rdds)
*   [使用 Spark 创建 RDDs】](#creation-of-rdds-using-spark)
*   [对 rdd 执行的操作](#operations-performed)
*   [RDDs 使用 Spark:口袋妖怪用例](#pokemon-use-case)

## ****需要 RDDs 吗？****

![Why do we need RDD?-RDD using Spark](img/3c4060202751cdca83445cb4230213b8.png)

世界在进化着 ****[人工智能](https://www.edureka.co/blog/artificial-intelligence-tutorial/)**** 和 ****[数据科学](https://www.edureka.co/blog/data-science-tutorial/)**** 因为 ****[机器学习](https://www.edureka.co/blog/what-is-machine-learning/)的进步。**** 算法基于**[聚类](https://www.edureka.co/blog/k-means-clustering-algorithm/)**[和 **C **分类****](https://www.edureka.co/blog/classification-algorithms/) 运行于 ****分布式********迭代计算****

传统的[****MapReduce****](https://www.edureka.co/blog/mapreduce-tutorial/)技术需要稳定的中间和分布式存储，如 [HDFS](https://www.edureka.co/blog/hdfs-tutorial) 包括重复计算和数据复制和数据序列化，这使得过程慢了很多。找到解决方案从来都不容易。

![Traditional HDFS-RDD using Spark](img/a9cc45135c8dac70def019f003bea251.png)

这就是(弹性分布式数据集)发挥作用的地方。

****此外，应用这些操作来处理它们。它们是一个 ****分布式内存集合**** ，权限为**只读**，最重要的是，它们是**容错** ****。********

![In memory computation of RDD-RDD using Spark](img/7ac4aedfc09661079acdf79f468a6595.png)

如果 an RDD 的任意 ****数据分区**** 丢失，可以通过对**沿袭**中那个丢失的分区应用相同的 ****变换**** 操作来重新生成，而不是从头开始处理所有数据。在实时场景中，这种方法可以在数据丢失或系统停机的情况下创造奇迹。

## ****rdd 是什么？****

或( ****弹性分布式数据集**** )是 Spark 中一个基本的 ****数据结构**** 。术语 ****弹性**** 定义了当发生意外灾难且有可能丢失数据时，自动生成数据或数据**回滚**到 ****原始状态**** 的能力。

![Data rolled back-RDD using Spark](img/8c40caa45684b54900dd6d466b096efe.png)

写入 RDDs 的数据被 ****分区**** 存储到 ****多个可执行节点**** ****。**** 如果一个正在执行的节点**在运行时**失败，那么它立即从下一个可执行的节点 得到备份。这就是为什么与其他传统数据结构相比，rdd 被认为是一种高级类型的数据结构。rdd 可以存储结构化、非结构化和半结构化数据。

![RDD Multiple Partitions-RDD using Spark](img/0ab6c01e5d08d01d59edc658138f1968.png)

让我们使用 Spark 博客继续我们的 RDD，并了解 RDDs 的独特特性，这些特性使它比其他类型的数据结构更有优势。

## ****RDD 的特色****

![Features of RDD-RDD using Spark](img/e20f1a23aca533bd05d96ecd40232199.png)

*   ****内存中********【RAM】********计算**** :内存中计算的概念将数据处理带到了一个更快、更高效的阶段，系统的整体性能 ****得到了提升。****
*   ****L********azy 求值**** :术语懒惰求值表示将 ****转换**** 应用于 RDD 的数据，但不生成输出。相反，应用的转换被记录在 ****中。****
*   ****持久性**** :生成的 rdd 总是 ****可重用。****
*   ****粗粒度操作**** :用户可以通过 ****映射、**** ****过滤**** 或 ****分组**** 操作对数据集中的所有元素进行变换。
*   :如果有数据丢失，系统可以通过使用记录的****回滚**** 到其 ****原始状态**** 。
*   ****不变性**** :定义、取数或创建的数据一旦登录系统，就不能再。如果您需要访问和修改现有的 RDD，您必须通过将一组 ****变换**** 函数应用到当前或之前的 RDD 上来创建一个新的 RDD。
*   ****分区**** :是 Spark ****RDD 中的的关键单元。**** 默认情况下，创建的分区数量取决于您的数据源。您甚至可以使用 ****自定义分区**** 功能来决定想要创建的分区数量。

## ****RDD 利用星火创作****

rdd 可以通过**三种方式创建:**

![Methods of creating RDD-RDD using Spark](img/8814df426cd4006561162d6f8df83450.png)

1.  从**并行化集合**中读取数据

```
val PCRDD = spark.sparkContext.parallelize(Array("Mon","Tue","Wed","Thu","Fri","Sat"),2)
val resultRDD = PCRDD.collect()
resultRDD.collect().foreach(println)

```

2.  将**转换**应用于之前的 rdd

```
val words = spark.sparkContext.parallelize(Seq("Spark","is","a","very","powerful","language"))
val wordpair = words.map(w =(w.charAt(0),w))
wordpair.collect().foreach(println)

```

3.  从**外部存储器**或 **HDFS** 或 **HBase** 等文件路径中读取数据

```
val Sparkfile = spark.read.textFile("/user/edureka_566977/spark/spark.txt.")
Sparkfile.collect()

```

## **对 rdd 执行的操作:**

在 rdd 上执行的操作主要有两种，即:

*   **变换**
*   **动作**

****![Transformations and actions-RDD using Spark](img/6290820b3c29dcfe6ffc2de35f515bd9.png)****

****变换******:******操作**** 我们对 RDDs 应用**过滤，访问******修改**** 中的数据，在父 RDD 生成一个逐次 RDD****变换**** 。新的 RDD 返回一个指向以前的 RDD 的指针，确保它们之间的依赖关系。

转换是 ****惰性求值，**** 换句话说，应用于您正在工作的 RDD 的操作将被记录，但不会执行 ****。**** 触发**动作**后，系统抛出结果或异常。

我们可以将转换分为以下两种类型:

*   **缩小变换**
*   **广变换**

**窄变换**我们将窄变换应用到父 RDD 的**单个分区**上，以生成新的 RDD，因为处理 RDD 所需的数据在**父 RDD 的单个分区**上可用。窄变换的例子有:

*   **地图()**
*   **【过滤()】**

*   **分区()**
*   **【映射分区()**

**宽变换:**我们在**多个分区**上应用宽变换来生成新的 RDD。处理 RDD 所需的数据在**父 RDD** 的多个分区上可用。宽变换的例子有:

*   减少量()减少量

****动作**** :动作指示 Apache Spark 应用 ****计算**** ，并将结果或异常传回给驱动程序 RDD。几个动作包括:

*   ****收藏()****
*   **计数()**
*   ****乘()****
*   第一

让我们实际应用 rdd 上的操作:

![IPL Teams-RDD using Spark](img/44cbd876212ec63b5acd1b3b93ebae08.png)

**IPL(印度超级联赛)**是一项板球赛事，其 hipe 处于巅峰水平。因此，让我们今天着手 IPL 数据集，并使用 Spark 执行我们的 RDD。

*   **首先，**让我们下载一份 IPL 的 CSV 比赛数据。下载后，它开始看起来像一个带有行和列的 EXCEL 文件。

![Matches.csv-RDD with Spark](img/d84d395d91b0a25093521e1621bd4c4c.png)

下一步，我们点燃火花并从其位置加载 matches.csv 文件，在我的例子中，我的 csv 文件位置是**"/user/edu reka _ 566977/test/matches . CSV "**

![Fire up the Spark-RDD using Spark](img/26e17088859b2bc66700c65227dc8343.png)

现在让我们先从**转换**部分开始:

![Transformation-RDD using Spark](img/6e5ac586f5462f397b302b3422aad535.png)

*   **地图():**

我们使用**地图变换**对 RDD 的每个元素应用特定的变换操作。在这里，我们创建一个名为 CKfile 的 RDD，在这里存储我们的 csv 文件。我们将创建另一个名为 States 的 RDD 来**存储城市细节**。

```
spark2-shell
val CKfile = sc.textFile("/user/edureka_566977/test/matches.csv")
CKfile.collect.foreach(println)
val states = CKfile.map(_.split(",")(2))
states.collect().foreach(println)

```

![Map Transformation in spark- RDD using Spark](img/b4e748de4f5e5bdcd61f30d4ef45a07d.png)

*   **滤镜():**

滤镜变换，名字本身就描述了它的用途。我们使用这个转换操作从给定的数据集合中过滤出选择性的数据。我们在这里应用**过滤操作**来获取 2017**年**的 IPL 比赛记录，并将其存储在 fil RDD 中。

```
val fil = CKfile.filter(line => line.contains("2017"))
fil.collect().foreach(println)

```

![Filter operation using Spark-RDD using Spark](img/8dd0c39d74cf632476b68e9d99ed7f89.png)

*   **flatMap():**

我们对 RDD 的每个元素应用了一个变换操作，以创建一个新的 RDD。它类似于地图转换。这里我们应用平面地图到**吐出海德拉巴市**的匹配，并将数据存储到 filRDD RDD。

```

val filRDD = fil.flatMap(line => line.split("Hyderabad")).collect()

```

![Flat Map Transformation in Spark-RDD using Spark](img/57b8fc228391991d4d26b84dea5a9a40.png)

*   **分区():**

我们写入 RDD 的每个数据都被分成一定数量的分区。我们使用这个转换来找到数据实际被分割成的分区数量。

```
val fil = CKfile.filter(line => line.contains("2017"))
fil.partitions.size

```

![Partition Transformation Output-RDD using Spark](img/c433b6097e50a643b7eafa2bc37e9417.png)

*   **图分区():**

我们认为映射部分是映射()和 foreach ()的替代。我们在这里使用 mapPartitions 来查找 fil RDD 中的行数。

```
val fil = CKfile.filter(line => line.contains("2016"))
fil.mapPartitions(idx => Array(idx.size).iterator).collect

```

![MapPartitions Transformation Output-RDD using Spark](img/a3c4336a20710d4abec113332a17cfa2.png)

*   **减量()**T3

我们在**键值对**上使用 ReduceBy ()。我们在我们的 csv 文件中使用了这种转换，来查找拥有**最高分**的玩家。

```
val ManOfTheMatch = CKfile.map(_.split(",")(13))
val MOTMcount = ManOfTheMatch.map(WINcount => (WINcount,1))
val ManOTH = MOTMcount.reduceByKey((x,y) => x+y).map(tup => (tup._2,tup._1))sortByKey(false)
ManOTH.take(10).foreach(println)

```

![ReduceBy Transformation Output-RDD using Spark](img/7b4635e28fb84b78946b03255acd37e2.png)

*   **工会():**

这个名字说明了一切，我们用 union 改造就是将**俱乐部的两个 rdd 组合在一起**。这里我们创建两个 rdd，即 fil 和 fil2。fil RDD 包含 2017 年 IPL 比赛的记录，fil2 RDD 包含 2016 年 IPL 比赛的记录。

```
val fil = CKfile.filter(line => line.contains("2017"))
val fil2 = CKfile.filter(line => line.contains("2016"))
val uninRDD = fil.union(fil2)

```

![Union Transformation in spark-RDD in Spark](img/31d3ee40c6cecd19cceddc24c9701082.png)

让我们从**动作**部分开始，这里我们显示实际输出:

![Action-RDD using Spark](img/c4d1d652d0611b276813b5494ba9c7a0.png)

*   ****收藏():****

收集是我们用来**在 RDD 中显示内容**的动作。

```
val CKfile = sc.textFile("/user/edureka_566977/test/matches.csv")
CKfile.collect.foreach(println)

```

![Collect Action Using Spark-RDD using Spark](img/139533fa904f98b39d7226b0459e4a8a.png)

*   **计数():**

Count 是一个动作，我们用它来计算 RDD 中存在的记录的数量**。这里我们使用这个操作来计算 matches.csv 文件中的记录总数。**

```
val CKfile = sc.textFile("/user/edureka_566977/test/matches.csv")
CKfile.count()

```

![Count Action-RDD using Spark](img/ed2f962244c6e561680839c2127f4f2d.png)

*   ****乘():****

Take 是一个类似于 collect 的动作操作，但唯一的区别是它可以根据用户的请求打印任意选择数量的**行**。这里我们应用下面的代码来打印**十大领先报告。**

```
val statecountm = Scount.reduceByKey((x,y) => x+y).map(tup => (tup._2,tup._1))sortByKey(false)
statecountm.collect().foreach(println)
statecountm.take(10).foreach(println)

```

![Take Action output-RDD using Spark](img/ebedc5449080d8553337751c1dc2df9c.png)

*   ****第一():****

First()是一个类似于 collect()和 take() 的操作，它用来打印最上面的报告 s。这里的输出我们使用 First()操作来查找**在一个特定的城市**中比赛的最大次数，我们得到孟买作为输出。

```
val CKfile = sc.textFile("/user/edureka_566977/test/matches.csv")
val states = CKfile.map(_.split(",")(2))
val Scount = states.map(Scount => (Scount,1))
scala&gt; val statecount = Scount.reduceByKey((x,y)=> x+y).collect.foreach(println)
Scount.reduceByKey((x,y)=> x+y).collect.foreach(println)
val statecountm = Scount.reduceByKey((x,y)=> x+y).map(tup => (tup._2,tup._1))sortByKey(false)
statecountm.first()

```

![First Action Output-RDD using Spark](img/c2ee1bd3b1217a9a1fbf6b9526fcd213.png)

为了让我们使用 Spark 学习 RDD 的过程更加有趣，我提出了一个有趣的用例。

## **RDD 使用 Spark:口袋妖怪用例**

## **![Pokemon-RDD using Spark](img/6072d033d99cb9dd7642ef20bbcfeee3.png)**

*   首先，让我们下载一个 Pokemon.csv 文件，并像加载 Matches.csv 文件一样加载到 spark-shell 中。

```
val PokemonDataRDD1 = sc.textFile("/user/edureka_566977/PokemonFile/PokemonData.csv")
PokemonDataRDD1.collect().foreach(println)

```

![Loading CSV-RDD using Spark](img/6fcc659e304bfbcdb16ecf91cd444ba7.png)

口袋妖怪其实种类繁多，我们来找几个品种。

*   **从 Pokemon.csv 文件中删除模式**

我们可能不需要 Pokemon.csv 文件的**模式**。因此，我们删除它。

```
val Head = PokemonDataRDD1.first()
val NoHeader = PokemonDataRDD1.filter(line => !line.equals(Head))

```

**![](img/e3bc06c04b7d97727fb88066255e0918.png)**

*   求**分区的数量**我们的 pokemon.csv 分发到。

```
println("No.ofpartitions="+NoHeader.partitions.size)

```

**![partition of pokemon.csv-RDD using Spark](img/b7ebe8f373d124d3b99c16c4d1de7a10.png)**

*   **水中口袋妖怪**

寻找**数量的水口袋妖怪**

```
val WaterRDD = PokemonDataRDD1.filter(line => line.contains("Water"))
WaterRDD.collect().foreach(println)

```

![Water Pokemon-RDD using Spark](img/40ca6870387fa2852b399381c9c12cef.png)

*   **火口袋妖怪**

寻找**数量的火口袋妖怪**

```
val FireRDD = PokemonDataRDD1.filter(line => line.contains("Fire"))
FireRDD.collect().foreach(println)

```

![Fire Pokemon-RDD using Spark](img/01017895956cb5681a657e7f50d2ea29.png)

*   我们还可以使用计数功能检测不同类型口袋妖怪的**数量**

```
WaterRDD.count()
FireRDD.count()

```

![Population count-RDD using Spark](img/1f0af4a1d2d34fa92370ef737aa1ad66.png)

*   既然我喜欢**防御策略**的游戏，那就让我们找到**最大防御的口袋妖怪吧。**

```
val defenceList = NoHeader.map{x => x.split(',')}.map{x => (x(6).toDouble)}
println("Highest_Defence : "+defenceList.max())

```

![maximum Defence - RDD using Spark](img/4e9ef02aa6452f23e05794585b26775e.png)

*   我们知道最大**防御强度值**却不知道是哪个口袋妖怪。所以，让我们来找出哪个是那个**口袋妖怪。**

```
val defWithPokemonName = NoHeader.map{x => x.split(',')}.map{x => (x(6).toDouble,x(1))}
val MaxDefencePokemon = defWithPokemonName.groupByKey.takeOrdered(1)(Ordering[Double].reverse.on(_._1))
MaxDefencePokemon.foreach(println)

```

![GroupBy to find max defence pokemon name-RDD usin Spark](img/541eb084247ab2aaad35ff728bceb036.png)

*   现在让我们来梳理一下**防御最少**的口袋妖怪

```
val minDefencePokemon = defenceList.distinct.sortBy(x => x.toDouble,true,1)
minDefencePokemon.take(5).foreach(println)

```

![Pokemon with least defence-RDD using Spark](img/5659270ecf21bef31353d5805993aca6.png)

*   现在让我们看看少了**防御策略的口袋妖怪。**

```
val PokemonDataRDD2 = sc.textFile("/user/edureka_566977/PokemonFile/PokemonData.csv")
val Head2 = PokemonDataRDD2.first()
val NoHeader2 = PokemonDataRDD2.filter(line => !line.equals(Head))
val defWithPokemonName2 = NoHeader2.map{x => x.split(',')}.map{x => (x(6).toDouble,x(1))}
val MinDefencePokemon2 = defWithPokemonName2.groupByKey.takeOrdered(1)(Ordering[Double].on(_._1))
MinDefencePokemon2.foreach(println)

```

![least defensive strategy-RDD using Spark](img/1b113eceb48b94a75818a8718f591c07.png)

就这样，我们结束了这篇 RDD 使用 Spark 的文章。我希望我们对您关于 rdd 的知识、它们的特性以及可以在其上执行的各种类型的操作有所启发。

*本文基于 [**Apache Spark 和 Scala 认证培训**](https://www.edureka.co/apache-spark-scala-certification-training) 为您准备 Cloudera Hadoop 和 Spark 开发者认证考试(CCA175)。您将深入了解 Apache Spark 和 Spark 生态系统，包括 Spark RDD、Spark SQL、Spark MLlib 和 Spark Streaming。您将获得关于 Scala 编程语言、HDFS、Sqoop、Flume、Spark GraphX 和 Kafka 等消息系统的全面知识。*