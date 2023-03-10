# 如何安装 JMeter 的分步指南

> 原文：<https://www.edureka.co/blog/how-to-install-jmeter/>

人工执行性能测试是相当困难的，所以不可避免地我们要依靠性能测试工具来完成这项工作。JMeter 用于确保及时优质交货。这篇关于“**如何安装 JMeter** ”的文章将按以下顺序提供一步一步的指导:

*   [JMeter 简介](#jmeter)
*   [安装 JMeter 的先决条件](#jmeterprerequisites)
*   [如何安装 JMeter](#installjmeter)

## **JMeter简介**

[Apache JMeter](https://www.edureka.co/blog/jmeter-tutorial/) 是一个[测试工具](https://www.edureka.co/blog/performance-testing-tools/)，用于分析和测量不同软件服务和产品的性能。这是一个纯 Java 开源软件，用于测试 Web 应用程序或 FTP 应用程序。

![Apache JMeter - how to install JMeter - edureka](img/b993eacf4ef099202537b8712be93f8f.png)

用于执行 web 应用的[性能测试](https://www.edureka.co/blog/performance-testing-tutorial/)、[负载测试](https://www.edureka.co/blog/load-testing-using-jmeter/)和[功能测试](https://www.edureka.co/blog/what-is-functional-testing/)。JMeter 还可以通过为 web 服务器创建大量虚拟并发用户来模拟服务器上的重负载。

**JMeter 如何执行测试？**

让我们看看 JMeter 在测试过程中执行的不同步骤:

1.  它创建一个请求并发送给服务器。
2.  它接收来自服务器的响应，收集它们，并在图表中显示这些细节。
3.  它处理来自服务器的响应。
4.  它以文本、XML、JSON 等多种格式生成测试结果，以便测试人员可以分析数据。

现在您已经知道了什么是 JMeter 以及它是如何工作的，让我们继续，看看安装 JMeter 的先决条件。

## **安装 JMeter 的先决条件**

JMeter 是一个纯 Java 的桌面应用程序。它需要完全兼容的 JVM 6 或更高版本。您需要下载并安装最新版本的 Java SE 开发工具包。

与 JMeter 兼容的操作系统有:

*   Linux 操作系统
*   Windows 操作系统
*   mac 操作系统
*   人的本质

现在让我们继续，看看 JMeter 安装过程中涉及的步骤。

**JMeter 安装| edu reka**



[//www.youtube.com/embed/hzoZmaeT4ww?rel=0&showinfo=0](//www.youtube.com/embed/hzoZmaeT4ww?rel=0&showinfo=0)

这个关于“如何安装 JMeter”的 edureka 视频将为您提供如何安装 JMeter 以及 JMeter 工作的先决条件的逐步指导。它还帮助您理解如何创建一个测试计划。

## **如何安装 JMeter**

JMeter 安装过程中涉及的步骤包括:

**步骤 1–安装 Java**

![InstallJava-install jmeter - edureka](img/df5f940fbb8fb55bd43fbec08ecbdaaa.png)

JMeter 是一个纯粹的 Java 桌面应用程序，它需要完全兼容的 JVM 6 或更高版本。您可以下载并安装最新版本的 Java SE 开发工具包。

您可以在命令提示符下检查安装是否成功。它将为您提供以下输出:

![java-output-install jmeter - edureka](img/c0261b4fa1d175b3c4af0fad53e3372b.png)

**步骤 2–下载 JMeter**

![download-jmeter-install jmeter - edureka](img/b1267300a9b600456a7b496f1d6206d9.png)

JMeter 的最新版本是 5.1。您可以下载任何二进制文件。

**步骤 3–安装 JMeter**

![Install-jmeter-edureka](img/d6d392ce6312d2b1e2f34c588d553378.png)

JMeter 的安装极其容易和简单。您只需将 zip/tar 文件解压到您希望安装 JMeter 的目录中。没有繁琐的安装屏幕需要处理。

如果你使用的是 Windows，只需运行文件 **/bin/jmeter.bat** 在 GUI 模式下启动 JMeter:

![Jmeter-GUI-install Jmeter - edureka](img/b2a79596f1dac63eb5fd703c49d8e045.png)

现在您已经理解了安装过程，您可以在 JMeter 中借助不同的元素创建您自己的测试计划。

JMeter 的不同组件被称为元素。每个元素都有特定的用途。一些主要因素是:

*   线程组
*   样品
*   听众
*   配置

**线程组** 线程组是线程的集合。每个线程代表一个使用被测应用程序的用户。它模拟一个真实的用户对服务器的请求。线程组的控件还允许您设置每个组的线程数量。

![Threads- install jmeter - edureka](img/29eda7bfbb2cb4a846ddd9ed2588f606.png)

### **采样器**

JMeter 支持测试 HTTP、FTP、JDBC 和许多其他协议。线程组模拟用户对服务器的请求。采样器帮助线程组知道哪种类型的请求(HTTP、FTP 等。)它需要制造。

![Samplers - edureka](img/f4f44b695507921419761d97ab2cd139.png)

*   **FTP 请求:**可以使用 JMeter 中的 FTP 请求采样器在 FTP 服务器上做性能测试。该控制器允许您向 FTP 服务器发送 FTP“下载文件”或“上传文件”请求。
*   这个采样器可以让你发送一个 HTTP/HTTPS 请求到一个 web 服务器。
*   **请求:**这个采样器让您执行数据库性能测试。它向数据库发送一个 JDBC 请求。
*   BSF 取样器:这个取样器允许你使用 BSF 脚本语言编写一个取样器。
*   **访问日志采样器:**这个采样器允许你读取访问日志并生成 HTTP 请求。
*   **SMTP 采样器:**该采样器用于使用 SMTP 协议发送电子邮件消息。

### **听者**

监听器显示测试执行的结果。它们可以以不同的格式显示结果，如树、表、图或日志文件。

![Listener- edureka](img/282e3c034a1643cfc246586d360bb44f.png)

*   图形结果监听器在图形上显示服务器响应时间
*   查看结果树以基本 HTML 格式显示用户请求的结果
*   表格结果以表格形式显示测试结果的总结
*   日志显示了摘要文本文件中的一个测试结果

### **配置元素**

配置元素用于设置缺省值和变量，供采样器以后使用。

![Configuration - edureka](img/a01a1251cf71d9fab1782ce3d3ccdd36.png)

*   **CSV 数据集配置:**CSV 数据集配置允许您从文本文件中读取不同的参数。它用于从文件中读取行，并将它们分成变量。
*   **HTTP Cookie Manager:**HTTP Cookie Manager 具有与 web 浏览器相同的功能。如果您有一个 HTTP 请求，并且响应包含一个 cookie，cookie 管理器会自动存储该 Cookie，以便在将来的所有请求中使用。
*   **HTTP 请求默认值:**这个元素允许您设置 HTTP 请求控制器使用的默认值。
*   **Login Config 元素:**log in Config 元素允许您添加或覆盖采样器中的用户名和密码设置。

至此，我们已经到了“如何安装 JMeter”这篇文章的末尾。您已经准备好为性能测试创建您自己的测试计划。

*既然您已经知道如何安装 JMeter，那么就来看看由 Edureka 提供的使用 [JMeter 认证](https://www.edureka.co/jmeter-training-performance-testing)课程的**性能测试吧，Edureka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。本课程让您深入了解工作负载期间的软件行为。在本课程中，您将学习如何检查软件的响应时间和延迟，以及测试软件包是否能够高效扩展。本课程将帮助您检查强度并分析应用在不同负载类型下的整体性能。***

有问题要问我们吗？请在“如何安装 JMeter”的评论部分提到它，我们会给你回复。