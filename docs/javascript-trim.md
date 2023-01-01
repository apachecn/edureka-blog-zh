# 如何实现 JavaScript Trim 方法？

> 原文：<https://www.edureka.co/blog/javascript-trim/>

处理想要使用的字符串中的空格可能是一项单调乏味的任务。 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) Trim 方法让你处理这个问题。在本文中，我们将详细探讨这个 JavaScript 概念。

因此，让我们从这篇关于 JavaScript Trim 的文章开始，让我们熟悉一下手头的主题，

## **JavaScript 修剪**

字符串是我们使用的 Java 编程的基本概念之一。有很多函数可以用来操作字符串，比如 length()、concat()、indexOf()、charAt()等。一个这样功能是微调。Trim 从字符串值中移除空格，并在不操作原始字符串的情况下给出经过修剪的字符串。

出现在字符串前后的空格、制表符等被删除，而不是字符串中单词之间的空格。javascript 中的修剪功能也很相似。IE9+，Opera 10.5+，Firefox 3.5+，Chrome 5+，Safari 5+以后的所有浏览器都支持该功能。要了解更多关于 Javascript 的知识，今天就来看看这个[网络开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

Javascript 提供了 3 种不同类型的修剪函数。

*   [trimRight()](#trimRight())
*   [修剪()](#trim())

让我们继续这篇 JavaScript Trim 文章，看看下面的函数，

## **trim left()**

顾名思义，它移除了字符串左侧的空格，即字符串开头或前导空格。

**例题**

```
var string = "Hi, Welcome to Edureka!";
console.debug(string.trimLeft());

```

**输出**

嗨，欢迎来到 Edureka！

接下来在这篇文章中我们有修剪右功能，

## **trimRight()**

顾名思义，它移除了字符串右侧的空格，即末尾或尾部的空格。

**例子**

```
var string = "Hi, Welcome to Edureka!";
console.debug(string.trimRight());

```

**输出**

嗨，欢迎来到 Edureka！

让我们继续这篇 JavaScript Trim 文章，看看下面的函数，

## **trim()**

这将删除前面和后面的空格，即前导和尾随空格。

**例子**

```
var string = "Hi, Welcome to Edureka!";
console.debug(string.trim());

```

**输出**

嗨，欢迎来到 Edureka！

**注意:** Trim 永远不会删除中间的空格。它只修剪前导和尾随空白。上面的例子很好地证明了这一点。

至此，我们已经结束了 JavaScript Trim 文章。我希望您了解连接字符串的不同方式。

*既然你已经了解了 JavaScript，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript Trim”的评论部分提到它，我们会给你回复。*