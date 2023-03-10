# Express.js 教程——初学者的一站式解决方案

> 原文：<https://www.edureka.co/blog/expressjs-tutorial/>

Express.js 是一个快速轻量级的框架，主要用于 web 应用程序开发，全世界的 Node.js 开发人员都非常喜欢这个框架。Express.js 提供了 web 应用程序的所有功能，而没有掩盖 Node.js 的功能。通过这篇 Express.js 教程，我将让你对 Express.js 的基础有一个完整的了解，这将帮助你开始使用它。以下是本 Express.js 教程涵盖的主题:

*   [什么是 Express.js？](#express)
*   [express . js 的特点](#features)
*   [Express.js 安装](#install)
*   ![express logo - Express.js Tutorial - Edureka](img/c07585e34ac43e6cd2f286778f279f71.png) [ Express.js 基本概念](#fundamentals)
    *   [路由和 HTTP 方法](#routing)
    *   [中间件](#middleware)
    *   [饼干](#cookies)
    *   [REST API](#rest)
    *   [脚手架](#scaffolding)
    *   [数据库连接](#db)
    *   [模板化](#templating)
    *   [错误处理](#errorhandling)

让我们从这个 Express.js 初学者教程开始吧。

## **什么是 Express.js？**

通俗地说， Express.js 是一个构建在 [Node.js](https://www.edureka.co/blog/nodejs-tutorial/) 之上的 web 应用框架。它提供了一个最小的接口，包含构建 web 应用程序所需的所有工具。Express.js 为应用程序增加了灵活性，npm 上有大量可用的模块，您可以根据需要直接将这些模块插入 Express。它有助于在服务器端应用程序中轻松管理服务器和路由之间的数据流。由 **TJ Holowaychuk** 研发，于 2010 年 5 月 22 日投放市场。以前它由 IBM 管理，但是现在，它被置于 Node.js Foundation 孵化器的管理之下。

Express 主要负责处理 MEAN 栈中的后端部分。Mean Stack 是开源的 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 软件栈，在市场上被大量用于构建动态网站和网络应用。在这里， **的意思是** 代表 **M** ongoDB， **E** xpress.js，[**A**ngularJS](https://www.edureka.co/blog/what-is-angular-a-comprehensive-guide-to-get-started-with-angular/)，以及 **N** ode.js.

也就是说，现在让我们继续学习这个 Express.js 教程，了解这个框架的各种特性。

## **express . js 的特点**

下面我挑选了 Express.js 的一些最重要的特性:

1.  Express 加快了 web 应用程序的开发速度。
2.  它还有助于创建单页、多页和混合类型的移动和 web 应用程序
3.  Express 可以使用各种模板引擎，如 Pug、Mustache 和 EJS。
4.  Express 遵循模型-视图-控制器(MVC)架构。
5.  它使得与数据库的整合过程变得毫不费力，比如与 T2 的 MongoDB、Redis、T4 的 MySQL 的整合。
6.  Express 还定义了一个错误处理中间件。
7.  它有助于简化应用程序的配置和定制步骤。

这些是在 web 应用程序开发中使用 Express.js 的一些主要优势。在这篇 Express.js 教程文章的下一节中，让我向您展示如何在您的系统中安装 Express.js。

## **安装 Express.js**

为了在您的系统中安装 Express.js，首先，您需要确保已经安装了 Node.js。如果没有，那么不要担心，只需参考我关于 [Node.js 安装](https://www.edureka.co/blog/node-js-installation/)的文章，它会一步一步地指导你。完成 Node.js 安装后，下一步是安装 Express。

要安装 Express.js，首先，您需要创建一个项目目录，并创建一个 [package.json 文件](https://www.edureka.co/blog/node-js-npm-tutorial/#jsonfile)，它将保存项目依赖项。下面是执行相同操作的代码:

```
npm init
```

现在，您可以在系统中安装 express.js 包了。要全局安装它，您可以使用下面的命令:

```
npm install -g express
```

或者，如果您想将它本地安装到您的项目文件夹中，您需要执行以下命令:

```
npm install express --save
```

既然您已经完成了安装过程，现在让我们开始使用 Express.js。在本 Express . js 教程的下一部分，我将带您了解 Express 框架的基本概念。

## **Express.js 基本概念**

因此，我将在 Express.js 基础下讨论的第一个主题是路由。

### **1。路由和 HTTP 方法**

路由是指确定应用程序特定行为的过程。它用于定义应用程序应该如何响应客户端对特定路由、路径或 URI 以及特定 HTTP 请求方法的请求。 每条路线可以包含多个处理函数，当用户浏览特定路线时执行。以下是快递路由的结构:

```
app.METHOD(PATH, HANDLER)
```

其中:

*   app 只是 E xpress.js 的一个实例，你可以使用任何你选择的变量 。
*   方法 是一种 HTTP 请求方法如 get、set、put、delete 等。
*   路径 是特定网页到服务器的路径
*   HANDLER 是找到匹配路由时执行的回调函数。

在请求中可以提供四种主要的 HTTP 方法。这些方法有助于指定用户请求的操作。下表列出了所有方法及其解释:

| **方法** | **描述** |
| 1.得到 | HTTP GET 方法有助于客户端请求特定资源的表示。具有 GET 的请求只是检索数据，不会产生任何影响。 |
| 2.邮政 | HTTP POST 方法有助于请求服务器接受包含在请求中的数据，作为由 URI 标识的资源的新对象。 |
| 3.放 | HTTP PUT 方法有助于请求服务器接受包含在请求中的数据，作为对由所提供的 URI 标识的现有对象的更改。 |
| 4.删除 | HTTP DELETE 方法有助于请求服务器从目的地删除特定的资源。 |

下面的例子展示了所有 HTTP 方法的用法。

```
var express = require('express');
const app = express();
app.use(express.json());

app.get('/', function (req, res) {
    console.log("GET Request Received");
    res.send('
<h2 style= "font-family: Malgun Gothic; color: blue; "> Welcome to Edureka's Express.js Tutorial!/h2>');
})

app.post('/addcourse', function (req, res) {
    console.log("POST Request Received");
    res.send('
<h2 style="font-family: Malgun Gothic; color: green; ">A course new Course is Added!</h2>

');
})
app.delete('/delete', function (req, res) {
    console.log("DELETE Request Received");
    res.send('
<h2 style="font-family: Malgun Gothic; color: darkred;">A Course has been Deleted!!</h2>

 ');
})
app.get('/course', function (req, res) {
    console.log("GET Request received for /course URI");
    res.send('
<h2 style="font-family: Malgun Gothic; color:blue;">This is an Available Course!</h2>

');
})

//PORT ENVIRONMENT VARIABLE
const port = process.env.PORT || 8080;
app.listen(port, () => console.log(`Listening on port ${port}..`));
```

在本 Express.js 教程的下一部分，我将向您介绍中间件。

### **2。中间件**

在 express 中，中间件功能是可以访问请求和响应对象的功能，以及应用程序的请求-响应周期中的下一个功能。这些功能能够执行下列任务:

*   任何代码的执行
*   修改请求和响应对象。
*   最终应用程序请求-响应周期。
*   调用循环中的下一个中间件。

注意，如果当前函数没有终止请求-响应循环，那么它必须调用 next()函数，以便将控制传递给下一个可用的中间件函数。如果没有完成，那么请求将是不完整的。下面我列出了任何 Express.js 应用程序中主要使用的中间件:

*   应用层中间件
*   路由器级中间件
*   错误处理中间件
*   内置中间件
*   第三方中间件

现在，为了详细了解中间件的功能，让我给你看一个同样的小例子:

```
var express = require('express')
var app = express()

var requestDate = function (req, res, next) {
    req.requestDate = Date.now()
    next()
}

app.use(requestDate)

app.get('/', function (req, res) {
    var responseMsg = '
<h2 style="font-family: Verdana; color: coral;">Hello Learners!!</h2>

' 
    responseMsg += '<small>Request genrated at: ' + req.requestDate + '</small>'
    res.send(responseMsg)
})

//PORT ENVIRONMENT VARIABLE
const port = process.env.PORT || 8080;
app.listen(port, () => console.log(`Listening on port ${port}..`));
```

### **3。饼干**

Express.js 中的 Cookies 是存储在用户电脑中的小信息文件。它们拥有大量特定于特定用户及其访问的网站的数据。每当客户在其浏览器上加载网站时，浏览器将隐式地将本地存储的数据发送回网站/服务器，以便识别用户。一个 cookie 通常包含以下内容:

1.  名字
2.  价值
3.  键值格式的零个或多个属性。这些属性可以包括 cookie 的有效期、域和标志等。

现在，为了在 express 中使用 cookie，首先您需要通过[***NPM***](https://www.edureka.co/blog/node-js-npm-tutorial/)将 cookie-parser 中间件安装到已经存在于项目文件夹中的***node _ modules***文件夹中。下面是执行相同操作的代码:

```
npm install cookie-parser
```

一旦完成，下一步就是将 cookie-parser 导入到您的应用程序中。下面是做同样事情的代码:

```
var express = require('express');&nbsp;&nbsp;
var cookieParser = require('cookie-parser');
var app = express();&nbsp;
app.use(cookieParser()); 
```

现在，让我向您展示如何使用 cookie-parser 创建和获取 cookie 的详细信息。

```
var express = require('express');
var cookie_parser = require('cookie-parser');
var app = express();
app.use(cookie_parser());

//Setting up a Cookie
app.get('/setcookie',function(req, res){
    res.cookie('cookie_name', 'Express_Demo');
    res.cookie('organization', 'Edureka');
    res.cookie('name', 'Swatee');

    res.status(200).send('
<h4 style="font-family: Tahoma; color: coral; text-align: center;">Setting up the Cookie</h4>

');
});

//Checking cookie is set or not
app.get('/getcookie', function(req, res) {
    res.status(200).send(req.cookies);
});

//Welcome Message
app.get('/', function (req, res) {
    res.status(200).send('
<h2 style="font-family: cursive; color: lightseagreen; text-align: center; ">Welcome to Edureka's Express Tutorial!</h2>

');
});

//PORT ENVIRONMENT VARIABLE
const port = process.env.PORT || 8080;
app.listen(port, () => console.log(`Listening on port ${port}..`));
```

您还可以检查浏览器控制台中是否设置了 cookie。为此，打开浏览器控制台并键入以下命令:

```
console.log(document.cookie);
```

现在你已经知道了如何在 Express 中使用中间件和 cookies，在本 Express.js 教程的下一部分，让我们更深入地学习如何创建 REST API。

### **4。REST API**

REST 或 RESTful 代表具象状态转移。它是一种架构风格，也是一种用于通信目的的方法，经常在各种 web 服务开发中使用。简单地说，它是一个应用程序接口(API ),利用 HTTP 请求在 WWW 上获取、上传、发布和删除数据。

由于 Express.js 是在 Node.js 的名为 connect 的中间件模块上开发的，它自动成为服务器的完美选择。这是因为 Express 简化了为服务器创建和公开 API 的过程，以便作为客户端与服务器应用程序进一步通信。在这里，connect 模块利用 http 模块与 Node.js 通信。因此，如果您正在使用任何基于 connect 的中间件模块，那么您可以很容易地与 Express.js 集成。

如果你想学习如何从头开始创建一个 REST API，你可以参考我的文章。

现在让我们在这个 Express.js 教程中更进一步，理解脚手架的概念。

### **5。脚手架**

在使用 REST APIs 时，您一定已经看到您需要处理各种文件，比如 HTML、 [CSS](https://www.edureka.co/blog/what-is-css/) 、JPEGs 等等。来完成任何特定的任务。但是管理和维护这些文件太麻烦了。因此，Express 为开发人员提供了一个简单的解决方案，称为脚手架。搭建是为 web 应用程序创建适当结构的过程，有助于管理适当目录中的文件，将我们从手工工作中解救出来。

因此，你可以说搭建有助于为我们的 express 应用程序创建框架，并让我们直接进入应用程序开发。Express 提供了各种搭建工具，比如 Yeoman 和 Express-generator。在这篇 Express.js 教程中，我将向您展示如何使用 Express-generator 来创建应用程序的基本结构。

**使用快速发电机**

在您可以使用 express-generator 之前，您需要在您的系统中安装它。在命令提示符下键入以下代码进行相同的操作:

```
npm install -g express-generator
```

现在您可以使用 express-generator 来创建项目框架。为此，您需要键入以下命令:

```
express
```

一旦你按下回车键，你的输出应该看起来像下面的截图: ![Scaffolding - Express.js Tutorial - Edureka](img/7586b13e362302d351a2c125ba8065ed.png) 如果你得到类似这样的输出，这意味着你的骨架已经创建好了。现在，您可以返回到您的项目文件夹，并检查由 scaffolding 创建的项目结构。下面我附上了我的脚手架截图。 ![Scaffolding skeleton - Express.js Tutorial - Edureka](img/3859be3f0c3b186e252808a7023ba4f4.png)

以上是关于 Express.js 中的搭建的全部内容。在本 Express.js 教程的下一部分，我将告诉您如何在 Express 应用程序中建立数据库连接。

### **6。数据库连接**

市场上有很多可用的数据库，其中最受前端开发人员欢迎的是 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 和 MongoDB。我写过一些博客，讲述如何从头开始与这些人建立联系:

1.  [连接 REST API 与**MySQL**](https://www.edureka.co/blog/node-js-mysql-tutorial/)
2.  [连接 REST API 与**MongoDB**](https://www.edureka.co/blog/node-js-mongodb-tutorial/)

在本 Express.js 教程的下一部分中，我将向您介绍模板化的概念，它主要用于 Express 和 Node.js 应用程序。

### 7 .**。模板**

模板引擎方便我们用最少的代码创建和使用静态的 HTML 模板。当您执行它们时，模板文件中的变量被实际值替换，整个模板被模板引擎转换成 HTML 文件。然后，它最终被发送到客户端，在那里数据被进一步注入到实际的模板中，以生成最终的 HTML 文档。这减少了页面加载时间以及设计的复杂性，因此主要用于设计 HTML 页面。

![Templating - Express.js Tutorial - Edureka](img/59455cca40392fa0d3778de9dd5cd747.png)

下面我列出了一些适用于 Express.js 的流行模板引擎:

*   [帕格(早先被称为杰德)](https://www.edureka.co/blog/nodejs-tutorial/#stepbystep)
*   髭
*   灰尘
*   把手
*   泥盖木屋
*   酒
*   太妃糖
*   强调
*   海象
*   胡须

现在让我们继续学习这个 Express.js 教程，看看如何在任何 Express.js 应用程序中处理异常。

### **8。错误处理**

Express.js 中的错误处理是一种机制，用于捕获和处理程序执行过程中可能出现的、扰乱正常流程的错误。Express 在中间件的帮助下处理错误，根据中间件函数接受的参数数量，中间件可以进一步分为不同的类型。这里，我将专门讨论“错误处理中间件”函数，它接受四个参数，即 err、req、res 和 next。只有发生错误时，才会调用该函数。下面我举了一个同样的例子:

```
app.use(function (err, req, res, next) {
	console.error(err.stack);
	res.status(500).send(' 
<h2 style="font-family: Malgun Gothic; color: darkred;">Ooops... Cant find what you are looking for!</h2>

');
});
```

到此，本 Express.js 教程到此结束。我希望我能够从头开始解释 Express.js 的概念。

*如果您发现此“Express.js 教程* *”、* *相关，请查看 Edureka 的 [**Node.js 认证培训**](https://www.edureka.co/nodejs-certification-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在本 Express.js 教程的评论部分提到它，我们会回复您。*