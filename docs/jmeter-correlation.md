# JMeter 相关性:提取变量的最佳方法

> 原文：<https://www.edureka.co/blog/jmeter-correlation/>

软件测试[中的动态响应](https://www.edureka.co/software-testing-certification-courses)为不同的迭代提供不同的值。这可能会影响后续请求。这篇 JMeter 相关性文章将向您展示如何存储来自响应的动态值，存储在一个变量中，并按照下面的顺序在所有需要的请求中使用它:

*   [什么是关联？](#correlation)
*   [我们为什么需要关联？](#whycorrelation)
*   [使用正则表达式提取器的步骤](#regexsteps)
*   [JMeter 关联:演示](#jmetercorrelation)

## **什么是关联？**

关联是从一个步骤的响应中提取一些值到另一个步骤的请求中的过程。它捕获并存储来自服务器的动态响应，并将其传递给后续请求。那么，什么是动态响应呢？

![Correlation - JMeter Correlation - Edureka](img/3a8688b3497c68a494f2d4f5d5af5466.png)

当一个响应为每个迭代请求返回不同的数据时，它被认为是动态的，偶尔会影响连续的请求。相关性是性能[负载测试](https://www.edureka.co/blog/load-testing-using-jmeter/)脚本编写期间的一个关键过程，因为如果我们不小心处理它，脚本将变得无用。

## **我们为什么需要关联？**

相关性是脚本最重要的方面之一。它从前面的请求中获取动态数据，并将其发送给后面的请求。让我们举个例子来找出我们到底为什么需要相关性。假设我们已经记录了一个场景:

*   用户输入登录详情并点击确定按钮
*   主页打开，用户采取进一步行动

![why need correlation - JMeter correlation - edureka](img/8de1b17b50cb3324951741eaa10d7a0c.png)

当我们登录网站时，会话变量是动态创建的。这些会话变量被传递给后续的请求并帮助验证&所执行的动作的认证。这里，我们需要将 web 请求与动态变量相关联，否则测试将会失败。为了进行关联，我们需要使用**正则表达式提取器**。

所以，在进入关联的细节之前，我们先来看看如何在 JMeter 中使用正则表达式提取器。

## **使用正则表达式提取器的步骤**

在 JMeter 中使用正则表达式提取器时，需要遵循 4 个步骤。它包括:

![](img/f7f3b435268ac156a32add8e37232956.png)

1.  **在 JMeter** 中创建一个测试计划
2.  在测试计划中增加**正则表达式提取器**
3.  **参考**下一步提取的值
4.  运行和**验证**测试

现在让我们继续，通过一个例子来看看如何在 JMeter 关联中使用这个提取器。

## **JMeter 关联:演示**

你需要做的第一件事是[下载](https://jmeter.apache.org/download_jmeter.cgi)并在你的系统中安装 JMeter 工具。如果你对这个工具有任何疑问，你可以查看 [JMeter 教程](https://www.edureka.co/blog/jmeter-tutorial/)和[如何安装 JMeter](https://www.edureka.co/blog/how-to-install-jmeter/) 获取更多知识。

### **JMeter 中实现关联的步骤**

*   首先，你必须启动你的 **JMeter** 并选择**测试计划**。
*   接下来，右击**测试计划**，添加一个**线程组**。

![Thread group - jmeter correlation - edureka](img/38b19ff6884b39e46f9f108f3df2186e.png)

*   然后你要添加 **HTTP 请求**，输入**服务器名称或者任何网站的 IP** 。这将是步骤 1 的请求。右键点击**线程组**，选择**采样器**，添加 **HTTP 请求**。

![HTTP Request - JMeter correlation - edureka](img/bbfe03754827cc66570b45e1f84ac140.png)

*   在 **HTTP 请求**中添加服务器名称后，需要添加**正则表达式提取器**从步骤 1 的响应中提取一些值。右键点击 **HTTP 请求**，选择**后处理器**，添加**正则表达式提取器**。

![](img/376e42356671d032af17471862c77dd7.png)

*   添加正则表达式提取器后，有四个重要字段需要填写，以便成功提取一些响应值。 1。**创建的变量名称**–指定任意变量名称 2。**Regular Expression**–添加您想要从服务器 3 获取的任何正则表达式。**模板**–在你的正则表达式 中添加组数 4。**匹配编号**–为您的正则表达式添加任意数量的匹配

![](img/517520771cb2bd04be2ebc27df5cd6fd.png)

*   现在，我们需要另一个 **HTTP 请求**，它的请求数据将从第一个 HTTP 请求的响应数据中提取。 1。右键点击**线程组**，添加另一个 **HTTP 请求**。 2。在第二步中，您不需要指定任何服务器名称。获取对**变量名**的引用，并将其设置为第二个 HTTP 请求的**路径**。 3。名称要用' **$** '和**花括号**来指定。

![HTTP Request Step 2 - JMeter Correlation - Edureka](img/c1ba0abbffd06c56ac7bd9c9644f9616.png)

*   要查看**测试结果**并查看两个步骤之间的相关性，您需要添加一个**监听器**。右键点击线程组，选择监听器，添加**查看结果树**。

![](img/e44cad7912570484559e1f50f9dde1c5.png)

*   最后一步是**运行**和**验证测试**。一旦测试成功，您将看到第一个 HTTP 请求的一些响应值被提取出来作为第二个 HTTP 请求的请求。这显示了两个步骤之间的**相关性**。

![Test Result - JMeter correlation - edureka](img/79b6157cee2fe153bb1a40c66a7dda16.png)

借助正则表达式提取器，这些步骤将帮助您在 JMeter 中实现关联。我希望你明白这个过程中涉及的不同步骤。

*既然你已经知道了如何在 JMeter 中实现关联，那就来看看 Edureka 的 [**性能测试使用 JMeter 课程**](https://www.edureka.co/jmeter-training-performance-testing) 。本课程让您深入了解工作负载期间的软件行为。在本课程中，您将学习如何检查软件的响应时间和延迟，以及测试软件包是否能够高效扩展。它将帮助您检查强度并分析应用程序在不同负载类型下的整体性能。*

*有问题吗？请在“JMeter 相关性”的评论部分提到它，我们会给你回复。*