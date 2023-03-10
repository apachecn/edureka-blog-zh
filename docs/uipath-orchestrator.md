# Uipath Orchestrator–了解如何使用 ui path 编排机器人

> 原文：<https://www.edureka.co/blog/uipath-orchestrator/>

[UiPath](https://www.edureka.co/blog/uipath-tutorial) 是 RPA 市场上最受欢迎的工具之一。该工具提供拖放功能，无需任何人工干预即可自动执行重复性任务，从而确保可扩展性和可靠性。在这篇关于 UiPath Orchestrator 的文章中，您将了解如何在一个地方控制和管理整个数字劳动力。

本文将介绍 UiPath Orchestrator 的以下主题:

*   [什么是 UiPath？](#What%20is%20UiPath?)
*   [ui path 中的 Orchestrator 是什么？](#What%20is%20Orchestrator%20in%20Uipath?)
*   [登录 Uipath Orchestrator](#Login%20to%20Uipath%20Orchestrator)
*   如何创建:
    *   [机器](#Machine)
    *   [机器人](#Robots)
    *   [环境](#Environments)
    *   [流程](#Process)
    *   [乔布斯](#Jobs)

*You may also go through this recording of UiPath Orchestrator where our [training expert](https://www.edureka.co/robotic-process-automation-training) has explained the topics in a detailed manner.*[https://www.youtube.com/embed/yY6GUoUNOD8?rel=0&showinfo=0](https://www.youtube.com/embed/yY6GUoUNOD8?rel=0&showinfo=0)So, let’s get started with our first topic: What is UiPath?

## **什么是 UiPath？【T2**

UiPath 是一个机器人进程自动化工具，主要用于 Windows 桌面自动化。该工具提供了一个社区版，终身免费，并支持拖放功能。

UiPath 提供各种产品来满足我们的需求，如 UiPath 企业平台、UiPath Studio、UiPath 机器人和 UiPath Orchestrator。

那么，现在，让我们理解什么是管弦乐队。

## **ui path 中的 Orchestrator 是什么？**

Orchestrator 是 UiPath 的一个产品，它使您能够编排 UiPath 机器人在各种平台上连续执行重复的过程。

Orchestrator 遵循以下流程:

![UiPath Orchestrator Process-UiPath Orchestrator Process-Edureka](img/14f53bf34e0a5b23028a3df09dd67911.png) First you have to create robots to execute your task. Then you have to create a Project and Publish it, so that you can use it as a process. Once you create a process, you have to assign a robot to execute this process in a specific environment, and this will create a Job.So, to make your orchestrator perform all the above actions, you have to first login to orchestrator. Let’s us look into the same.

## **登录 Uipath Orchestrator**

To login to UiPath Orchestrator, you first have to register yourself, i.e, to become a Tenant, follow the below steps:**Step 1:**  Go to [https://platform.uipath.com/](https://platform.uipath.com/) and then choose the option “**Become a Tenant**” Refer below.![UiPath Orchestrator Login-UiPath Orchestrator Process-Edureka](img/d036891f192404202f8c0b3045ac40f2.png)**Step 2:** As soon as you click on the option, you will be redirected to the registration page. Here, you have to mention the Tenant name, Username, Name, Surname, Email Address, Admin Password and Confirm Password. Then agree to the Terms of Conditions and click on Create The Tenant. Refer to the snapshot below.![UiPath Orchestrator Register-UiPath Orchestrator Process-Edureka](img/10985ab433b332bd9b7a2e9dcd0be624.png)

**第三步:**成为租户后，返回登录页面，输入用户名和密码。之后，点击登录。这一步将登录到您的 Orchestrator。

![UiPath Orchestrator Dashboard-UiPath Orchestrator Process-Edureka](img/8a19c3ef6dc5f215005008aa6b1d4b28.png)

在 Orchestrator 中登录您的帐户后，您将会看到控制面板。这个仪表板由各种选项组成，供您创建和了解流程、队列、机器、作业等。

现在，我已经告诉你如何登录到 UiPath 的 Orchestrator，接下来让我告诉你如何设置机器人、流程、环境和作业。

## **如何创建机器人、环境、流程、作业？【T2**

为了理解 Orchestrator 的工作原理，让我们考虑一个向用户询问细节并在消息框中显示这些细节的示例项目。

在流程部分，我将向您展示如何创建这个自动化任务。但是，在此之前，让我先向您展示如何添加一台机器，然后我们将创建一个机器人。

### **如何在 Orchestrator 中添加机器？**

要创建机器，请转到 Machines 选项卡，并单击“ **+** ”选项。当您单击加号选项时，您将看到以下三个选项:

*   创建独立机器的选项。
*   创建浮动机器模板的选项。
*   关闭的选项

根据您的需要，您可以选择创建以上两个选项中的任何一个。在这里，我将创建一个独立的机器。

要添加您的机器，您必须提及机器名称。现在，要知道你的机器名，去我的电脑的**属性，你的**电脑名**就会是**的机器名**。然后点击**供应**添加您的机器。**

### **![Add a Machine-UiPath Orchestrator-Edureka](img/52967a8dfadc468c3732b78795a4c5c9.png)**

将机器添加到 Orchestrator 后，下一步是创建机器人。接下来，在这篇文章中，让我们看看如何创造机器人。

### **如何在 Orchestrator 中创建机器人？**

要创建机器人，请转到“机器人”选项卡，并单击“ **+** ”选项。当您单击加号选项时，您将看到以下三个选项:

*   创建独立机器人的选项。这个机器人只能在一台标准机器上工作。
*   创建浮动机器人的选项。这个机器人可以在任何机器上工作
*   关闭的选项

你可以选择创造任何类型的机器人，根据你的需要。在这里，我将创建一个独立的机器人。

所以，一旦你选择了创建一个独立机器人的选项，你就必须提到机器名、名字、域名、密码、选择类型和描述。然后点击创建。

**注意:**要知道域名，可以到命令提示符下键入命令“ **whoami** ”。参考下文。

这将创建你的机器人。下一步是启用 UI 机器人。

因为默认情况下 UI Robot 是不启用的，所以您必须启用它。要启用 UI 机器人，您必须转到安装 UiPath 的目录。然后双击 UI 机器人。

以上步骤将启用 UI 机器人。现在，下一步是启动机器人。

要激活你的机器人，你必须**在 **UI 机器人符号**上右击**，然后你必须进入**设置**。

在 UI 机器人的设置中，提到 **Orchestrator URL** 和**机器键**。然后点击**连接**。这将激活您的 UI 机器人。参考下文。

![Activate Robot-UiPath Orchestrator-Edureka](img/9fa5816a7e0b9b4bf090d5dc48df2709.png)

如果您希望检查您的机器人是否可用，您可以到[https://platform.uipath.com/robots](https://platform.uipath.com/robots)查看状态是否可用。参考下文。

![Sample Robot Active Status-UiPath Orchestrator-Edureka](img/8a6ecfbe52ac197d5e6fb206242b38a0.png)

**注意:** UI 机器人默认不启用。要启用 UI 机器人，您必须转到安装 UiPath 的目录。然后双击 UI 机器人。

现在你的机器人已经可以使用了，下一步就是创建一个环境。

### **如何在 Orchestrator 中创建环境？**

要创建机器人，进入**环境选项卡**，点击“+”选项。当你点击加号选项时，你会看到下面的对话框来创建一个环境。如下提及**名称**和**描述**，然后点击**创建**。

![Sample Environment-UiPath Orchestrator-Edureka](img/51e70c2fe2060740a11c9c5f8c7bc474.png)

一旦你点击**创建**，你将看到另一个**对话框**，在其中你必须选择将在创建的环境中执行任务的机器人。然后点击**更新**。

### **![Manage Sample Environment-UiPath Orchestrator-Edureka](img/d8b089f5e31cb04754ca84e135e6a9ff.png)**

这将创造你的环境。现在，您已经创建了一个环境，下一步是创建一个流程。

### **如何在 Orchestrator 中创建流程？**

要在 Orchestrator 中创建流程，首先必须在 UiPath Studio 中创建一个项目，然后发布它。

因此，为了做到这一点，让我们考虑一个项目，其中，我们要求用户提供细节，然后我们将在一个消息框中显示细节。有关顺序，请参考下文。

![Sample Sequence-UiPath Orchestrator-Edureka](img/8521d60946c3ea0c30364a9e2da29ce7.png)

**注意:**在保存项目时，请记住以 0 开头保存，因为 Orchestrator 不会列出所有已发布的项目。因此，为了确保您的项目在 Orchestrator 中列出，请以“0s”开头，然后以一个名称结尾。在这里，我按项目命名为 0000000001_edureka。

现在，一旦你的项目被保存，通过选择**功能区标签**中的**发布选项**来发布你的项目。这将把您的项目发布给 orchestrator。

一旦您的项目发布，下一步就是创建一个过程。

要创建流程，请转到**流程选项卡**，并点击“+”选项。当您单击加号选项时，您将看到下面的对话框来创建一个流程。提以下 **:**

*   包名(您发布的项目名)
*   包版本
*   环境(您在上面创建的环境)
*   描述

提到所有这些细节后，点击 **Create** 创建一个流程。参考下文。

![Sample Process-UiPath Orchestrator-Edureka](img/072a1e69008357819ef16cc40df3b43b.png)

上述步骤将创建一个流程。现在，一旦创建了流程，下一步就是创建一个作业来执行您的任务。

### **如何在 Orchestrator 中创建作业？**

要在 Orchestrator 中创建作业，您必须单击播放按钮。然后你必须提到你想要安排工作的过程，并选择将执行任务的机器人。然后点击**开始**。

![Sample Job-UiPath Orchestrator-Edureka](img/6117e4c9e9a10ae809279692138be2c2.png)

一旦你点击**开始**，你的工作将自动开始执行。在这里，我不得不提到对话框中的**输入，你会在**消息框**中看到提到的输入作为输出。**

![Sequence Output -UiPath Orchestrator-Edureka](img/3d2c70db10006456a3d1d3a5325101d8.png)

一旦您的作业被执行，您将看到状态为成功。参考下文。

![Sequence Output -UiPath Orchestrator-Edureka](img/2e04afd572ae645bdb4c6906094a4462.png)

至此，我结束了这篇关于 UiPath Orchestrator 的文章。如果你对学习机器人过程自动化有进一步的兴趣，这个博客系列会经常更新，请订阅。我们在 edureka！还提供 ***[机器人过程自动化培训使用 UiPath](https://www.edureka.co/robotic-process-automation-training)*** 。如果您有兴趣将职业生涯转移到 RPA，您可以在此注册课程[，并开始学习。](https://www.edureka.co/robotic-process-automation-training)

*有问题吗？请在“ **UiPath Orchestrator** ”的评论区提出来，我会回复你。*