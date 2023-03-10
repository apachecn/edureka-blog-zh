# 使用 Python 的 MacChanger 您迈向道德黑客的第一步

> 原文：<https://www.edureka.co/blog/macchanger-with-python-ethical-hacking/>

道德黑客很有趣，但是一个道德黑客应该知道很多事情。比如掩盖他的行踪。其中一种方法是使用 MacChanger。在本教程中，我将教你如何用 Python 编写一个 。

我将讲述以下主题:

*   [Python 为什么要进行伦理黑客攻击？](#WhyPythonforEthicalHacking)
*   [什么是 M a cChanger？](#WhatisaMacChanger)
*   [在 Ubuntu 上安装 py charm](#InstallingPyCharmonUbuntu)
*   [](#WritingaMacChanger)

在编写 MacChanger 之前，我们先来看看为什么要用 Python 进行道德黑客攻击。

## **Python 为什么要进行伦理黑客攻击？**

道德黑客是在系统中寻找攻击者可以利用并造成损害的漏洞的过程。然后，利用这些结果来提高网络和系统的安全性。我们已经有很多可用的[道德黑客工具](https://www.edureka.co/blog/ethical-hacking-tools/)，那么还需要 Python 做什么呢？

Python 被用来**自动化****道德黑客**的过程。道德黑客不是一蹴而就的。道德黑客行为有不同的阶段,其中一些你将不得不进行不止一次。使用 Python 进行合乎道德的黑客攻击使这变得很容易。

假设你想测试一个网站的漏洞，你必须在网站上运行测试。完成这个项目后，你可能需要测试另一个网站。现在，您将不得不从头开始遵循相同的步骤。这里可以使用 Python 来自动化这些测试步骤。所以，你写一次代码，每次你想测试一个网站的时候就用它。如果你想了解更多关于道德黑客的知识，今天就加入[在线道德黑客课程](https://www.edureka.co/ceh-ethical-hacking-certification-course)。

现在我们知道了我们要处理的是什么，让我们来了解一下什么是 MacChanger！

## **什么是 MacChanger？**

设备制造商为每个网络设备分配了一个 MAC 地址，这有助于与其他设备进行通信。MAC 地址是硬编码在设备上的，不可能永久更改。但是，我们可以使用 MacChanger 临时改变它。MAC changer 是一种将 MAC 地址更改为所需(或随机)地址的工具，直到设备重新启动。一旦设备重新启动，该设备的 MAC 地址将被设置为其原始 MAC 地址。

现在我们知道了什么是 MacChanger，让我们使用 Python 来构建它！

对于这篇用 Python 编写 MacChanger 的教程，我们将在 PyCharm 中运行我们的 Python 脚本，py charm 是一个集成开发环境。因此，要运行我们的 Python 脚本，我们需要首先安装 PyCharm。我们来看看如何在 Ubuntu 上安装 PyCharm。

## **在 Ubuntu 上安装 py charm**

要在 Ubuntu 上安装 PyCharm，先去这个链接:[https://www.jetbrains.com/pycharm/download/#section=linux](https://www.jetbrains.com/pycharm/download/#section=linux)

在这里，你会发现两个版本，对于本教程，我们将使用社区版。

![PyCharm Download - macchanger- Edureka](img/01f74b2d43f9eb6ddcf383fa7f3e7696.png)

当您点击下载按钮时，下载应该开始。下载完成后，我们必须安装 PyCharm。默认情况下，这个文件会被下载到“**下载”**目录下。打开终端并运行以下命令:

```
$ cd Downloads
$ tar -xvf pycharm-community-2018.3.4.tar.gz
```

记住将上述命令中的文件名替换为您系统中下载的文件名。

上面的命令将提取 PyCharm 文件。而现在，要运行 PyCharm，你就要进入**py charm****-community-2018 . 3 . 4/bin**文件夹，运行 **pycharm.sh** 文件。为此，运行以下命令:

```
$ cd pycharm-community-2018.3.4/
$ cd bin/
$ ./pycharm.sh
```

![Running PyCharm-macchanger-Edureka](img/b03b4e10eef00f96160cfd133d3b22c1.png)

当您第一次运行它时，您必须接受条款和条件。完成后，PyCharm 将开始运行。

现在我们已经安装了 PyCharm，让我们继续编写 MacChanger。

您将使用 PyCharm 编写 MacChanger 脚本。要启动 PyCharm，请转到 PyCharm 被解压缩的目录并运行 shell 脚本。

```
$ cd pycharm-community-2018.3.4/ 
$ cd bin/
$ ./pycharm.sh
```

您将看到 PyCharm 的欢迎屏幕。点击**“创建新项目”。**

![PyCharm welcome-macchanger-edureka](img/b01c676c99677916bab376a5d1b346bd.png)

输入项目的名称。我将把这个**命名为 Mac_changer。**然后点击**创建**。

![pycharm-name-macchanger-edureka](img/3b870c70e27da0884589e91dcb3b7315.png)

现在你将看到工作场所。接下来，让我们创建一个 Python 文件。要做到这一点，右击项目名称，进入“**新建**，点击“ **Python 文件**”。

![new python file-macchanger-edureka](img/88a2a7c191ad38d4be938dacbf0cae56.png)

现在你可以在这里编写 python 脚本了。但是首先，您应该决定要更改哪个网络设备的 MAC 地址。为此，打开终端并运行以下命令:

```
$ ifconfig
```

您应该会看到网络接口及其各自 MAC 地址的列表。您可能有不同的接口名称或 MAC 地址。当使用本博客中的脚本时，请确保将接口名称更改为您系统中的名称。在本教程中，我将更改" **ens33** "的 MAC 地址。

![ifconfig-macchanger-edureka](img/24225aae772affcd5fee51c4f0ff96c4.png)

更改 MAC 地址的脚本如下:

```
import subprocess

subprocess.call(["sudo","ifconfig","ens33","down"])
subprocess.call(["sudo","ifconfig","ens33","hw","ether","00:11:22:33:44:55"])
subprocess.call(["sudo","ifconfig","ens33","up"])
```

我将把 MAC 地址更改为 **00:11:22:33:44:55。**现在运行这个脚本。要运行脚本，点击顶部的**“运行”**选项卡，然后点击“**运行**”。

运行脚本后，为了检查接口的 MAC 地址是否已经更改，我们将再次检查详细信息。只需在终端中运行 **ifconfig** 命令。

![ifconfig2-macchanger-edureka](img/0fe139a99c2b60e8a4b98795f24c1677.png)

你看到 MAC 地址的变化了吗？新的 MAC 地址是 **00:11:22:33:44:55** 。就是这么简单。现在，每当您需要更改 MAC 地址时，您所要做的就是在 Python 脚本中更新 MAC 地址和/或接口名称。

但是这并没有什么不同或者节省很多时间，对吗？我的意思是，这只是 3 个命令，我们可以手动完成。为什么要为此编写 Python 脚本呢？

让我告诉你它是如何产生影响的。想象一下每 5 分钟就必须更改 MAC 地址的场景。假设您正在工作一个小时，您将不得不运行这三个命令 12 次。所以，你总共需要运行 **3 * 12 = 36 个**命令。好吧，现在看起来太多了，不是吗？

当你写 Python 脚本时，你可以循环运行这个脚本，每 5 分钟改变一次 MAC 地址。现在你看到你可以节省多少时间和精力。

*恭喜恭喜！您已经用 Python 编写了一个 MacChanger，并看到了它的运行。现在您已经知道 Python 如何有益于道德黑客，学习更多的模块、命令，并开始使用 Python 自动化道德黑客。*

*有问题吗？请将它发布在 [Edureka 社区](https://edureka.co/community)上，我们将会回复您。*

如果您希望学习网络安全，并在网络安全领域建立丰富多彩的职业生涯，那么请查看我们的 [***网络安全认证培训***](https://www.edureka.co/cybersecurity-certification-training) ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解网络安全，并帮助您掌握该主题。

*您还可以看看我们新推出的关于 [**CompTIA Security+认证**](https://www.edureka.co/comptia-security-plus-certification-training) 的课程，这是 Edureka & CompTIA Security+首次与官方合作。它为您提供了一个获得全球认证的机会，该认证侧重于安全和网络管理员不可或缺的核心网络安全技能。*

通过 Edureka 的 [**研究生项目** 和 **NIT Rourkela**](https://www.edureka.co/post-graduate/cybersecurity) 以正确的方式学习网络安全，保护世界上最大的公司免受网络钓鱼者、黑客和网络攻击。