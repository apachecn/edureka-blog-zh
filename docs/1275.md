# Java 中的动态网页:如何用 Java 创建网页？

> 原文：<https://www.edureka.co/blog/dynamic-web-pages-in-java/>

动态网页是当前的需要。主要原因是需要满足快速不断变化的内容的要求。本文重点介绍了在 [Java](https://www.edureka.co/blog/java-tutorial/) 中的动态网页。本文将涉及以下几点。

*   [Java 中的动态网页](#DynamicWebPagesInJava)
*   什么是 web 服务器？
*   [什么是 CGI？](#WhatisCGI?)
*   [什么是 servlet 容器](#Whatisservletcontainer)

让我们从 Java 文章中的动态网页开始，

**动态网页**

动态网页是服务器端的网页，每次浏览时，我们看到不同的内容。它由处理服务器端脚本的应用服务器控制。动态网页也可以根据客户端的请求改变其内容。他们有能力根据时间和需要生成新的内容。这意味着动态网页对所有用户来说都不一样。

我们都很清楚在日常生活中对动态网页的需求。

我们经常看到的动态网页的最好例子是验证码。

静态网页和动态网页的主要区别在于，静态网页对所有客户端或用户保持不变，而动态网页会根据时间和用户的请求改变自己。

**servlet**

在 Java 中，servlet 是创建动态网页的一种方式。Servlets 只不过是 java 程序。 在 java 中，servlet 是一种运行在服务器端 JVM(java 虚拟机)上的 Java 类。Java servlet 在服务器上工作 side.Java servlet 能够处理大型复杂的问题和用户的请求。

让我们进一步了解 java 中的动态网页

什么是 web 服务器？

web 服务器用于以 HTTP 协议的形式传输数据。客户只需在浏览器中键入 URL，web 服务器就会向她/他提供所需的网页以供阅读。那么，它是如何工作的..？web 服务器在内部做什么？

web 服务器将客户端键入的 URL 转换成 HTTP 协议，以便响应请求，并在 Servlets 的帮助下，为客户端的请求提供服务。

**servlet 的属性**

*   Servlets 在服务器端扩展上工作，以处理复杂的问题。
*   Servlets 涵盖了 **CGI 的所有限制。**

让我们进入本网页的下一个主题 Java 文章，

**什么是 CGI？**

CGI(common gateway interface)，是一个用来产生网页动态内容的应用程序。可以使用任何编程语言创建通用的网关接口，如 **c、c++** 等。

使用 CGI 时，当客户端请求任何东西时，web 服务器依次执行以下任务:-

*   它接收请求和所需的 CGI。
*   它生成一个新的进程并调用所需的 CGI 应用程序。
*   CGI 得到客户端请求的信息后，生成输出。
*   它将输出(响应)发送到 web 服务器，并销毁该进程。
*   Web 服务器将它显示在客户端的屏幕上。

在 CIG 中，it 必须为每个请求创建和销毁新的流程，随着客户端数量的增加，工作负载也会增加，因此性能会降低，处理请求的时间也会增加，因为 CGI 无法直接与 web 服务器通信。为了克服它的局限性，引入了 servlets。

Servlets 比 CGI 便宜，并且能够处理 cookies。java servlet 遵循一个简单的过程，如下面的框图所示:-

**步骤**

*   客户端将请求发送到网络服务器。
*   web 服务器接收来自客户端的请求。
*   Servlets 接收请求。
*   Servlets 处理请求并产生输出。
*   Servlet 将输出发送到 web 服务器。
*   web 服务器将它发送到客户端的浏览器，浏览器将它显示在客户端的屏幕上。

servlets 可以通过两个包来构建

*   javax.servlet(基本)
*   javax.servlet.http(高级)

**servlet 的优势**

*   它们是独立于平台的。
*   它们比 CGI 便宜。
*   他们有能力处理饼干。
*   他们克服了 CGI 的局限性。
*   无需为任何请求创建新流程。
*   由于它是服务器端应用程序，因此可以继承 web 服务器的安全性。

让我们进入 Java 网页文章的下一个主题，

## **什么是 servlet 容器**

用户没有请求和访问静态页面的功能，但也有动态的功能，其中动态网页每次可以根据不同的输入和时间以不同的方式工作。

servlet 容器只不过是使用它们的一个概念或想法

Java 语言开发动态网页(Servlet)。

Servlet 容器是 web 服务器的一部分，可以方便地与 java servlets 通信。

**客户端可以根据需要调用三种基本方法:-**

*   Init()
*   服务()
*   销毁()

### **Java 网页我们的第一个 servlet 程序**

为了开发我们的第一个 servlet 应用程序，我们将遵循三个步骤

首先，我们需要创建 HTML 页面，这将需要一些来自 servlet 的请求。

```
<html>
<head>
<title>First Servlet Program</title>
</head>
<body>
<form action=&rdquo;Servlet&rdquo;>
<input type="submit" value="invoke servlet">
</form>
</body>
</html>

```

这个页面只会有一个按钮 **调用 MyFirstServlet** 。当你点击这个按钮时，它将调用 **MyFirstServlet。** 现在我们将创建 servlet，我们将在其中实现三个方法:-

*   Init()
*   服务()
*   销毁()

```
Import javax,servlet. *;
Import java.io.*;
Public class OurFirstServlet implements Servlet{
ServletConfig config=null;
Public void init(ServletConfig sc)
{
Config = sc;
System.out.println(&ldquo;in&nbsp; init&rdquo;);
}
public void service(ServletRequest req, ServletResponse res)
throws ServletException, IOException
{
res.setContenttype("text/html");
PrintWriter pw = res.getWriter();
pw.println("<h2>hello from servlet</h2>");
System.out.println("in service");
}
//destroy method
public void destroy()
{
System.out.println("in destroy");
}
public String getServletInfo()
{
return "MyFirstServlet";
}
public ServletConfig getServletConfig()
{
return config;
}

```

在第 1 行和第 2 行中，我们导入了两个包，第二个是用于 PrintWriter 的。

在第 3 行，我们通过实现 servlet 接口来创建一个 Servlet。

在一个类的第一行，我们创建了一个 ServletConfig 对象 Config，它将包含 Servlet 的配置。最初，它被设置为 null，因为那里没有 Servlet。

然后我们创建了一个 init 方法，它接受一个 ServletConfig sc 类型的对象。当一个请求到达 Servlet 时，就会调用这个函数。这用于初始化配置对象。

有一个 destroy()用来标记 Servlet 的结束

getServletInfo()用于返回 Servlet 的名称

getServletConfig 在被调用时返回配置对象。

最后，在请求到达后，创建两个 ServletRequest 和 ServletResponse 类型的对象来标记它们与客户端的连接，并传递给服务()。这里，我们将 ServletResponse 对象的响应类型设置为 HTML 类型。然后我们通过调用 getWriter()从响应对象 res 中获取 PrintWriter 对象 pw。最后，我们使用 pw 对象的 println()编写要打印的内容以响应客户机。

这样，我们就结束了这篇关于“Java 网页”的文章。如果您希望了解更多信息，请查看值得信赖的在线学习公司 Edureka 提供的 [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。