# Python Spyder IDE 是什么，怎么用？

> 原文：<https://www.edureka.co/blog/spyder-ide/>

创建软件应用程序总是需要交互式环境，当你在数据科学、工程和科学研究领域工作时，这一点变得非常重要。Python Spyder IDE 也是为了同样的目的而创建的。在本文中，您将学习如何安装和使用 Spyder 或科学的 [Python](https://www.edureka.co/blog/python-programming-language) 和开发 [IDE](https://www.edureka.co/blog/best-ide-for-python/) 。

在继续之前，让我们看看这里讨论的所有主题:

*   [什么是 Python Spyder IDE？](#whatisspyder)
*   [Spyder 的特点](#features)
*   [Python Spyder IDE 安装](#installation)
*   [创建文件/启动项目](#newfile)
*   [编写代码](#writingthecode)
*   [变量浏览器](#variableexplorer)
*   [文件浏览器](#fileexplorer)
*   [配置 Spyder](#configuring)
*   [帮](#help) 帮

我们开始吧。

## **什么是 Python Spyder IDE？**

Spyder 是一个开源的跨平台 IDE。 [Python](https://www.edureka.co/blog/python-tutorial/) Spyder IDE 完全是用 Python 写的。它由科学家设计，专供科学家、[数据分析师](https://www.edureka.co/blog/data-analyst-roles-and-responsibilities/)和工程师使用。它也被称为科学 Python 开发 IDE，具有一系列显著的特性，这些特性将在下面讨论。

## **Spyder 的特点**

Spyder 的一些显著特点是:

*   可定制的语法突出显示
*   断点的可用性(调试和条件断点)
*   交互式执行，允许您运行行、文件、单元格等。
*   运行工作目录选择、命令行选项、当前/专用/外部控制台等的配置
*   可以自动清除变量(或进入调试)
*   通过大纲浏览器可以实现在单元格、函数、块等中的导航
*   它提供了实时代码自省(检查什么是函数、关键字和类，它们在做什么以及它们包含什么信息的能力)
*   在 if、while 等后面自动插入冒号
*   支持所有 IPython 魔术命令
*   使用 [Matplotlib](https://www.edureka.co/blog/python-matplotlib-tutorial/) 生成的图形的内联显示
*   还提供帮助、文件资源管理器、查找文件等功能

## **Python Spyder IDE 安装(使用 Anaconda 安装–推荐)**

Python Spyder IDE 是 Anaconda Python 发行版的默认实现。这不仅是推荐的方法，也是最简单的方法。按照下面给出的步骤安装 Python Spyder IDE:

*   使用以下链接进入 Anaconda 官方网站:[https://www.anaconda.com](https://www.anaconda.com)
*   点击右上方的下载选项，如下图:![Anaconda download-Python Spyder IDE-Edureka](img/d39392e145984bdcd5891ef5527a627a.png)
*   选择适合您的操作系统的版本，然后单击下载。![Anaconda download2-Python Spyder IDE-Edureka](img/587cf23b0a7a441b45682f5dab60f703.png)
*   安装程序下载完成后，您会看到一个安装对话框。完成设置，然后单击完成。
*   然后，在系统的搜索栏中搜索 Anaconda Navigator 并启动 Spyder。启动后，您将看到类似于下图的屏幕:

## ![spyder-Edureka](img/65307d066541b30dda3b2b42e02d0ee3.png)

## **创建文件/启动项目:**

*   要创建新文件，请按如下方式浏览:

*文件—>新文件*

*   要创建新项目:

*项目—>新项目*

## **编写代码:**

借助 Spyder 的多语言代码编辑器和许多强大的工具，在 Spyder 中编写代码变得非常容易。如前所述，编辑器具有语法突出显示、代码实时分析、风格分析、按需完成等功能。当您编写代码时，您还会注意到它为方法提供了一个清晰的调用堆栈，给出了可以与该方法一起使用的所有参数。

看看下面的例子:

![editor-Python Spyder IDE-Edureka](img/7bb08bb030544728584d7dcdf1e0f548.png)

在上面的例子中，你可以注意到编辑器显示了 [*打印*函数](https://www.edureka.co/blog/print-in-python/)的完整语法。不仅仅是这样，如果你在任何一行中犯了错误，你会在行号前得到通知，并有一条消息描述这个问题是什么。请看下图:

![editor2-Python Spyder IDE-Edureka](img/bc6258bb85331882bde0ab43293fb3de.png)要运行任何文件，您可以选择*运行*选项并点击运行。执行后，将在控制台上看到输出，如下图所示:

### **![output Spyder-Edureka](img/91d306d1b179d88eadd01334ffa4f4c0.png)**

### **编码单元格:**

您可以使用以下内容轻松定义代码单元格:

| 类型 | 描述 |
| #%% | 标准细胞分离器 |
| # %% | 标准单元格分隔符，当用 Eclipse 编辑文件时 |
| #<code cell> | IPython 笔记本细胞分离器 |

例如，当您使用标准单元格分隔符时，您会看到代码已被分隔如下:

![Cell separator-Edureka](img/3335c734f01dee05c76928e7896eedc1.png)

## **变量浏览器:**

变量浏览器显示当前 IPython 控制台的所有全局对象引用，如模块、变量、[方法](https://www.edureka.co/blog/python-method-overloading/)等。不仅如此，您还可以使用各种基于 GUI 的编辑器与它们进行交互。

![Variable Explorer-Edureka](img/86a313d9751047324cf871ad1f9f1b5a.png)

## **文件浏览器:**

文件浏览器基本上是一个文件系统和目录浏览器，它允许您浏览、打开和执行其他管理任务。您可以利用上下文菜单功能来操作它们。

## **![File Explorer-Python Spyder IDE-Edureka](img/8eed688d12adf4a808a59c46b1616adf.png)**

## **配置 Spyder:**

使用首选项菜单中的选项可以方便地配置 Python Spyder IDE。您可以更改任何内容，如主题、语法颜色、字体大小等。为此，导航至*工具*菜单，然后选择 P *参考*选项。您将看到以下窗口，允许您根据自己的选择配置 Spyder:

![Preferences-Python Spyder IDE-Edureka](img/4e2e42fc280abf974a28f341f9570384.png)

## **帮助:**

*帮助*窗格允许您查找和显示您想要的任何对象的文档。当您选择*帮助*选项时，您将能够看到以下选项:

如你所见，它有许多选项可以帮助你解决在使用 Python Spyder IDE 时遇到的任何问题。

Hope you are clear with all that has been shared with you in this tutorial. This brings us to the end of our article on Python Sypder IDE. ***Make sure you practice as much as possible and revert your experience.*  **

*有问题吗？请在这个“Python Spyder IDE”博客的评论部分提到它，我们会尽快回复您。*

*要深入了解 Python 及其各种应用，您可以注册参加实时 **[Python 在线培训](https://www.edureka.co/data-science-python-certification-course)** ，该培训提供全天候支持和终身访问。*