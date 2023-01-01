# 关于 Java 会话你需要知道的一切？

> 原文：<https://www.edureka.co/blog/session-in-java/>

这将向您介绍一个名为 Java 中的会话的主题，并简要介绍会话管理在 [Java](https://www.edureka.co/blog/java-tutorial/) 中是如何工作的。本文将涉及以下几点:

*   http session interface
*   [index.html](#index.html)
*   [Servlet1.java](#Servlet1.java)
*   [Servlet2.java](#Servlet2.java)
*   [web.xml](#web.xml)
*   [优势](#Advantages)
*   [缺点](#Disadvantages)

那么让我们开始吧，

## **Java 中的会话**

两个系统(即客户端和服务器)相互通信的时间间隔可以称为会话。简而言之，会话是由客户端和服务器之间的几个请求和响应组成的状态。

众所周知，HTTP 和 Web 服务器都是无状态的。因此，维护用户状态的唯一方法是利用实现会话跟踪的技术。servlets 中的会话跟踪可以通过多种方法实现，cookies 就是其中之一。然而，它们有许多缺点:

*   他们只能保存文本信息。
*   如果用户禁用了 cookies，web 应用程序就无法使用它们。
*   一个 cookie 不能包含超过 4kb 的数据。
*   实现会话跟踪的另一种方法是在 java servlet 中为每个用户创建具有唯一会话 id 的会话。

继续这篇关于 Java 会话的文章

## **Http 会话接口**

java 中的 Servlets 提供了一个名为“HttpSessionInterface”的接口。它们由各种方法组成，下面将讨论其中一些方法:

*   public http session getSession(boolean create):该方法获取与请求相关联的会话。如果它不可用或不存在，则会基于指定的布尔参数创建一个新会话。
*   public String getId():这个方法返回唯一的会话 Id。
*   public long getCreationTime():该方法返回会话创建的时间。它以毫秒为单位。
*   public long getLastAccessedTime():此方法返回上次访问会话的时间。它以毫秒为单位。
*   public void invalidate():可以使用此方法使会话无效。

**示例:** 在下面给出的示例中，我们使用了 HttpSession 接口的 getAttribute()和 setAttribute()方法。

继续 Java 文章的第一个例子

## **index.html**

```
<form action="loginform">
User Name:<input type="text" name="userName"/>
Password:<input type="password" name="userPassword"/>
<input type="submit" value="submit"/>
</form>

```

继续第二个例子

## **年代**ervlet1.java**年代**

```
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class Servlet1 extends HttpServlet {
public void doGet(HttpServletRequest request, HttpServletResponse response){
try{
response.setContentType("text/html");
PrintWriter pwriter = response.getWriter();
String name = request.getParameter("userName");
String password = request.getParameter("userPassword");
pwriter.print("Welcome "+name);
pwriter.print("Here is your password: "+password);
HttpSession session=request.getSession();
session.setAttribute("usname",name);
session.setAttribute("uspass",password);
pwriter.print("<a href='Welcome'>view details</a>");
pwriter.close();
}catch(Exception exp){
System.out.println(exp);
}
}

```

继续第三个例子

## **Servlet2.java**

```
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class Servlet2 extends HttpServlet {
public void doGet(HttpServletRequest request, HttpServletResponse response){
try{
response.setContentType("text/html");
PrintWriter pwriter = response.getWriter();
HttpSession session=request.getSession(false);
String myName=(String)session.getAttribute("usname");
String myPass=(String)session.getAttribute("uspass");
pwriter.print("Name: "+myName+" Pass: "+myPass);
pwriter.close();
}catch(Exception exp){
System.out.println(exp);
}
}
}

```

继续 Java 文章的第四个例子

## **web.xml**

```
<web-app>
<servlet>
<servlet-name>MyServlet1</servlet-name>
<servlet-class>Servlet1</servlet-class>
</servlet>
<servlet-mapping>
<servlet-name>MyServlet1</servlet-name>
<url-pattern>/loginform</url-pattern>
</servlet-mapping>
<servlet>
<servlet-name>MyServlet2</servlet-name>
<servlet-class>Servlet2</servlet-class>
</servlet>
<servlet-mapping>
<servlet-name>MyServlet2</servlet-name>
<url-pattern>/Welcome</url-pattern>
</servlet-mapping>
</web-app>

```

下面列出了该接口的各种优点和缺点:

## **Java 中的会话**

**优点:**

*   所有类型的对象，如数据库和文本，都可以存储到一个会话中。
*   会话是安全的。

带着缺点继续前进

**缺点:**

*   因为会话对象存储在服务器上，所以存在性能开销。
*   序列化和反序列化也会导致开销。

使用 session 接口来实现会话跟踪是非常有利的。

这样，我们就结束了这篇关于“Java 中的会话”的文章。如果您希望了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 认证课程](https://www.edureka.co/java-j2ee-training-course)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。