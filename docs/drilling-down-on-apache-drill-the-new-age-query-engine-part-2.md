# 深入研究 Apache Drill，新时代的查询引擎(第 2 部分)

> 原文：<https://www.edureka.co/blog/drilling-down-on-apache-drill-the-new-age-query-engine-part-2>

在第二篇 Apache Drill 博文中，我们将了解如何将 Hive 和 HBase 与 Apache Drill 集成。Apache Drill 为 Hive 和 HBase 集成提供了内置的存储插件。我们只需要编辑这些存储插件的配置并连接 Drill。

点击 查看该系列的第一篇阿帕奇训练博客 [。](https://www.edureka.co/blog/drilling-down-on-apache-drill-the-new-age-query-engine)

首先，让我们看看如何连接 Apache Drill 和 Hive 存储插件。

在下面的快照中，您可以看到我有一个包含一些数据的表 customer。现在，我们将连接 Hive 和 Drill，并从 Drill 访问同一个表。

![table-Apache-Drill](img/b6c8a333cc159a379622970b983a99ca.png)

启动钻头服务

**命令:**。/bin/Drillbit.sh 开始

![command-Apache-Drill](img/303138794877fd348f7d09f106885cb5.png)

开始钻壳

**命令:**钻取-确认

![drill-conf-apache-drill](img/a09dfc7aab8767410f8cb7781fff1897.png)

接下来，在浏览器中打开钻取 UI**localhost:8047**

您将在禁用的存储插件中看到 Hive。单击配置单元的更新。

![plugins-apache-drill](img/753ea30ddb5c6c6c8d382d41a3dc0809.png)

根据 hive-site.xml 中提供的现有配置单元设置编辑配置

编辑后，点击启用。

![configuration-apache-drill](img/1e53436135a0510763321eb68c85fa37.png)

你现在可以在已启用的存储插件中找到 Hive now。

![hive-apache-drill](img/4698404f6f932b8aa4075792966a4d0d.png)

在 Drill shell 中运行下面的命令，从 Drill 访问配置单元。

**命令:**使用蜂巢；

![use-hive-apache-drill](img/e2facbfab0eaf934fb1b4ffb81a96030.png)

现在，您可以从 Drill 中访问 customer 表。您已经成功地将 Hive 与 Drill 集成在一起。

**命令:**从客户中选择*；

![command-1-apache-drill](img/eeb97d13f5c220dae50f3f8a8e653a91.png)

接下来，要启用 HBase 存储插件，我们将遵循与 Hive 相同的步骤。单击 HBase 的更新，并相应地编辑配置。

![storage-plugin-apache-drill](img/5dbf99f6eb660b7e2acbee4e0813855c.png)

编辑配置后，单击启用:

![complete-configuration-apache-drill](img/4174b293a23b713f1d3c592f8983db71.png)

现在，我的 HBase 中有一个“学生”表，其中有一些数据。让我们看看现在是否能通过钻探接近它。

![Hbase-apache-drill](img/9281fe21099699ebbea2f77323459bca.png)

在 Drill 中运行以下命令以使用 HBase 存储插件。

**命令:**使用 HBase

![use-hbase-apache-drill](img/7c6394cc952635840d08f0fd3a837356.png)

运行对 HBase student 表的查询。

**命令:**从学生中选择*；

![command-2-apache-drill](img/fa15de94cc1bb2f1843fc61a60cfd1bb.png)

上述查询返回了不可用的结果。下一步，我们必须将数据从字节数组转换成有意义的 UTF8 类型。

发出以下包含 CONVERT_FROM 函数的查询，将 students 表转换为类型化数据:

**命令:**选择 CONVERT_FROM(row_key，' UTF8 ')作为 studentid，

CONVERT _ FROM(students . account . name，' UTF8 ')作为名称，

CONVERT _ FROM(students . address . state，' UTF8 ')作为州，

CONVERT _ FROM(students . address . street，' UTF8 ')作为街道，

将 _FROM(students.address.zipcode，' UTF8 ')转换为 zipcode

来自学生；

![command-3-apache-drill](img/e62fd672e2953fd2dad920e166cac529.png)

现在，您可以通过 Apache Drill 成功访问 HBase。

有问题要问我们吗？在评论区提到它们，我们会回复你。

**相关帖子:**

[Apache Spark 和 Scala](https://www.edureka.co/apache-spark-scala-training "Get started with Apache Spark and Scala")T3【入门】

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop "Get started with Big Data & Hadoop")

[下钻 Apache Drill，新时代查询引擎第 1 部分](https://www.edureka.co/blog/drilling-down-on-apache-drill-the-new-age-query-engine)