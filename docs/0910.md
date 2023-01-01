# 关于 DDOS 你需要知道的一切

> 原文：<https://www.edureka.co/blog/what-is-ddos-attack/>

分布式拒绝服务，通常缩写为 DDOS，是一种[网络攻击](https://www.youtube.com/watch?v=Dk-ZqQ-bfy4)，因电影和互联网而臭名昭著。简单地说，这是一种任何种类的服务都被拒绝的情况。在这篇“什么是 DDOS 攻击”的文章中，我将全面解释这种攻击是如何工作的，并介绍它的不同类型。我还将演示如何在无线网络上执行自己的 DOS 攻击。以下是本文涵盖的主题:

*   [什么是 DOS & DDOS？](#what-is-ddos)
*   [它是如何工作的？](#working)
*   [DDOS 攻击的类型](#types)
*   [自己的 DOS 攻击](#demo)

## **什么是 DOS & DDOS？**

为了理解什么是 DDOS 攻击，理解 DOS 攻击的基础是很重要的。

**DOS**——简称**D**enial**O**f**S**service。这种服务可以是任何类型的，例如，想象一下你的母亲在你准备考试时没收你的手机，以帮助你不受任何干扰地学习。虽然你母亲的意图确实是出于关心和担忧，但你被拒绝提供电话服务和手机提供的任何其他服务。

就计算机和计算机网络而言，或者在[道德黑客](https://www.edureka.co/blog/ethical-hacking-tutorial/)活动期间，拒绝服务的形式可能是:

*   劫持网络服务器
*   请求使端口过载，导致端口不可用
*   拒绝无线认证
*   拒绝互联网上提供的任何服务



这种意图的攻击可以从一台机器上进行。虽然单机攻击更容易执行和监控，但也更容易检测和缓解。为了解决这个问题，可以从分布在广阔区域的多台设备上执行攻击。这不仅使阻止攻击变得困难，而且几乎不可能指出罪魁祸首。这种攻击被称为分布式拒绝服务或 **DDOS 攻击**。

## **它是如何工作的？**

如上所述，DOS 攻击的主要思想是使某项服务不可用。由于受到攻击的一切实际上都是在机器上运行的，如果机器的性能下降，服务就可能变得不可用。这是 DOS 和 d DOS 背后的基本原理。

一些 DOS 攻击通过向服务器发送大量连接请求来执行，直到服务器过载并被认为无用。其他攻击是通过向服务器发送无法处理的未分段数据包来执行的。当僵尸网络执行这些方法时，它们所造成的损害会呈指数级增加，并且它们减轻损害的难度也会突飞猛进。

为了更好地了解攻击的工作原理，让我们来看看不同的攻击类型。

## **DDOS 攻击类型**

虽然进行 DDOS 攻击的方法有很多，但我将列出一些更著名的方法。这些方法因其成功率和造成的损害而闻名。值得注意的是，随着技术的进步，越有创造力的人已经设计出越迂回的方法来执行 DOS 攻击。

以下是攻击的类型:

### **平之死**

根据 TCP/IP 协议，数据包的最大大小可以是 65，535 字节。死亡攻击的 ping 利用了这个特殊的事实。在这种类型的攻击中，当数据包片段相加后，攻击者发送的数据包会超过最大数据包大小。计算机通常不知道如何处理这些数据包，最终会死机，有时甚至完全崩溃。

### **反射攻击**

这种类型的攻击是在僵尸网络的帮助下进行的，在本例中，僵尸网络也被称为反射者。攻击者使用僵尸网络向大量无辜的计算机发送连接请求，看起来像是来自受害者的机器(这是通过在数据包报头中伪装来源来实现的)。这使得计算机主机向受害计算机发送确认。由于从不同的计算机到同一台机器有多个这样的请求，这使计算机过载并使其崩溃。这种类型也称为 smurf 攻击。

### ![Reflected Attack -DDOS Attack explained - Edureka](img/55b5205dba17b8036c80e00ed4771b66.png) **邮件炸弹**

邮件炸弹攻击通常攻击电子邮件服务器。在这种类型的攻击中，充满随机垃圾值的超大电子邮件被发送到目标电子邮件服务器，而不是数据包。这通常会使电子邮件服务器崩溃，因为负载会突然增加，在修复之前，它们会变得无用。

### **![Mailbomb -DDOS Attack explained - Edureka](img/01494933b9c448d52c6f49f9942519ae.png)泪珠**

在这种类型的攻击中，数据包的碎片偏移字段被滥用。IP 报头中的一个字段是“片段偏移”字段，指示包含在片段化分组中的数据相对于原始分组中的数据的起始位置或偏移。如果一个分段包的偏移量和大小之和不同于下一个分段包的偏移量和大小之和，则包重叠。当这种情况发生时，易受 teardrop 攻击的服务器无法重组数据包，从而导致拒绝服务情况。

匿名只是道德黑客的一件简单的事情&网络安全。如果您对这个领域感兴趣，请查看现场的 [CompTIA Security+认证培训](https://www.edureka.co/comptia-security-plus-certification-training)。

## **自己的 DOS 攻击**

在“什么是 ddos 攻击”这一节中，我将演示如何在无线网络上进行拒绝服务攻击，实际上是拒绝他们从特定接入点访问互联网。这种攻击是非法的，如果被抓住，你可能会被起诉，所以我敦促你在获得许可的情况下进行这种攻击，只是为了教育目的，而不是引起任何不必要的混乱。道德黑客的工作就是减轻这些攻击，而不是引发它们。

对于这种特殊的攻击，你需要一台 Linux 机器，你可以在一个虚拟机器上安装它或者双引导你的机器。还需要安装以下工具:

*   air crack-ng(apt-get install air crack-ng)
*   MAC changer(apt-get install MAC changer)

**第一步**:启动你的 [Linux](https://www.edureka.co/blog/ethical-hacking-using-kali-linux/) 机器，以 root 身份登录。登录后，检查您的网络接口卡的名称，对于我的情况是 **wlo1** 。您可以通过键入' *ifconfig '找到您的网卡名称。*

![step 1 - what is a ddos attack - edureka](img/b588f2b902a1a36dabef750c03be0726.png)

**第二步**:现在我们知道了网络接口卡的名称，我们需要将它设置为监控模式。有关命令，请参见下图。

![step 2 - what is a ddos attack - edureka](img/b41a9617eba4b818e0cb0e0e05fff7db.png)

**第三步**:在监控模式下成功设置您的接口卡后，检查可能会干扰我们扫描的进程。用他们的 PID 杀死他们。检查图片中的命令。继续杀死进程，直到一个也不剩。

![step 3 - what is a ddos attack - edureka](img/42a32c4298c837553397070273eac910.png)

第四步:现在我们需要扫描可用的接入点。我们需要通过选择接入点的 BSSID 来从该列表中选择接入点。要运行扫描，你必须输入' ***airodump-ng wlo1** '。你必须使用你的接口名，而不是 wlo1。*

![step 4 - what is a ddos attack - edureka](img/12d618aab97537981bd05b3261bcc4ad.png)

**第五步**:选择好想要进行 DOS 攻击的无线接入点后，复制下 BSSID，打开一个新的终端窗口。在这里，我们将持续取消所有设备的身份认证，这些设备将无法使用该特定接入点连接到互联网，简而言之，拒绝它们在互联网上的任何服务以及互联网本身。确保您的网卡也运行在相同的通道上。查看代码的截图。

![step 5 - what is a ddos attack - edureka](img/fdb0ba378bff378c7158fda52bae277a.png)

这就把我们带到了“什么是 DDOS 攻击？”博客。关于[网络安全](https://www.edureka.co/blog/what-is-cybersecurity/)的更多信息，你可以看看我的其他[博客](https://www.edureka.co/blog/?s=cybersecurity)。如果您希望学习网络安全并在这一领域建立丰富多彩的职业生涯，那么请查看我们的 [***网络安全认证培训***](https://www.edureka.co/cybersecurity-certification-training) ，该培训带有讲师指导的现场培训和真实项目经验。本培训将帮助您深入了解网络安全，并帮助您掌握该主题。

*你也可以看看我们新推出的关于[**CompTIA Security+**](https://www.edureka.co/comptia-security-plus-certification-training)的课程，这是 Edureka & CompTIA Security+之间的首次官方合作。它为您提供了一个获得全球认证的机会，该认证侧重于安全和网络管理员不可或缺的核心网络安全技能。*

<article class="maincontentblog">Got a question for us? Please mention it in the comments section of the “What is DDOS attack?” blog and we will get back to you.</article>

<article>Learn Cybersecurity the right way with Edureka’s [**POST-GRADUATE PROGRAM** with **NIT Rourkela**](https://www.edureka.co/post-graduate/cybersecurity) and defend the world’s biggest companies from phishers, hackers and cyber attacks.</article>