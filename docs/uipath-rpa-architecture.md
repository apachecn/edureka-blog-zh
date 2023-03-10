# UiPath RPA 体系结构—ui path 组件的解构

> 原文：<https://www.edureka.co/blog/uipath-rpa-architecture/>

了解一个工具的内部工作原理和架构很有帮助，尤其是如果你每天都在使用一个工具的话。错误修复和故障排除变得轻而易举，您可能会经常发现自己以新的和创造性的方式使用相同的平凡工具。在这篇关于 UiPath RPA 架构的文章中，我将讨论 UiPath 的不同组件如何协同工作来满足客户需求，并帮助您成为 RPA 方面的 [*熟练专业人员。*](https://www.edureka.co/robotic-process-automation-training)

本文将涵盖以下主题:

*   [RPA 是什么？](#What%20is%20RPA?)
*   [什么是 UiPath？](#What%20is%20UiPath?)
*   [UiPath 平台组件](#UiPath%20Platform%20Components)
    *   [UiPath 工作室](#UiPath%20Studio)
    *   [【uipath 机器人】](#UiPath%20Robot)
    *   [UiPath 编制器](#UiPath%20Orchestrator)
*   [ui path 的架构](#Architecture%20of%20UiPath)

我们开始吧！

## **RPA 是什么？**

借助机器人实现业务运营自动化以减少人工干预的过程被称为 [***【机器人流程自动化(RPA)*** 。](https://www.edureka.co/blog/what-is-robotic-process-automation/)

如果我必须逐一阐述这些术语，那么

*   **机器人**是模仿人类行为的实体，称为机器人。
*   一个**过程**是导致有意义活动的一系列步骤。比如泡茶的过程或者你喜欢的菜等等。
*   **自动化**是机器人在没有人类干预的情况下完成的任何过程。

因此，当我们将所有这些术语总结在一起时，然后模仿人类的动作来执行一系列步骤，从而导致有意义的活动，而无需任何人类干预，也被称为 [***【机器人流程自动化】***](https://www.edureka.co/blog/robotic-process-automation) 。

现在，既然你知道 RPA 是什么，接下来在本文中我将向你介绍 UiPath 的要点。

## **什么是 UiPath？**

UiPath 是 [RPA 工具](https://www.edureka.co/blog/rpa-tools-list-and-comparison/)的主要市场领导者之一。该工具用于自动化重复性任务，并提供拖放功能。因此，您希望执行的任何操作都可以通过拖放到工作窗格中的活动来满足。 现在，您已经了解了 UiPath，让我们来看看 [UiPath](https://www.edureka.co/blog/uipath-tutorial/) 的各个组件，了解它的架构是如何构建的。

## **UiPath 平台组件**

![UiPath Studio, Robot and Orchestrator - UiPath RPA Architecture - Edureka](img/76f5fb65472f24cb9621a87f6119cc44.png)ui path 平台主要由以下三部分组成:

*   [UiPath 工作室](#UiPath%20Studio)
*   [【uipath 机器人】](#UiPath%20Robot)
*   [UiPath 编制器](#UiPath%20Orchestrator)

让我们逐一了解这些组件。

### **UiPath 工作室**

UiPath 是一个可视化设计器，它允许您使用预构建的活动来构建自动化工作流。以下是 UiPath Studio 的特色:

![UiPath Studio Features - UiPath RPA Architecture - Edureka](img/2b5757a7f9596197276ee93abf92613c.png)

*   **GUI 仪表板**–提供可视化仪表板，其中包含预定义的活动以构建自动化工作流。
*   **3 个复杂级别**–ui path Studio 允许您基于序列、流程图和状态机等 3 个复杂级别创建项目。
*   **记录器类型**–ui path Studio 提供[各种类型的记录器](https://www.edureka.co/blog/uipath-recording/)来记录基本、桌面、Web、图像、原生 Citrix 等多个平台上的动作。
*   **日志记录&异常处理**–ui path Studio 的功能区选项卡提供了调试和异常处理的各种选项，如调试、打开日志、慢速等。如果你想学习如何使用这些选项，你可以参考我关于[错误处理的文章。](https://www.edureka.co/blog/error-handling-in-uipath/)
*   **集成 OCR 技术**–ui path Studio 可以集成各种 OCR 技术来执行屏幕抓取。
*   **可重用组件**–使用 UiPath Studio，您可以创建可重用组件，并将它们作为库一起发布。

因此，简单来说，UiPath Studio 用于创建自动化工作流，在它的帮助下，您可以自动化任务。

现在，您已经了解了什么是 UiPath Studio，接下来在这篇关于 UiPath RPA 架构的文章中，我将告诉您关于 UiPath Robot 的信息。

### **【uipath 机器人】**

由 UiPath Studio 创建的自动化工作流程由 UiPath 机器人执行。因此，要执行您的任何任务，您需要确保 UiPath 机器人处于运行状态。此外，您可以同时运行一个或多个机器人。

接下来，让我们了解 UiPath 平台的第三个组件，即 UiPath Orchestrator。

### **UiPath 编制器**

Orchestrator 是 UiPath 的产品，使您能够在各种平台上协调 UiPath 机器人连续执行重复流程。

Orchestrator 遵循以下流程:

![UiPath Orchestrator Process-UiPath Orchestrator Process-Edureka](img/14f53bf34e0a5b23028a3df09dd67911.png)First, you have to create robots to execute your task. Then you have to create a Project and Publish it so that you can use it as a process. Once you create a process, you have to assign a robot to execute this process in a specific environment, and this will create a Job.
Now, this was the basic workflow of how Orchestrator works. But, let me take an example and show you how it works in the architecture of UiPath.

#### **场景:**

Consider a scenario, where you have created an automation workflow in the UiPath Studio. Now, once you publish your project a NuGet Package gets automatically created. A NuGet package is designed for Microsoft Development Platform and is used to read the .NET files. After that, Project is uploaded via Orchestrator Server. Refer below.
![UiPath Orchestrator Example - UiPath RPA Architecture - Edureka](img/2080ab5a79de090091b4ab4ef5e1ad6e.png)Now, you can deploy this particular project on any number of computers by mentioning the Machine Key. Automatically the Ui.Robots execute and monitor the tasks if it is a back office process. Similarly, if it is a front-office process, then the user executes the project or task and the Ui.Robot just monitors the task.
So, that’s how folks the UiPath Orchestrator works. If you wish to know more about UiPath Orchestrator, you can refer to my article on [Orchestrator](https://www.edureka.co/blog/uipath-orchestrator/) which talks about how to login to the Orchestrator and deploy a Robot.
Now, that you have understood the components of UiPath Platform, let me next show you how these platforms fit together and form the architecture of UiPath.

## **UiPath 架构**

The UiPath Architecture has the following 3 layers:

*   客户端层
*   服务器层
*   持久层

![UiPath Architecture - UiPath RPA Architecture - Edureka](img/c825cfc1223c9f8b212c9c8dbdfb1304.png)下面我们一层一层的说。

从客户端层开始，客户端层由 UiPath Studio 和 UiPath Robot 组成。正如我之前提到的，UiPath Studio 是您创建自动化工作流的地方，然后，UiPath 机器人执行那些任务。

现在，UiPath 机器人有两个你需要了解的组件:

*   **UiPath 代理服务:**该服务用于显示系统托盘中可用的作业。它还可以请求启动/停止作业和更改设置。
*   **UiPath Executor 服务:**该服务用于在 Windows 会话下运行给定的作业。

现在，一旦您的机器人准备好执行任务，项目就可以上传到 Orchestrator 服务器上。在 Orchestrator 的帮助下，您可以在各种 PC 上运行该项目。Orchestrator 监控部署、配置、队列管理和日志记录。

进入画面的下一层是持久层。这一层由一个数据库组成，它负责队列和队列中的项目。它还包含有关机器人配置及其分配流程的信息。

如果你希望进一步了解 UiPath 架构，那么我建议你去看看下面这个有趣的视频。

## UiPath RPA 架构| UiPath Studio，机器人& Orchestrator | UiPath 平台组件| Edureka

[https://www.youtube.com/embed/mYGbp1gVcmQ?rel=0&showinfo=0](https://www.youtube.com/embed/mYGbp1gVcmQ?rel=0&showinfo=0)This session on UiPath RPA Architecture will cover the different components of the UiPath Architecture.With this, we come to an end to this article on UiPath RPA Architecture. I hope you enjoyed reading this article and learned how different components of UiPath work together.If you wish to further learn about Robotic Process Automation and build your career as an [RPA Developer](https://www.edureka.co/blog/rpa-developer-roles-and-responsibilities/), then you can check out our course on ***[Robotic Process Automation Using UiPath](https://www.edureka.co/robotic-process-automation-training). ***This course will let you enhance your knowledge of RPA and will give you extensive hands-on experience in UiPath.

*有问题吗？请在这篇 **UiPath RPA 架构**文章的评论部分提到它，我们会给你回复。*