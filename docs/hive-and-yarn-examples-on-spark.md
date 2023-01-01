# Spark 上的蜂巢和纱线示例

> 原文：<https://www.edureka.co/blog/hive-and-yarn-examples-on-spark>

我们已经学会了如何在星火上 [建造蜂巢和纱线](https://www.edureka.co/blog/yarn-hive-get-electrified-by-spark/ "Building Hive and Yarn on Spark") 。现在让我们在 Spark 上尝试一下 Hive 和 Yarn 示例。

[![Learn-Spark-Now](img/7cd08326a481c4e83aaba01b9e90f6e4.png)](https://www.edureka.co/apache-spark-scala-training)

## Spark 上的配置单元示例

我们将在 Spark 上运行一个 Hive 示例。我们将创建一个表，在该表中加载数据并执行一个简单的查询。使用 Hive 时，必须构造一个继承自 **SQLContext** 的 **HiveContext** 。

**命令:** cd 火花-1.1.1

**命令:**。/bin/spark-shell

![hive-and-yarn-practicals-on-spark-7](img/afbe3419e18a1636d086757754a93664.png "hive-and-yarn-practicals-on-spark-7")

在您的主目录中创建一个输入文件**‘sample’**，如下图所示(制表符分隔)。

![hive-and-yarn-practicals-on-spark-8](img/d16b25a906968ded7684f507053266e2.png "hive-and-yarn-practicals-on-spark-8")

**命令:**val sqlContext = new org . Apache . spark . SQL . hive . hive context(sc)

![hive-and-yarn-practicals-on-spark-9](img/472a1bc32381eca4a775bd7bcca7df2f.png "hive-and-yarn-practicals-on-spark-9")

**命令:**sqlcontext . SQL(" CREATE TABLE IF NOT EXISTS test(name STRING，rank INT)行格式分隔的字段以' '行终止于'' ' ")

![hive-and-yarn-practicals-on-spark-10](img/d2f9f14063c1b2d885582682d5d6ecf4.png "hive-and-yarn-practicals-on-spark-10")

**命令:**sqlcontext . SQL(" LOAD DATA LOCAL in path '/home/edu reka/sample ' INTO TABLE test ")

![hive-and-yarn-practicals-on-spark-11](img/10b49a3e3deb8e1c85b0e013743b826f.png "hive-and-yarn-practicals-on-spark-11")

**命令:**sqlcontext . SQL(" SELECT * FROM test WHERE rank<5 ")。收集()。foreach(println)

![hive-and-yarn-practicals-on-spark-12](img/f6e0977506dc714999e6ae11604d0653.png "hive-and-yarn-practicals-on-spark-12")

## 火花上的纱线示例

我们将在纱线上运行 SparkPi 示例。我们可以在 Spark 上以两种模式部署 Yarn:集群模式和客户端模式。在 yarn-cluster 模式下，Spark 驱动程序在一个应用程序主进程中运行，该进程由集群上的 yarn 管理，客户端可以在启动应用程序后离开。在 yarn-client 模式下，驱动程序在客户端进程中运行，应用程序主机仅用于向 yarn 请求资源。

**命令:** cd 火花-1.1.1

**命令:** SPARK_JAR=。/assembly/target/Scala-2.10/spark-assembly-1 . 1 . 1-Hadoop 2 . 2 . 0 . jar。/bin/spark-submit–master yarn–deploy-mode cluster–class org . Apache . spark . examples . spark pi–num-executors 1–driver-memory 2g–executors-memory 1g–executors-cores 1 examples/target/Scala-2.10/spark-examples-1 . 1 . 1-Hadoop 2 . 2 . 0 . jar

![hive-and-yarn-practicals-on-spark-1](img/98fccb9ed2173085e0eb051107767356.png "hive-and-yarn-practicals-on-spark-1")

执行上述命令后，请等待一段时间，直到得到**成功**的消息。

![hive-and-yarn-practicals-on-spark-2](img/aa56d0fc889ec1e54dc26775dad20fae.png "hive-and-yarn-practicals-on-spark-2")

浏览 **localhost:8088/cluster** 并点击 Spark 应用程序。

![hive-and-yarn-practicals-on-spark-3](img/7483e1804a220c378f383ddd1f3fd9c3.png "hive-and-yarn-practicals-on-spark-3")

点击**日志**。

![hive-and-yarn-practicals-on-spark-4](img/71c686ac07b92fd6a4826686d4039312.png "hive-and-yarn-practicals-on-spark-4")

点击 **stdout** 检查输出。

![hive-and-yarn-practicals-on-spark-5](img/0abc3715ca846b65a45fe14b23eb9f9f.png "hive-and-yarn-practicals-on-spark-5")

![hive-and-yarn-practicals-on-spark-6](img/99f0a805e4caac470955179feea64839.png "hive-and-yarn-practicals-on-spark-6")

要在客户端模式下在 Spark 上部署纱线，只需将**–deploy-mode**设为**“客户端”。**现在，你知道如何在 Spark 上建造蜂巢和纱线了。我们也对他们进行了实践。

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子**

[阿帕奇火花点亮大数据世界](https://www.edureka.co/blog/apache-spark-lighting-up-the-big-data-world1/ "Apache Spark Lighting up the Big Data World")

[Apache 与 Hadoop 的火花——为什么重要？](https://www.edureka.co/blog/apache-spark-with-hadoop-why-it-matters/ "Apache Spark with Hadoop-Why it matters")

[蜂巢&纱线被火花充电](https://www.edureka.co/blog/yarn-hive-get-electrified-by-spark/ "Hive and Yarn get Electrified by Spark")

[开始你在 Apache Spark 的训练&Scala Today](https://www.edureka.co/apache-spark-scala-training "Apache Spark & Scala Training")