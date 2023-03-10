# 什么是 Java Web 应用程序？

> 原文：<https://www.edureka.co/blog/java-web-application/>

Web 应用程序是任何编程语言不可或缺的一部分。在本文中，我们将详细了解 [Java](https://www.edureka.co/blog/java-tutorial/) Web 应用。

*   什么是 Web 应用程序？
*   [Java Web 应用技术](#tech)
*   [总结](#summary)

## 什么是 Web 应用程序？

Web 应用程序本质上是分布式应用程序。这意味着任何在多台计算机上运行并使用网络和服务器进行通信的程序。Web 应用程序是使用 web 浏览器访问的，因此它们非常受欢迎，因为可以轻松地将浏览器用作用户客户端。无需在数千台客户端计算机上安装任何软件即可更新和维护 web 应用程序的能力成为这一需求的关键原因。

使用许多组件可以创建 web 应用程序，其中一些有用户界面，一些不需要图形用户界面(GUI)。此外，web 应用程序经常需要额外的标记或脚本语言，如 [HTML](https://www.edureka.co/blog/what-is-html/) 、CSS 或 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 编程语言。许多应用程序只使用 Java 编程语言，这是理想的，因为它的多功能性。

![java web application](img/4b65ebf8b3792cd1e05e68326ca8f237.png)

web 应用程序可以是一个显示当前日期和时间的简单页面，也可以是一组复杂的页面，您可以在这些页面上查找并预订下次度假最方便的航班、酒店和汽车租赁。

用于创建 web 应用程序的 Java 技术是 Java EE 平台的一部分。为了让这些技术在服务器上工作，服务器必须安装一个容器或 web 服务器，它可以识别并运行您创建的类。

## **Java Web 应用技术**

一篇文章中可以列出许多 Java 技术，所以这篇文章将描述最常用的技术。web 应用程序通常只包含一个用 JavaServer Pages (JSP)技术创建的页面。有时候你会结合三种或者更多这样的技术。无论您最终使用了多少，了解哪些是您可用的，以及如何在 web 应用程序中使用每一个都是很好的。

**Java Servlet API**

Java [Servlet](https://www.edureka.co/blog/servlet-and-jsp-tutorial/) API 允许您定义特定于 HTTP 的类。servlet 类扩展了承载通过请求-响应编程模型访问的应用程序的服务器的功能。尽管 servlets 可以响应任何类型的请求，但最常见的用途是扩展 web 服务器托管的应用程序。例如，您可以使用 servlet 从在线表单中获取文本输入，并以 HTML 页面和格式将其打印回屏幕，或者您可以使用不同的 servlet 将数据写入文件或数据库。servlet 运行在服务器端，没有自己的应用程序 GUI 或 HTML 用户界面(UI)。Java Servlet 扩展使许多 web 应用成为可能。

**JavaServer Pages 技术**

JavaServer Pages (JSP)技术提供了一种简单、快速的方法来创建动态 web 内容。JSP 技术支持独立于服务器和平台的基于 web 的应用程序的快速开发。JSP 技术允许您将 servlet 代码片段直接添加到基于文本的文档中。通常，JSP 页面是基于文本的文档，包含两种类型的文本:

*   静态数据，可以用任何基于文本的格式表示，如 HTML、无线标记语言(WML)或 XML

*   JSP 技术元素，决定页面如何构造动态内容

**JavaServer Pages 标准标签库**

JavaServer Pages 标准标记库(JSTL)封装了许多基于 JSP 技术的应用程序共有的核心功能。您不用在应用程序中混合来自众多供应商的标签，而是使用一组标准的标签。这种标准化允许您在任何支持 JSTL 的 JSP 容器上部署应用程序，并使标记的实现更有可能得到优化。

JSTL 有迭代器和条件标签用于处理流控制，标签用于操作 XML 文档，国际化标签，标签用于使用 SQL 访问数据库，标签用于常用函数。

**JavaServer Faces 技术**

JavaServer Faces 技术是一个用于构建 web 应用程序的 UI 框架。JavaServer Faces 技术的主要组件包括一个 GUI 组件框架，一个用各种标记语言和技术呈现组件的灵活模型，以及一个用于生成 HTML 标记的标准 RenderKit。

**Java 消息服务 API**

消息传递是软件组件或应用程序之间的一种通信方式。消息传递系统是一种对等设备。换句话说，消息客户端可以向任何其他客户端发送消息，也可以从任何其他客户端接收消息。每个客户端都连接到一个消息代理，该代理提供创建、发送、接收和读取消息的工具。通过将 Java 技术与企业消息传递相结合，Java 消息服务(JMS) API 为解决企业计算问题提供了一个强大的工具。

![Messaging](img/ae22b64eb7f4aa9fa084a6321c7e97b8.png)

企业消息传递为整个企业的业务数据交换提供了可靠、灵活的服务。JMS API 在此基础上增加了一个通用 API 和提供者框架，支持用 Java 编程语言开发可移植的基于消息的应用程序。如何使用 JMS 的一个例子是一个为汽车制造商跟踪库存的应用程序。

当产品的库存水平低于某个水平时，库存组件可以向工厂组件发送消息，这样工厂就可以生产更多的汽车。工厂组件可以向零件组件发送消息，以便工厂可以组装它需要的零件。零件组件又可以向它们自己的库存和订单组件发送消息，以更新它们的库存和从供应商处订购新零件，等等。

**JavaMail API 和 JavaBeans 激活框架**

Web 应用程序可以使用 JavaMail API 来发送电子邮件通知。API 有两个部分:应用程序组件用来发送电子邮件的应用程序级接口和服务提供者接口。服务提供商实施特定的电子邮件协议，例如 SMTP。JavaMail API 包中包含了几个服务提供者，其他服务提供者可以单独获得。Java EE 平台包括带有服务提供者的 JavaMail 扩展，允许应用程序组件发送电子邮件。

**用于 XML 处理的 Java API**

作为 Java SE 平台的一部分，Java API for XML Processing (JAXP)支持使用文档对象模型(DOM)、简单 XML API(SAX)和可扩展样式表语言转换(XSLT)来处理 XML 文档。JAXP 使应用程序能够独立于特定的 XML 处理实现来解析和转换 XML 文档。

JAXP 还提供了名称空间支持，这让你可以使用可能会有命名冲突的模式。JAXP 设计得非常灵活，允许您在应用程序中使用任何符合 XML 的解析器或 XSL 处理器，并支持 W3C 模式。

**JDBC API**

JDBC API 允许你从 Java 编程语言方法中调用数据库 SQL 命令。当您需要访问数据库时，可以在 servlet、JSP 技术页面或企业 bean 中使用 JDBC API。

JDBC API 有两个部分:应用程序组件用来访问数据库的应用程序级接口和服务提供者接口。

**Java 持久性 API**

Java 持久性 API 是一个基于 Java 技术标准的持久性解决方案。持久性使用对象关系映射方法来弥合面向对象模型和关系数据库之间的差距。Java 技术的持久性包括三个方面:

*   Java 持久性 API

*   查询语言

*   对象关系映射元数据

**Java 命名和目录接口**

Java 命名和目录接口(JNDI)提供命名和目录功能，使应用程序能够访问多种命名和目录服务。它为应用程序提供了执行标准目录操作的方法，例如将属性与对象相关联，以及使用对象的属性来搜索对象。使用 JNDI，web 应用程序可以存储和检索任何类型的命名 Java 技术对象，允许应用程序与许多遗留应用程序和系统共存。

命名服务为应用程序客户机、企业 beans 和 web 组件提供了对 JNDI 命名环境的访问。命名环境允许开发人员定制组件，而不必访问或更改组件的源代码。容器实现组件的环境，并将其作为 JNDI 命名上下文提供给组件。

## **总结**

至此，我们结束了这篇 Java Web 应用程序文章。

*查看 Edureka 提供的  [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。*

有问题要问我们吗？请在这个“Java Web 应用程序”博客的评论部分提到它，我们会尽快回复您。