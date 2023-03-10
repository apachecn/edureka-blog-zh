# 面向初学者的 Azure 虚拟网络–使用 VPC 保护您的应用程序

> 原文：<https://www.edureka.co/blog/azure-virtual-network-tutorial/>

欢迎来到蔚蓝虚拟网的这个博客。 在这篇博客中，你将学习如何使用 Azure 虚拟网络保护你的应用程序。在继续之前，让我们先了解一下，为什么我们首先需要虚拟网络。

## **为什么要虚拟网络？**

虚拟网络充当云中启动的资源之间的通信渠道。为什么虚拟？因为云中没有实际的路由器或交换机。例如、如果你在云端启动一个数据库服务器和一个网站服务器、、，它们就需要一个媒介来交互。这种交互媒介被称为虚拟网络。

**同虚拟网络:**

## **![With Virtual Network - Virtual Networks - Edureka](img/5909b4e9642c395188e654fb62c38069.png)**

## **什么是 Azure 虚拟网络？**

**Azure 虚拟网络** ( **VNet** )是你自己的网络在云端的一种表示。它是专用于您的订阅的 **Azure** 云的逻辑隔离。

![Virtual Networks - Azure Virtual Networks - Edureka](img/a6b0c195844061bc8d5970eb5907386b.png)

你在定义中看到了一些沉重的词汇，例如，“逻辑隔离”和“你自己网络的表现”。暂时忘记定义，只要记住这个:

如果两台计算机必须相互交互，它们需要有权限。您可以在虚拟网络设置中添加/删除这些权限。一旦这些 权限被加上 ，就把这些电脑纳入这个虚拟网络，瞧！你准备好了。这三行是对我们今天要完成的任务的总结。

您可以浏览一下 Azure 虚拟网络的这段录音，在这段录音中，我们的 *Azure 认证*专家已经用示例详细解释了这些主题，这将有助于您更好地理解这个概念。或者你也可以参加我们的 [Azure 培训！](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training)

## **蔚蓝虚拟网教程|蔚蓝培训| Edureka 直播**

[https://www.youtube.com/embed/kj1iW0ovjEw?rel=0&showinfo=0](https://www.youtube.com/embed/kj1iW0ovjEw?rel=0&showinfo=0)

接下来，虚拟网络被进一步划分为多个组件。

## **虚拟网络组件**

以下是虚拟网络组件:

*   子网
*   网络安全组

## **什么是子网？**

**![Subnet - Azure Virtual Networks - Edureka](img/116acc81869e3b095568b359c4304aad.png)**

每个虚拟网络可以被分成子部分，这些子部分被称为子网。

子网可以进一步分为:

*   **私有子网**——没有互联网接入的网络。

*   **公共子网**——有互联网接入的网络。

让我们看一个例子，了解虚拟网络实际上是如何使用的:

![Subnets - Azure Virtual Networks - Edureka](img/a7221623cff8d5771b260a9a2bd3a771.png)

在上图中，一个虚拟网络被划分为多个子网，每个子网包含一台服务器。

*   **子网 A** 是一个网络服务器，因此它是一个公共子网，因为你的网站可以通过互联网访问。
*   **子网 B** 是一个数据库服务器，因为数据库应该能够连接到 web 服务器，所以不需要互联网连接，因此它是一个私有子网。

您可能想知道，在哪里进行所有这些设置，允许哪些连接，不允许哪些连接，对吗？这就是第二个组件出现的地方，即网络安全组。

**了解我们在顶级城市/国家的 Microsoft Azure 培训**

| **印度** | **美国** | **其他城市/国家** |
| [班加罗尔](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-bangalore) | [纽约](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-new-york-city) | [英国](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-uk) |
| [海德拉巴](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-hyderabad) | [芝加哥](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-chicago) | 伦敦 |
| [德里](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-delhi) | 亚特兰大 | [加拿大](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-canada) |
| [钦奈](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-chennai) | [休斯顿](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-houston) | [多伦多](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-toronto) |
| [孟买](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-mumbai) | 洛杉矶 | [澳大利亚](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-australia) |
| [浦那](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-pune) | [波士顿](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-boston) | 阿联酋 |
| 加尔各答 | [迈阿密](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-miami) | [迪拜](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-dubai) |
| 艾哈迈达巴德 | [旧金山](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-san-francisco) | [菲律宾](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training-philippines) |

## **网络安全组**

这是您进行所有连接设置的地方，比如打开哪些端口，默认情况下所有端口都是关闭的。不要害怕，这个博客会指导你完成所有的设置，而且所有的设置都非常容易。

但首先，让我向您展示虚拟网络的最终架构:

![Architecture - Virtual Networks Tutorial - Edureka](img/87494355f5fa3ddb7304f0a45a53fcbb.png)

虚拟网络是这样工作的:

*   首先你创建一个虚拟网络。
*   然后，在这个虚拟网络中创建子网。
*   您将每个子网与各自的虚拟机或云实例相关联。
*   将相关的网络安全组连接到每个子网。
*   在 NSG 中配置属性，一切就绪！

现在让我们通过一个演示来尝试一下。

## **演示**

我们将在虚拟网络中部署两台服务器，一台数据库服务器和一台网站服务器，它们将相互交互。你甚至可以用 [Azure 云工程师认证](https://www.edureka.co/masters-program/azure-cloud-engineer-certification-training) 查看 Azure 的详细信息。让我们看看如何构建这个网络。

**第一步:**首先，我们将创建一个网络安全组。转到你的 A zure 仪表盘，按照下图中的步骤操作。

![Select NSG - Azure Virtual Networks - Tutorial](img/74b1c203caae012369d8980025818e51.png)

**第二步 :** 接下来，你将到达这个屏幕，其中你将在 你的 NSG 中填充所有的细节 ，最后点击创建。注意在第二步的图像中，您正在创建一个资源组。试着把你所有的资源放在同一个组里，这样更容易管理。

![Create NSG - Azure Virtual Networks Tutorial - Edureka](img/26536c4229e2ddb942a4c1cd7b03a83e.png)

**第三步:**我们现在将创建一个虚拟网络，按照下图中的说明创建一个。请记住，在资源组中选择“使用现有的”，然后选择您之前创建的同一资源组。

![Create VNet - Virtual Networks Tutorial - Edureka](img/715c02a4e91070dd2c881bf8a79ba896.png)

**步骤 4:** 接下来，我们将创建 2 个子网，一个用于我们的网站，一个用于我们的数据库。遵循下图中的步骤:

![Create Subnet - Virtual Networks Tutorial - Edureka](img/7bf5c9b4fa8a1c2d388a6b0b6c142a1b.png)

**步骤 5:** 在下一个屏幕上，创建两个子网。按照相同的步骤，一个用于数据库，一个用于 web 服务器。此外，附加相应的网络安全组。

![Create Subnet2 - Virtual Networks Tutorial - Edureka](img/5b8f8d712ddec30a49ea6ee396cfee35.png)

**第六步:**好了，我们的网络设置好了，我们现在要做的就是配置网络安全组，并在这个虚拟网络中创建我们的服务器。让我们首先创建 web 服务器。

![Add VM - Azure Virtual Networks Tutorial - Edureka](img/18b2d319f507cd44284a17c07270775d.png)

**第七步:**在下一个屏幕上，选择你喜欢的操作系统。对于我们的演示，我们将选择一个 Ubuntu 操作系统。最后点击创建。

![Create VM1 - Virtual Networks Tutorial - Edureka](img/db91a4dcc132922a9d370279ce495aa0.png)

**第八步:**在第一页输入所有相关信息:

![Create VM2 - Virtual Networks Tutorial - Edureka](img/a63467563a23af43088d41c0dd5aad1e.png)

接下来，选择相关配置。我们选择最基本的配置，因为这是一个演示:

![Create VM3 - Virtual Networks Tutorial - Edureka](img/db5045d24f7913af6722ef69a77f6b65.png)

**第 9 步:**在下一页，您将选择要部署虚拟机的虚拟网络。

![Create VM4 - Virtual Networks Tutorial - Edureka](img/384e4092a17a0b62cad5e34ebc0a16ba.png)

接下来，选择子网:

![Create VM5 - Virtual Networks Tutorial - Edureka](img/1495bc6f04feb06d954fccba516465ae.png)

打开网络安全组窗格，选择“无”选项，因为我们已经将网络安全组连接到我们的虚拟网络。最后，单击 Ok，您的虚拟机将开始部署。对您的数据库服务器也做同样的事情。

![Create VM6 - Virtual Networks Tutorial - Edureka](img/eb6824facec7b5023227a59a3ff63c02.png)

**第十步:**你可以浏览博客开头所附的视频，了解如何配置 webserver 和 DB server，它们会指导你如何做同样的事情。让我向你展示我的网络服务器安全组现在的样子:

![NSG - Virtual Networks Tutorial - Edureka](img/30dcade2d2d17caf8ec286b753e51b77.png)

由于到目前为止入站安全规则中没有添加任何内容，如果我尝试使用 IP 地址连接到我的服务器，我会得到以下错误:

![NSG1 - Virtual Networks Tutorial - Edureka](img/a8b485a1aeaf9978085f56da77d6166e.png)

**步骤 11:** 添加任何连接属性，如下图:

![NSG2 - Virtual Networks Tutorial - Edureka](img/0a9fb9c84b0fa2e34e508c278595efea.png)

我已经添加了以下连接:

![](img/317b46a353d860119be3673705d1ceb4.png)

要访问您的网站，您需要添加 HTTP 和 HTTPS。最后，您需要 SSH 来配置您的服务器。如果我现在尝试连接我的网络服务器，我会看到下面的屏幕:

![NSG5 - Virtual Networks Tutorial - Edureka](img/6f1899eeb47f8e3c06027ded95b792fc.png)

这是 SSH 窗口:

![NSG3 - Azure Virtual Network Tutorial - Edureka](img/f3af279fc60d56d5f600fdd7ab89f331.png)

**第十二步:**这是我的数据库网络安全组的样子:

![NSG6 - Azure Virtual Network Tutorial - Edureka](img/494c730eaedc42ef0077cb1bb2820c38.png)

详细的演示，可以参考博客开头的视频。请放心，这是您配置虚拟网络的方式。

想了解更多信息？我们在 edureka！ *提出了一套课程，涵盖了你通过微软考试所需要的全部内容！关于 [**微软 Azure 认证**](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training) 培训的 [Azure 云工程师课程](https://www.edureka.co/masters-program/azure-cloud-engineer-certification-training)详情可以在这里看一下。*

此外，这个 Azure 虚拟网络博客系列将随着我们关于 Azure 服务的博客部分的扩展而频繁更新，敬请关注！

*有问题吗？请在这个 Azure 虚拟网络博客的评论部分提到它，我们将会回复你或者今天参加我们在贝尔法斯特的 Azure 培训。*