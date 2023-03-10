# JavaScript Cookies——如何创建、读取和删除 Cookies？

> 原文：<https://www.edureka.co/blog/javascript-cookies/>

Cookies 帮助您在网页中存储用户信息。这是记忆和跟踪偏好、购买、佣金和其他更好的访问者体验或网站统计所需信息的最有效方法之一。在这篇 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) Cookies 文章中，我们将按照以下顺序深入探讨 Cookies:

*   什么是饼干？
*   它是如何工作的？
*   [JavaScript cookie](#javascriptcookies)
    *   [创建 cookie](#createcookies)
    *   [读饼干](#readcookies)
    *   [换饼干](#changecookies)
    *   [删除一个 Cookie](#deletecookies)

## 什么是饼干？

Cookies 是存储在系统中的小文本文件中的数据。当 web 服务器向浏览器发送网页时，连接会关闭，服务器会忘记用户的所有信息。

Cookies 是为了解决记忆用户信息的问题而发明的。例如:

*   当用户访问网页时，他/她的名字可以存储在 cookie 中。

*   下次用户访问该页面时，cookie 会记住用户名。

它会记住所有网页中的用户信息。它包含的信息是一个[字符串](https://www.edureka.co/blog/javascript-string-functions/)，并且是由分号分隔的名称-值对的形式，比如:

```
username = Daisy Green
```

现在让我们看看这些饼干是如何工作的。

## 它是如何工作的？

服务器以 cookie 的形式向访问者的浏览器发送一些数据。现在，浏览器可能会接受 cookie。如果有，它会以纯文本记录的形式存储在访问者的硬盘上。

当访问者到达你网站的另一个页面时，浏览器会将相同的 cookie 发送给服务器进行检索。一旦它被检索到，你的服务器就知道或记得以前存储了什么。

Cookies 由 **5 个可变长度字段**组成:

*   **到期**—显示 cookie 到期的日期。如果此项为空，cookie 将在访问者退出浏览器时过期。

*   **域**——域字段提供您站点的域名。

*   **路径**—它是设置 cookie 的目录或网页的路径。如果您想从任何目录或页面中检索 cookie，可以将其留空。

*   **Secure**—如果该字段包含单词“Secure ”,则只能通过安全服务器检索 cookie。如果该字段为空，则没有此类限制。

*   **Name = Value**—这描述了以键值对的形式设置和检索的 cookies。

现在你已经知道什么是 cookie 以及它是如何工作的，让我们深入了解 JavaScript cookies。

## **JavaScript cookie**

在 JavaScript 中，你可以用文档对象的 cookie 属性来操作 cookie。JavaScript 可以读取、创建、修改和删除应用于当前网页的 cookies。所以让我们来看看例子，了解一下 JavaScript 中是如何使用 cookies 的。

### **创建 cookie**

JavaScript 可以用 **document.cookie** 属性创建 cookie。您可以通过以下方式创建 cookie:

```
document.cookie = "username=Daisy Green";
```

您还可以为您的 cookie 添加到期日期。默认情况下，当浏览器关闭时，cookie 将被删除:

```
document.cookie = "username=Daisy Green; expires=Mon, 26 Aug 2019 12:00:00 UTC";
```

您还可以借助一个参数告诉浏览器 cookie 属于哪个路径。默认情况下，cookie 属于当前页面。

```
document.cookie = "username=Daisy Green; expires=Mon, 26 Aug 2019 12:00:00 UTC"; path=/";
```

### **读一块饼干**

由于文档的价值，读取 cookie 和编写 cookie 一样简单。cookie 对象就是 cookie。每当您想要访问 cookie 时，都可以使用这个字符串。document.cookie 字符串保留一个由分号分隔的 name=value 对列表，其中 name 表示 cookie 名称，value 是它的字符串值。

JavaScript Cookies 可以通过以下方式读取:

```
var x = document.cookie;
```

**举例:**

```

<html>
   <head>   
      <script type = "text/javascript">
         <!--
            function ReadCookie() {
               var allcookies = document.cookie;
               document.write ("All Cookies : " + allcookies );

               // Get all the cookies pairs in an array
               cookiearray = allcookies.split(';');

               // Now take key value pair out of this array
               for(var i=0; i<cookiearray.length; i++) {
                  name = cookiearray[i].split('=')[0];
                  value = cookiearray[i].split('=')[1];
                  document.write ("Key is : " + name + " and Value is : " + value);
               }
            }
         //-->
      </script>      
   </head>

   <body>     
      <form name = "myform" action = "">
         <p> click the Button to View Result:</p>
         <input type = "button" value = "Get Cookie" onclick = "ReadCookie()"/>
      </form>      
   </body>
</html>

```

**输出:**

### **![read cookie - javascript cookies - edureka](img/07fcf50c7a222c495b06ffa6bf7acde4.png)**

### **换饼干**

JavaScript Cookies 的更改方式与您创建它的方式相同:

```
document.cookie = "username=Mary Lian; expires=Fri, 18 Sep 2019 12:00:00 UTC; path=/";
```

在这里，旧的 cookie 将被覆盖。

**举例:**

```
<html>
   <head>   
      <script type = "text/javascript">
         <!--
            function WriteCookie() {
               var now = new Date();
               now.setMonth( now.getMonth() + 1 );
               cookievalue = escape(document.myform.customer.value) + ";"

               document.cookie = "name=" + cookievalue;
               document.cookie = "expires=" + now.toUTCString() + ";"
               document.write ("Setting Cookies : " + "name=" + cookievalue );
            }
         //-->
      </script>      
   </head>

   <body>
      <form name = "myform" action = "">
         Enter name: <input type = "text" name = "customer"/>
         <input type = "button" value = "Set Cookie" onclick = "WriteCookie()"/>
      </form>      
   </body>
</html>
```

**输出:**

### **![](img/09bbbc19dd256ad8af94f6fe5eface20.png)**

### **删除一个 Cookie**

您可能希望删除一个 cookie，以便以后尝试读取该 cookie 时不返回任何内容。要删除 cookie，您只需将到期日期设置为过去的某个时间。

```
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
```

**举例:**

```
<html>
   <head>   
      <script type = "text/javascript">
         <!--
            function WriteCookie() {
               var now = new Date();
               now.setMonth( now.getMonth() - 1 );
               cookievalue = escape(document.myform.customer.value) + ";"

               document.cookie = "name=" + cookievalue;
               document.cookie = "expires=" + now.toUTCString() + ";"
               document.write("Setting Cookies : " + "name=" + cookievalue );
            }
          //-->
      </script>      
   </head>

   <body>
      <form name = "myform" action = "">
         Enter name: <input type = "text" name = "customer"/>
         <input type = "button" value = "Set Cookie" onclick = "WriteCookie()"/>
      </form>      
   </body>
</html>
```

至此，我们已经走到了 JavaScript Cookies 的尽头。我希望你知道如何创建、读取、修改和删除 cookies。

*既然你已经了解了 JavaScript 循环，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript Cookies”的评论部分提到它，我们会回复您。*