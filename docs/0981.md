# 知道如何从头开始用 Node.js 构建 REST API

> 原文：<https://www.edureka.co/blog/rest-api-with-node-js/>

自从 WWW 发明以来，各种 web 技术如 RPC 或 SOAP 被用来创建和实现 web 服务。但是这些技术在处理任何通信任务时都使用了严格的定义。因此，REST 被开发出来，它有助于降低复杂性，并为设计基于网络的应用程序提供了一种架构风格。由于 Node.js 技术为前端开发人员带来了服务器革命，所以在本文中，我将从头开始演示使用 [Node.js](https://www.edureka.co/blog/nodejs-tutorial/) 构建 REST API 的过程。

下面是我将在本文中涉及的主题:

*   [什么是 REST API？](#restapi)
*   [休息原则](#principles)
*   [实战演示:](#restapiwithnode) [用 Node.js 构建 REST API](#restapiwithnode)

## **什么是 REST API？**

REST 或 **REST** ful 代表**RE**presentational**S**state**T**transfer。它是一种架构风格，也是一种用于通信目的的方法，经常在各种 web 服务开发中使用。简单地说，它是一个应用程序接口(API ),利用 HTTP 请求在 WWW 上获取、上传、发布和删除数据。

REST 架构风格有助于利用较少使用的带宽，使应用程序更适合互联网。它通常被认为是互联网的 ***语言*** 。它完全基于资源，其中每个组件都被视为一个组件，单个资源可以通过使用标准 HTTP 方法的公共接口进行访问。

为了更好地理解，让我们深入一点，看看 REST API 到底是如何工作的。基本上，REST API 分解一个事务，以便创建小模块。现在，这些模块中的每一个都用于处理交易的特定部分。这种方法提供了更多的灵活性，但是需要从头开始进行大量的工作。

在任何基于 REST 的架构中使用的主要函数有:

*   **GET**—提供对资源的只读访问。
*   **PUT**—创建新资源。
*   **删除**—删除资源。
*   **发布**—更新现有资源或创建新资源。

但凡是声称的都不能称为 RESTful API。 为了被视为 RESTful API，你的应用必须满足一定的约束或原则。在本文关于使用 Node.js 构建 REST API 的下一节中，我将详细讨论这些原则。

## **休息原则**

菲尔丁博士在 2000 年定义了 REST API 设计，他制定了六个基本原则。以下是休息的六大指导原则:

1.  **无状态** 从客户端发送到服务器的请求包含完全理解它所需的所有必要信息。它可以是 URI、查询字符串参数、正文甚至标头的一部分。URI 用于唯一标识资源，主体保存请求资源的状态。一旦服务器完成处理，一个适当的响应将通过头、状态或响应体发送回客户端。
2.  **客户端-服务器** 它有一个统一的接口将客户端和服务器分开。分离关注点有助于提高跨多个平台的用户界面的可移植性，并增强服务器组件的可伸缩性。
3.  **统一接口** 为了获得整个应用的统一性，REST 定义了四个接口约束，它们是:
    *   资源标识
    *   使用表示的资源操作
    *   自我描述信息
    *   超媒体作为应用状态的引擎
4.  **可缓存** 为了提供更好的性能，应用程序通常都是可缓存的。这是通过隐式或显式地将来自服务器的响应标记为可缓存或不可缓存来实现的。如果响应被定义为可缓存的，那么客户机缓存可以在将来为等效的响应重用响应数据。它还有助于防止过时数据的重用。
5.  **分层系统** 分层系统架构通过限制组件行为，让应用更加稳定。这种体系结构支持负载平衡，并提供共享缓存来提高可伸缩性。分层架构还有助于增强应用程序的安全性，因为每一层中的组件都不能与其所在的下一层之外的组件进行交互。
6.  **按需编码** 按需编码是一个可选约束，使用最少。它允许通过接口下载和扩展客户代码或小应用程序，以便在应用程序中使用。本质上，它通过创建一个不依赖于自身代码结构的智能应用程序来简化客户端。

现在你已经知道了什么是 REST API，以及为了交付一个高效的应用程序你需要注意什么，让我们更深入地了解使用 [Node.js](https://www.edureka.co/blog/nodejs-tutorial/) 构建 REST API 的过程。

## **实战演示:使用 Node.js 构建 REST API**

在这里，我们将使用 [Node.js 和 Express.js](https://www.edureka.co/blog/nodejs-tutorial/) 创建一个简单的用于图书馆管理的 CRUD REST 应用程序。要构建这个应用程序，您需要安装以下软件:

1.  Node.js
2.  Express.js
3.  Joi
4.  节点监控器

在这个例子中，我将使用 WebStorm IDE 来编写和执行代码。您可以根据自己的选择使用任何 IDE 或代码编辑器。那么，我们开始吧。

首先，你需要创建你的项目目录。接下来，打开命令提示符并导航到您的项目目录。在那里，您需要使用下面的命令调用 NPM:

```
npm init
```

当你点击回车键时，Node.js 会要求你输入一些细节来构建。json 文件如:

![cmd npm - Building REST API with Node.js - Edureka](img/2af6f72a82ec1e5a4d6b805a962d2003.png) 在这里你可以定义你的切入点以及其他几个信息。对于这个演示，我将使用 **script.js** 作为切入点。接下来，我们将使用下面的命令安装 express . js:

```
npm i express
```

最后，我将安装一个名为 **nodemon 的节点监控包。**它监视这个文件夹中所有扩展名为任何类型的文件。此外，有了观察器上的 nodemon，您不必在每次进行任何更改时都重新启动 Node.js 服务器。nodemon 将隐式地检测这些更改，并为您重新启动服务器。

```
npm i -g nodemon
```

**package . JSON**

```

{
"name": "samplerestapi",
"version": "1.0.0",
"description": "Edureka REST API with Node.js",
"main": "script.js",
"scripts": {
"test": "echo "Error: no test specified" &amp;&amp; exit 1"
},
"author": "Edureka",
"license": "ISC",
"dependencies": {
"express": "^4.16.4",
"joi": "^13.1.0"
}
}

```

**script . js**

```

const express = require('express');
const Joi = require('joi'); //used for validation
const app = express();
app.use(express.json());

const books = [
{title: 'Harry Potter', id: 1},
{title: 'Twilight', id: 2},
{title: 'Lorien Legacies', id: 3}
]

//READ Request Handlers
app.get('/', (req, res) => {
res.send('Welcome to Edurekas REST API with Node.js Tutorial!!');
});

app.get('/api/books', (req,res)=> {
res.send(books);
});

app.get('/api/books/:id', (req, res) => {
const book = books.find(c => c.id === parseInt(req.params.id));

if (!book) res.status(404).send('<h2 style="font-family: Malgun Gothic; color: darkred;">Ooops... Cant find what you are looking for!</h2>');
res.send(book);
});

//CREATE Request Handler
app.post('/api/books', (req, res)=> {

const { error } = validateBook(req.body);
if (error){
res.status(400).send(error.details[0].message)
return;
}
const book = {
id: books.length + 1,
title: req.body.title
};
books.push(book);
res.send(book);
});

//UPDATE Request Handler
app.put('/api/books/:id', (req, res) => {
const book = books.find(c=> c.id === parseInt(req.params.id));
if (!book) res.status(404).send('<h2 style="font-family: Malgun Gothic; color: darkred;">Not Found!! </h2>');

const { error } = validateBook(req.body);
if (error){
res.status(400).send(error.details[0].message);
return;
}

book.title = req.body.title;
res.send(book);
});

//DELETE Request Handler
app.delete('/api/books/:id', (req, res) => {

const book = books.find( c=> c.id === parseInt(req.params.id));
if(!book) res.status(404).send('<h2 style="font-family: Malgun Gothic; color: darkred;"> Not Found!! </h2>');

const index = books.indexOf(book);
books.splice(index,1);

res.send(book);
});

function validateBook(book) {
const schema = {
title: Joi.string().min(3).required()
};
return Joi.validate(book, schema);

}

//PORT ENVIRONMENT VARIABLE
const port = process.env.PORT || 8080;
app.listen(port, () => console.log(`Listening on port ${port}..`));

```

现在，下一步是检查处理器是否正常工作。为此，我们将使用名为 Postman 的 Chrome 扩展。要安装 Postman，你可以访问 **[这里](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en)** ，点击“添加到 Chrome”。

成功安装 Postman 后，打开它并开始测试你的应用程序。所以，让我们从测试 GET 方法开始。现在，为了做到这一点，您需要从下拉列表中选择 GET，键入定义的 URI 并点击 send。如果您的代码运行良好，那么您将会看到我们在代码中手动添加的所有书籍的列表。在下面的图片中，你可以看到我的结果。

![GET - Building REST API with Node.js - Edureka](img/105b184c4d8f2e7823e8b6422d6c741e.png) 现在，让我们试着给我们的库存清单添加一本新书。为此，从下拉列表中选择“POST ”,并输入为 POST 方法定义的 URI。现在，单击“Body ”,选择“raw ”,然后从下拉列表中选择“JSON ”,如下图所示。现在，在文本区，键入你的书名，如图所示，然后点击发送。

![POST - Building REST API with Node.js - Edureka](img/b61b60b46fdee5d51207e1fc5dc13345.png) 如果你的发布方法运行良好，你的回复正文将包含书名和图书 id。现在，让我们尝试更新书名。目前，我的书名是“天使与魔鬼”，我将更新为“天使&魔鬼”。因此，要更新数据，您需要首先从下拉列表中选择“PUT ”,并输入 PUT 请求的 URI 以及您希望更新的图书 id。接下来在“正文”中，输入新书标题，然后按回车键。

![PUT - Building REST API with Node.js - Edureka](img/62a8542c6efcad6ed8fefa86ac4016e8.png) 这将给你一个带有图书 id 和更新的书名的响应。

最后，让我们发送一个“删除”请求来删除一个现有记录。从下拉列表中选择 DELETE，并键入删除请求处理程序的 URI 以及您想要删除的书的详细信息，然后按 enter 键。如果您的交易成功，您将在回复正文中看到已删除条目的完整详细信息。【T2![DELETE - Building REST API with Node.js - Edureka](img/23e9e491b8d7b14e3f650d60b804ef9a.png)

现在，让我们发送一个获取最终图书列表的请求。

![GET ALL - Building REST API with Node.js - Edureka](img/98901511d8cda678ba53b2f92dc14344.png) 从上面的截图中可以看出，响应正文中总共包含了三本书，其中缺少图书 id 3，因为我们已经删除了该条目。

至此，我们结束了这篇关于用 Node.js 构建 REST API 的文章。现在，如果你想了解 Node.js 的更多细节，你可以看看我在 [Node.js 教程](https://www.edureka.co/blog/nodejs-tutorial/)上的文章。

*如果您发现这个“REST API with Node.js* *”相关，* *请查看 Edureka 的 [**Node.js 培训**](https://www.edureka.co/nodejs-certification-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在这个 *REST API with Node.js* 的评论部分提到它，我们会给你回复。*