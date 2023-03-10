# Java 中的 JSP 是什么？了解所有 Java Web 应用程序

> 原文：<https://www.edureka.co/blog/jsp-in-java/>

思考什么是 JSP 及其用法？嗯，你来对地方了！ **Java 服务器页面**，俗称 [JSP](https://www.edureka.co/blog/servlet-and-jsp-tutorial/) 技术是 Java web 技术之一。它是一种服务器端技术，主要用于创建 web 应用程序。我来和大家深入探讨一下 JSP 的概念。

在本文中，我将讨论以下几点:

*   [什么是 JSP 页面？](#WhatisaJSPpage?)T3
*   [JSP 技术的特点](#FeaturesofJSPtechnology)
*   [JSP 页面的生命周期](#LifecycleofaJSPpage)
*   [JSP 的语法](#SyntaxofJSP)
*   [什么是 Java Servlet？](#WhatisJavaservlet?)T3
*   [一个简单的 JSP 页面](#AsimpleJSPpage)
*   [如何运行一个 JSP 页面？](#HowtorunaJSPpage?)

从简化 JSP 技术的概念开始，我先给大家介绍一下基础知识。

*JSP 技术基本上是一种广泛用于开发 JSP 页面的语言。这项技术创建了由动态和静态组件组成的 web 内容。*

现在，让我解释一下什么是 JSP 页面！

## **什么是 JSP 页面？**

一个 JSP 页面就是一个 文本文档。它包含两种类型的文本:*静态内容和动态内容*。静态内容可以用任何基于文本的格式表示，比如说， [HTML](https://www.edureka.co/blog/what-is-html/) 。而动态内容由 Java 代码组成。这里的 JSP 技术将静态内容与 Java 代码结合起来，从而使它成为一个动态的网页。 一个 [JSP](https://www.edureka.co/blog/servlet-and-jsp-tutorial/#JSP) 页面的源文件的文件扩展名应该是**。jsp** 。JSP 页面片段的源文件扩展名为 **.jspf.**

现在您已经熟悉了 JSP 页面和 JSP 技术的概念，让我们继续了解 JSP 的特性吧！

## **JSP 技术的特点**

**1。简易编码**

JSP 允许基于标签的编程。因此，不需要 Java 语言方面的专业知识。HTML 标签易于使用，因此代码易于阅读。

**2。互动网页**

构建能够在实时环境中与用户互动的动态网页。

### **3。轻松连接到数据库**

它允许我们轻松地连接到数据库，因为它主要与服务器连接。

在学习了这些特性之后，让我们继续向前，看看 JSP 页面的生命周期。

## JSP 页面的生命周期

**![JSp Life Cycle - JSP in Java - Edureka](img/e736b823b2264524233f485874cd9944.png)**

让我解释一下上图中的步骤。

**1。JSP 页面翻译:**

从 JSP 源文件创建一个 Java servlet 文件。在翻译阶段，容器验证 JSP 页面和标记文件的正确性。

**2。JSP 页面编译:**

将创建的 java servlet 文件编译成 Java [servlet](https://www.edureka.co/blog/servlet-and-jsp-tutorial/) 类。

**3。类别加载:**

从 JSP 源代码编译的 java servlet 类现在被加载到容器中。

**4。执行阶段:**

在执行阶段，容器创建这个类的一个或多个实例来响应请求。 接口 JsP 页面包含 jspInit()和 jspDestroy()。JSP 为专门用于 HTTP 请求的 JSP 页面提供了特殊的接口 HttpJspPage，该接口包含 _jspService()。

**5。初始化:**

*创建实例后立即调用 jspInit()* 方法。

**6。jspDestroy()执行:**

这个方法在 JSP 被销毁的时候被调用。通过这个调用，servlet 完成了它的目的，并进入垃圾收集，从而结束了 JSP 生命周期。

JSP 中提供了某些生命周期方法，它们是:jspInit()，_jspService()和 jspDestroy()，如上所述。

了解生命周期很重要。它让你深入了解实际的功能。现在，让我们看看并理解创建 JSP 页面时使用的语法。

**JSP 语法**

JSP 中以下内容的语法:

### **1。JSP 表达式**

```
<%= expression %>
```

**举例:**

```
&<%marks1 = marks1 + marks2 %>
```

### **2。申报标签**

```
<%! Dec var %>
```

**举例:**

```
<%! int var = 50; %>
```

### **3。JSP scriptlet**

```
<% java code %>
```

在这里，您可以插入各自的 Java 代码。

### **4。JSP 评论**

```
<% -- JSP Comments %>
```

我们都熟悉 JSP 的语法，现在让我简单介绍一下术语“Java servlet”。

## 什么是 servlet？

Java servlets 是在 Web 应用程序中获得 Java 全部功能的第一次尝试。它们是用 [Java](https://www.edureka.co/blog/java-tutorial/) 编写的。为了让您更熟悉 servlets，让我向您展示代码。要了解更多信息，请浏览“[Java servlet 简介](https://www.edureka.co/blog/java-servlets) ”博客！

现在，让我给你看一段代码，它将教你创建一个 JSP 页面。

**一个简单的 JSP 页面**

```
<HTML>
<HEAD>
<TITLE>A Web Page</TITLE>
</HEAD>
<BODY>
<% out.println ("JSP in JAVA") ; %>
</BODY>
</HTMl>
```

从上面的代码中可以看出，创建一个 JSP 页面是多么容易。这种更简单的方法帮助 JSP 取得了如此好的成绩。已经使用了简单的 HTML 标签。一个附加元素**<% out . println(" JAVA 中的 JSP ")；% >** 可见一斑。这个元素叫做 scriptlet！它包括一个在 HTML-JSP 代码中使用的 java 代码。

进一步，让我们深入学习如何运行 JSP 页面。

## **如何运行 JSP 页面**

JSP 的执行包括几个步骤。下面提到这些:

1.  首先，创建一个 HTML 文件，比如说 ana.html，从这里一个请求将被发送到服务器。

2.  其次，创建一个. jsp 文件，比如说 ana1.jsp，这将处理用户的请求。

3.  第三，创建项目文件夹结构。

4.  现在，您需要创建一个 XML 文件，然后创建一个 WAR 文件。

5.  之后，启动 Tomcat

6.  最后，您已经准备好运行应用程序了。

在 JSP 文件中执行上面编写的代码时，输出如下所示:

![JSP in Java Output - JSP in Java - Edureka](img/cbc66c674b3decbdadd9757dc976d6a0.png)

至此，我们已经接近了本文的结尾。我希望你读的内容是有益的。我们将继续用更多的话题探索 Java 世界。敬请期待！

*查看 Edureka 的* [***Java 培训***](https://www.edureka.co/java-j2ee-soa-training)*，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这个“*[*JSP in Java*](https://docs.google.com/document/d/1Nh6o8u4eGVn-utJI1JcuCX_s2r0q7Szz_6dAhi3HRt0/edit?ts=5d19dccd#heading=h.gjdgxs)*”博客的评论区提出来，我们会尽快回复您。*