# RDS AWS 教程:关系数据库服务入门

> 原文：<https://www.edureka.co/blog/rds-aws-tutorial/>

## **RDS AWS 教程**

在今天的 RDS AWS 教程中，我们将详细讨论亚马逊的关系数据库管理服务 RDS AWS，并动手操作，但首先让我们了解它为什么会出现。

世界在不断变化，每一个想法都被转化为应用，每天都有数以百万计的新应用上线。现在，任何应用程序或项目要取得成功，背后都应该有一个独特的想法。

让我们来谈谈你，你刚刚有了一个世界上最惊人的想法，你想围绕它创建一个应用程序。

现在想象一下 10 年前的自己，当应用程序启动并准备就绪时，你必须设置一个后端服务器，研究并安装各种软件来支持你的应用程序，在完成所有这些累人的任务后，你将开始开发你的应用程序。

嘿，等等！*它的保养呢？*你必须为你的后端服务器安装所有最新的安全补丁和更新，并确保它保持健康状态。

现在，当您处理所有这些时，您的应用一夜成名，大量流量流向您的应用，扩展需求成为您的首要任务，现在让我们甚至不要考虑您将在这项任务上进行的投资，您将如何快速完成扩展和配置所有这些额外服务器的任务？

吓人吧？如果我告诉你，有人会为你做所有这些工作，你只需专注于你的应用程序。此外，其成本只是您之前投资的一小部分。

从 [AWS 开发者课程](https://www.edureka.co/aws-developer-certification-training)中了解更多关于 AWS 开发者及其框架的信息。

岂不是很神奇？

好神奇的是，不好意思 **亚马逊** 在这里，亚马逊网络服务(AWS)提供了一种叫做 RDS AWS(关系数据库服务)的服务，它自动为你完成所有这些任务(即设置、操作、更新)。你可以从 [AWS 课程](https://www.edureka.co/aws-certification-training)中学到更多。

您只需选择想要启动的数据库，只需点击一下，您就拥有了一个后端服务器，该服务器将被自动管理！

这里举个例子，假设你开了一家小公司。

你想启动一个由 MySQL 数据库支持的应用程序 由于有大量的数据库工作，开发工作有可能会落后。

![aws example - rds aws tutorial - Edureka](img/dc2b3042b7f109392e7871dd3169c65a.png)

再想象一下这个场景，用亚马逊 RDS，图像不言自明！

这只是一个例子。对于更大的公司，你有一个更大的团队来管理你的数据库服务器；使用 RDS，该团队可以减少到一个相当大的数量，并且可能得到最佳部署！

让我们继续阅读 RDS AWS 教程，看看亚马逊是如何定义他们的服务的:

**亚马逊关系数据库服务(RDS AWS)** 是一种 web 服务，它使得在云中建立、操作和扩展关系数据库变得更加容易。它在行业标准的关系数据库中提供了经济高效、可重新调整大小的容量，并管理常见的数据库管理任务。

因此，当人们将 RDS 与数据库混淆时，往往会产生误解。

*RDS 是**不是**一个数据库*，是一个管理数据库的服务，说了这么多，我们来讨论一下截至目前 RDS 可以管理的数据库:

![amazon-aurora - rds aws tutorial - edureka](img/0ff101cf6045c6ae6d9e3cc3b272e738.png)

它是由 amazon 开发的关系数据库引擎，结合了高端商业数据库的速度和可靠性以及开源数据库的简单性和成本效益。亚马逊声称 Aurora 比 RDS MySQL 快 5 倍。

![mysql-logo - aws rds tutorial - Edureka](img/1249d6bf6510a6a55485f94c974090fe.png)

它是一个开源的数据库管理系统，使用 SQL(结构化查询语言)来访问存储在其系统中的数据。

![postgresql-logo - rds aws tutorial - edureka](img/ec334f476a088480153007700d39a8b1.png)

PostgreSQL 是另一个使用 SQL 访问数据的开源数据库管理系统。

![sql-server - rds aws tutorial - edureka](img/9de54c715c17ce473de95b830eb07964.png)

SQL Server 是一个关系数据库管理系统，由微软在 2005 年为企业环境开发。

![oracle - rds aws tutorial - edureka](img/b8ecab17f65d441f523b628fe69f493f.png)

Oracle 公司开发的对象关系数据库管理系统

![mariadb - rds aws tutorial - edureka](img/cf88f0d7ac682434260f744600b0d19e.png)

MariaDB 是社区开发的 **fork** 的 MySQL DBMS。其分叉的原因是对甲骨文收购 MySQL 的担忧

**叉** 的意思是复制原应用程序的源代码，开始开发新的应用程序。

有趣的是，RDS 支持的数据库引擎是现有的关系数据库，因此，在现有的应用程序中使用 RDS 时，您不必更改应用程序的代码或学习新的查询语言。

现在你可能想知道普通的 MySQL 和由 RDS 管理的 MySQL 有什么区别。

因此，就使用而言，您将像使用自己的数据库一样使用它，但现在，作为开发人员，您将不再担心底层基础设施或数据库的管理。更新、安装 SQL 的系统的健康监控、定期备份等。，所有这些任务将由 RDS AWS 管理。

AWS 还提供 EC2 关系数据库 ami，现在*你可能会问，既然我们已经有了 AWS RDS，为什么还要增加一个关系数据库服务？*

因此，EC2 关系数据库 ami 允许您在 AWS 基础设施上完全管理您自己的关系数据库，而由 RDS 为您管理它们。因此，根据您的使用情况，您可以选择 AWS 服务。希望，你现在清楚了吧！详细的，你甚至可以通过 [AWS 云迁移培训](https://www.edureka.co/migrating-to-aws)了解迁移到 AWS 的细节。

在本 RDS AWS 教程中，我们继续讨论 RDS 的组件。

## **RDS AWS 组件:**

*   数据库实例
*   地区和可用区
*   安全组
*   DB 参数组
*   数据库选项组

我们来详细讨论一下每一个:

**DB 实例**

*   它们是 RDS 的积木。It 是云中的一个隔离的数据库环境，它可以包含多个用户创建的数据库，并且可以使用与独立数据库实例相同的工具和应用程序进行访问。
*   可以使用 AWS 管理控制台、Amazon RDS API 或 AWS 命令行界面创建 DB 实例。
*   数据库实例的计算和内存容量取决于数据库实例类。对于每个数据库实例，您可以选择 5GB 到 6TB 的关联存储容量。
*   数据库实例有以下几种类型:
    *   标准实例(m4，m3)
    *   记忆优化(r3)
    *   微实例(t2)

**地区和可用区**

*   AWS 资源位于高度可用的数据中心，这些数据中心位于世界各地。这个“区域”称为地区。
*   每个区域都有多个可用性区域(AZ ),它们是不同的位置，被设计为与其他 AZ 的故障相隔离。
*   您可以在多个 AZ 中部署您的数据库实例，这确保了故障转移，即在一个 AZ 关闭的情况下，还有第二个 AZ 可以切换到。故障转移实例称为备用实例，原始实例称为主实例。

**安全组**

*   安全组控制对数据库实例的访问。它通过指定一个 IP 地址范围或您希望授予访问权限的 EC2 实例来实现这一点。
*   Amazon RDS 使用 3 种类型的安全组:

*   VPC 安全集团
    *   它控制 VPC 内部的数据库实例。
*   EC2 安全组
    *   它控制对 EC2 实例的访问，并且可以与 DB 实例一起使用。
*   数据库安全组
    *   它控制不在 VPC 中的数据库实例。

**DB 参数组**

*   它包含可应用于同一实例类型的一个或多个数据库实例的引擎配置值。
*   如果您没有将数据库参数组应用到您的实例，您将被分配一个具有默认值的默认参数组。

**DB 选项组**

*   一些数据库引擎提供了简化数据库管理的工具。
*   RDS 通过使用选项组使这些工具可用。

**查看我们在顶级城市的 AWS 认证培训**

| 印度 | 美国 | 其他国家 |
| [在海德拉巴的 AWS 培训](https://www.edureka.co/aws-certification-training-hyderabad) | [亚特兰大 AWS 培训](https://www.edureka.co/aws-certification-training-atlanta) | [AWS 伦敦培训](https://www.edureka.co/aws-certification-training-london) |
| [班加罗尔的 AWS 培训](https://www.edureka.co/aws-certification-training-bangalore) | [波士顿 AWS 培训](https://www.edureka.co/aws-certification-training-boston) | [阿德莱德的 AWS 培训](https://www.edureka.co/aws-certification-training-adelaide) |
| [钦奈的 AWS 培训](https://www.edureka.co/aws-certification-training-chennai) | [纽约市的 AWS 培训](https://www.edureka.co/aws-certification-training-new-york-city) | [新加坡 AWS 培训](https://www.edureka.co/aws-certification-training-singapore) |

**RDS AWS 优势**

让我们来谈谈您在使用 RDS AWS 时获得的一些有趣优势，

*   因此，当您谈论数据库服务时，通常会将 CPU、内存、存储和 IOs 捆绑在一起，也就是说，您无法单独控制它们，但有了 AWS RDS，这些参数中的每一个都可以单独调整。
*   就像我们之前讨论的那样，它可以管理您的服务器，将它们更新到最新的软件配置，进行备份，一切都是自动进行的。
*   备份有两种方式
    *   自动备份，您可以在其中设置完成备份的时间。
    *   数据库快照，在中，您可以手动备份数据库，您可以根据需要随时拍摄快照。
*   它自动为故障转移创建一个辅助实例，因此提供了高可用性。
*   RDS AWS 支持读取副本，即从源数据库创建快照，所有到源数据库的读取流量在读取副本之间分配，这降低了源数据库的总体开销。
*   RDS AWS 可以与 IAM 集成，为使用该数据库的用户提供定制的访问权限。

RDS AWS 中对数据库的更新应用于 **维护窗口** 。这个维护窗口是在创建数据库实例的过程中定义的，它的工作方式如下:

*   当您的数据库有更新时，您会在 RDS 控制台中收到通知，您可以采取以下措施之一
    *   延期维修项目。
    *   立即应用维护项目。
    *   为那些维护项目安排一个时间。
*   一旦维护开始，您的实例必须离线更新，如果您的实例在多 AZ 中运行，在这种情况下，首先更新备用实例，然后将其提升为主实例，然后主实例离线更新，这样您的应用程序就不会停机。
*   如果您想要扩展您的数据库实例，对您的数据库实例所做的更改也发生在维护窗口期间，您也可以立即应用它们，但是如果您的应用程序处于单个 AZ 中，那么您的应用程序将会经历停机。

![aws conclusion - rds aws tutorial - Edureka](img/da31f5b4ecb2b6f7869f04684eb00d22.png)

图 RDS AWS 优势

## **定价**

RDS AWS 基于以下参数计费:

*   **实例类** 即你正在选择的实例类型。
*   **运行时间** 即一个实例运行的时间量，不足的小时按完整的小时计费。

*   **存储，即您为数据库实例调配的存储量**

*   每月的 I/O 请求，即每月对数据库实例的 I/O 请求

*   **数据传输** : 数据传输进出您的数据库实例。

另一种为 AWS RDS 付费的方式是预订一些实例。

**保留实例** 也是使用 AWS RDS 的一种方式，在这种情况下，您可以在一段时间内保留一个 RDS 实例，这可以是一年或三年，通过一次性付款，与每月支付的账单相比，这是一种更便宜的方式。

### **自由层**

AWS 的大多数服务都有惊人的免费层使用，因此客户可以先使用服务，然后再做必要的事情。

同样，它为 RDS AWS 提供免费的层使用，包括以下优势:

*   从注册之日起，每月为 db.t2.micro 实例在单 AZ 中使用亚马逊 RDS 750 小时。
*   20 GB 数据库存储:通用(SSD)或磁性存储的任意组合。
*   1000 万次 IOs
*   20GB 的备份存储

足够的理论，让我们使这个 RDS AWS 教程更有趣，*让我们现在在 RDS* 中启动一个 MySQL DB。

## **动手**

**第一步:**首先从 AWS 管理控制台选择 RDS 服务。

![select service - rds aws tutorial - edureka](img/b9378002234e59dfaa6001c64fb3bbfc.png)

**步骤 2:** 因为我们将启动一个 MySQL 实例，所以从数据库列表中选择 MySQL 实例。在本 RDS AWS 教程中，让我们转到步骤 3。

![select db - rds aws tutorial - edureka](img/1d9af752348c738b9d0f520f72f141f6.png)

**第 3 步:**由于我们是出于演示目的创建这个实例，我们将选择开发/测试选项，然后单击下一步。

![select dev - rds aws tutorial - edureka](img/5c9c104c727a7ff39af92b4fb553c329.png)

**第 4 步:**在下一页，您将填写以下详细信息:

*   您可以在这里选择您想要的数据库实例
*   您可以选择是否要在 MySQL 数据库中启用多 AZ。
*   您可以选择要分配给数据库实例的空间大小，可以从 5GB 到 6TB 不等。
*   最后，您将为您的数据库实例设置用户名和密码

![detail fill - rds aws tutorial - edureka](img/9503a0ef9ec64ba2700ddfa81837124a.png)

**第 5 步:**在下一步中，您将为您的数据库配置高级设置

*   您将在此选择 VPC，如果您不希望在 VPC 中启动实例，您可以保留默认设置并继续。
*   在下一部分，您可以选择想要使用的数据库版本，在我们的示例中，我们使用的是 MySQL 5.6
*   在下一部分，您可以设置备份首选项，如保留期等。
*   之后，我们将设置维护窗口，这是您的数据库实例将被更新的时间段。
*   一旦您填写了所有的细节，您就可以启动数据库实例了！

![launch db - rds aws tutorial - edureka](img/a773f72b4fc164048297aadf75ec1bb1.png)

**恭喜恭喜！**您已经成功启动了您的第一个 RDS 数据库实例！

我们 Edureka 在这里为您成为 AWS 解决方案架构师的每一步提供帮助，因此除了本 RDS AWS 教程之外，我们还提供了一个课程，涵盖了您通过解决方案架构师考试所需的所有内容！

我希望你喜欢这个 RDS AWS 教程。您在 RDS AWS 教程博客中学习的主题是招聘人员在 AWS 解决方案架构师专业人员中最需要的技能。以下是 AWS 面试问题的收集，帮助你准备下一次 AWS 工作面试。你可能还想阅读一些关于 AWS 服务的有趣的教程博客，即 [S3 博客](https://www.edureka.co/blog/s3-aws-amazon-simple-storage-service/)、 [EC2 博客](https://www.edureka.co/blog/ec2-aws-tutorial-elastic-compute-cloud/)、 [Lambda 博客](https://www.edureka.co/blog/aws-lambda-tutorial)。

*有问题吗？请在本 RDS AWS 教程的评论部分提到它，我们将会回复您。*