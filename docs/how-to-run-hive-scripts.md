# 如何运行 Hive 脚本？

> 原文：<https://www.edureka.co/blog/how-to-run-hive-scripts/>

作为建立在 Hadoop 之上的数据仓库包，Apache Hive 越来越多地用于数据分析、数据挖掘和预测建模。组织正在寻找牢牢掌握 ***[蜂巢& Hadoop 技能](https://www.edureka.co/big-data-and-hadoop)*** 的专业人士。在这篇文章中，让我们看看如何运行 Hive 脚本。一般来说，我们使用脚本一次执行一组语句。Hive 脚本的使用方式非常相似。这将减少我们手动编写和执行每个命令的时间和精力。

Hive 0.10.0 及以上版本支持 Hive 脚本。由于配置单元 0.90 版本安装在 CDH3 中，我们无法在 CDH3 中运行配置单元脚本。您可以在 CDH4 中尝试以下步骤，因为其中安装了 Hive 0.10.0 版本。你知道如何创建一个配置单元脚本吗？如果没有，点击 [此处](https://www.edureka.co/blog/apache-hadoop-hive-script/) 获得更多澄清。

[![Master-Hive-Now](img/20750f70adc0bfff222ebd7e90ec857b.png)](https://www.edureka.co/big-data-and-hadoop)

现在，让我们看看如何在 Hive 中编写脚本并在 CDH4 中运行它们:

## **第一步:编写 Hive 脚本。**

要编写配置单元脚本，文件应该与一起保存。sql 扩展。在 Cloudera CDH4 发行版中打开一个终端，给出以下命令来创建一个 Hive 脚本。命令: sudo gedit sample.sql

[![Writing a Hive script.](img/9864623b3e442314fbc0fce1777a1084.png "Writing a Hive script.")](https://cdn.edureka.co/blog/wp-content/uploads/2014/01/01-1.png)

在执行上述命令时，它将打开包含需要执行的所有 Hive 命令列表的文件。

在这个脚本中，将创建和描述一个表，并从表中加载和检索数据。

**1。在配置单元中创建表:**

*命令:*创建表产品(productid: int，productname: string，price: float，category: string)行格式分隔字段，以'，'结尾；

这里，product 是表名，{ productid，productname，price，category}是该表的列。

以'，'结尾的字段表示输入文件中的列由符号'，'分隔。

默认情况下，输入文件中的记录由新行分隔。

**2。描述表格:**

*命令:*描述产品；

#### **3。将数据加载到表中。**

要将数据加载到表中，首先我们需要创建一个输入文件，其中包含需要插入到表中的记录。

让我们创建一个输入文件。

*命令:* sudo gedit input.txt

[![Loading the Data into the Table.](img/8d01e014f9ac7a429882dbd56d421b4f.png "Loading the Data into the Table.")](https://cdn.edureka.co/blog/wp-content/uploads/2014/01/02-1.png)

编辑文件中的内容，如图所示。

#### [![Loading the Data into the Table.](img/e01bcebec8b99ed2cd8b878ad98203b5.png "Loading the Data into the Table.")](https://cdn.edureka.co/blog/wp-content/uploads/2014/01/03-1.png)

**4。检索数据:**

为了检索数据，使用 select 命令。

*命令:*从产品中选择*；

上面的命令用于检索表中所有列的值。该脚本应该像下图所示。

现在，我们已经完成了 Hive 脚本的编写。现在可以保存文件 sample.sql 了。

#### [![ Retrieving the Data](img/274168548ace6aebc10c1de6a3eaed76.png " Retrieving the Data")](https://cdn.edureka.co/blog/wp-content/uploads/2014/01/04-1.png)

## **第二步:运行蜂巢脚本**

以下是运行配置单元脚本的命令:

*命令:*hive–f/home/cloud era/sample . SQL

[![Running the Hive Script](img/1a86e27d39970bfb9d454319e03c51d6.png "Running the Hive Script")](https://cdn.edureka.co/blog/wp-content/uploads/2014/01/05-1.png)

执行脚本时，请确保脚本文件位置的完整路径存在。

我们可以看到所有命令都成功执行了。

[![Running the Hive Script](img/c283171a174048642a413d554abe7be0.png "Running the Hive Script")](https://cdn.edureka.co/blog/wp-content/uploads/2014/01/06-1.jpg)

这就是在 CDH4 中运行和执行 Hive 脚本的方式。

Hive 是 Hadoop 的关键组件，您在 Hive 方面的专业知识可以让您获得高薪的 Hadoop 工作！Edureka 有专门策划的 Hadoop 课程，帮助你掌握 MapReduce、Yarn、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 等概念。单击下面的按钮开始。

[![Become-a-Hive-Expert](img/667a8fea4556f6582f3c580213776c42.png)](https://www.edureka.co/big-data-and-hadoop)

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[Hadoop 入门](https://www.edureka.co/big-data-and-hadoop)

[蜂巢命令](https://www.edureka.co/blog/hive-commands-with-examples "Hive Commands")

[蜂巢数据模型](https://www.edureka.co/blog/hive-data-models/ "Hive Data Models")

[学习 Hadoop 的 5 个理由](https://www.edureka.co/blog/5-reasons-to-learn-hadoop "5 Reasons to Learn Hadoop")