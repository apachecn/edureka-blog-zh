# 什么是持续集成？

> 原文：<https://www.edureka.co/blog/continuous-integration/>

持续集成是一种开发实践，在这种实践中，开发人员经常将代码集成到一个共享的存储库中，每个集成都通过自动化构建和自动化测试来验证。It 是 DevOps 最重要的部分，用于集成各个 DevOps 阶段。在这篇博客中，我们将讨论开发人员在编写、测试和向最终用户交付软件时面临的问题，以及他们如何使用 CI 解决这些问题。

在这篇博客中，我们将关注以下主题:

## **传统融合**

在传统的集成或/软件开发周期中，

*   每个开发人员都会从中央存储库中获得一份代码副本。
*   所有开发人员都从同一个起点开始工作。
*   每个开发人员通过独立工作或团队合作来取得进步。
*   他们添加或更改类、方法和函数，修改代码以满足他们的需求，最终，他们完成了分配给他们的任务。
*   与此同时，其他开发人员和团队继续完成他们自己的任务，修改代码或添加新代码，解决他们被分配的问题。
*   如果我们后退一步，看看整个项目，我们会发现，所有参与项目的开发人员在开发源代码的同时，也在为其他开发人员改变环境。

可能使这些问题升级的主要因素:

*   项目团队的规模。
*   自从开发人员从中央存储库获得最新版本的代码以来所经过的时间。



## 想探索更多关于 DevOps 的知识？ [<button>上手</button>](https://www.edureka.co/devops)

## **与传统融合的问题**

![Problem with Traditional Integration - Continuous Integration - Edureka](img/fe6d9561c5a62cd225a99a0e35d3c3a5.png)

## **传统集成面临的问题有什么解决方案？**

那么，下面是解决上述问题的**步骤**:

![Solution for Problems faced in Traditional Integration - Continuous Integration - Edureka](img/0262730e7135dc6a956812b6986e3bd9.png)

那么，让我们看看持续集成到底是什么？

## **什么是持续集成？**

**![Continuous Integration - Continuous Integration - Edureka](img/92e20c8908bd25010f4be215f51dcac6.png)我们先从马丁·福勒的定义开始:**

持续集成是一种软件开发实践，团队成员经常集成他们的工作，通常每个人至少每天集成一次，导致每天多次集成。每个集成都由一个自动化构建(包括测试)来验证，以尽可能快地检测集成错误。许多团队发现这种方法可以显著减少集成问题，并允许团队更快地开发内聚的软件。

**——马丁** **福勒**

自动化你的构建、测试和部署过程会增加项目中经常发生的问题。因此，我们应该有一个可靠的集成方法，确保尽早发现错误。

## **什么是持续集成？|爱德华卡**



[//www.youtube.com/embed/yse_OrdueKk?rel=0&showinfo=0](//www.youtube.com/embed/yse_OrdueKk?rel=0&showinfo=0)

这个关于持续集成的 Edureka 视频解释了持续集成的概念、好处和工具(Jenkins)。

让我们继续，看看持续集成有什么好处。

## **持续整合的好处**



**![Benefits of Continuous Integration - Continuous Integration - edureka](img/827c1764652d52af3d5d39db86b9dbd1.png)**

1.  **降低集成风险:**通常，从事项目意味着多人在从事不同的任务或代码部分，这使得集成变得有风险。调试和解决这个问题可能非常痛苦，并且可能意味着对代码进行大量的更改。更频繁地集成有助于将此类问题减少到最低程度。
2.  **更高的代码质量:**更加关注代码的功能会产生更高质量的产品。
3.  **版本控制中的代码起作用:**如果您提交了一些破坏构建的东西，您和您的团队会立即得到通知，并且问题会在其他人退出“破坏的”代码之前得到解决。
4.  **减少团队成员之间的摩擦:**建立公正的制度减少了团队成员之间争吵的频率。
5.  **对 QA 团队来说很容易:**拥有不同版本和构建的代码可以帮助有效地隔离和跟踪 bug，这让 QA 团队的生活变得更容易。
6.  **更少的部署时间:**部署项目可能是非常乏味和耗时的，自动化这一过程是非常有意义的。

## **对 CI 系统的要求**

![Requirements for Continuous Integration System - Continuous Integration - Edureka](img/8552ffe24f911973cedc5f9b3e3686e5.png)但是您可能想知道根据您的需求安装 CI 系统有什么要求。如果您想在自己的环境中安装 CI 服务器，您首先需要一些东西。

*   **【版本控制系统(VCS)** 。它提供了一种可靠的方法来集中和保存随着时间的推移对项目所做的更改。
*   **虚拟机:**对于现场解决方案，您应该有一台备用服务器或至少一台虚拟机。一台干净的机器来构建你的系统是至关重要的。
*   **托管 CI 工具解决方案:**为了避开服务器或虚拟机，你可以选择托管 CI 工具解决方案，它有助于整个流程的维护，并提供更容易的可扩展性。
*   **工具:**如果你选择自托管版本，你将需要安装一个持续集成工具，如 Jenkins、TeamCity、Bamboo 等。

## 大师持续集成 [<button>止现</button>](https://www.edureka.co/devops)

## **什么是 Jenkins——终极 CI 工具**

詹金斯是一个用 Java 编写的开源自动化工具，带有为持续集成目的而构建的插件。Jenkins 用于不断构建和测试您的软件项目，使开发人员更容易将更改集成到项目中，并使用户更容易获得新版本。它还允许您通过集成大量的测试和部署技术来持续地交付您的软件。

有了 Jenkins，组织可以通过自动化加速软件开发过程。Jenkins 集成了所有类型的开发生命周期过程，包括构建、文档、测试、打包、登台、部署、静态分析等等。

Jenkins 借助插件实现持续集成。插件允许集成各种 DevOps 阶段。如果你想集成一个特定的工具，你需要安装这个工具的插件。**例如** Git，Maven 2 项目，亚马逊 EC2，HTML publisher 等。

下图描绘了 Jenkins 正在整合不同的 DevOps 阶段:

![What is Jenkins - Continuous Integration - Edureka](img/ff3bf7e802f0a3a1e16cbb0e54ea7489.png)

## **使用詹金斯进行持续集成演示**

一家名为 Sanders & Fresco Private Ltd .的公司从一个客户那里获得了这个项目，它包括 4 个模块。项目经理将这些模块分配给两个开发人员。现在，为了保持项目流程的一致性，他们建立了一个连续的交付管道，在这里他们根据作业执行所有的模块(一个作业将有两个模块)。在构建了这些作业之后，他们在管道中进行了同步。他们还在开发项目时定期检查构建。因此，git hub 仓库中的项目路径是通过 Jenkins 提供的。使用 CI 的概念，他们在固定的时间间隔后构建他们的项目，该时间间隔可以通过 Jenkins 中的构建触发器选项来定义。

因此，让我们看看如何使用 Jenkins 来实现这一点。

**第一步:**在你的虚拟机中打开你指定端口号上的 Jenkins。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/215186110ff5cb9b6925720d20acea5e.png)

**第二步:**点击新建项目创建新工单。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/5adf31ba8e6e33e618d11317b4b5ad4f.png)

**第三步:**给出自由式项目的名称。这里我给出了 Job1。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/c717b6367dd4e6c453c022e95eae8946.png)

**第四步:**现在进入**源代码管理- > Git** 。填充项目路径以从 Git 中提取项目，然后单击 Apply。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/47c0bd9b11e0f27dca996aeeb00c6de7.png)

**第五步:**点击立即构建。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/d6d82ddf181e34d78b8dbaea2066d1e8.png)

**第六步:**job 1 将开始构建它。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/781b5b09df16ff5af9489d905b020738.png)

**现在我们将创建一个项目/作业 2，它将在固定的时间间隔后(即每分钟后)构建，我们可以使用 Poll SCM 定义该时间间隔。**

**第七步:**点击新建项目创建新工单。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/4950e1bb5af89f24cf92dd1561acb1d1.png)

**第八步:**说出自由式项目的名称。这里我给出了 Job2。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/32b180471e37401606d5e324aae97369.png)

**第九步:**现在转到**源代码管理- > Git** 。填充项目路径以从 Git 中提取项目，然后单击 Apply。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/f5209c246b2f4bdc41ed9b586b549a15.png)

**第十步:**然后进入**构建触发器- >轮询 SCM** 。输入“* * * * *”以在每分钟后构建工单 2，然后单击“应用”。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/37e2372cce900369bef3c107068b14ea.png)

点击应用后，将显示一条消息。点击**保存**按钮。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/395ac04ca05d042f386b2526b20ebb6f.png)

**第 11 步:**点击立即构建。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/ee5200680a8cd83b2c44d9122d1a0956.png)

**第 12 步:**job 2 将在每分钟后开始构建。

**注意:**要检查构建状态，点击 **Git 轮询日志。**这将显示 Job2 的详细信息，即它的建造时间。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/0f663f3ce6ca098a1418eb024b930bd9.png)

**现在，我们将建立一条詹金斯管道来展示持续交付。**

**第十三步:**现在点击詹金斯，进入詹金斯主页。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/530a2e52de145727e27bc9880ad2fb5a.png)

**第十四步:**点击“+”创建一个管道视图。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/0c8640bfe6d7dfe2a794415954bfb651.png)

**第 15 步:**命名视图并勾选**“构建管道视图”**，点击 OK。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/427dcad0d45e8551469425093bc2ac18.png)

**第十六步:**转到**流水线流程**，在**选择初始作业中添加**作业 1** 。**点击确定。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/15068b09c0b48c89a9734fbe31677333.png)

**第十七步:**现在点击 Job1。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/7171ef945f63facb73fa7c6867ccde01.png)

**第十八步:**然后点击**配置**。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/a0d6c5199ee6e6758df6796713dcba9c.png)

**步骤 19:** 转到**后期构建动作**，选择**构建其他项目。**将 Job2 添加到要构建的项目中，并选中“**触发器，前提是构建稳定**”。点击**保存**。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/ac65d2061fe3497ec4ec68db63f73f3c.png)

**第二十步:**现在点击 Job2，点击**配置**。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/84a52192cbab5d048ba7dd717d13c865.png)

**第 21 步:**到**构建触发器- >** 选择**构建在其他项目构建完成之后。**在要观察的项目标签中添加 Job1。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/912f2d07bda94c52eb523124125b2271.png)

**第 22 步:**点击您创建的 **pipeline1** 视图。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/cc4983da264be2f24b321877db912902.png)

**第二十三步:**点击**运行。** Job1 将开始建造。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/2f5defde62ded8665caead9b43b46f05.png)

构建 Job1 后，Job2 会自动构建自身。

![Hands-On - Continuous Integration Using Jenkins - Continuous Integration - edureka](img/3baf16eb047f4632e223b92700fe8d06.png)

所以，这是关于什么是持续集成及其使用 Jenkins 的实施。

 #### 订阅我们的 youtube 频道以获取新的更新..！