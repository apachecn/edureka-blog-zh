# Power BI 架构:如何致力于数据安全

> 原文：<https://www.edureka.co/blog/power-bi-architecture/>

[Power BI](https://www.edureka.co/blog/what-is-power-bi/) 是微软的数据可视化、报告和分析工具及服务的总称。Power BI 可以从各种来源导入数据，并组织它们来运行查询、构建报告仪表板和数据可视化。Power BI 有一组可用于不同平台和用途的组件。在本 Power BI 架构[教程](https://www.edureka.co/blog/power-bi-tutorial/)中，我们将了解以下主题:

*   [**什么是微软 Power BI 架构？**](#what)
    *   [**Web 前端集群**](#front-end)
    *   [**后端集群**](#back-end)
*   [**数据存储安全**](#security)
*   [**用户认证**](#user)
*   [**数据&修复安全**](#repair)

那么，让我们开始这篇 Power BI 架构教程吧。

## **什么是微软 Power BI 架构？**

Power BI 架构是基于 Azure 构建的服务。Azure 是微软的云计算基础设施和平台。

该服务设计基于两个集群——在线前端(Web 前端)集群和 T2 后端(后端)集群。Web 前端集群负责对 ability bismuth 服务的初始关联和认证，并且一旦被记录，后端集群处理所有产生的用户交互。

**Power BI gateway** 将内部数据源连接到 Power BI 桌面或 Power BI 云服务，以获得用于报告和分析的连续数据。

![power bi architecture](img/a0fb77dedbcb616320172270c3f8d2f6.png)Power BI 架构使用**Azure Active Directory(AAD)**来存储和管理用户身份。它还管理知识和数据受害者的存储 **Azure BLOB** 和 **Azure SQL** 信息。

您可以浏览一下这份 Microsoft Power BI 记录，其中我们的专家通过示例详细解释了这些主题，这将有助于您更好地理解这些概念。

[https://www.youtube.com/embed/3u7MQz1EyPY](https://www.youtube.com/embed/3u7MQz1EyPY)

## **Web 前端集群** **: Power BI 架构**

Web 前端负责初始连接、客户端认证和请求路由到 Power BI 中最近的数据中心。 Power BI 使用 **Azure 流量管理器(ATM)** 将用户流量定向到最近的数据中心，该数据中心由试图连接到 Power BI 进行身份验证流程并下载静态内容和文件的客户端的**域名系统(DNS)** 记录确定。Power BI 还使用 **Azure 内容交付网络(CDN)** 根据地理位置向用户高效分发必要的静态内容和文件。

## **![front end cluster](img/3615a511e8186eb2fdca3aba3bc72868.png)后端集群:** **电力 BI 架构**

后端集群管理 Power BI 服务中的可视化、用户仪表板、数据集、报告、数据存储、数据连接和数据刷新。

**Power BI 网关**将内部数据源连接到 [Power BI 桌面](https://www.edureka.co/blog/power-bi-desktop/)或 Power BI 云服务，以获得用于报告和分析的连续数据。它基本上充当用户和 Power BI 服务之间的网关。除了网关角色，用户不直接与任何角色进行交互。![power bi architecture - back end cluster](img/45525205fd3b53a28b02a66a195a1280.png)

所有数据都存储在 Azure BLOB 存储和用户 Azure 存储帐户中，并由 Azure Active Directory 进行身份验证。

## **数据存储安全**

Power BI 体系结构使用两个主要存储库来存储和管理知识。

从用户上传的数据通常被发送到 Azure BLOB 存储，每个人的数据作为系统本身的工件保存在 Azure SQL 信息中。

后端集群图像中的线(如前一部分虚线左侧所示)阐明了 square 度量的用户可访问的唯一 2 个元素与 square 度量的系统仅可访问的角色之间的边界。

一旦关联文档用户连接到服务，消费者的关联和任何请求都由**网关角色**接受和管理，最终由 **Azure API 管理处理。**

然后，它代表用户与服务的其余部分进行交互。此外，一旦消费者试图查看仪表板，网关角色接受该请求，然后单独向**演示角色**发送邀请函，以检索浏览器呈现仪表板所需的信息。

## **用户认证**

用户通过用于建立其 Power BI Services 帐户的电子邮件地址登录服务。

Power BI 用户的体系结构因为有效用户名而登录电子邮件，每当用户试图访问一条信息时，该用户名被传递给资源。有效用户名被映射到一个**用户主体名称(UPN)** ，所有与 windows 域帐户相关联的解析都应用于它。

对于使用工作电子邮件登录 Power BI 架构的组织(如 username@mail.com)，有效的用户名到 UPN 的映射非常容易。对于无法使用工作电子邮件登录 Power BI 体系结构的组织，AAD 和内部凭据之间的映射将强制对其进行目录同步。

面向架构的平台安全性包括多租户环境安全性和网络安全性，因此能够提供额外的基于 AAD 的安全措施。

## **数据和修复安全**

如本文前面所述，本地 Active Directory 服务器使用用户的 Power BI 体系结构登录来映射到凭证的 UPN。然而，重要的是要注意到用户对他们的分享承担责任。如果连接到数据源的用户牺牲其凭据并共享支持该数据的报表，则共享仪表板的用户不能被授予对该报表的访问权限。

一个例外是与**SQL Server associate analysis Services 的连接。对底层报告或数据集的访问为试图访问报告的用户启动身份验证。并且如果用户具有访问信息的备用凭证，则可以单独授予访问权。**

所以，这就是微软 Power BI 架构教程。希望你喜欢这个解释。

*如果您希望学习 Power BI，并在数据可视化或 BI 领域建立职业生涯，请查看我们的 [**Power BI 课程**](https://www.edureka.co/power-bi-training) ，该课程提供有讲师指导的现场培训和真实项目经验。本培训将帮助您深入了解 Power BI，并帮助您掌握该主题。*

*有问题吗？请在评论区提到它，我们会给你回复。*