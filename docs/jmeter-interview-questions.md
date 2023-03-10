# 2023 年你需要掌握的 30 个 JMeter 面试问题

> 原文：<https://www.edureka.co/blog/interview-questions/jmeter-interview-questions/>

如果你的软件加载时间过长或者在运行时停止，用户会直接关掉它。你需要最好的测试工具来留住你的客户。这些 **JMeter 面试问答**将帮助你开始你的软件测试职业生涯**。**这些都是向 **[JMeter 培训](https://www.edureka.co/jmeter-training-performance-testing)** 专家咨询后收集的。

## **阿帕奇 JMeter 面试问题**

### **Q1。JMeter 是什么？**

![Apache JMeter - JMeter interview questions - edureka](img/2c49de5c8a34cd530eca3946af5b4cc5.png)

JMeter 是 Java 工具之一，用于执行客户端/服务器应用程序的负载测试。 [Apache JMeter](https://www.edureka.co/blog/jmeter-tutorial/) 是一款开源软件，一款 100%纯 Java 桌面应用，旨在加载测试功能行为和测量应用性能。

### **Q2。JMeter 是如何工作的？**

![working of jmeter - jmeter interview questions - edureka](img/6b240835b73be803017e0c3a63715464.png)

JMeter 就像一组向目标服务器发送请求的用户。它收集来自目标服务器的响应和其他统计数据，这些数据通过图表或表格显示应用程序或服务器的性能。

### **Q3。JMeter 中有哪些正则表达式？**

正则表达式用于搜索和操作文本。JMeter 用于解释在整个 JMeter 测试计划中使用的正则表达式或模式的形式。

### **Q4。JMeter 支持哪些协议？**

JMeter 支持的协议有:

*   Web: HTTP，HTTPS 网站‘Web 1.0’Web 2.0
*   Web 服务:SOAP / XML-RPC
*   通过 JDBC 驱动程序的数据库
*   目录:LDAP
*   通过 JMS 面向消息传递的服务
*   服务:POP3，IMAP，SMTP
*   FTP 服务

### **Q5。JMeter 中的测试计划是什么？**

测试计划提供了 web 应用程序以及客户端-服务器应用程序的布局。它可以被视为运行测试的容器。一个完整的测试计划将由一个或多个元素组成，比如线程组、逻辑控制器、样本生成控制器、监听器、定时器、断言和配置元素。测试计划必须至少有一个线程组。

### **Q6。什么是采样器&线程组？**

**采样器**–采样器生成一个或多个样本结果。这些样本结果有许多属性，如运行时间、数据大小等。它允许 JMeter 向服务器发送特定类型的请求，通过采样器，线程组决定它需要发出哪种类型的请求。一些有用的采样器是 HTTP 请求，FTP 请求，JDBC 请求等。

**![samplers & threadgroups - performance testing interview questions - edureka](img/1469ffa8f1019b9ec388e4cd35fed265.png)线程组**–JMeter 是线程组元素的开始部分。它是 JMeter 的一个重要元素，在这里你可以设置用户数量和时间来加载线程组中给定的所有用户。

### **Q7。JMeter 中的处理器有哪些类型？**

JMeter 的两种类型是:

![jmeter processor - jmeter interview questions - edureka](img/88b2536611a8dcb5dcd4d00b9c64605e.png)

*   预处理器
*   后处理器

### **Q8。什么是预处理器元素？列出一些元素。**

预处理器是在采样器执行之前发生的事情。为了在执行之前配置样本请求或者更新不是从响应文本中提取的变量，使用了预处理元素。

一些预处理**元素**包括:

*   HTTP URL 重写修饰符
*   HTTP 用户参数修饰符
*   HTML 链接解析器
*   BeanShell 预处理器

### **Q9。JMeter 中的定时器是什么？它有哪些类型？**

默认情况下，JMeter 线程会不间断地发送请求。计时器用于在请求之间获得暂停。

![](img/2f3fe2cd4f2b63f9db622f845ff30d3e.png)

JMeter 中不同类型的定时器有:

*   **常量计时器**–这个元素将线程组中的每个请求延迟相同的时间。
*   **高斯定时器**–该元素用于将每个用户请求延迟一段随机的时间。
*   **同步定时器**–该元素用于在给定点释放线程数。
*   **统一随机定时器**–该元素用于将每个请求延迟一段随机时间。

### **Q10。什么是测试片段？**

测试片段是一种类似线程组元素的元素类型。唯一的区别是测试片段没有被实现，除非它被模块控制器或包含控制器引用。

### **Q11。JMeter 中的断言是什么？列出断言的类型。**

**断言**有助于验证测试中的服务器是否返回预期的结果。

断言的类型包括:

![](img/3cb62ead6541a2cd6bf5e03f36d53bd1.png)

*   **响应断言**–它通过将服务器响应与字符串模式进行比较来检查结果是否符合预期，从而方便用户。
*   **持续时间断言**–您可能需要测试服务器的响应是否达到用户定义的时间。如果花费的时间超过定义的时间，服务器响应将失败。
*   **大小断言**–测试来自服务器的每个响应是否包含预期的字节数。它便于用户指定尺寸。
*   **XML 断言**–它验证来自服务器的响应以正确的 XML 格式保存数据。
*   **HTML 断言**–它有助于检查响应数据的语法。

### **Q12。测试元素的执行顺序是什么？**

测试元素的执行顺序如下:

*   配置元素
*   预处理器
*   定时器
*   采样器
*   后处理器(除非 SampleResult 为空)
*   断言(除非 SampleResult 为空)
*   监听器(除非 SampleResult 为空)

### **Q13。什么是配置元素？**

配置元素帮助您创建采样器使用的默认值和变量。它们还用于添加或修改采样器发出的请求。这些元素在它们所属的作用域开始时执行。因此，只能从放置配置元素的分支内部访问配置元素。

### **Q14。如何降低 JMeter 中的资源需求？**

减少 JMeter 中的资源需求:

*   使用[非 GUI](https://www.edureka.co/blog/load-testing-using-jmeter/) 模式。
*   在加载期间，测试不使用“查看结果树”或“查看表中的结果”监听器。它仅在脚本阶段使用。
*   不要使用功能模式。
*   不要使用类似的取样器。相反，在循环中使用相同的采样器，并使用变量来改变采样。

### **Q15。** **你如何确保 JMeter 脚本的可重用性？**

您可以通过以下方式确保可重用性:

*   使用配置元素，如“ **CSV 数据集配置**”、“**用户定义变量**”等，以实现更好的数据重用。
*   将共享任务模块化，并通过一个**模块控制器**调用它们。
*   编写自己的 **BeanShell** 函数，并重用它们。

### **Q16。如何在 JMeter 中进行尖峰测试？**

通过同步，可以实现定时器 JMeter 尖峰测试。同步计时器，阻塞线程，直到特定数量的线程被阻塞，然后将它们一起释放，从而产生巨大的瞬时负载。

### **Q17。提到一些 JMeter 监听器。**

一些 JMeter 监听器是 **:**

*   样条可视化器
*   汇总报告
*   查看结果树
*   查看表中的结果
*   监控结果
*   分布图
*   BeanShell 监听器
*   总结报告

### **Q18。如何在 JMeter 中抓取认证窗口的脚本？**

![Authentication - jmeter interview questions - edureka](img/d18f495f1f4b03fc78f1dc5ca4929fcb.png)您可以通过以下方式录制捕获[剧本](https://www.edureka.co/blog/jmeter-script-recording/):

*   首先你必须在 Testplan 中使用 Threadgroup，然后在 Workbench 中使用 HTTPProxyServer。
*   接下来，在全局设置框中设置端口号，并在 IE 中修改您的连接设置为地址中的本地主机。
*   然后你可以在 JMeter 中启动 http 代理服务器，运行你的应用程序进行登录。

### **Q19。JMeter 中的控制器有哪些类型？**

JMeter 中的两种控制器是:

![Types of Controllers - jmeter interview questions - edureka](img/971b9c6a8d5009e5409202658943230f.png)

*   **采样器控制器**–采样器允许 JMeter 向服务器发送特定类型的请求。它们模拟用户从目标服务器请求页面。
*   **逻辑控制器**–逻辑控制器让您控制线程中采样器的处理顺序。它可以改变来自任何子元素的请求的顺序。

### **Q20。什么是前置处理器&后置处理器元素？**

**预处理器**–预处理器是在采样器执行之前发生的事情。它们通常用于在运行之前修改示例请求的设置。

**后处理器**–后处理器在采样器完成执行后执行。这个元素最常用于处理响应数据。

### **Q21。监听测试有什么用？**

监控测试的一些用途有:

*   监视器对于[压力测试](https://www.edureka.co/blog/stress-testing-using-jmeter/)和系统管理很有用。
*   与压力测试一起使用，监视器提供关于服务器性能的附加信息。
*   监视器使得在客户端查看服务器性能和响应时间之间的关系变得更加容易。
*   作为一种系统管理工具，显示器提供了一种从一个控制台监控多台服务器的简单方法。

### **Q22。JMeter 为性能测试提供了哪些好处？**

JMeter 为[性能测试](https://www.edureka.co/blog/performance-testing-tutorial/)提供的一些好处有:

*   它可用于测试静态资源和动态资源的性能。
*   JMeter 可以处理的并发用户数量超过了你的网站所能处理的最大数量。
*   它提供性能报告的图形分析。

### **Q23。什么是分布式负载测试&如何实现它？**

**![](img/67332775362590742ed86e03f2d11755.png)**

**分布式[负载测试](https://www.edureka.co/blog/load-testing-using-jmeter/)** 是可以用众多系统来模拟大量用户的负载的过程。JMeter 可以在主从配置的帮助下进行分布式负载测试。

### **Q24。JMeter 中数据参数化有哪些不同的方式？**

**![Data parameterization - jmeter interview questions - edureka](img/bebb69bed17976e0f6cbf2dee57f39c3.png)**

**数据参数化**使得脚本可以重用，不需要为具有不同参数的相同请求硬编码值。

### **Q25。 [JMeter & LoadRunner](https://www.edureka.co/blog/jmeter-vs-loadrunner/) 有什么区别？**

| **JMeter** | **【加载者】** |
| 

*   Open source tool developed by Apache

*   It is lacking in UI
*   is not technically sound
*   SAP & Xibei is not supported.

 | 

*   Authorized software
*   by Mercury
*   The developed UI is very impressive
*   It has more technical capabilities
*   Support SAP, Xibei & PeopleSoft

 |

### **Q26。JMeter 支持哪些重要的插件？**

JMeter 支持的重要[插件](https://www.edureka.co/blog/jmeter-plugins/)有:

![plugins - jmeter interview questions - edureka](img/67979465d5bde9a6d1e9e8d01fe64c33.png)

*   线程组插件
*   监听器插件
*   采样器插件

### **Q27。提到 JMeter 和 SoapUI 的区别。**

|  | **肥皂泡** |
| 

*   It is used for load and performance testing HTTP, JDBC, JMS, Web Service(SOAP), etc.
*   Support distributed load test
*   [ IDE needs JMeter suite and load generator plug-in

 | 

*   It is dedicated to web services and has a more user-friendly IDE
*   It does not support distributed load testing
*   For most IDEs, it has plug-in support

 |

### **Q28。什么是工作台？**

**工作台**是添加一些组件的存储区，如果需要可以添加到测试计划中。工作台的组件不会自动与测试计划一起保存。它们必须作为测试片段单独保存。

### **Q29。JMeter 中有必要显式调用嵌入式资源吗？**

你可以避免所有嵌入的资源被显式调用。请求底部有一个名为“检索嵌入资源”的复选框它会抓住所有的 CSS，JPG 等。这是在 web 应用程序中查找资源和断开的链接的一个绝妙方法。

### **Q30。正则表达式中的“包含”和“匹配”表示什么？**

在正则表达式中，**包含**表示正则表达式至少匹配目标的某个部分。而**匹配**意味着正则表达式匹配整个目标。所以，alphabet 和 al 是匹配的。*t.'

说到这里，我们已经到了 JMeter 面试问题篇的结尾。我希望这些 **JMeter 面试问题**能对你的面试有所帮助。如果你最近参加过面试，请把这些面试问题贴在评论区，我们会回答。

*此外，请查看 Edureka 的[性能测试认证培训](https://www.edureka.co/jmeter-training-performance-testing)，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。本课程让您深入了解工作负载期间的软件行为。在本课程中，您将学习如何检查软件的响应时间和延迟，以及测试软件包是否能够高效扩展。本课程将帮助您检查强度并分析应用在不同负载类型下的整体性能。*