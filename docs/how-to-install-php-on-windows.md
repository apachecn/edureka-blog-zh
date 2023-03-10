# 如何在 windows 上安装 PHP？

> 原文：<https://www.edureka.co/blog/how-to-install-php-on-windows/>

理解 PHP 是 [web 开发旅程](https://www.edureka.co/blog/web-developer-career/)的一部分，在你的机器上安装 PHP 可以被认为是这个旅程的第一步。在本文中，我们将看看在运行 Windows 的机器上安装 PHP 的各种方法。

*   [使用软件包安装 PHP](#installphp)
*   [在 Windows 上手动安装 PHP](#manuallyinstall)

我们开始吧。

## **使用软件包安装 PHP**

在开始这些步骤之前，首先记下操作系统版本和您的 CPU 架构。只需右击“ThisPC”图标并选择“属性”即可。在这里，您可以检查操作系统的版本(如 Windows 7、Windows 10)。在这里，我们还可以找到 CPU 架构的类型(例如 x32、x64)。

![System Configuration - How to install PHP - Edureka](img/af5324984519c69e979457f43161d07b.png)

就我而言，我使用的是 64 位操作系统和 Windows 10。

了解系统规格后，我们就可以开始安装过程了。有几个软件包可供下载，可以毫不费力地帮助安装 [Apache spark](https://www.edureka.co/blog/spark-tutorial/) 、 [MySQL](https://www.edureka.co/blog/mysql-tutorial/) 和 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 。[WampServer](http://www.wampserver.com/en/)和[XAMPP](https://www.apachefriends.org/index.html)是可供下载的软件包。

## **在 Windows 上手动安装 PHP**

在 Windows 10 机器上安装 PHP 一点也不困难。首先，让我们了解所涉及的步骤，然后，我们将详细介绍每个步骤。

1.  首先从 [PHP 网站](https://www.php.net/downloads.php) 做最新的 PHP 包。

2.  一旦我们有了 zip 文件，我们将在 c 盘中创建一个 PHP7 文件夹，并提取这个文件夹中 zip 文件的内容。

3.  在 PHP.ini 文件中做一些修改。

4.  改变 path 环境变量。

现在，让我们详细介绍每一步。前两步非常简单，因此我们将从第 3 步开始。

一旦我们在 c 盘上创建了文件夹“PHP7 ”,我们需要提取从 PHP 网站上下载的 zip 文件，并把它的所有组件放在“PHP7”文件夹中。之后，我们需要找到一个名为“php.ini-development”的文件，复制这个文件并将其重命名为“php.ini”。

一旦我们制作了副本，我们需要借助记事本或 notepad++打开“php.ini ”,进行一些修改。首先，我们需要找到' extension_dir '并删除' extension_dir = "ext " '旁边的分号。

之后，我们需要启用一些重要的扩展，这可以通过简单地向下滚动一点来完成，你会看到所有可用扩展的列表。在这里，您可以根据需要启用扩展。

**![enable extensions - How to install PHP - Edureka](img/3ed578f614aa55eec520d1ebb92ebab8.png)注意**——我的列表顺序可能和你的不一样。

在执行大部分功能时，我已经启用了所有必要的扩展。启用扩展后，保存“php.ini”文件，现在我们将进入第 4 步。

打开控制面板，搜索“变量”。然后点击“编辑系统环境变量”。然后点击“环境变量”，然后从系统变量中选择“路径”，选择“路径”后点击“编辑”，现在我们需要添加一个路径，因此我们点击“新建”，然后添加“C:PHP7”。

![Path - How to install PHP - Edureka](img/d4f510413fef83df70c0921b2a637083.png)

添加完路径后，安装过程就完成了。您可能需要重新启动以使所有更改生效。现在打开命令提示符并键入'php-v【T4]'你会看到你的系统上安装的 PHP 版本和其他相关细节。

至此,“如何安装 PHP”博客到此结束。我希望你们喜欢这篇文章，并准备好开始使用 PHP。你可以参考这个 [PHP 教程](https://www.edureka.co/blog/php-tutorial-for-beginners/)，不再是一个脚本语言新手。

*如果您发现这个 PHP 教程博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“如何安装 PHP”的评论部分提到它，我会回复你。*