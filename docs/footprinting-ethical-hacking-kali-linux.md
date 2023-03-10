# 足迹——道德黑客的底层结构

> 原文：<https://www.edureka.co/blog/footprinting-ethical-hacking-kali-linux/>

这篇博客将讲述如何从道德黑客开始。我将讨论足迹的阶段，以及收集关于您想要测试漏洞的应用程序的信息的一些方法。要详细了解其他阶段，请查看[爱德华卡的](https://www.edureka.co/cybersecurity-certification-training) 网络安全培训 *。*

本博客涉及的主题有:

*   [什么是足迹？](#WhatisFootprinting)
*   [为什么足迹很重要？](#WhyisFootprintingimportant)
*   [足迹的种类](#TypesofFootprinting)
*   [如何采集足迹中的信息？](#HowtoGatherInformationinFootprinting)

## **什么是足迹？**

假设你是一名著名的道德黑客，你得到一份检查 Web 应用程序漏洞的工作。你得到你要测试的网站的组织的名字。您将如何开始测试网站的漏洞？你可以从收集关于那个网站的信息开始。这就是足迹。

足迹是道德黑客的[侦察](https://www.edureka.co/blog/what-is-ethical-hacking/#reconnaissance)阶段的一部分，在这个阶段你收集关于系统/应用的信息。足迹的主要目的是收集尽可能多的关于系统/应用程序的信息，以缩小攻击的范围和技术。

大多数人觉得足迹很无聊，但它是道德黑客行为中非常重要的一部分。下一节将告诉你为什么。

## **为什么足迹很重要？**

足迹被认为是道德黑客行为最重要的阶段之一。我们以一个电影情节为例。假设你正在看一部银行抢劫电影，里面有计划抢劫银行的人。像《十一罗汉》、《意大利人的工作》或者《速度与激情》这样的电影，人物是不是直接买枪和面具进银行抢劫？不要！如果他们这样做了，他们就不可能成功地抢劫银行。

那么他们在抢银行之前会做什么？他们就如何进入银行，如何处理安全问题制定了一个适当的计划，并准备了一个逃跑计划。为了计划抢劫，他们需要观察银行的某些事情，银行的运作方式，安全系统如何工作等等。了解银行在制定计划时起着重要的作用。

同样，了解系统/应用程序对于道德黑客攻击非常重要，因为这将让您知道可以找到什么类型的漏洞，以及什么样的攻击是合适的。

现在你已经了解了什么是足迹以及它为什么重要。如果你很想知道道德黑客的足迹，今天就加入在线的[道德黑客课程。](https://www.edureka.co/ceh-ethical-hacking-certification-course)

是时候了解一下不同类型的足迹了。

## **足迹的种类**

类似于侦察，足迹可以分为两种:

1.  **主动足迹**
2.  **被动足迹**

### **主动足迹**

主动足迹是一种通过直接与系统交互来收集系统/应用信息的足迹。当您使用主动足迹时，您试图收集信息的系统很可能会保存一些信息，如您的 IP 地址。

### **被动足迹**

在被动足迹的情况下，您在没有与您试图了解的系统/应用程序互动的情况下收集信息。你通过搜索引擎或公共记录收集信息。当您使用被动足迹时，系统无法保存您的 IP 地址。

现在你已经了解了足迹的基本知识，不再拖延，让我们开始足迹的实践部分

## **如何采集足迹中的信息？**

在这一部分，我将向你展示一些收集信息的方法。为此，我将使用 Kali Linux 操作系统。如果你没有 Kali Linux，你可以[访问这个链接](https://www.edureka.co/blog/how-to-install-kali-linux/)来学习如何安装 Kali Linux。

在这篇博客中，我们将尝试收集关于 **Edureka 社区**的信息。假设你对 Edureka 社区一无所知，你会如何开始收集信息？第一步是使用搜索引擎。

### **使用搜索引擎的足迹**

打开浏览器，搜索“Edureka 社区”。

![search engine - footprinting - edureka](img/644e687f1076b1f26166985734bd94de.png)

你会找到爱德华卡社区的网址，即**www.edureka.co/community**。这是你找到的第一条信息。

使用网站的 URL，你可以 ping 到网站的 IP 地址。

### **Ping 查找 IP 地址**

要找到 Edureka 社区网站的 IP 地址，请打开终端并运行以下命令:

T2`$ ping www.edureka.co`

等等，我们想找到**www.edureka.co/community**的 IP 地址，那我们为什么 ping 到**www.edureka.co**？

这是因为 **Edureka 社区**隶属于**www.edureka.co**域，并且该 web 应用程序的结构使得该社区的 IP 地址与该域的 IP 地址相同。

运行上述命令，您应该会看到类似的输出。

![ping edureka community - footprinting - edureka](img/90e163122f071c030e42ffdb040d036d.png)

你可以看到我们找到了 Edureka 社区的 IP 地址。IP 地址是**54.218.30.250。**

IP 地址只是网站的一个微小信息。为了获得更多信息，我们将使用 **Whois 查找。**

### **Whois 查找**

Whois Lookup 是一款用于查找 DNS、域名、名称服务器、IP 地址等信息的工具。让我们使用 Whois 查找来查找关于 Edureka 社区网站的一些更多信息，打开浏览器并转到**http://whois.domaintools.com/**

输入网站名称(或 IP 地址)，点击**搜索**

![whois search - footprinting - edureka](img/3cd0e013935cedff297ba4efd98660b5.png)

此搜索将显示网站的各种信息。

![whois lookup - footprinting - edureka](img/0188a47433d7daf30a44c01b9aea9b2a.png)

![whois lookup 2 - footprinting - edureka](img/d8b51aae250178f49173d09a9b34854c.png)

在上面的截图中可以看到，Edureka 社区正在使用的服务器类型是 **Apache/2.4.27。**这给了一个有道德的黑客开始测试的机会。此外，您可以将攻击限制在适用于 **Apache/2.4.27 服务器的范围内。**

这就是足迹帮助道德黑客的方式。使用足迹收集的信息越多，寻找漏洞的地方就越多。探索更多查找信息的方法，看看使用足迹还能收集到哪些信息。如果您有任何问题，请在 [Edureka 社区](https://www.edureka.co/community)上提问，我们将会回复您。

如果您希望学习网络安全，并在网络安全领域建立丰富多彩的职业生涯，那么请查看我们的 [***网络安全认证培训***](https://www.edureka.co/cybersecurity-certification-training) ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解网络安全，并帮助您掌握该主题。

您还可以看看我们新推出的关于 ***[CompTIA Security+认证](https://www.edureka.co/comptia-security-plus-certification-training)*** 培训的课程，这是 Edureka & CompTIA Security+之间首次正式合作。它为您提供了一个获得全球认证的机会，该认证侧重于安全和网络管理员不可或缺的核心网络安全技能。

通过 Edureka 的 [**研究生项目** 和 **NIT Rourkela**](https://www.edureka.co/post-graduate/cybersecurity) 以正确的方式学习网络安全，保护世界上最大的公司免受网络钓鱼者、黑客和网络攻击。