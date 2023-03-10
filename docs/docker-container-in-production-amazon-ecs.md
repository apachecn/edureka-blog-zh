# 使用 Amazon ECS 在生产中运行 Docker

> 原文：<https://www.edureka.co/blog/docker-container-in-production-amazon-ecs/>

我相信你听说过最近科技行业的“Docker 炒作”。Docker 使得在任何环境下运行应用程序都变得非常容易。你知道是什么让 Docker 更加高效吗？和亚马逊的 ECS 一起使用。这篇关于 Amazon ECS 的文章详细解释了如何在使用 Amazon ECS 的生产中使用 Docker。

本文议程:

*   [码头工人介绍](#IntroductiontoDocker)
*   [亚马逊 ECS 简介](#IntroductionToAmazonECS)
*   [ECS 如何工作](#HowECSworks)
*   [使用 ECS 的特点和优势](#FeaturesAndBenefitsofusingECS)
*   [演示:使用 Amazon ECS 在生产环境中运行 Docker 映像](#Demo)

## **码头工人介绍**

[Docker](https://www.edureka.co/blog/docker-tutorial) 是一个软件开发平台。它基于集装箱化的概念。它将应用程序及其所有依赖项包装到一个容器映像中。这个容器可以部署在任何平台上运行那个应用程序。因此，基本上这些应用程序运行完全相同，无论它们运行在哪里或运行在什么系统上。它使用一个名为 DockerHub 的在线云存储库来存储所有这些容器图像。

## **亚马逊 ECS 简介**

既然你已经理解了 Docker，那我们就来看看 ECR 吧。作为容器服务平台的一部分，AWS 提供了亚马逊 EC2 容器注册中心(Amazon ECR)。这是一个完全托管的 docker 容器注册表。

现在您有了自己的容器，您需要的只是一个托管它们的平台。这就是 ECS 发挥作用的地方。

ECS 代表弹性集装箱服务。这是一种容器管理服务。在 ECS 集群上运行、停止或管理 Docker 容器就像在公园散步一样。您可以通过几个简单的 API 调用来启动、停止或扩展任何基于容器的应用程序。

我相信你们一定听说过微服务这个术语，它现在在技术市场上非常热门。Amazon ECS 可以让您通过在微服务模型上构建复杂的应用程序架构来创建一致的部署。

![Amazon ECS](img/3d19644305fa18f247ef0e9bd27d6761.png)

ECS 还跟踪您的实例及其资源。在上图中，有一个运行两个容器的请求。ECS 将寻找拥有运行这些容器的资源的实例，从注册中心下载容器，并相应地将它们部署到容器上。

## AWS 上的集装箱| AWS 弹性集装箱服务| AWS EKS | AWS 培训| Edureka



[//www.youtube.com/embed/3gFxARn9Ruc?rel=0&showinfo=0](//www.youtube.com/embed/3gFxARn9Ruc?rel=0&showinfo=0)

edu reka 制作的“AWS 弹性容器服务(ECS)”视频将向您展示如何使用 AWS ECS 和 Fargate 在 AWS 上运行容器

## **ECS 如何工作**

现在您已经理解了理论概念，让我们更深入地了解一下 ECS 是如何工作的。让我们看一个非常常见的场景，假设您正在运行一个使用两个 docker 容器的应用程序。例如，一个容器包含实际的应用程序，另一个包含所有的依赖项。您需要这两者来成功运行应用程序。

Amazon ECS 由以下部分组成:

### **任务定义**

任务定义基本上是描述用于运行应用程序的 docker 容器的蓝图。在我们的例子中，它将是两个 docker 容器、所用图像的细节、要分配的 CPU 内存、要声明和使用的环境变量、要公开的端口等。

### **任务**

任务是任务定义的实例。它运行容器以及任务定义中提到的容器细节。需要时，单个类定义可以创建多个任务。

![](img/9416d86c64f808745b88a7e6766eda0f.png)

### **服务**

服务定义了在任何给定点从单个任务定义运行的最小和最大任务。在我们的示例中，如果一个任务定义中有一个任务正在运行，并且 CPU 达到极限，ECS 将添加另一个任务。此时，服务将是 2，因为两个任务从一个任务定义中运行。

### **ECS 容器实例和 ECS 容器代理**

每个 docker 容器都将在 EC2 实例上运行。这样的 EC2 实例被称为 ECS 容器实例。

每个 ECS 容器实例都将运行一个 ECS 容器代理。该代理在实例和 ECS 之间进行通信，这有助于管理正在运行的容器，甚至添加新的容器。

### **集群**

我们现在有了任务定义、任务和服务。我们只需要一个平台来托管这些。这个平台就是集群。集群是一组 ECS 容器实例。一个集群可以运行许多服务。例如，您的项目中有多个应用程序，您可以在一个集群上运行其中的几个。这减少了资源的浪费，间接节省了你的钱。

## **![image2b - Amazon ECS - Edureka](img/ad4bc1da8c77ad116842cae7298188e3.png)**

## **使用 ECS 的特点和优势**

*   它允许您在一个区域内的多个可用性区域中以高度可用的方式运行应用程序容器
*   它允许您在没有基础设施管理的情况下使用容器。
*   您可以将任何东西都容器化，并让 ECS 来管理。
*   它是超级安全的，因为你可以将你的容器图像存储在 EC2 容器注册表中，这是非常安全的，因为你的图像在静止时是加密的。
*   ECS 的另一个令人惊奇的特性是，它让 IAM 角色在每个任务中保持独立，这是我非常喜欢的。对每个任务的控制访问是非常受指导的。

## **演示:使用 Amazon ECS 在生产环境中运行 Docker 映像**

在这个演示中，我将向您展示如何使用 Amazon ECS 并在其上运行 docker 映像。让我们开始吧。

前往[亚马逊的登录页面](https://aws.amazon.com/console/)并登录(如果你已经有账户的话)。如果你没有，那就创建一个免费账户吧。这是您登录后将看到的控制台。

![1 - Amazon ECS - Edureka](img/e5d9e42aca785a02d1190438fdfafb6b.png)

键入“ECS ”,然后单击该服务。如果您之前没有创建集群，您会看到一个**开始**按钮。继续点击**开始**。

![2 - Amazon ECS - Edureka](img/4ae1d55e20a32ef173060b31c4e526f5.png)

在 AWS ECS 上运行 docker 映像有 4 个主要步骤，**容器定义、任务定义、服务、集群**。

![3 - Amazon ECS - Edureka](img/85a09ac3e70139a88616b8dc30e12ccb.png)

**配置容器定义:**为您的容器选择一个图像。您有 4 个选项——一个样例应用程序映像、Nginx 映像、tomcat-webserver 和一个自定义映像。

![4 - Amazon ECS - Edureka](img/5a4a1ddf25506f84780e4be026acafd7.png)

对于这个演示，我选择了 sample-app。

![5 - Amazon ECS - Edureka](img/20bcd6d204ef9b737b5c53ba9c6c6b0e.png)

如果您希望更改配置，请单击右上角的编辑。

![6 - Amazon ECS - Edureka](img/180c54d3f98085c640e04f1a67e390ca.png)

您可以编辑**容器名称、要使用的映像、内存限制、端口映射、健康检查配置、环境配置、容器超时配置、网络设置、存储和日志记录配置、资源限制、**和 **Docker 标签。**在本次演示中，我使用了所有默认配置。

**配置** **任务定义:**由**任务定义名称**、**网络模式**、**任务执行角色**、**能力**、**任务内存、**和**任务 CPU** 组成。

![7 - Amazon ECS - Edureka](img/50488424913127ff4cb267d51d7772df.png)

可以点击右上角的**编辑**，根据需要进行配置。对于这个演示，我使用所有的默认配置。完成后，点击右下角的**下一个**。

![8 - Amazon ECS - Edureka](img/43001f3ee143456ed1c192b97621e63b.png)

**配置服务:**您可以继续更改**服务名称、所需任务数量**、**安全组**，并选择**负载均衡器类型**。对于这个演示，我没有使用负载平衡器。点击**下一步。**

![9 - Amazon ECS - Edureka](img/eccae6b3a6cb7d3678781f2d0be0685c.png)

**配置集群:**通过添加一个**集群名称**来配置您的集群，然后单击 **Next。**

![10 - Amazon ECS - Edureka](img/6d751bd34d08b151825579bc12f44b10.png)

回顾:一旦你配置好了所有的东西，你应该会看到这样的东西。

![11 - Amazon ECS - Edureka](img/cf23bfe09e60b11ffc015ea34fdf7a44.png)

查看所有内容，然后点击右下角的**创建**。现在将创建所有的服务。这可能需要大约 10 分钟。

![12 - Amazon ECS - Edureka](img/3815622f0d9c1566866d22bf2e65bbe1.png)

一旦一切都处于**完成**状态，点击**查看服务**

![](img/c6f4262abc65b336828777331cd4b02b.png)

你会看到这样的东西。它将向您显示您的**集群详细信息、任务定义**和一个选项，用于**删除**和**更新**它。

![14 - Amazon ECS - Edureka](img/fead843bb059dfdf519d6efdf9979e64.png)

您可以查看进一步的细节，如 **VPC** 、**子网**、**任务**、**事件**、**自动缩放**、**部署**、**指标**、**标签**和**日志**。

![15 - Amazon ECS - Edureka](img/c91c6f42df81b34bb483d839fa6de93b.png)

现在，点击**任务**来检查已部署的容器。

![16 - Amazon ECS - Edureka](img/1c3d4270c60f4df978e7b13f2f9f6da7.png)

点击**任务名称**，如下图所示。

![17 - Amazon ECS - Edureka](img/467426822f50188258d79ad3e03ba075.png)

点击**网**栏目下的 **ENI Id** 。

![15 - Amazon ECS - Edureka](img/588cc34cb8a891bcb7ef28c28c129c2d.png)

您将被带到**网络接口**页面，如下所示:

![16 - Amazon ECS - Edureka](img/b4636da277a4c60e98144bccea62db0f.png)

向下滚动，你会看到你的 IPV4 公共 IP。复制它。

![17 - Amazon ECS - Edureka](img/e171fe1bef6e398581fd2a2dedccb611.png)

像贴网址一样贴在任何浏览器上。您将在那里看到 docker 容器输出。您将看到您的示例应用程序。

![op - Amazon ECS - Edureka](img/390ed6d2821193e1f00557d14be48055.png)

这只是一个示例应用程序。只需几个步骤，您就可以运行任何类型的应用程序或任何类型的 Docker 映像。

这就把我们带到了这篇亚马逊 ECS 文章的结尾。您可以将该服务与各种 DevOps 工具集成在一起，从而简化构建过程。我希望这篇博客对你有所帮助。  更多此类博客，请访问“ **[Edureka 博客](https://www.edureka.co/blog/)** ”。

*如果您希望了解更多关于云计算的知识，并在云计算领域建立自己的事业，请查看我们的[云计算课程](https://www.edureka.co/cloud-computing-certification-courses)，该课程提供有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解云计算，并帮助您掌握这门学科。*

*有疑问？请在评论区提及它或将其发布在 [**Edureka 社区**](https://www.edureka.co/community) 上，我们将会回复您。在 Edureka 社区，我们有超过 100，000 名技术狂热分子随时准备提供帮助。*