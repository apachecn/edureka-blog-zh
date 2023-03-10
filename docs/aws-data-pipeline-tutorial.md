# AWS 数据管道教程-数据工作流程编排服务

> 原文：<https://www.edureka.co/blog/aws-data-pipeline-tutorial/>

**AWS 数据管道教程**

随着技术的进步&连接的便利，生成的数据量正在飞速增长。在这座数据之山的深处埋藏着“被控制的情报”，公司可以用它来扩展和改善他们的业务。公司需要移动、排序、过滤、重新格式化、分析和报告数据，以便从中获取价值。为了在市场中保持稳定，他们可能不得不重复并快速地这样做。亚马逊的 AWS 数据管道服务是完美的解决方案。要了解更多关于亚马逊网络服务的信息，你可以参考 [AWS 在线培训](https://www.edureka.co/aws-certification-training)。

让我们来看看这篇 AWS 数据管道教程所涉及的主题:

## **需要 AWS 数据管道**

数据呈指数级增长，而且还在以更快的速度增长。各种规模的公司都意识到，管理、处理、存储&和迁移数据变得比过去更加复杂&耗时。因此，下面列出了公司面对不断增长的数据所面临的一些问题:

**![data - AWS Data Pipeline - Edureka](img/4523e7bf1588e085fb574d60ba0836da.png)批量数据量:**有很多原始的&未处理的数据。还有日志文件、人口统计数据、从传感器收集的数据、交易历史&等等。

**![data - AWS Data Pipeline - Edureka](img/9ebfc675c31d3fff82635a3486e510b7.png)多种格式:**数据有多种格式。将非结构化数据转换成兼容的格式是一项复杂而耗时的任务。

**![data - AWS Data Pipeline - Edureka](img/0a63b97a69e8b37442036a986fa3ed39.png)不同的数据存储:**有多种数据存储选项。公司有自己的数据仓库，基于云的存储，如亚马逊 S3、[亚马逊关系数据库服务](https://www.edureka.co/blog/rds-aws-tutorial/) (RDS) &运行在 [EC2 实例](https://www.edureka.co/blog/ec2-aws-tutorial-elastic-compute-cloud/)上的数据库服务器。

**![data - AWS Data Pipeline - Edureka](img/facb93a1f0f5fa6c4c06f0a5fa7e96f9.png)耗时&成本高:**管理大量数据耗时&成本非常高。大量资金将用于转换、存储&流程数据。

所有这些因素都使公司自行管理数据变得更加复杂和具有挑战性。这就是 **AWS 数据管道** 可以派上用场的地方。它使用户更容易集成分布在多个 AWS 服务中的数据，并从一个位置对其进行分析。因此，通过这个 AWS 数据管道教程，让我们探索数据管道及其组件。

## AWS 数据管道教程| AWS 初学者教程| AWS 认证培训| Edureka



[https://www.youtube.com/embed/5eq6fiw1dPA?rel=0&showinfo=0](https://www.youtube.com/embed/5eq6fiw1dPA?rel=0&showinfo=0)This “AWS Data Pipeline Tutorial” video by Edureka will help you understand how to process, store & analyze data with ease from the same location using AWS Data Pipeline.

## **什么是 AWS 数据管道？**

***![datapipelinelogo - AWS Data Pipeline Tutorial- Edureka](img/d77887c7481020abf2dbf022b56fe851.png) AWS 数据管道* ** *是一种 web 服务，帮助您以指定的时间间隔在不同的 AWS 计算和存储服务以及内部数据源之间可靠地处理和移动数据。*

通过 AWS Data Pipeline，您可以轻松地从存储位置访问数据，转换&大规模处理数据，并高效地将结果传输到亚马逊 S3、亚马逊 RDS、亚马逊 DynamoDB 和亚马逊 EMR 等 AWS 服务。它允许您创建容错、可重复和高度可用的复杂数据处理工作负载。

现在为什么选择 AWS 数据管道？

## **AWS 数据管道的好处**

![Benefits - AWS DataPipeline Tutorial- Edureka](img/cb9a70563a76aacf50b229d0b067e9f0.png)



好了，谈完好处之后，让我们来看看 AWS 数据管道的不同组件&它们如何协同工作来管理您的数据。

想让你的‘云’知识更上一层楼？ [<button>今天获得云认证！</button>](https://www.edureka.co/masters-program/cloud-architect-training)

**查看我们在顶级城市的 AWS 认证培训**

| 印度 | 美国 | 其他国家 |
| [在海德拉巴的 AWS 培训](https://www.edureka.co/aws-certification-training-hyderabad) | [亚特兰大 AWS 培训](https://www.edureka.co/aws-certification-training-atlanta) | [AWS 伦敦培训](https://www.edureka.co/aws-certification-training-london) |
| [班加罗尔的 AWS 培训](https://www.edureka.co/aws-certification-training-bangalore) | [波士顿 AWS 培训](https://www.edureka.co/aws-certification-training-boston) | [阿德莱德的 AWS 培训](https://www.edureka.co/aws-certification-training-adelaide) |
| [钦奈的 AWS 培训](https://www.edureka.co/aws-certification-training-chennai) | [纽约市的 AWS 培训](https://www.edureka.co/aws-certification-training-new-york-city) | [新加坡 AWS 培训](https://www.edureka.co/aws-certification-training-singapore) |

## **AWS 数据管道的组件**

AWS 数据管道是一个 web 服务，您可以使用它来自动移动和转换数据。您可以定义数据驱动的工作流，以便任务可以依赖于先前任务的成功完成。您定义数据转换的参数，AWS 数据管道执行您设置的逻辑。

![datapipeline - AWS Data Pipeline Tutorial - Edureka](img/4f0326e6942611818e65fc0a7c298fc0.png)

Fig 1: AWS Data Pipeline – AWS Data Pipeline Tutorial – Edureka



基本上，你总是通过选择 ***数据节点**来开始设计管道。*然后数据管道与计算服务一起工作来转换数据。大多数情况下，这个步骤会产生大量额外数据。因此，可选地，您可以拥有输出数据节点，其中可以存储转换数据的结果。

**数据节点**:在 AWS 数据管道中，数据节点定义了管道活动用作输入或输出的数据的位置和类型。它支持如下数据节点:

*   DynamoDBDataNode
*   SqlDataNode
*   红移数据节点
*   S3 数据节点

### 现在，让我们考虑一个实时示例来了解其他组件。

用例:从不同的数据源收集数据，执行 Amazon Elastic MapReduce(EMR)分析&生成每周报告。

![pipeline - AWS Data Pipeline - Edureka](img/25d91fbb8ac11ef129dacafdf89e3b5c.png)

在这个用例中，我们设计了一个管道来*从像亚马逊 S3 & DynamoDB 这样的数据源*提取数据到*每天执行 EMR 分析* & *生成每周数据报告*。

现在我斜体的字叫做 ***活动**。*可选地，为了运行这些活动，我们可以添加 ***前置条件**。*

**活动:**活动是一个管道组件，它使用计算*资源*以及典型的输入和输出数据节点来定义要按计划执行的工作。活动示例有:

*   将数据从一个位置移动到另一个位置
*   运行配置单元查询
*   生成亚马逊 EMR 报告

**前提条件:**前提条件是包含条件语句的管道组件，在活动可以运行之前，这些条件语句必须为真。

*   在管道活动试图复制源数据之前，检查源数据是否存在
*   是否存在各自的数据库表

**资源:**资源是执行管道活动指定的工作的计算资源。

*   执行由管道活动定义的工作的 EC2 实例
*   一个 Amazon EMR 集群，执行由管道活动定义的工作

最后，我们有一个叫做*动作的组件。*

**动作:**动作是管道组件在某些事件发生时采取的步骤，例如成功、失败或延迟活动。

*   根据成功、失败或后期活动向主题发送 SNS 通知
*   触发取消未完成或未完成的活动、资源或数据节点

现在你已经对 AWS 数据管道&的组件有了基本的了解，让我们看看它是如何工作的。

你甚至可以通过 [AWS 云迁移认证](https://www.edureka.co/migrating-to-aws)查看迁移到 AWS 的细节。

## **AWS 数据管道上的演示**

在 AWS 数据管道教程文章的演示部分，我们将看到如何 ***将 DynamoDB 表的内容复制到 S3 桶*** 。AWS 数据管道触发一个操作来启动具有多个 EC2 实例的 EMR 集群(确保在完成后终止它们以避免费用)。EMR 集群从 dynamoDB 获取数据并写入 S3 存储桶。

### **创建 AWS 数据管道**

**第一步:**用样本测试数据创建一个 DynamoDB 表。

![DynamoDB - AWS Data Pipeline - Edureka](img/d7796e64fef55e36341c5f5d13c86d29.png)

**第二步:**为要复制的 DynamoDB 表的数据创建一个 S3 桶。

![S3bucket - AWS Data Pipeline - Edureka](img/ece57cf2adcf38440c7d1399ab7f71e4.png)

**第三步:**从 AWS 管理控制台访问 AWS 数据管道控制台&点击*开始*创建数据管道。

![DataP - AWS Data Pipeline - Edureka](img/f527321349d67484056485c6c99d0f52.png)

**第四步:**创建数据管道。给你的管道取一个合适的名字&合适的描述。指定源&目的数据节点路径。安排您的数据管道&点击激活。

![DataP - AWS Data Pipeline - Edureka](img/a7ef73897ae44cef86d8785449a1ef5c.png)

### **监控&检测**

**第五步:**在*列表管道*中可以看到状态为“等待跑步者”。

![DataP - AWS Data Pipeline - Edureka](img/b4cca576f10511b4087f7d8f795d89c0.png)

**步骤 6:** 几分钟后，您可以看到状态再次变为“正在运行”。此时，如果您转到 EC2 控制台，您可以看到两个自动创建的新实例。这是因为管道触发的 EMR 集群。

![DataP - AWS Data Pipeline - Edureka](img/3fec183b0056f55691ec6b5d090cafa1.png)

**第七步:**完成后，可以进入 S3 桶，查看是否。txt 文件已创建。它包含 DynamoDB 表的内容。下载它并在文本编辑器中打开。

**那么，现在你知道如何使用 AWS 数据管道从 DynamoDB 导出数据了。**同样，通过反转源&目的地，您可以将数据从 S3 导入 DynamoDB。

继续探索吧！

*原来如此！我希望这篇 AWS 数据管道教程能够提供丰富的信息，增加你的知识。如果你有兴趣将你在亚马逊网络服务方面的知识提升到一个新的水平，那么就报名参加 Edureka 在圣荷西举办的 [AWS 培训。](https://www.edureka.co/aws-certification-training-san-jose)*

*有问题吗？请在“AWS 数据管道”的评论部分提到它，我们将回复您。*