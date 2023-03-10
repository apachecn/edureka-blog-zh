# 亚马逊 VPC 教程-保护您的 AWS 环境

> 原文：<https://www.edureka.co/blog/amazon-vpc-tutorial/>

*“Security is the forefront of innovation.“*

**AWS 集中了大量精力来确保他们的客户不会成为数据泄露的受害者。当某些资源需要与合同工或第三方公司共享时，安全性变得更加重要，因为您面临着将敏感数据暴露给他们的风险。在这篇亚马逊 VPC 教程中，我将解释如何在 AWS 上创建一个隔离空间，并为这些用户提供访问权限。**

***如果你有兴趣了解更多关于云计算的知识，可以看看 Edureka 的[直播课程。](https://www.edureka.co/cloud-computing-certification-courses)***

**在 AWS 云基础设施中，亚马逊 VPC 也可以被视为您的私有网络。安全性是顶尖的，因为有亚马逊照顾。在这篇文章中，我将讨论 AWS 作为亚马逊 VPC 的一部分所提供的以下服务。**

***   [亚马逊 VPC 及其类型](#Amazon-VPC-And-Its-Types)*   [子网及其效用](#Subnet-And-Its-Utility)*   [什么是路由表？](#What-Is-Route-Table)*   [什么是互联网网关？](#What-Is-Internet-Gateway)*   [演示:使用 AWS 控制台创建 VPC。【T2](#Creating-A-VPC-Using-AWS-Console)*   [演示:创建一个非默认 VPC，并在 VPC 内部创建一个私有和公共子网。](#Creating-A-VPC-From-Scratch)**

**让我们详细讨论一下亚马逊 VPC 教程中的每一个组件。**

## ****亚马逊 VPC 及其类型****

**AWS 提供了很多服务，这些服务足以运行你的架构。该架构的安全基础是 VPC(虚拟私有云)。VPC 基本上是 AWS 环境中的一个私有云，帮助您在您定义的私有空间中使用 AWS 的所有服务。您可以控制虚拟网络，还可以使用安全组限制传入流量。**

**总的来说，VPC 可以帮助您保护您的环境，并让您完全控制传入的流量。有两种类型的 VPC，默认 VPC 是由 Amazon 创建的，非默认 VPC 是由您创建的 以满足您的安全需求。**

## ****AWS 网络基础| AWS VPC | AWS 网络服务| Edureka****

****

**[//www.youtube.com/embed/HD8flZnbQqg?rel=0&showinfo=0](//www.youtube.com/embed/HD8flZnbQqg?rel=0&showinfo=0)****This “AWS Networking Fundamentals” video by Edureka will give you an idea about a few of the important Networking Services available in AWS such as VPC, Elastic Load Balancing, Direct Connect, Route 53 and will also talk about AWS VPC in detail with a demo.**

**现在你已经了解了 VPC 是如何运作的，我将带你了解亚马逊 VPC 提供的不同服务。**

## ****子网及其效用****

**子网就像是将一个大型网络分成多个子网。与维护大型网络相比，维护小型网络更容易。**

**以一个组织为例。有财务、支持、运营、 技术、 HR、销售&营销等不同的团队。技术团队可以访问的数据不能提供给销售&营销团队，人力资源团队的数据不能提供给运营团队，反之亦然。在这里，您可以创建子网，从而使 访问和维护网络变得更加容易。**

**现在，我将向你展示这种隔离是如何进行的。有不同的组件用于授权和限制访问。让我带你看一下每一个。**

## ****什么是路由表？****

**路由表可以被理解为包含用于在子网内外路由流量的规则的表。路由表也用于将互联网网关添加到子网中。一个 VPC 中可以有多个路由表。**

**现在您已经了解了路由表的工作原理。让我们继续亚马逊 VPC 教程，了解互联网网关，看看它如何帮助管理流量。**

## ****什么是互联网网关？****

**互联网网关是一个非常重要的组件，它允许您的实例连接到互联网。它允许用户通过提供到 internet 的路由来公开子网。借助 Internet Gateway，实例可以访问 Internet，实例外部的资源也可以访问实例。**

**总的来说，互联网网关是 VPC 非常重要的组成部分。 现在，您已经了解了 VPC 的所有不同组成部分，让我们来看看如何为自己创建一个。**

**现在你已经了解了亚马逊 VPC 的组件，让我们继续学习亚马逊 VPC 教程，了解如何使用默认设置和公共子网创建 VPC。**

## ****演示:使用 AWS 控制台**创建 VPC**

**使用 AWS 控制台创建 VPC 非常简单。只需点击几下鼠标。让我向您介绍一下这个过程:**

****步骤 1:** 导航至 VPC 仪表盘。在这里你会看到一个"**启动 VPC 向导**点击它。**

**![Create VPC-Amazon VPC Tutorial-Edureka](img/2a6a82ba17ffa02f608cb9e8c309d97f.png)**

**VPC 仪表盘-亚马逊 VPC 教程**

****第二步:**这是 *VPC 创作*的向导。在这里你可以找到 4 个不同的选项:**

***   我们将要选择的具有单一公共子网的 VPC。*   带有公有子网和私有子网的 VPC。*   具有公共和私有子网以及硬件 VPN 访问的 VPC。*   只有私有子网和硬件 VPN 访问的 VPC。**

**因此，让我们从创建一个带有单个公共子网的 VPC 开始。点击*选择*。**

**![Create VPC-Amazon VPC Tutorial-Edureka](img/d93560e76fa12994a7f2d0da2ce3ad37.png)**

****第三步:**这里你要提到一些创建 VPC 的细节。**

***   IP v4 CIDR 区块*   VPC 的名字*   公共子网的 IPv4 CIDR*   您希望在其中创建 VPC 的可用性区域*   子网名称*   硬件租赁**

**提到所有细节后，点击*创建 VPC* 。**

**![Create VPC-Amazon VPC Tutorial-Edureka](img/e964b77071ab2b464e19e986d533fde9.png)**

****第四步:**你会得到一条信息“*你的 VPC 已经成功创建*”。点击*确定*。**

**![Create VPC-Amazon VPC Tutorial-Edureka](img/4721eef2fad180b3186986ace6164427.png)**

****第五步:**在“你的 VPC”部分，你可以看到有一个名为“ *EdurekaDemo* 的新 VPC 被创建。**

**![Create VPC-Amazon VPC Tutorial-Edureka](img/d870e5029724e943d20abb4d7976299a.png)**

****第六步:**现在我们来验证一下公有子网。您可以看到创建了一个名为“Public Subnet”的子网。该子网附有一个路由表，其中包含带有互联网网关的本地和公共访问。**

**![Create VPC-Amazon VPC Tutorial-Edureka](img/593eadd52d2b0e45915925f75b3bb812.png)**

**这样，VPC 就创建了一个公共子网。很容易不是吗？**

**现在，让我们转到亚马逊 VPC 教程的另一个演示，并找出从头开始创建 VPC 的另一种方法。在这里，我将向您展示如何手动创建一切。**

## ****演示:创建非默认 VPC，并在 VPC** 内创建私有和公共子网**

**让我们走一条长路，创建一个有两个子网的非默认 VPC，一个公有，一个私有。**

****第一步:**导航到 *[你的 VPC](https://console.aws.amazon.com/vpc/home?region=us-east-1)* ，点击*创建 VPC* 。**

****![Create VPC-Amazon VPC Tutorial-Edureka](img/a9147554de7e708b3e1e9cd7ccd792e0.png)****

**创建 VPC-亚马逊 VPC 教程**

****第二步:**给你的 VPC 起个名字，提一下 IPv4 CIDR 块。点击“创建”。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/24478aa112f726cc38f07a3e4de19f7f.png)****

**创建 VPC-亚马逊 VPC 教程**

****第三步:**你得到一个消息*下面的 VPC 是用你的 *VPC ID* 创建的*。点击*关闭*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/1f34f87cb681d49078bb4e34189bcd69.png)****

**创建 VPC-亚马逊 VPC 教程**

****第四步:**现在，创建子网。为此，导航到“*子网*，在“*VPC 过滤*”中，选择您的 VPC，然后您将看到没有子网。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/240f13e3cb2b87100811fc9b37480562.png)****

**VPC 仪表盘-亚马逊 VPC 教程**

****第五步:**创建一个名为 Private 的子网。选择您的 VPC、可用性区域和 IPv4 CIDR 块。点击*创建*。**

****![](img/d426854a34847d403b69b3b2c72d1780.png)****

**您将收到一条消息，显示“*以下子网已创建*”，以及“*子网 ID* ”。点击*关闭*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/fd7388a15936fdd66ffcc3c901d1e9eb.png)****

****第六步:**创建一个公共子网，按照我创建私有子网时的做法，填写所有相关的详细信息。点击*创建*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/a1eb6c8646e6bd25ea4c6877853aae5f.png)****

**您将收到一条消息，提示“*以下子网是由“*创建的，子网 ID 为“”。点击*关闭*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/00cefdc939d435ada99d26bc355ef049.png)****

****第 7 步:**现在我们必须创建一个互联网网关，使子网公开。**

**导航至互联网网关，点击创建*互联网网关*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/96948be93688c50110853449097e7ed4.png)****

**为您的互联网网关命名。点击*创建*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/3191f75bd11762c5d2e8c56f3297ff0a.png)****

**您将收到一条消息，提示“*以下互联网网关已创建”*，以及“*互联网网关 ID* ”。点击*关闭*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/ccfc707b06c03aaf51c3f8c38d839581.png)****

****第八步:**仅仅创造一个互联网网关是不够的。你必须将互联网网关连接到 VPC 上。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/0ac6372d98ef59324853d8d5ab9b0f00.png)****

**选择您要连接互联网网关的 VPC。点击*附上*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/7b9bc6a51da203da2687145f80b5e061.png)****

****第 9 步:**现在，您已经将互联网网关连接到了您的 VPC，是时候制定使用路由表管理流量的规则了。导航到路由表，点击“*创建路由表*”。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/cba7d6820c0e2a9a643ea3f07ad0230b.png)****

**为您的路由表命名，并选择路由表适用的 VPC。点击*创建*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/74dea8e6b40b24d880e81618b8841f06.png)****

**您将收到一条消息“*以下路由表已创建*”和“*路由表 ID* ”。点击*关闭*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/26cd7ce26568df9ccdeafa26b11c1f24.png)****

****第十步:**现在你已经创建了一个路由表。添加用于管理流量的路由。导航至“*路线*，点击“*编辑路线*”。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/0c86dd6dba57a7d535b46909c976a2ab.png)****

**点击*添加路线*并提及目的地 **0.0.0.0/0** ，因为您希望它对公众开放，然后选择目标作为您之前创建的互联网网关。点击*保存路线*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/94d0196be09cb7f262256aeb7330f8f5.png)****

****第 11 步:**现在规则已经添加到路由表中，该将其附加到公共子网了。选择公共子网，导航到路由表，点击“*编辑路由表关联*”。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/10d2782f38e1417c4914d405c9a45cfb.png)****

**选择路由表，点击*保存*。**

****![Create VPC From Scratch-Amazon VPC Tutorial-Edureka](img/cb50d7849aeb2bc5dbca4b62a08a1241.png)****

**您已经成功地公开了子网。**

**通过这种方式，你可以走很长的路来创建一个有两个子网的亚马逊 VPC，一个公共子网和一个私有子网。**

***我希望你对亚马逊 VPC 及其组件有一个简要的了解。 如果您希望了解更多关于云计算的知识，并在云计算领域建立自己的事业，那么请查看我们的[云计算课程](https://www.edureka.co/cloud-computing-certification-courses)，该课程提供有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解云计算，并帮助您掌握这门学科。***

***有问题吗？请在评论区提及，我们会回复您**或**在[**edu reka | Community**](https://www.edureka.co/community)发布您的问题。在 Edureka 社区，我们有超过 100，000 名技术狂热分子随时准备提供帮助。***