# UiPath ReFramework 教程——机器人企业框架的综合指南

> 原文：<https://www.edureka.co/blog/uipath-reframework/>

[UiPath](https://www.edureka.co/robotic-process-automation-training) 是 RPA 市场的主要领导者之一，使用其机器人企业框架或 UiPath ReFramework 来自动化复杂的业务流程。在这个关于 UiPath 重新架构的教程中，我将讨论重新架构的功能和阶段。

本文将讨论以下主题:

*   为什么要使用 ReFramework？
*   什么是 ReFramework？
*   [重构架构](#reframeworkarchitecture)

让我们开始吧！

## 为什么要使用 ReFramework？

[机器人流程自动化](https://www.edureka.co/blog/robotic-process-automation/)是使用顶级 [RPA 工具](https://www.edureka.co/blog/rpa-tools-list-and-comparison/)将手动任务自动化的流程，但是，任何自动化的任务都依赖于人类员工。因此，为了避免对人类员工的依赖，我们必须以这样一种方式定义机器人，即它们可以执行或完成任务。

![Why use ReFramework - UiPath ReFramework Tutorial - Edureka](img/a86153508c0d920c5f47ff6c393920eb.png)

谈到机器人，生产中部署的所有机器人都必须能够执行多个事务，并且在事务失败时能够同时重新执行事务。机器人还必须保持工作流程的一致性，以管理处理、日志格式、输出等所需的各种参数。除此之外，所有的机器人必须有适当的记录和分析系统，以向用户提供适当的健康报告。这就是重构在当今工业中扮演重要角色的地方。

所以，现在你知道为什么你应该使用 ReFramework，让我告诉你到底什么是 ReFramework。

## 什么是 ReFramework？

Robotic Enterprise Framework 或 Re-Framework 是一个模板，用于以模块化方式为大规模部署创建自动化工作流。现在，我很确定你可能还不知道它在现实生活中的应用。因此，为了向你们解释同样的情况，让我考虑一个例子。

考虑一个业务流程，它有三个组件。

*   让第一个组件包含需要每天执行的过程，以读取竞争对手公司提供的课程价格，并在数据库中更新它们。
*   第二部分用于比较该公司提供的课程价格与竞争对手公司提供的课程价格。
*   类似地，第三个组件更新数据库中的价格，并将更新后的价格通知各个团队。

现在，所有这些组件可以进一步划分为小型业务事务，然后您可以为每一个事务设计自动化。

上面讨论的组件可以按以下方式划分为业务事务:

![Business Transactions - UiPath Re Framework Tutorial - Edureka-min-min](img/883051a9fa2ffbb2c161be37970a0c43.png)

现在，这些事务可以被分离为不同的任务，并且可以一个接一个地自动化。这就是你可以使用机器人企业框架或 ReFramework 的地方，因为它提供了各种状态来为各种事务设计自动化。借助 ReFramework，您可以为每个循环设置一组配置，并执行一组操作。

现在，您已经知道了什么是 UiPath ReFramework，让我带您了解一下 ReFramework 的架构。

## **UiPath ReFramework 架构**

重构使用状态机图，并具有以下 4 种状态:

1.  ![ReFramework Architecture - UiPath ReFramework Tutorial - Edureka-min-min](img/3e72fb5c8d456eab359b6a8a4f699c42.png)初始状态
2.  获取事务数据状态
3.  处理事务状态
4.  结束流程状态

所有这些状态相互协作，以下列方式处理业务事务:

### **初始状态**

*   你**在**框架中启动的任何 [RPA 项目](https://www.edureka.co/blog/rpa-projects)在**初始状态**中启动。这是机器人**读取初始项目配置**并初始化应用程序的状态。
*   一旦所有的**配置被读取并且应用被初始化** **并且成功**，事务进入下一个状态，即获取事务数据状态，否则它通过显示系统错误来结束该过程。

### **获取交易数据状态**

“获取事务数据”状态是 Init 状态之后的下一个状态。在这种状态下，你有两种可能。如果一个**新流程被检索到**，则它进入下一个状态，即流程事务状态，否则如果所有事务都被处理，则它进入结束流程状态。

### **处理交易**

*   在流程事务状态中，可能会出现三种结果，即成功状态、业务事务和系统错误状态。成功状态是执行循环并考虑下一个事务数据的状态。
*   当执行一个特定的操作，然后执行状态返回到获取事务数据状态时，就会发生业务规则异常。系统错误事务用于通过错误采取所有必要的步骤。所以在这个事务中，所有的应用程序都被关闭，执行循环回到 Init 状态。

### **结束流程状态**

在所有事务都被执行之后，这是事务进入的最终状态。所以，简单来说，就是用来结束流程的。

我希望我已经给了你一个关于 UiPath 框架的基本概念。如果你想对这个框架有一个详细的了解，可以参考下面这个关于 UiPath ReFramework 的教程。

[https://www.youtube.com/embed/Fw5uxAbULO4?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent](https://www.youtube.com/embed/Fw5uxAbULO4?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent)

至此，我们结束了关于 UiPath ReFranework 教程的这篇文章。我希望你发现它信息丰富。您还可以使用 Edureka 的 UiPath 来检查 **[RPA 培训，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。两者，这些认证将帮助你分别在 UiPath 和 Automation Anywhere 获得深入的知识。](https://www.edureka.co/robotic-process-automation-training)**

*有问题吗？请在“UiPath ReFramework”的评论部分提到它，我们会给你回复。*