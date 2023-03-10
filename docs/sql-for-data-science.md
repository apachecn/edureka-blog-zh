# 数据科学的 SQL:初学者的一站式解决方案

> 原文：<https://www.edureka.co/blog/sql-for-data-science/>

自从数据科学被评为这个时代最有前途的工作以来，我们都在努力加入学习数据科学的竞赛。这篇关于 SQL for Data Science 的博客文章将帮助您理解如何使用 SQL 来存储、访问和检索数据以执行数据分析。

以下是本博客将涉及的主题列表:

## **为什么数据科学需要 SQL？**

您知道我们每天生成超过 25 万亿字节的数据吗？这种数据生成的速度是高端技术流行的原因，如[数据科学](https://www.edureka.co/blog/data-science-tutorial/)、[人工智能](https://www.edureka.co/blog/artificial-intelligence-tutorial/)、[机器学习](https://www.edureka.co/blog/machine-learning-tutorial/)等等。

报名参加[数据科学课程](https://www.edureka.co/executive-programs/advanced-program-data-science-course-iitg)，这是 Edureka 的一个研究生项目，旨在提升您的职业生涯。

从数据中获得有用的见解被称为数据科学。数据科学涉及提取、处理和分析大量数据。目前我们需要的是能够用来存储和管理这些海量数据的工具[T2。](https://www.edureka.co/blog/data-science-tools/)

![What Is Data Science - Edureka](img/d1284a5d5590c739debcda6d429a60ad.png)

这就是 SQL 的用武之地。

SQL 可以用来存储、访问和提取海量数据，以便更顺利地进行整个数据科学过程。

看看这个由 Edureka 提供的 [**自然语言处理课程**](https://www.edureka.co/python-natural-language-processing-course) ，让你的人工智能技能更上一层楼。

## **什么是 SQL？**

SQL 表示结构化查询语言，是一种旨在管理关系数据库的查询语言。

但是什么是关系数据库呢？

关系数据库是一组定义明确的表，从这些表中可以访问、编辑、更新数据等等，而不必改变数据库表。SQL 是关系数据库的标准(API)。

回到 SQL，SQL 编程可用于对数据执行多种操作，如查询、插入、更新、删除数据库记录。使用 SQL 的关系数据库的例子包括 MySQL 数据库、Oracle 等。

要了解更多关于 SQL 的信息，你可以浏览下面的博客:

1.  [SQL 命令——SQL 初学者指南](https://www.edureka.co/blog/sql-commands)
2.  [了解 SQL 数据类型——关于 SQL 数据类型您需要知道的一切](https://www.edureka.co/blog/sql-data-types/)
3.  [用 SQL 创建表格——关于用 SQL 创建表格你需要知道的一切](https://www.edureka.co/blog/create-table-in-sql/)
4.  [SQL&NoSQL 数据库之间的差异——MySQL&MongoDB 对比](https://www.edureka.co/blog/sql-vs-nosql-db/)

在开始演示 SQL 之前，让我们先熟悉一下基本的 SQL 命令。

## **SQL 基础知识**

SQL 提供了一组简单的命令来修改数据表，让我们来看看一些基本的 SQL 命令:

*   创建数据库-*创建一个新的数据库*
*   创建表格-*创建一个新表格*
*   插入-*将新数据插入数据库*
*   选择-*从数据库中提取数据*
*   更新—*更新数据库中的数据*
*   删除-*从数据库中删除数据*
*   更改数据库-*修改数据库*
*   修改表格-*修改表格*
*   删除表格-*删除表格*
*   创建索引—*创建一个索引来搜索元素*
*   删除索引-*删除一个索引*

为了更好地理解 SQL，让我们安装 MySQL，看看如何处理数据。

报名参加 Edureka 的  [数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course)，提升您的职业生涯。

## **安装 MySQL**

安装 MySQL 是一项简单的任务。这里有一个[逐步指南](https://www.edureka.co/blog/install-mysql/)，它将帮助你在你的系统上安装 MySQL。

一旦你完成了 MySQL 的安装，按照下面一节的简单演示，它将告诉你如何插入、操作和修改数据。

[https://www.youtube.com/embed/AIV9JprNneo](https://www.youtube.com/embed/AIV9JprNneo)

**用于数据科学的 SQL–MySQL 演示**

在本演示中，我们将了解如何创建和处理数据库。这是一个初级演示，让您开始使用 SQL 进行数据分析。

所以让我们开始吧！

**第一步:创建一个 SQL 数据库**

SQL 数据库是一个存储仓库，数据可以以结构化格式存储在其中。现在让我们使用 MySQL 创建一个数据库:

```

CREATE DATABASE edureka;
USE edureka;

```

在上面的代码中，有两个 SQL 命令:

**注意** : SQL 命令用大写字母定义，分号用于终止 SQL 命令。

1.  创建数据库:该命令创建一个名为“edureka”的数据库

2.  使用:该命令用于激活数据库。在这里，我们正在激活“edureka”数据库。

**第二步:创建一个包含所需数据特征的表格**

创建表就像创建数据库一样简单。您只需用各自的数据类型定义变量或表的特性。让我们来看看如何做到这一点:

```

CREATE TABLE toys (TID INTEGER NOT NULL PRIMARY KEY AUTO_INCREMENT, Item_name TEXT, Price INTEGER, Quantity INTEGER);

```

在上面的代码片段中，发生了以下事情:

1.  使用“创建表格”命令创建一个名为“玩具”的表格。
2.  玩具表包含 4 个特征，即 TID(交易 ID)、项目名称、价格和数量。
3.  每个变量都用各自的数据类型定义。
4.  TID 变量被声明为主键。主键基本上表示可以存储唯一值的变量。

您可以使用以下命令进一步检查已定义表的详细信息:

```

DESCRIBE toys;

```

**![Data Description - SQL For Data Science - Edureka](img/561e31b85891f17ef6e5e44299651648.png)**

**第三步:将数据插入表格**

现在我们已经创建了一个表，让我们用一些值填充它。在这篇博客的前面，我提到了如何通过使用一个命令，即 INSERT INTO，将数据添加到一个表中。

让我们看看这是如何做到的:

```

INSERT INTO toys VALUES (NULL, "Train", 550, 88);
INSERT INTO toys VALUES (NULL, "Hotwheels_car", 350, 80);
INSERT INTO toys VALUES (NULL, "Magic_Pencil", 70, 100);
INSERT INTO toys VALUES (NULL, "Dog_house", 120, 54);
INSERT INTO toys VALUES (NULL, "Skateboard", 700, 42);
INSERT INTO toys VALUES (NULL, "G.I. Joe", 300, 120);

```

在上面的代码片段中，我们简单地使用 INSERT INTO 命令将 6 个观察值插入到“toys”表中。对于每个观察值，在括号中，我指定了创建表时定义的每个变量或特性的值。

TID 变量被设置为空，因为它从 1 开始自动递增。

现在让我们显示表中的所有数据。这可以通过使用以下命令来完成:

```

SELECT * FROM toys;

```

![Insert Data - SQL For Data Science - Edureka.html](img/40b26478636dfa7e33188e9d1e352e68.png) **第四步:修改数据条目**

假设你决定提高特种部队的价格，因为它为你带来了很多顾客。如何更新数据库中变量的价格？

很简单，只需使用下面的命令:

```

UPDATE toys SET Price=350 WHERE TID=6;

```

UPDATE 命令允许您修改表中存储的任何值/变量。SET 参数允许您选择一个特定的特性，WHERE 参数用于标识您想要更改的变量/值。在上面的命令中，我已经更新了 TID 为 6 的数据条目的价格。

现在让我们来查看更新后的表格:

```

SELECT * FROM toys;

```

![Update Data - SQL For Data Science - Edureka](img/7842a7cbc0ed170aa0484f6b16309e32.png)

您还可以通过引用您想要查看的列来修改您想要显示的内容。例如，below 命令将只显示玩具的名称及其各自的价格:

```

SELECT Item_name, Price FROM toys;

```

**![Filter Data - SQL For Data Science - Edureka](img/2c43e0a3ea6afed68b4b22733b3a250f.png)**

**第五步:检索数据**

所以在插入数据并对其进行修改之后，最后是根据业务需求提取和检索数据的时候了。这是可以为进一步的数据分析和数据建模检索数据的地方。

请注意，这是一个让您开始使用 SQL 的简单示例，但是，在真实的场景中，数据要复杂得多，而且规模也大得多。尽管如此，SQL 命令仍然保持不变，这就是 SQL 如此简单易懂的原因。它可以用一组简单的 SQL 命令处理复杂的数据集。

现在让我们通过一些修改来检索数据。参考下面的代码，在不看输出的情况下，试着理解它做了什么:

```

SELECT * FROM toys LIMIT 2;

```

你猜对了！它显示了我的表中出现的前两个观察结果。

![Limit Data - SQL For Data Science - Edureka](img/cea9fb40347df91e2bb2fc1642ccc015.png)

让我们试试更有趣的东西。

```

SELECT * FROM toys ORDER BY Price ASC;

```

![Ascending Order Data - Edureka](img/296780b98625d23e7b2114136cbb5a03.png)

如图所示，这些值按照价格变量的升序排列。如果你想找三个最常买的物品，你会怎么做？

真的很简单！

```

SELECT * FROM toys ORDER BY Quantity DESC LIMIT 3;

```

![Order by descending order - Edureka](img/2fd0a59c97c41e099d71ce3666c65619.png)

让我们再试一次。

```

SELECT * FROM toys WHERE Price > 400 ORDER BY Price ASC;

```

![Price greater than 400 - SQL For Data Science - Edureka](img/30f523a1dc36283e965dafe1d3401689.png) 该查询提取价格超过 400 的玩具的详细信息，并按照价格的升序排列输出。

这就是你使用 SQL 处理数据的方式。既然您已经了解了数据科学的 SQL 基础知识，我相信您一定很想了解更多。这里有几个博客可以帮你入门:

1.  [什么是数据科学？数据科学入门指南](https://www.edureka.co/blog/what-is-data-science/)
2.  [MySQL 教程——学习 MySQL 的入门指南](https://www.edureka.co/blog/mysql-tutorial/)
3.  [SQL 命令——SQL 初学者指南](https://www.edureka.co/blog/sql-commands)
4.  [2019 年你必须准备的前 65 个 SQL 面试问题](https://www.edureka.co/blog/interview-questions/sql-interview-questions)

*如果你希望报名参加人工智能和机器学习的完整课程，Edureka 有一个专门策划的  [**机器学习工程师硕士项目**](https://www.edureka.co/masters-program/machine-learning-engineer-training) ，它将使你精通监督学习、非监督学习和自然语言处理等技术。它包括人工智能&机器学习方面的最新进展和技术方法的培训，如深度学习、图形模型和强化学习。*

此外，Edureka 有一个专门策划的[数据科学培训](https://www.edureka.co/masters-program/data-scientist-certification)，帮助你获得机器学习算法的专业知识，如 K-Means 聚类、决策树、随机森林和朴素贝叶斯。您将学习统计学、时间序列、文本挖掘的概念，以及深度学习的介绍。您将解决媒体、医疗保健、社交媒体、航空和人力资源方面的真实案例研究。本课程的新批次即将开始！！