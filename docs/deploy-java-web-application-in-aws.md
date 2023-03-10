# 如何在 AWS 中部署 Java Web 应用？

> 原文：<https://www.edureka.co/blog/deploy-java-web-application-in-aws/>

您是否在配置和管理服务器以部署 Java Web 应用程序方面遇到了困难？如果是，那么你来对地方了。因此在本文中，我将向您展示如何在 **[AWS](https://www.edureka.co/blog/videos/aws-tutorial/)** 上部署 Java Web 应用程序。在 AWS 上部署 Java web 应用程序的过程完全没有麻烦，而且耗时更少。通过 [AWS 在线课程](https://www.edureka.co/aws-certification-training)了解所有关于 AWS 的信息。

在这里，我将讨论以下几点:

*   [什么是 AWS？](#what)
*   [为什么在 AWS 中使用 Java Web 应用程序？](#why)
*   [如何在 AWS 中部署 Java Web 应用？](#how)

让我们从第一个话题开始。

## **什么是 AWS？![AWS Logo - Deploy Java Web App in AWS - Edureka](img/2ad1ed767594803ae9b732cc71ad3339.png)**

**【亚马逊网络服务(AWS)** 是来自亚马逊的云服务，它以构建块的形式提供服务，这些构建块可以用来在云中创建和部署任何类型的应用程序。 借助 [云架构师大师计划](https://www.edureka.co/masters-program/cloud-architect-training) ，深入了解云计算、AWS 架构原则、云上迁移应用等知识。

这些服务或构建块被设计成彼此协同工作，并产生复杂且高度可伸缩的应用程序。

每种类型的服务被分类到一个域中，广泛使用的几个域是:

现在您已经知道 AWS 是什么，让我列出在 AWS 中部署 Java Web 应用程序的好处。

从 [AWS 云迁移](https://www.edureka.co/migrating-to-aws)中了解更多关于 AWS 及其框架的信息。

**为什么要在 AWS 上使用 Java Web 应用？**

**易于使用**

AWS 旨在允许应用程序提供商、ISV 和供应商快速、安全地托管您的应用程序，无论是现有应用程序还是基于 SaaS 的新应用程序。您可以使用 AWS 管理控制台或文档完善的 web 服务 API 来访问 AWS 的应用程序托管平台。

**灵活**

AWS 使您能够选择操作系统、编程语言、web 应用程序平台、数据库和您需要的其他服务。借助 AWS，您可以获得一个虚拟环境，让您加载应用程序所需的软件和服务。这简化了现有应用程序的迁移过程，同时保留了构建新解决方案的选项。

**性价比**

您只需为您使用的计算能力、存储和其他资源付费，没有长期合同或前期承诺。如需了解更多关于 AWS 与其他托管方案成本比较的信息，请参见 [AWS 经济中心](https://aws.amazon.com/economics/)

**可靠**

通过 AWS，您可以利用可扩展、可靠且安全的全球计算基础设施，这是亚马逊数十亿美元在线业务的虚拟主干，已经磨砺了十多年。

**可扩展的高性能**

使用 AWS 工具、自动伸缩和[弹性负载平衡](https://www.edureka.co/blog/elastic-load-balancer-tutorial-application-load-balancer)，您的应用程序可以根据需求进行伸缩。在亚马逊庞大基础设施的支持下，您可以在需要时访问计算和存储资源。

**安全**

AWS 利用端到端方法来保护和强化我们的基础设施，包括物理、运营和软件措施。更多信息，请参见 [AWS 安全中心](https://aws.amazon.com/security/)。

## **如何在 AWS 中部署 Java Web 应用？**

在我们了解如何部署 Java Web 应用程序之前，让我分享一些您必须遵循的最佳实践。

### **一般最佳实践**

web 应用程序的规模和安装复杂性可能会有很大的不同，因此很少有一个放之四海而皆准的解决方案来部署和托管 Java 应用程序。但是，在部署任何 web 应用程序时，有一些通用的最佳实践需要考虑:

*   了解应用程序的部署、安装和配置特征。

*   从初始部署到未来的可扩展性、可用性以及备份和恢复要求，了解应用程序的期望。

*   对于一致性非常重要的部署和其他任务，尽可能使用自动化。

*   利用源代码或应用程序库来保护您的应用程序。

现在让我们看看各种类型的 Java 应用程序及其机制。

从 [AWS 云迁移培训](https://www.edureka.co/migrating-to-aws)中了解更多关于迁移到 AWS 及其框架的信息。

下面的视频有助于总结在 AWS Elastic Beanstalk 中部署 Java Web 应用程序的所有内容

[https://www.youtube.com/embed/Ozc5Yu_IcaI](https://www.youtube.com/embed/Ozc5Yu_IcaI)

你甚至可以通过 [AWS 开发者助理](https://www.edureka.co/aws-developer-certification-training)查看 AWS 开发者的详细信息。

## **在 AWS 上的应用**

AWS 提供了几个工具和服务来支持 AWS 管理的和客户管理的 Java 应用程序部署。下表是一个高层次的参考，有助于确定最适合特定场景的选项。下面几节将更详细地描述这些不同的方法及其适用的用例。

| **应用特征** | **包装** **工具** | **展开机构** | **部署方法/环境** |
| 在 Eclipse 中开发的定制 Java 应用程序 | 黯然失色 | 从 Eclipse 中单击部署 | 用于 Eclipse 的 AWS 工具包 |
| Java web 应用程序部署为 JAR、WAR 或 ZIP 文件，只需对操作系统进行最少的更改 | 罐子，战争，还是拉链 | 使用 AWS Elastic Beanstalk 自动部署打包的应用程序 | [AWS 弹性豆茎](https://www.edureka.co/blog/aws-elastic-beanstalk/) |
| 任何 Java 应用程序或服务器配置，尤其是那些需要定制操作系统或第三方安装程序的应用程序或服务器配置 | 现有的自定义安装程序、应用程序存档(JAR、WAR、ZIP)、手动文件复制等。 | 现有的软件部署工具和流程或自动化部署服务，如 AWS CodeDeploy 或 AWS OpsWorks。 | [EC2 实例](https://www.edureka.co/blog/ec2-aws-tutorial-elastic-compute-cloud/) |

### **AWS 弹性豆茎**

Elastic Beanstalk 是一个易于使用的服务，用于部署和扩展 Java web 应用程序。Elastic Beanstalk 支持 Java 应用程序的几种[平台配置](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html#concepts.platforms.java)，包括带有 Apache Tomcat 应用服务器的多个版本的 Java，以及不使用 Tomcat 的应用程序的纯 Java 配置。

纯 Java 选项允许客户在不使用 web 容器或使用不同容器(如 Jetty 或 GlassFish)的 Java web 应用程序的源代码包中包含任何所需的库 JAR 文件。部署后，Elastic Beanstalk 会自动管理容量供应、负载平衡和自动扩展。这种方法适用于部署包含以下标准的 Java 应用程序的公司:

*   需要最少的操作系统更改。(请注意，Elastic Beanstalk 配置文件支持高级平台和操作系统配置选项。然而，这需要额外的弹性豆茎包装的努力和专业知识。)
*   要么在 Apache Tomcat 7 或 8 中运行，要么打包在自己的 web 容器中

Elastic Beanstalk 支持以下打包和部署机制:

*   使用 Eclipse 和 [AWS Toolkit for Eclipse](https://aws.amazon.com/eclipse/) 开发并直接部署到 Elastic Beanstalk 的定制应用程序

*   应用程序打包到一个 JAR、WAR 或 ZIP 文件中，然后使用 Elastic Beanstalk 控制台、EB CLI 或 Elastic Beanstalk API 调用进行部署。要将多个应用程序部署到一个弹性 Beanstalk 环境中，客户可以将多个 WAR 文件捆绑到一个 ZIP 文件中。

**查看我们在顶级城市的 AWS 认证培训**

| 印度 | 美国 | 其他国家 |
| [在海德拉巴的 AWS 培训](https://www.edureka.co/aws-certification-training-hyderabad) | [亚特兰大 AWS 培训](https://www.edureka.co/aws-certification-training-atlanta) | [AWS 伦敦培训](https://www.edureka.co/aws-certification-training-london) |
| [班加罗尔的 AWS 培训](https://www.edureka.co/aws-certification-training-bangalore) | [波士顿 AWS 培训](https://www.edureka.co/aws-certification-training-boston) | [阿德莱德的 AWS 培训](https://www.edureka.co/aws-certification-training-adelaide) |
| [钦奈的 AWS 培训](https://www.edureka.co/aws-certification-training-chennai) | [纽约市的 AWS 培训](https://www.edureka.co/aws-certification-training-new-york-city) | [新加坡 AWS 培训](https://www.edureka.co/aws-certification-training-singapore) |

**将 Java 应用程序部署到 AWS 云的步骤**

在继续之前，有几个先决条件。

1.  JDK 8 或更高
2.  Tomcat 8 或更高版本
3.  [Eclipse IDE for Java EE](https://www.edureka.co/blog/setup-eclipse-ide/)
4.  免费 AWS 帐户

一旦你有了这些，我们就可以开始了。

1.  首先，让我们在 Eclipse 中创建一个示例 Java Web 应用程序。为此，请单击“文件”->“新建”->“动态 Web 项目”。现在用你想要的名字命名这个项目。在这里，我将其命名为 DemoWebApp。单击下一步，然后单击完成。在这之后，您将会看到您的项目已经在您的工作区中创建好了。![Step 1 - Deploy Java Web App in AWS - Edureka](img/61a4d284731a301e91cbfa6d690ce30f.png)

2.  现在，您可以创建任何 web 应用程序，如 servlets、JSP 等。这里我将选择 JSP。右键单击 DemoWebApp -> New -> [JSP](https://www.edureka.co/blog/jsp-in-java/) 文件。将文件命名为 sample.jsp。一旦你这样做了，那么在这个文件的主体部分，写一个简单的文本，比如“这是一个示例 JSP”或者你想要的任何东西。![Step 2 - Deploy Java Web App in AWS - Edureka](img/caabbd261622aef2ee6a079cacf8433f.png)

3.  现在，在使用 AWS 之前，我将在本地测试这个应用程序。为此，您需要使用命令提示符导航到您的 tomcat 目录(因为我使用的是 Windows 10 操作系统)并使用 startup.bat 命令。

4.  一旦 Tomcat 启动，转到您在 Eclipse 上的项目。右键单击项目，然后单击属性。然后点击服务器并选择 Tomcat 服务器。点击应用并关闭。![Step 3 - Deploy Java Web App in AWS - Edureka](img/e34a3db7cc8189566ae24f29036c151d.png)

5.  现在右键单击您的项目->运行方式->在服务器上运行。如果一切正常，您将能够看到文本“这是一个示例 JSP”的输出。这样，我们已经在本地测试了我们的应用程序。现在右键单击您的项目->导出-> WAR 文件。在此输入保存 war 文件的目的地。

6.  现在我们将在 AWS 上部署这个应用程序。为此，请访问 AWS 主页。点击服务->计算->弹性豆茎。现在点击创建一个新的应用程序。输入应用程序的名称，并为其创建一个新环境。现在选择 Web 服务器环境。现在在基本配置中，选择预配置平台中的 Tomcat。在应用程序代码中，选择我们在上一步中创建的 WAR 文件。现在点击上传。![Step 4 - Deploy Java Web App in AWS - Edureka](img/2fc4cd2d1362d98d88c6fd4e007d5191.png)

7.  上传 WAR 文件需要几分钟时间。完成后，您将看到以下页面。在这里你可以看到网址。点击 URL，您将看到一个 JSP，其中包含您的文本消息。![Step 6 - Deploy Java Web App in AWS - Edureka](img/b13c6332a8e4dbd3d38fe990ee256945.png)

这就是如何在 AWS 中部署 Java web 应用程序。至此，我们已经结束了这篇关于在 AWS 中部署 Java Web 应用程序的文章。我希望你已经理解了我在这里解释的一切。

*如果您发现这与如何在 AWS 中部署 Java Web 应用程序相关，您可以查看 Edureka 在 Kolkata 由行业从业者共同创建的关于 [AWS 培训的现场和讲师指导课程。](https://www.edureka.co/aws-certification-training-kolkata)*

*有问题吗？请在如何在 AWS 中部署 Java Web 应用程序的评论部分提到它，我们会回复您。*