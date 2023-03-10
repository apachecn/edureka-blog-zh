# 亚马逊雅典娜是什么？–全新的无服务器数据分析工具

> 原文：<https://www.edureka.co/blog/amazon-athena-tutorial>

数据分析是一个非常复杂的过程，人们一直试图简化它。有许多分析工具，甚至流行的科技巨头亚马逊也提供名为*亚马逊雅典娜*的 AWS 服务。这篇 Amazon Athena 教程将指导你了解 Amazon Athena 的基础和高级用法。

Amazon Athena 是一款交互式数据分析工具，用于在相对较短的时间内处理复杂的查询。它是无服务器的，因此没有设置的麻烦，也不需要管理基础架构。这不是一个数据库服务，因此，你只需为你运行的查询付费。您只需将您的数据指向 S3，定义所需的模式，使用标准 SQL 就可以了。通过 [AWS 培训](https://www.edureka.co/aws-certification-training)了解亚马逊网络服务。

本文涉及的话题如下:

*   [亚马逊雅典娜](#AmazonAthena)简介
*   [微软 SQL Server 与亚马逊雅典娜的区别](#DifferenceBetweenMySqlAndAmazonAthena)
*   [利用亚马逊的](#UseofAthena)
*   [访问亚马逊](#AccessAthena)
*   [雅典娜的特征](#FeaturesOfAthena)
*   [Demo–I(在雅典娜创建表格)](#CreatingTableInAthena)
*   [Demo–II(MySQL 与雅典娜的对比)](#ComparisionBetweenMySQLAndAthena)

## **亚马逊雅典娜**简介

2016 年 11 月 20 日，亚马逊推出雅典娜作为其服务之一。如前所述，Amazon Athena 是一种无服务器查询服务，使用标准 SQL 简化了存储在亚马逊 S3 的数据分析。只需在 [AWS 管理控制台](https://www.edureka.co/blog/what-is-aws/)点击几下，客户就可以将 Amazon Athena 指向他们存储在亚马逊 S3 的数据，并使用标准 SQL 运行查询，在几秒钟内获得结果。

使用 Amazon Athena，不需要设置或管理基础设施，客户只需为他们运行的查询付费。Amazon Athena 自动扩展，并行执行查询，即使是大型数据集和复杂的查询，也能快速给出结果。现在，你知道什么是 Amazon Athena 了，让我带你了解一下它与 SQL Server 的区别。

## **微软 SQL Server 与亚马逊雅典娜**的区别

| **特征** | 

### 微软 SQL Server

 | 

### **Amazon Athena** T3]

 |
| 

### 定义

 | 微软 SQL Server 是一个数据库管理和分析系统。 | Amazon Athena 是一种交互式查询服务，可以简化数据分析。 |
| 

### 用法

 | 用于对数据库进行 DML、DCL、DDL 和 TCL 操作。 | 用于对数据库进行 DML 操作。 |
| 

### 好处

 | 1\. Reliable and easy to use.2。高性能。3。易于维护。4。轻松安装服务器。5。多种工具集成成为可能。 | 1\. Easy to use.2。高性能。3。无需维护。4。不需要服务器配置。5。多种工具集成成为可能。 |
| **整合** | 1\. Sequlize2。SQLDep3。转眼间 | 1\. Amazon S32。AWS 胶水3。转眼间 |
| **局限性** | 1\. Limited RDS storage.2。有限的实例。3。无法处理递归。 | 1\. No DDL’s supported. 2。仅适用于外部表格。3。不支持用户定义的函数。 |

## *MySQL vs 亚马逊雅典娜*

## **利用亚马逊的**

如果你是一名数据分析师，并且有分析存储在 S3 上的数据的经验，你会与此相关，

数据分析师/开发者:你们提供存储吗？ AWS:是的。数据分析师/开发人员:你们有分析工具吗？ AWS:不确定。

亚马逊致力于此，开发出了*亚马逊雅典娜*。现在，您有了一个处理数据的工具。 Athena 帮助你分析存储在亚马逊 S3 的非结构化、半结构化和结构化数据。使用 Athena，您可以为数据集创建动态查询。Athena 还与 AWS Glue 一起工作，为您提供一种在 S3 中存储元数据的更好方法。

使用 AWS CloudFormation 和 Athena，可以使用命名查询。命名查询允许您命名查询，然后使用名称调用它。

数据科学家和开发人员可以使用 AWS 提供的这种交互式服务来偷偷查看表格，而不是运行完整的查询。它还用于从 S3 获取数据，使用雅典娜 JDBC 驱动程序将其加载到不同的数据存储，用于日志存储/分析和数据仓库事件。

现在你知道了 Athena 是一个有趣的工具，让我们在亚马逊 Athena 教程中了解一下如何使用亚马逊的这项神奇服务。

## **访问亚马逊雅典娜**

访问 Athena 非常简单，可以通过以下方式完成:

*   [AWS 控制台](https://console.aws.amazon.com/athena/)
*   [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/athena/)
*   [雅典娜与你的](https://docs.aws.amazon.com/athena/latest/ug/connect-with-jdbc.html)

这些是访问亚马逊雅典娜的几种方式。到目前为止，您已经非常了解 Amazon Athena 的所有重要内容。让我带你了解一下雅典娜的不同特征。

## **雅典娜**的特征

在亚马逊提供的众多服务中，雅典娜是其中之一。它有许多适合数据分析的特性。下面就让我们来逐一看看不同的特性。

1.  **易实现**:雅典娜不需要安装。它可以从 AWS 控制台直接访问，也可以通过 AWS CLI 直接访问。
2.  **无服务器**:它是无服务器的，因此最终用户不需要担心基础设施、配置、扩展或故障。雅典娜独自处理一切。
3.  **按查询付费** : Athena 只对你运行的查询收费，即每次查询管理的数据量。如果您能够压缩它们并相应地格式化您的数据集，您可以节省很多。
4.  **快速** : Athena 是一个非常快速的分析工具。它可以在更短的时间内执行复杂的查询，方法是将复杂的查询分解成更简单的查询并并行运行，然后将结果组合起来以给出所需的输出。
5.  **安全**:借助 IAM 策略和 AWS 身份，Athena 让您完全控制数据集。由于数据存储在 S3 存储桶中，IAM 策略可以帮助您管理对用户的控制。
6.  **高可用**:在 AWS 的保证下，Athena 具有高可用性，用户可以全天候执行查询。就像 AWS 是 99.999%可用一样，Athena 也是。
7.  **集成**:雅典娜最大的特点就是可以用 AWS 胶水集成。AWS Glue 将帮助用户创建一个更好的统一数据存储库。这有助于您创建更好的数据版本、更好的表、视图等。

很棒吧？Athena 同时提供了很多功能，性价比很高。

到现在为止，你一定对 AWS Athena 印象深刻。既然你对雅典娜了解很多。让我们卷起袖子，通过一个小演示来了解 Athena 的工作原理。在这个亚马逊雅典娜教程中，我们将进行两个演示，让我们看看他们是什么。

## **演示–I(在雅典娜创建表格)**

正如你对 Amazon Athena 的了解，让我们来看看如何查询你的数据存储为。亚马逊 S3 使用雅典娜的 json 文件。

1.  创建多个包含条目的 JSON 文件
2.  将文件存储到 [S3 斗](https://www.edureka.co/blog/s3-aws-amazon-simple-storage-service/)
3.  为保存在 S3 的文件创建一个外部表
4.  编写用于访问数据的查询

下面我们来逐一了解一下如何做好上述任务。

1.  创建 JSON 文件。(不使用换行符创建数据)![JSON File- Amazon Athena Tutorial ](img/84b0c474e42c61c037fd8938611a4333.png)*JSON**File-亚马逊雅典娜教程*
2.  我们将使用 AWS CLI 访问 S3 存储桶
    1.  配置 IAM 用户![Configure IAM User - Amazon Athena Tutorial-Edureka](img/83faaa1683cd6f65f55c3be0fa2f848b.png) 
    2.  创造 S3![Create S3 Bucket- Amazon Athena Tutorial- Edureka](img/8faeddf7016b341340108330527c7fc2.png)
    3.  复制文件到 S3![Copy Json File To S3- Amazon Athena Tutorial- Edureka](img/ebe17b89c3f53c2b285ab0595a8938a6.png)
3.  在雅典娜中创建外部表格。有两种方法可以做到这一点:
    1.  使用 AWS 胶水爬虫
    2.  手动
4.  我们将手动创建:
    1.  创建表格。*![Create External Table1-Amazon Athena Tutorial- Edureka](img/4a9c8991cd625814b11fc1507d2805d5.png)**亚马逊雅典娜控制台 * 
    2.  如果没有数据库，创建一个新的。给一个表名。给出你的文件的位置。![Creating external table2-Amazon Athena Tutorial- Edureka](img/06ccf897dc64afa466fb80ec1d3d24c2.png)*亚马逊雅典娜控制台 * 
    3.  选择您将使用的文件类型。S 选择你文件中数据的架构。![Creating external table4-Amazon Athena Tutorial- Edureka](img/177f7e595cff1dbd69aab2192d115a7f.png)*亚马逊雅典娜控制台*
    4.  由于输入的数据没有那么复杂，我们不需要分区。点击“创建表格”。![Creating external table5-Amazon Athena Tutorial- Edureka](img/89dd870bb4eeab35ca0cbae4b9a2a3ff.png)*亚马逊雅典娜控制台——亚马逊雅典娜教程*
    5.  Athena 会自动生成创建外部表的查询并运行。![Creating external table6-Amazon Athena Tutorial- Edureka](img/aefcec2b57f913e0fc3f58c33e7aa7ef.png)*亚马逊雅典娜控制台*你已经准备好了你的外部表。
5.  我们编写一个查询来从表中选择所有数据。
    1.  **select * from**testdb**；**
    2.  点击 Run Query，你就有了表中的所有信息。![Running Query- Amazon Athena Tutorial- Edureka](img/441d5646cf697dca59c9538c0581c8b3.png)*亚马逊雅典娜教程* 

## **Demo–II(亚马逊雅典娜与 MySQL 对比)**

在这篇 Amazon Athena 教程中，我们将比较 MySQL 和 Athena，了解在 Athena 中，即使是简单的查询也能花费更少的时间。

1.  将 CSV 文件加载到 MySQL 需要大约 1 个小时，但在 Athena 中，将 CSV 文件上传到 S3 只需 3 分钟，创建一个表格只需 0.42 秒。【T2
2.  选择查询。select * from table。![Athena Select query-AmazonAthena Tutorial-Edureka](img/2f47bcfec3009b8097106247d71bd126.png)在 Athena 中选择查询。![Mysql Select Query-AmazonAthena Tutorial-Edureka](img/daa3dd6bac02d681c82df2a9038fb6d3.png)在 MySQL 中选择查询。
3.  从表格中选择特定的列。![SelectQuery-AmazonAthena Tutorial-Edureka](img/652dca95e2ab651db26cde55b1623f82.png)在雅典娜![SelectQueryMySql-AmazonAthena Tutorial-Edureka](img/761eede25d9e733e9859f3fdcbfec2bd.png)中选择特定的列在 MySQL 中选择特定的列。
4.  获取特定列的计数。![CountQueryAthena-AmazonAthena Tutorial-Edureka](img/2e4f05e728b7f6c2d39b1a002f722436.png)Athena 中特定列的计数。![CountQueryMysql-AmazonAthena Tutorial-Edureka](img/9a62dbe6396cc250e7b9409b51f39a5a.png)MySQL 中特定列的计数。
5.  统计表中的记录数。![CountQueryAthena-AmazonAthena Tutorial-Edureka](img/fa0599fffcbfddfe55a19e97ff2d79d9.png)统计雅典娜中的所有记录。![CountQueryMySql-AmazonAthena Tutorial-Edureka](img/9cf24df09d4aed40754efd4cd91595ed.png)C统计 MySQL 中的所有记录。 
6.  选择指定范围的查询。![SelectQueryAthena-AmazonAthena Tutorial-Edureka](img/4d0da4aaa9ba2342c1d7560019c72e2e.png)在 Athena 中选择所述范围内的查询。![SelectQueryMysql-AmazonAthena Tutorial-Edureka](img/9edb30541484d3f3f4433f50abf0befa.png)S在 MySQL 中选择所述范围内的查询。

以上是 MySql 和 Amazon Athena 之间基本 SQL 命令的简单比较。

我希望这篇博客是信息丰富的，有助于获得一个关于 AWS 雅典娜的想法。[选择 AWS 职业](https://www.edureka.co/blog/10-reasons-to-learn-aws/)并获得 AWS 认证，这将促进你的职业生涯。看看正在革新业务的[不同用例。万事如意！](https://www.edureka.co/blog/top-6-aws-cloud-use-cases/)

*如果您希望了解更多有关 AWS 和 Athena 等令人惊叹的服务的信息，请查看我们在阿格拉的 [AWS 培训，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 AWS 提供的不同服务，并帮助您掌握该主题。](https://www.edureka.co/aws-certification-training-agra)*