# 如何将 Python 添加到 Path 中？

> 原文：<https://www.edureka.co/blog/add-python-to-path/>

本文将提出一个非常简单而重要的概念，即如何将 [Python](https://www.edureka.co/blog/python-tutorial/) 添加到 path 中，并给出详细的实践演示。本文将涉及以下几点:

*   [将 Python 添加到路径](#AddPythonToPath)
*   [安装 Python](#InstallingPython)
*   [设置路径](#SettingupPath)
*   [如何给 Windows 添加 Python 路径？](#HowtoaddPythonPathtoWindows?)
*   [在 Unix 或 Linux 中设置路径](#SettingPathinUnixorLinux)
*   [环境变量](#EnvironmentalVariables)

那么让我们开始吧，

**将 Python 添加到路径**

今天，你能想到的任何问题都有应用程序。无论是以 web 应用程序的形式，还是以在智能手机上运行的形式，应用程序的世界实际上都是一个充满机会的无底洞，这使得 Python 成为全世界许多开发人员的显而易见的选择。Python 之所以成为如此受欢迎的选择，是因为该平台提供了过多的特性。

对于刚刚开始学习 Python 的开发人员来说，可能会在没有首先满足先决条件的情况下错误地在 Windows 中安装 Python。我们从开发人员那里听到的最常见的问题之一是如何在 Python 中添加路径，在本文中，我们将讨论这个问题。

但是首先让我们了解一下基本情况。

继续这篇关于如何将 Python 添加到 Path 的文章，

**Python 的味道**

与市场上其他可用的编程平台类似，Python 也受到目前存在的所有操作系统的支持，最突出的是 Linux、Mac OS 和 Windows。

## **安装 Python**

可以下载的最新版本的 Python 非常容易安装。您只需要下载适用于您的操作系统的二进制代码并安装它。如果您发现二进制代码不适用于您正在使用的操作系统，您需要使用 C 编译器来手动编译源代码。

手动编译源代码的最大优势之一是，在安装过程中，您可能需要更多的灵活性。

继续这篇关于如何将 Python 添加到 Path 的文章，

## **设置路径**

一旦你在你的系统上安装了 Python，现在是设置路径的棘手部分，这样你就可以轻松地访问 python.exe 文件。根据您当前使用的操作系统，设置 path 的过程会有很大的不同。下面提到的是同时为 Windows、Mac 和 Linux 设置 Path 的步骤。

**向窗口添加 Python 路径**

如果您像大多数其他开发人员一样通过在线教程在 Windows 中安装了 Python，在大多数情况下，Python 可执行文件可能没有添加到 Windows Path 变量中。虽然这在开始时听起来像是一件小事，但当您开始全面使用 Python 时，这将会导致一个问题。Python 可执行文件负责列出当您在 Python 窗口的命令提示符中键入命令时将执行的目录。一旦在 Windows 目录中添加了 python 可执行文件，只需输入 Python 关键字，即可访问 python.exe 文件。添加这个特性的一个主要优点是，每次你需要访问 python.exe 文件时，你不需要指定程序的完整路径。

现在让我们考虑一种情况，Python 可执行文件没有被添加到 Windows 路径。在这种情况下，当您在命令提示符下输入 Python 命令时，您将会看到以下消息的重复。

C: > python

‘python’不被识别为内部或外部命令，

可操作的程序或批处理文件。

此消息清楚地表明 python.exe 文件尚未添加到 Windows 路径，因此您将无法访问它。 在这样的场景中，如果你想访问 python.exe 文件你需要指定文件的完整地址。它看起来会像这样，

C:>C:python 34 python–版本

Python 3.4.3

从这个例子中可以看出，这个过程肯定比看起来要复杂，因此建议您在安装过程的最开始就将 python 可执行文件添加到 Windows 路径中。

继续这篇关于如何将 Python 添加到 Path 的文章，

## **如何给 Windows 添加 Python 路径？**

现在我们已经意识到不在 Windows 中添加 Python 路径的影响，这里有一个简单的添加方法。

1.  使用快捷键 ctrl+R 启动 Windows 电脑上的运行功能。
2.  一旦运行提示符启动并运行，键入 sysdm.cpl
3.  按回车键，您将被重定向到系统属性。在这一部分中，找到“高级”选项卡，然后单击显示“环境变量”的按钮。
4.  在环境变量下，找到系统变量并定位路径。
5.  点击编辑并找到显示变量值的选项。在本节中，在短语的末尾添加已经存在的路径。这里需要注意的最重要的一点是，在添加路径之前，您需要包含一个分号(；)以便两者可以容易地区分。
6.  在上面的例子中，我们添加了如下路径:丙:Python34。

![Demo - Add Python To Path - Edureka](img/5bb3d19bdeb3f767bf5eb6a1e68dc1ae.png)

完成后，按 OK，路径将被添加到特定位置。保存所有操作并重新启动系统，以获得更有效的性能。

继续这篇关于如何将 Python 添加到 Path 的文章，

## **在 Unix 或 Linux 中设置路径**

在 Unix 或 Linux 中添加 Path 的步骤相当简单，只需遵循下面列出的步骤。

1.  在 csh shell 中，键入以下句子:PATH " $ PATH:/usr/local/bin/python "并按 Enter 键。
2.  如果您使用的是标准版本的 Linux，打开 bash shell 并输入以下短语，export PATH = " $ PATH:/usr/local/bin/python "并按 Enter 键。
3.  如果您可以访问 sh 或 ksh shell，则打开终端并键入以下内容，PATH = " $ PATH:/usr/local/bin/python "并按回车键。

在 Unix 或 Linux 中向 python 添加路径时，需要注意的最重要的一点是，/usr/local/bin/python 是 Python 目录的默认路径。

继续这篇关于如何将 Python 添加到 Path 的文章，

## **环境变量**

现在您已经成功地将 Path 添加到 Python 中，下面是 Python 可以识别的一些最重要的环境变量。

1.  PYTHONPATH:这是 Python 识别的最常见的环境变量之一，它的作用类似于原始路径。这个变量的使用告诉 Python 模块文件的位置以及如何将它们导入到程序中。使用此函数时，请确保包含 Python 源代码库目录以及包含 Python 源代码的目录。在某些情况下，PYTHONPATH 已经预置在 Python 目录中。

2.  PYTHONSTARTUP:使用这个文件包含一个初始化文件的路径，这个文件包含 Python 源代码。每次在 Python 中启动解释器时都会执行这个函数。在 Unix 或 Linux 中，它被命名为 pythonrc.py，使用这个命令可以加载修改 PYTHONPATH 的实用程序。

3.  PYTHONCASEOK:这是一个特定于 Windows 的环境变量。当您使用这个变量时，Python 将在 import 语句中找到第一个不区分大小写的匹配。为了激活这个变量，您可以将它设置为您选择的任何值。

4.  PYTHONHOME:这是可以在 Python 中使用的模块搜索路径的替代方法。在大多数场景中，这被嵌入到 PYTHONSTARTUP 或 PYTHONPATH 中，以便使库之间的模块切换变得相当容易。

这就把我们带到了这篇文章的结尾，关于如何将 Python 添加到 Path？

*要深入了解 Python 及其各种应用，您现在就可以注册参加实时 [Python 课程](https://www.edureka.co/python-programming-certification-training)培训，该课程提供全天候支持和终身访问。*

*有问题吗？在“Python 教程”的评论部分提到它们，我们会回复你。*