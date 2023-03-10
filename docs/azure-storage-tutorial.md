# Azure 存储教程 Microsoft Azure 中的表、Blobs、队列和文件存储

> 原文：<https://www.edureka.co/blog/azure-storage-tutorial/>

Azure Storage 是微软管理的云存储服务，如果您要手动管理它，它可以提供高度可用、持久、可扩展和冗余的存储，而成本只是它的一小部分。在这篇关于 Azure 存储的博客中，你将了解 Azure 的不同存储产品，比如*表、blob、文件存储*和*队列*！你也可以加入我们的 [Azure 培训！](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training)

最后，我们还在 Azure 中展示了所有这些服务。你也可以参考这篇教程来了解关于 Azure 存储的概述:

[https://www.youtube.com/embed/tbJWxcjfMpo?rel=0&showinfo=0](https://www.youtube.com/embed/tbJWxcjfMpo?rel=0&showinfo=0)

以下是我们今天要讨论的话题:

1.  [我们为什么需要储物？](#need)
2.  [存储 Vs 数据库](#vs)
3.  [什么是 Azure 存储？](#what)
4.  [天蓝色](#replication)
5.  [演示](#demo)

## **我们为什么需要储物？**

让我们通过一个例子来理解这一点，考虑以下架构:

![Architecture1 - Azure Storage Tutorial - Edureka](img/875250ca3532d7d268da7ed3bb6906fc.png)

这个架构是一个图像处理网站。我们尝试在两类服务器中分配负载，即网站服务器和后端服务器。网站服务器的唯一工作是处理我们网站的传入页面请求。后端服务器将处理任何与操作相对应的“处理”,在我们的例子中是图像处理。有两个未知的空白“实体”。

第一个实体将需要存储从我们的网站服务器传入的工作。这些作业将被后端服务器拾取以执行作业。一旦一个任务完成了，它就必须从这个实体中删除，这样就没有其他的服务器再去处理它，因为它已经被处理过了。

你可能会想，为什么我们不能把这个列表存储在后端服务器上呢？ 这是因为， 我们将需要多个后端服务器用于我们的用例。因此，这个列表必须出现在每个后端服务器上，并且在每个成功的作业完成时，所有的服务器都必须更新它们的列表。现在，这变成了一项艰巨的任务。

因此，我们需要一个更好的解决方案。因此，我们想出了一个所有后端服务器都可以访问的公共位置，在这里我们所有的作业都可以按照先到先服务的原则存储，这就是所谓的队列。

需要第二个未知实体来存储处理后的图像。 我们需要一些东西 能够以最小的处理开销存储我们的图像。 显而易见的答案是用于存储的文件系统。

最后，我们需要一个 ***队列*** 来存储我们的第一个实体，我们需要一个 ***文件系统*** 。但是，为什么我们需要文件系统而不是数据库来存储我们的图像或作业呢？

## **存储 vs 数据库**

![Storage vs Database - Azure Storage Tutorial - Edureka](img/33b67d2a1164def93e548fb07e18af10.png)

文件系统不仅需要较少的处理，而且易于访问。如果你在数据库中存储图像，每次你需要一个图像的时候，你就必须向数据库发出一个查询请求。想象一下文件系统的情况，它不会进行太多的处理，因为访问一个文件是非常简单和轻量的。此外，数据库存储比文件系统存储更昂贵。

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

## **什么是 Azure 存储？**

**Azure Storage** 是现代应用程序的云存储解决方案，这些应用程序依靠耐用性、可用性和可扩展性来满足客户的需求。

要使用 azure 中的存储，你首先需要的是一个**存储帐户。**

**存储账户**

![Storage Icon - Azure Storage Tutorial - Edureka](img/4ac854114fe0214e3f113ceaeece3f69.png)

要在 azure 中使用任何存储类型，你首先必须在 Azure 中创建一个帐户。创建帐户后，您可以在储存帐户中的服务之间传输数据。创建一个存储帐户，在云中存储多达 500 TB 的数据。使用 Blob 存储帐户和热或冷访问层 ，根据对象数据的访问频率优化成本。

存储账户可以有两种类型:

1.  通用目的
2.  斑点存储

我们来详细讨论一下每一个:

**通用存储账户**

通用存储帐户提供了一个空间，在这个空间中，您可以在一个统一的帐户中访问 blobs、队列、文件和表，以及所有这些服务。一个通用的存储账户可以用来存储对象数据，可以用作 NoSQL 数据存储，可以用来定义和使用队列进行消息处理，在云端设置 ***文件共享*** 。使用 [天蓝色课程](https://www.edureka.co/masters-program/azure-cloud-engineer-certification-training) 可以更好的理解。

如前所述，azure 中主要有 4 种存储类型:

*   表格
*   斑点
*   队列
*   文件存储

## **表**

![Tables - Azure Storage Tutorial - Edureka](img/bb5197fd372808dceadd6edcf54c7255.png)**Azure Table**存储服务存储大量结构化数据。该服务是一个 NoSQL 数据存储，接受来自 Azure cloud 内部和外部的认证调用。Azure 表非常适合存储结构化的非关系数据。

**![Blobs - Azure Storage Tutorial - Edureka](img/5947964b678171b54a4f594b2af2640d.png)Azure Blob**storage 是一种将非结构化数据作为对象/**Blob**存储在云中的服务。Blob 存储可以存储任何类型的文本或二进制数据，如文档、媒体文件或应用程序安装程序。 **Blob** 存储也称为对象存储。

## **队列**

![Azure Queue - Azure Storage Tutorial - Edureka](img/383d0659a7a22eede3c55dbc1d8da035.png)

**Azure Queue**storage 是一项用于存储大量消息的服务，这些消息可以通过使用 HTTP 或 HTTPS 的认证呼叫从世界任何地方进行 访问。单个**队列**消息的大小可以达到 64 KB，一个**队列**可以包含数百万条消息，达到一个存储帐户的总容量限制。

## **文件存储**

![File Service - Azure Storage Tutorial - Edureka](img/d764629553104217f772ee175a5e70af.png)

一个**文件存储**共享是 **Azure** 中的一个 SMB **文件**共享。所有目录和**文件**必须在父共享中创建。一个账户可以包含无限数量的份额，一个份额可以存储无限数量的**文件**，最多可达**文件**份额的 5 TB 总容量。

## **斑点存储**

Blob 存储帐户专门用于存储 Blob 数据，也可用于选择**访问层**，允许您指定访问帐户中数据的频率。您可以选择适合您的存储和费用的访问层。

有两种类型的访问层:

**![Rabbit - Azure Storage Tutorial - Edureka](img/7c5a71d34cf5a6ae98c1ff26708f4abf.png)**

**热:**此访问层为我们提供了最低的延迟。因此，它应该用于频繁访问的数据。自然，因为它提供低延迟，所以更贵。

![Turtle - Azure Storage Tutorial - Edureka](img/bc78fbda1df7daaf97812ff80a4fa7d8.png)

**冷:**此访问层的性能不如“热”访问层，即比以前的 访问层提供更高的延迟。也就是说，它的价格较低，因此可用于访问频率较低的数据。

接下来，这两种存储帐户类型，即 **blob 存储**和**通用存储帐户**，都被设计为高度可用。有了高可用性，您可以确保 azure 上托管的文件全天候可用。高可用性只有通过复制才能实现。

## **复制**

Azure 中基本有 4 种复制类型:

**本地冗余存储**

本地冗余存储(LRS)在一个存储规模单位内(即数据中心内)将您的数据复制三次。数据中心位于您创建存储帐户的区域。只有在写入所有三个复制副本后，写请求才会成功返回。这些副本中的每一个都驻留在一个存储扩展单元中独立的容错域和升级域中。

**区冗余存储**

分区冗余存储(ZRS)除了存储三个类似于 LRS 的副本之外，还可以在一两个区域内的数据中心之间异步复制您的数据，从而提供比 LRS 更高的耐用性。即使主数据中心不可用或不可恢复，存储在 ZRS 的数据也是持久的。

地理冗余存储(GRS)将您的数据复制到远离主区域数百英里的辅助区域。如果您的存储帐户启用了 GRS，则即使在整个区域中断或主区域不可恢复的灾难情况下，您的数据也是持久的。

**读取访问地理冗余存储**

读访问地理冗余存储(RA-GRS)通过提供对辅助位置数据的只读访问，以及 GRS 提供的跨两个区域的复制，最大限度地提高您的存储帐户的可用性。

好了，现在你已经有了所有你需要的信息。让我们开始吧，让我们的手指随着演示动起来吧！

## **演示**

我们将分两部分进行演示:

**第 1 部分:** 我们将尝试建立一个网站，将能够上传文件到 blob 服务。一旦文件被上传，文件的详细信息也将被添加到 Azure 队列中，这将用于在刷新时更改网页的背景。

**第一步:**就像我们之前提到的，第一步应该是创建你的存储账户。请按照下图中的说明进行操作。

1.  首先，在左侧窗格中点击存储账户
2.  然后，点击添加
3.  最后，输入所有相关字段并点击创建。

![Create Storage Account - Azure Storage Tutorial - Edureka](img/df9577a72f751158df95d01a43684f20.png)

**第二步:** 就是这样！我们已经成功创建了我们的存储帐户。我们的帐户中有四种类型的存储服务，即 Blobs、队列、文件和表。在这个 Azure 存储教程中，我将在这一部分演示 Blob 服务和队列服务。另外，关于详细的演示，请参考我们在博客开头附加的关于 Azure 存储教程的视频。让我们首先配置 blob 服务。转到您的存储帐户，然后单击 Blobs。

![Blobs Select - Azure Storage Tutorial - Edureka](img/cced4fd29730b1304ab1f86fb88513cf.png)

**第三步:**点击*容器*，创建一个新的容器。首先，输入容器的名称，这对于您将在这个特定帐户中创建的所有容器应该是唯一的。接下来，为其分配公共访问级别。Blobs 只不过是文件。如果您指定了 ***私人访问级别*** ，则只有您能够下载该容器的内容。如果您分配了 ***blob 访问级别，*** 任何链接到此帐户**的容器的用户都可以访问其中的文件**。使用 ***容器访问级别*** ，任何拥有链接**的用户都可以访问该容器内的文件和文件夹**。我们将为我们的演示选择 Blob 访问级别。最后，单击确定。

![Create Container - Azure Storage Tutorial - Edureka](img/c47cd1b43e5cb289d52a785cc50f33cc.png)

**第四步:** 在你的网站代码中指定你的存储账户的连接字符串。连接字符串对您的代码进行身份验证，以便与指定的存储帐户及其服务进行交互。为此，只需选择您的存储帐户，然后选择访问密钥，最后复制任何一个连接字符串。将这个连接字符串粘贴到您网站的代码中，就大功告成了！

![Connection String - Azure Storage Tutorial - Edureka](img/84c3bc1bb770ff9897a9bd30e28323b0.png)

**第五步:**现在开始排队吧。在您的存储帐户概述页面上，选择队列。

![Select Queues - Azure Storage Tutorial - Edureka](img/7b56da58fe62117673c90722e798a61a.png)

**第六步:**接下来，我们将创建一个队列。为此，单击 Add Queue，为队列指定一个相关的名称，然后单击 OK。最后，替换代码中的相关信息。

![Create Queue - Azure Storage Tutorial - Edureka](img/27bbc83600f921459b879afd341b053c.png)

**第七步:**这是我们做好的网站，选择你要上传的文件，点击上传。

![](img/0fe704850ebb388b714c99a88ecad5d7.png)

这是文件上传后屏幕的样子。

![](img/83300763147a536a348a119998dd6e2b.png)

这样，我们就成功地将我们的文件添加到了容器和队列中。您可以在下面的屏幕中看到相同的内容:

![Recieve Queue - Azure Storage Tutorial - Edureka](img/b6f38c4fcdacc1e710e53df8b5a75c27.png)

现在让我们检查一下在 blob 中是否也有一个条目:

![Blob Store - Azure Storage Tutorial - Eduerka](img/eeffb9858c742946551e54f23d87b092.png)

**第八步:**让我们进入网站中的流程页面，看看队列和 blob 中的条目是否可以读取，可以！如你所见，图像名称是相同的。

![Process - Azure Storage Tutorial - Edureka](img/e067b0d22908fa1ac7f1797f89001953.png)

至此，我们结束了演示的第 1 部分。让我们进入第 2 部分。

**第二部分:** 在这部分的 Az ure 存储教程中，我们将探索 azure 中的 ***文件服务*** 。**Azuure 中的**文件服务**使用 SMB 3.0 协议进行文件传输，该服务可以附加到您的 windows 操作系统上，就像它是一个外部驱动器一样。现在让我们在 Azure Portal 中尝试一下:**

**第一步:**进入您的存储账户概览页面，选择文件服务。

![Select File - Azure Storage Tutorial - Edureka](img/2a861c1ab74661684bf4c73216d42d5d.png)

**第二步:**在下一页，输入文件实例的名称，以及实例的大小。最后，单击确定。

![Create File Service - Azure Storage Tutorial - Edureka](img/5567f00bcc2bd79431a05acc9dbef553.png)

**第三步:**选择你的文件服务，然后点选连接。

![Connect - Azure Storage Tutorial - Edureka](img/4ce9bd88cabaabd93a9eb57bde5afed6.png)

在属性窗格中，复制如图所示的链接:

![Copy Connection - Azure Storage Tutorial - Edureka](img/9154fc2acece521a9e20296296d554b9.png)

并粘贴到记事本中，这样您就可以区分元素:

![Details - Azure Storage Tutorial - Edureka](img/0ad9f70f7896323116bf15415b4dfbe0.png)

*   第一点是地址栏
*   第二点是用户名
*   第三点是你的密码

保存这些细节，它们将用于本 azure 存储教程的下一步。

**第四步:**右键点击你桌面上的我的电脑图标，然后点击映射网络驱动器。

![Map Network Drive - Azure Storage Tutorial - Edureka](img/312b9ce2fe0c084e3f75ef9ae5a22e56.png)

**第五步:**在文件夹文本框中输入你从记事本复制的第一个点，点击完成。

![Enter Destination - Azzure Storage Tutorial - Edureka](img/a8d39e9ae7d91e8a28b22cb7cd641153.png)

**第六步:**下一步，从记事本中输入用户名和密码，最后点击确定。

![User Password - Azure Storage Tutorial - Edureka](img/277b1b823a98535a9cb27436d0e4c5e4.png)

**第七步:**恭喜你！你的 a zure 存储硬盘准备好了。您现在可以像使用计算机上的任何其他驱动器一样使用它了！

![Save Drive - Azure Storage Tutorial - Edureka](img/034517f9dfbc204fbb672c7feae5b7f7.png)

我们的演示到此结束。想了解更多关于 Azure 的信息吗？爱德华卡。是来帮你的！你可以在左边的菜单中查看我们的博客，我们已经广泛覆盖了突出的 Azure 服务，并且这个列表将会经常更新。

如果你是其中一员，想要向微软 Azure 认证的专业人士学习这项技术，并且是领先的行业专家，那么你来对地方了。我们在 edureka！致力于你的学习。我们提供 [Azure master certification](https://www.edureka.co/masters-program/azure-cloud-engineer-certification-training) 课程，帮助你获得认证，从而帮助你追逐梦想中的工作！

此外，如果你希望掌握 Azure 和 DevOps 的原理，并致力于对商业世界有重大意义的分步任务，行业专业人士开发了 [Azure DevOps 在线课程](https://www.edureka.co/microsoft-azure-devops-solutions-training) 。完成培训课程后，你可以申请全球薪酬最高的跨国公司顶级职位之一。

我们已经想出了一套课程，涵盖了你通过微软考试所需要的全部内容！你可以在这里看看微软[蔚蓝 T **霏霏**的课程详情。](https://www.edureka.co/microsoft-certified-azure-solution-architect-certification-training)

此外，这个 Azure 教程博客系列将随着我们关于 Azure 服务的博客部分的扩展而频繁更新，敬请关注！

*有问题吗？请在这个 Azure 存储教程的评论部分提到它，我们会回复你或者加入我们在布里斯托尔的 Azure 培训。*