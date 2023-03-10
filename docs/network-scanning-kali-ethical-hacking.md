# 道德黑客网络扫描快速指南

> 原文：<https://www.edureka.co/blog/network-scanning-kali-ethical-hacking/>

*“Knowing your enemy is winning half the war..”*

**同样，当你知道了你的目标，黑客的任务就完成了一半。有不同的方法来收集关于你的目标的信息。在之前的博客中，我解释了如何使用[足迹](https://www.edureka.co/blog/footprinting-ethical-hacking-kali-linux/)收集信息。但是知道基本信息是不够的。因此，在这篇博客中，我将告诉你如何使用网络扫描来收集道德黑客攻击的具体细节。如果您对道德黑客或网络安全感兴趣，请查看 Edureka 的现场培训。**

**本博客涵盖的主题有:**

***   [什么是网络扫描？](#WhatisNetworkScanning)*   [网络扫描与侦察有何不同？](#HowisNetworkScanningdifferentfromReconnaissance)*   [针对道德黑客行为的网络扫描类型](#TypesofNetworkScanning)*   [如何使用网络扫描工具？](#HowtouseNetworkScanningTools)**

## ****什么是网络扫描？****

**网络扫描是识别目标应用程序使用的活动主机、端口和服务的过程。假设你是一个有道德的黑客，想要找到系统中的漏洞，你需要系统中有一个你可以尝试攻击的点。道德黑客的网络扫描用于找出系统中的这些点，黑帽黑客可以利用这些点来入侵网络。然后各自的团队致力于提高网络的安全性。如果你想了解更多关于道德黑客的知识，请立即加入[在线道德黑客课程](https://www.edureka.co/ceh-ethical-hacking-certification-course)。**

**每个组织都有一个网络。这个网络可以是由所有相互连接的系统组成的内部网络，也可以是连接到互联网的网络。在这两种情况下，要侵入网络，您必须找到网络中可以被利用的脆弱点。网络扫描用于找出网络中的这些点。**

## ****网络扫描与侦察有何不同？****

**想象一下:你是一名军官，你和你的团队正计划袭击一个恐怖分子的巢穴。你已经找到了老巢的位置和周围的细节，还找到了将队伍送到老巢的方法。你可以把这一切看作是你利用[侦察](https://www.edureka.co/blog/what-is-ethical-hacking/#reconnaissance)收集的信息。现在你必须找到一个点，通过它你可以进入巢穴并攻击敌人。这是**网络扫描**。**

**简单来说，侦察是用来搜集信息，了解你的目标，而网络扫描是用来发现网络中可能存在的脆弱点的方法，你可以通过它来黑掉网络。**

**根据扫描识别的信息类型，网络扫描可以分为不同的类型。**

## ****针对道德黑客行为的网络扫描类型****

**网络扫描可以分为两大类:**

***   **端口扫描***   **漏洞扫描****

### ****端口扫描****

**顾名思义，端口扫描是用来找出网络上活动端口的过程。端口扫描器将客户端请求发送到目标网络上的一系列端口，然后保存发回响应的端口的详细信息。这就是如何找到活动端口的。**

**端口扫描有不同的类型。下面是一些最常用的列表:**

***   TCP 扫描*   SYN 扫描*   UDP 扫描*   ACK 扫描*   窗口扫描*   鳍扫描**

### ****漏洞扫描****

**漏洞扫描是一种针对道德黑客的网络扫描，用于找出网络中的弱点。这种类型的扫描可以识别由于编程不当或网络配置错误而出现的漏洞。**

**现在你知道什么是网络扫描了，我给你介绍一些工具，告诉你如何使用它们进行网络扫描。**

## ****如何使用网络扫描工具？****

**在道德黑客博客的网络扫描部分，我将向你展示如何使用一些网络扫描工具。我为此使用的操作系统是 [Kali Linux](https://www.edureka.co/blog/ethical-hacking-using-kali-linux/) ，因为它带有许多内置的黑客工具。如果你想学习如何安装 Kali Linux，[参考这个链接](https://www.edureka.co/blog/how-to-install-kali-linux/)。如果你在这方面遇到任何问题，你可以在 [Edureka 社区](https://www.edureka.co/community)寻求帮助。**

**我要说的第一个工具是 Nmap。**

### ****1。用于网络扫描的 nmap****

**Nmap 是一个免费的开源网络扫描器。您可以使用 Nmap 扫描网络，方法是使用目标的 IP 地址:**

**T2`$ nmap 1.2.3.4`**

**或使用主机名**

**T2`$ nmap example.com`**

**注意，未经组织事先授权，扫描任何组织的网络都是非法的。所以不要试图扫描任何随机的网络。但是如果我们不能在未经许可的情况下扫描任何网络，那么我们将如何了解 Nmap？别担心，Nmap 组织已经为我们提供了一个使用 Nmap 练习扫描的网站:[scanme.nmap.org](http://scanme.nmap.org)**

**让我们试着扫描一下这个。在系统中打开一个终端，运行下面的命令:**

**T2`$ nmap -v -A scanme.nmap.org`**

**![nmap scan - network scanning for ethical hacking - edureka](img/f3889b0464ffe9f93a61403e98df9aa8.png)**

**您可以在结果中看到 Nmap 如何显示网络上开放的端口。在上面的命令中，选项' **v** 用于详细输出，选项' **A** 用于检测操作系统。**

**Nmap 工具有许多选项可以用来获得不同种类的结果。要了解更多关于使用 Nmap 工具的信息，请查看这个 [Nmap 教程](https://www.edureka.co/blog/nmap-tutorial/)。**

**我们要使用的下一个工具是 Nikto。**

### ****Nikto 进行网络扫描****

**Nikto 是一种网络服务器扫描程序，用于检测危险文件和过时的服务软件。这些细节可以被利用来入侵网络。Nikto 旨在以最快的速度扫描网络服务器。**

**要使用 Nikto，请打开终端并运行以下命令:**

**T2`$ nikto -host scanme.nmap.org`**

**您应该会看到类似的输出**

**![nikto scan - network scanning for ethical hacking - edureka](img/b06408afa7200fd9876fcf76370dd646.png)**

**上面截图中突出显示的部分显示了 Nikto 已经找到的结果。这些结果有助于了解被扫描的网络或应用程序的弱点。一旦发现网络的弱点，就可以选择相关的攻击来黑掉网络。**

**我要说的下一个工具是 Nessus。**

### ****Nessus 进行网络扫描****

**Nessus 是目前最强大的漏洞扫描器之一。该扫描仪没有预装 Kali Linux。所以，在告诉如何使用它之前，我会告诉你如何安装它。**

**打开浏览器，进入[www.tenable.com/downloads/nessus](http://www.tenable.com/downloads/nessus)，点击**获取激活码**。**

**![nessus activation code - network scanning for ethical hacking - edureka](img/314e67b50d9872be2e2d6d5e897faab4.png)**

**你会看到两个版本的 Nessus:免费版(Nessus Home)和付费版。我们将使用免费版本，所以点击“ **Nessus Home** ”下的“**立即注册**”按钮。**

**![nessus home - network scanning for ethical hacking - edureka](img/1ecc304a63dbaefbb19272a7e4d60f28.png)**

**在下一页中，输入您的名字、姓氏和电子邮件 Id。一个链接将发送到您的电子邮件 Id，您将被重定向到下载页面。**

**下载合适的文件。我正在下载**。deb** 文件用于 **AMD64** 架构，因为它与我正在使用的 Kali Linux 兼容。**

**![nessus download - network scanning for ethical hacking - edureka](img/9c9373b09c9040e44dea1dd94269ca55.png)**

**下载完成后，打开终端，运行以下命令安装 Nessus:**

```
**$ cd Downloads
$ dpkg -i Nessus-8.3.0-ubuntu910_amd64.deb**
```

**![install nessus - network scanning for ethical hacking - edureka](img/762e83e7ecedff20e223c19ac21548ef.png)**

**Nessus 将被安装，现在您必须启动 Nessus 服务才能使用它。参考下面的命令:**

**T2`$ /etc/init.d/nessusd start`**

**服务启动后，打开网页浏览器，进入//kali:8834/**

**![create nessus account - network scanning for ethical hacking - edureka](img/6659e48c933e6948305e87599985a19e.png)**

**输入用户名和密码，在下一页中，输入发送到您的电子邮件 Id 的激活码。**

**激活成功后，等待 Nessus 下载必要的插件。一旦 Nessus 完成设置，您将看到类似这样的内容:**

**![Nessus home - network scanning for ethical hacking - edureka](img/e55c437ecb40b76a4ed6dc6df4832a0b.png)**

**要扫描网络，点击右上角的**新扫描**。**

**在下一页，您将看到 Nessus 提供的不同类型的扫描。我会选择**基本网络扫描**。**

**![Nessus scan list - network scanning for ethical hacking - edureka](img/799a9cc997ab341c378ea63a62b0dfb7.png)**

**输入扫描的名称、描述、文件夹和目标，然后点击**保存**。对于这个道德黑客教程网络扫描，我将扫描我的本地网络。**

**![Nessus scan save - network scanning for ethical hacking - edureka](img/e5bc1d74d4f4b82e36078983e30c969d.png)**

**接下来，选择扫描并点击开始图标。**

**![nessus start - network scanning for ethical hacking - edureka](img/4489999b4017903836ec0000fcda86c6.png)**

**扫描完成后，可以在“**漏洞**选项卡下看到漏洞报告。**

**![Nessus scan result - network scanning for ethical hacking - edureka](img/6ead9e3948ca01aa36c5e54035343b66.png)**

**扫描结果显示发现的信息和漏洞。这就是 Nessus 如何被用于道德黑客的网络扫描。**

**您对目标了解得越多，就越容易测试漏洞。多尝试使用 [OpenVAS](http://openvas.org/) 、 [Core Impact](https://www.coresecurity.com/core-impact) 、 [Retina](https://www.beyondtrust.com/resources/datasheets/retina-network-security-scanner) 等网络扫描工具。如果您有任何问题，请在 [Edureka 社区](https://www.edureka.co/community)上提问，我们将会回复您。**

***如果您希望学习网络安全，并在网络安全领域建立丰富多彩的职业生涯，那么请查看我们的[网络安全认证培训](https://www.edureka.co/cybersecurity-certification-training)，它提供有讲师指导的现场培训和真实项目体验。* *您还可以看看我们新推出的课程 [**CompTIA Security+认证**](https://www.edureka.co/comptia-security-plus-certification-training) ，这是 Edureka & CompTIA Security+首次与官方合作。它为您提供了一个获得全球认证的机会，该认证侧重于安全和网络管理员不可或缺的核心网络安全技能。***

**通过 Edureka 的 [**研究生项目** 和 **NIT Rourkela**](https://www.edureka.co/post-graduate/cybersecurity) 以正确的方式学习网络安全，保护世界上最大的公司免受网络钓鱼者、黑客和网络攻击。**