# 如何在 Windows 10 上安装 Java 12

> 原文：<https://www.edureka.co/blog/install-java-on-windows/>

***Oracle JDK*** 是一个高度通用的套件，可用于使用 Java 编程语言测试应用程序和程序开发。这篇文章将是一个关于如何在 Windows 10 上下载和安装 Java 12 的简要指南，适用于初学者 。

[***Java***](https://www.edureka.co/blog/java-tutorial/) 是使用最广泛的计算机语言之一。它是一种 [***面向对象编程***](https://www.edureka.co/blog/object-oriented-programming/) 语言，非常容易学习。为了编写和运行 Java 代码，我们需要在我们的计算机上安装 ***Oracle Java 开发套件(JDK)*** 。为 [***程序***](https://www.edureka.co/blog/java-programs/) 、基于***Java***的应用和工具提供了开发环境。T36

***Java SE 12.0.1*** 是目前，Java SE 平台最新发布的。

因此，如果你遵循这些简单的步骤，你应该能够下载 JDK 12 并安装在你的操作系统上，完全没有麻烦。

*   [**从甲骨文网站下载 Java/JDK**](#jdkdownload)
*   [**在系统上安装 Java/JDK**](#jdkinstall)
*   [**在 Windows 10 上设置 Java 环境变量**](#environmentvariables)

**从甲骨文网站下载 Java/JDK**

在 Windows 上安装 JDK，打开任意浏览器，搜索下载 Java/JDK 12，打开 ***甲骨文官网*** 。

### **第一步:访问甲骨文网站下载页面**

*   前往屏幕左上角的  ***菜单*** 按钮(看起来像 3 条短线条相互堆叠在一起)并继续进入  ***产品> > Java > >下载面向开发者的 Java(JDK)***

![oracle website - how to install java on windows - edureka](img/85f5bb36e5b0f0378bdb688343532e4e.png)或者，

你可以直接登陆  ***[下载页面](https://www.oracle.com/technetwork/java/javase/downloads/index.html)*** 上  ***甲骨文官网*** 。![Java website - how to install java on windows - edureka](img/4ce7646d2286e0d5c217cc759fb97aad.png)

*   点击 ***下载按钮*** 。它看起来像一个带有 Java 标志的正方形。

### **第二步:Java SE 开发套件**

*   向下滚动。你会看到一个类似下图的盒子。你会看到有太多的选项可以下载用于 Linux、MacOS 和 Windows 的 ***Java SE 12 安装文件*** 。 ![JDK SE - install java on windows - edureka](img/7f5cf7dca1c0b3897f29de87429c19c8.png)

*   在框的顶部，您会看到一个名为  ***的选项，接受许可协议*** 。选择它旁边的气泡。

*   然后，你必须选择你的操作系统。对于 Windows 10，点击

***注**:你需要 64 位操作系统才能安装 JDK 9 之后的任何版本 Java **。**如果你还在用 32 位操作系统，**你就无法安装 Java JDK 12。***

## **在你的系统上安装 Java JDK 12**

下载完成后，可以按照几个简单的步骤 ***在 Windows 10*** 上安装***Java JDK 12******。***

*   打开下载的文件，它会带你到一个 ***安装向导*** 只需点击 ***下一个*** 。![installation wizard 1 - install java on windows - edureka](img/af784c0c00d00113f6a4a5a1e96327c0.png)

*   你可以继续改变你的安装位置，但我认为你应该保持默认位置，点击  **下一个**。 ![installation wizard 2 - install java on windows - edureka](img/f152c296caf978d5e85874cdd36c45c1.png)

您现在已经在 Windows 10 系统上安装了 Java JDK 12！

## **在 Windows 10 上设置 Java 环境变量**

希望到目前为止你已经发现它非常简单。但是有个问题！

仅仅通过下载和安装 JDK 12，Java 是不行的。您需要设置环境变量，这将有助于编译 Java 代码。现在，要设置一个 Java 环境，您需要做以下事情。

### **第一步:设置 Java 环境变量**

*   导航到 ***C:Program Files*** 并查找 ***Java*** 文件夹。打开就会发现 ***jdk 12*** 文件夹。

*   转到 bin 文件夹，复制 ***bin*** 文件夹的路径。

*   接下来，导航通过这个路径， ***控制面板>系统和安全>系统>高级系统设置>环境变量***

*   在 ***系统变量*** 下，你会发现一个名为 ***的变量，路径*** 只需转到编辑并添加 bin 的文件夹位置即可。![environment variables - install java on windows - edureka](img/782d55286c23cf185235853fdc39b4fc.png)

Java 不一定需要设置任何环境变量。然而，设置环境变量确实使某些事情变得更容易。环境变量指向安装您的首选 Java 版本的文件夹位置。外部程序和工具主要需要这些环境变量来计算 Java 在机器上的确切安装位置。

### **步骤 2:检查变量设置是否正确**

现在要检查你是否已经成功设置了 Java，打开 ***窗口命令提示符*** 并键入以下命令

*   **java 版本**

*   **建议**

您应该会看到类似下图的内容。![cmd - install java on windows - edureka](img/abc5782782133670ce57784e95a96d26.png)

恭喜你！您刚刚成功学会在 Windows 10T5 上安装 ***Java 12。现在，您马上就可以在 [***Java***](https://www.edureka.co/blog/advanced-java-tutorial) 中运行复杂的代码了！***

*想要更多的 Java？去看看 Edureka 的 **[Java 培训项目](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 带你走过学习 Java 之旅的每一步。我们有一个课程，是为想成为 Java 开发人员的学生和专业人士设计的。*

*有问题吗？请在* *下面的评论区提出来，我们会尽快回复您。*