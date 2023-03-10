# 了解如何发出 Node.js 请求——发出 HTTP 请求的 3 种最佳方式

> 原文：<https://www.edureka.co/blog/node-js-requests/>

Node.js 是最流行的前端框架之一，在业界被大量用于创建基于服务器的应用程序。反过来，这些应用程序有助于向用户提供各种数据和信息。但是用户如何将他的需求传递给服务器呢？嗯，这是使用 HTTP 请求完成的，这有助于 **[Node.js 开发人员](https://www.edureka.co/blog/nodejs-tutorial)** 简化整个过程。通过这篇关于 Node.js 请求的文章，我将为您提供一个完整的 Node.js 请求以及如何绕过它们的演练。

以下是我将在本文中涉及的主题:

*   [node . js 中的 HTTP 请求是什么？](#httprequest)
*   [制作 Node.js 请求](#makingrequest)
*   [Node.js 请求对象](#requestobject)

让我们从本文的第一个主题开始，理解什么是 Node.js 请求。

## **节点中的 HTTP 请求是什么？**

在 Node.js 中，HTTP 请求基本上是客户端通过 HTTP 向服务器请求的消息，即 超文本传输协议。您可以将它视为两台计算机之间发送的信息包，作为主要数据集。然后，这个请求由服务器处理，另一个信息包被发送回客户机。此数据包包含客户端请求的所有必要数据，称为响应。在本文中，我们将主要关注请求部分。

![HTTP Request Response - Node.js Requests - Edureka](img/80afdf49372e7551059552f50248b77b.png)

因此，让我们从更细的角度来理解 HTTP 请求。HTTP 请求 是在客户端和 web 服务器之间传输数据的浏览器模式。这些数据可以是任何东西，包括一个 [API](https://www.edureka.co/blog/rest-api-with-node-js/) ，一个网站，一张图片，文本等等。

一个 *HTTP 请求* 通常由以下几个部分组成:

1.  *请求行*
2.  *【0 或以上】*
3.  *正文请求【可选】*

有各种模块，您可以使用这些模块在 web 服务器空间中发出 HTTP 请求并处理服务器请求。在这篇 Node.js Requests 文章中，我将讨论一些在行业中被大量使用的请求。

## **制作 Node.js 请求**

下面我列出了 3 种最流行的 HTTP 请求方式:

1.  HTTP 模块
2.  请求模块
3.  轴

因此，让我们从 HTTP 模块开始，更深入地研究一下每一个模块。

这里，为了方便大家，我将通过查询一个【假】**[API:JSON 占位符 API](https://my-json-server.typicode.com/edurekaDemo/noderequest)** 来发出 Node.js 请求。

### **1。HTTP 模块**

HTTP 模块是标准的，也是一种老式的 HTTP 请求方式。这是一个默认的模块，你只需要插入并开始使用它，而不必安装任何显式的依赖。T3 是使用 [Node.js](https://www.edureka.co/blog/node-js-express-tutorial/) 组网的核心和关键模块之一。

一般来说，Node.js 的初学者在尝试从 API 请求或获取某些东西时，倾向于使用 http.get 和 https.get。这个模块的主要优点是，它是 API 的原生，因此它减少了安装任何第三方的需要。这使得过程稍微快了一点。下面我写了一个使用 HTTP 模块请求数据的代码。

```
const https = require("https");
const url = "https://my-json-server.typicode.com/edurekaDemo/noderequest/db";
https.get(url, res => {
res.setEncoding("utf8");
let body = "";
res.on("data", data => {
body += data;
});
res.on("end", () => {
body = JSON.parse(body);
console.log(body);
});
});
```

这将在控制台中为您提供所需的数据。下面我附上了我的代码输出。

但是正如所说，每个硬币都有两面，http 模块也有它的缺点。Node.js 的 HTTP 模块有点啰嗦，不支持‘promises’。这样，用于开发就变得有点不可靠和笨拙了。

在这篇 Node.js Requests 文章的下一节中，我将讨论请求模块，它只不过是 HTTP 模块的一个高级或修改版本。

### **2。请求模块**

![request module - Node.js Requests - Edureka](img/2a030beb6bd138f5f3155226f683e1cf.png)node . js 的请求模块是业内最流行的用于 HTTP 请求的 [Node.js 包](https://www.edureka.co/blog/rest-api-with-node-js/)之一。 与  HTTP  模块相比，这个软件包更加用户友好，这也是它多年来被认为是社区避风港的原因。 换句话说，它被设计成以尽可能简单的方式方便 HTTP 请求。它之所以能够这样做，是因为它只是 Node.js 的内置 HTTP 包的包装器。因此，使用 request，您可以以更简单的方式利用 HTTP 的所有功能。

下面我写了一段代码，使用请求模块请求数据。但是在您使用这个模块发出请求之前，您需要使用下面的命令将它安装到您的系统中:

```
npm i request
```

一旦您成功地安装了请求模块，您就可以继续下面给出的例子。

```
const request = require("request");
const url = "https://my-json-server.typicode.com/edurekaDemo/noderequest/db";
request.get(url, (error, response, body) => {
let json = JSON.parse(body);
console.log(body);
}); 
```

这将在控制台中为您提供所需的数据。下面我附上了我的代码输出。

因此，如果你正在寻找一个可以轻松处理 HTTP 请求的简单易用的库，请求模块是最好的选择。

但是，尽管它使请求过程变得更容易，但它对承诺没有任何支持，并且有许多依赖性。这就引出了我们的第三种方式，即使用 axios 包进行 Node.js 请求。

### **3。Axios 模块**

![axios module - Node.js Requests - Edureka](img/6213dfcbb3e3c2be911e5ed11948ddd5.png) Axios  是一个基于  Promise  的 HTTP 客户端，既可以在 [Node.js](https://www.edureka.co/blog/nodejs-tutorial/) 环境下工作，也可以在浏览器上工作。是因为 ** Axios ** 提供了单一的 API 来处理 XMLHttpRequest 和 node 的 HTTP 接口。这个软件包通常用于处理一系列复杂的事件。由于构建异步代码确实令人困惑，Promises 已经成为这个问题最突出的解决方案之一。

下面我写了一段代码，使用请求模块请求数据。但是在您使用这个模块发出请求之前，您需要使用下面的命令将它安装到您的系统中:

```
npm i axios
```

一旦您成功地安装了请求模块，您就可以继续下面给出的例子。

```
const axios = require("axios");
const url = "https://my-json-server.typicode.com/edurekaDemo/noderequest/db";
const getData = async url => {
  try {
    const response = await axios.get(url);
    const data = response.data;
    console.log(data);
  } catch (error) {
    console.log(error);
  }
};
getData(url); 
```

这将在控制台中为您提供所需的数据。下面我附上了我的代码输出。

![axios output - Node.js Requests - Edureka](img/ef4b66adeb5f45b4195979551a3f6c39.png)既然您已经知道了生成 Node.js 请求的各种方法，现在让我们来看看什么是请求对象及其各种属性。

## **Node.js 请求对象**

Node.js 中的 **请求对象** 帮助检索客户端浏览器通过 HTTP **请求** 传递给 Node.js 服务器的值。它保存来自用户的信息，并在动态创建网页时进行评估。基于用户输入，它还能够执行各种服务器端操作。你可以说，请求对象用于获取当前 HTTP 请求的信息，如 URL、请求头和数据等。下面我列出了请求对象最常用的属性。

| **属性** | **描述** |
| **req.app** | 这有助于保存对使用中间件的快速应用程序的当前实例的引用 |
| **req.baseUrl** | 这用于安装路由器实例的 URL 路径 |
| **请求体** | 这有助于保存客户端在请求主体中提交的数据的键值对。 |
| **req.params** | 这用于保存属性的对象，这些属性通过标记为“参数”的路线进行映射 |
| **请求路径** | 用于保存请求 URL 的路径 |
| **请求协议** | 这用于通过 TLS 请求时的请求协议字符串，如“http”或“https” |
| **请求安全** | 这只是一个布尔值，如果 TLS 连接成功建立，则返回 true |

至此，我想结束这篇关于 Node.js 请求的文章。为了让你容易理解，我尽了最大努力保持内容清晰明了。如果这激起了你对 Node.js 更多了解的兴趣，你也可以参考我在 Node.js 上的 **[其他文章。](https://www.edureka.co/blog/nodejs-tutorial/)**

*如果您发现此“Node.js 请求* *”、* *相关，请查看 Edureka 提供的 [**Node.js 培训**](https://www.edureka.co/nodejs-certification-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在这个 *Node.js 请求*的评论部分提到它，我们会给你回复。*