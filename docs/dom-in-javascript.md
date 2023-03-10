# 关于 JavaScript 中的 DOM，您只需要知道

> 原文：<https://www.edureka.co/blog/dom-in-javascript/>

您知道我们可以使用 JavaScript 来操作网页上的内容吗？似乎很有趣，对吗？我们先来了解一下什么是文档对象模型 ie。JavaScript 中的 DOM，如下所示:

*   [JavaScript 中的 DOM 是什么？](#what)
*   [JavaScript 中 DOM 的动作](#actions)
*   [查询 DOM](#query)
*   [监听事件](#events)
*   [与表单交互](#forms)
*   [创建 HTML 元素](#elements)
*   [添加 CSS](#css)

## **JavaScript 中的 DOM 是什么？**

加载网页时，浏览器会创建文档对象模型或 DOM。在图形形式中，它就像一个元素树，也称为节点，用于表示页面上的每个元素。

我们网页的所有 DOM 都位于文档对象中。从程序上来说，这种模型允许我们通过 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 读取甚至改变页面的内容。是不是很酷？

## **JavaScript 中 DOM 的动作**

我们可以使用该模型执行的一些操作有:

*   更改/删除 DOM/页面上的 HTML 元素。

*   改变 CSS 样式并添加到元素中

*   读取和更改属性(href，src，alt)等。

*   创建新元素并将其插入 DOM/page。

*   将事件监听器附加到元素(点击、按键、提交)

## **在 JavaScript 中查询 DOM**

抓取一个 HTML 元素或获取它来添加/更改或内容被称为查询。

HTML 代码:

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Javascript and the DOM</title>
<style>
h1{
font-size: 60px;
}
</style>
</head>
<body>
<h1 id="title">Edureka is cool!</h1>

<script src="./script.js"></script>
</body>
</html>
```

JavaScript 代码:

```
// grab hold of title
var title = document.getElementById("title");

// changing the text content
title.textContent = "Learning is fun";

```

![DOM in JavaScript](img/b9fc0231cc3317b7d47266f9ba0a0c05.png)

这里，我们使用 **document.getElementById(" ")抓取了 id 为“title”的 H1 标签；**并使用*改变其内容**。**text content*属性。

我们可以通过**document . getelementbyclass name(" "**)事件使用 [HTML](https://www.edureka.co/blog/what-is-html/) 类来改变内容

## **监听事件**

我们甚至可以听到网页上的事件并做出反应。用户与网页交互的任何操作都称为事件。比如:点击按钮、提交表单、上下滚动等。 JavaScript 以用户交互性和行为性著称！

HTML 代码:

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Javascript and the DOM</title>
<style>
h1{
font-size: 60px;
}
</style>
</head>
<body>
<h1 id="title">Edureka is cool!</h1>
<button id="my-button">CLICK ME</button>

<script src="./script.js"></script>
</body>
</html>

```

JavaScript 代码:

```
// grab hold of button
var btn = document.getElementById("my-button");

// adding and event listener
btn.addEventListener("click", function(){

//call back function
var title = document.getElementById("title");

// changing the text content
title.textContent = "Learning is fun";
})

```

![Listening to Events DOM](img/8c2eef3c1652c2ce6a19b7c1d2b59f31.png)

我们用一个按钮点击改变了我们网页的标题，哇！

首先，我们使用 document.getElementById(" ")获取按钮，然后使用 addEventListener()方法向该按钮添加一个事件侦听器，该方法接受两个参数——事件的名称和一个回调函数，我们必须在该函数中指定要执行的操作。就像我们改变了网页的标题。

## **与表单交互**

JavaScript 帮助我们与用户表单进行交互。用户可以填写表单字段，并通过 JavaScript 提交给服务器进行验证。

HTML 代码:

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Javascript and the DOM</title>
<style>
h1{
font-size: 60px;
}
</style>
</head>
<body>
<h1 id="title">Forms</h1>
<form action="">
<label for="name">Name:</label>
<input type="text" name="username">
<label for="age">Age:</label>
<input type="text" name="age">
<label for="email">Email:</label>
<input type="text" name="email">
<button type="submit">SUBMIT</button>
</form>

<script src="./script.js"></script>
</body>
</html>
```

JavaScript 代码:

```
// a HTML collection of forms
var forms = document.forms;

// creating an array of those forms
forms = Array.from(forms);

// console log that array to console
console.log(forms)

forms[0].addEventListener("submit", function(e){
e.preventDefault();

var name = e.target['username'].value;
var age = e.target['age'].value;
var email = e.target['email'].value;

console.log(name);
console.log(age);
console.log(email)
})

```

![Forms](img/a0bbd0db27e6264ad7d31bf9066e112f.png)

我们的 HTML 用户表单的准系统如上图所示。HTML 表单可以通过 **document.forms** 定位，这返回给我们一个 HTML 集合，我们可以使用 JavaScript 中的 **Array.from()** 方法将它转换成一个数组。

![forms-2-DOM-in-javascript](img/d0d207ee9b0ee9e0af5dd71ffc3b4fad.png)

我们可以通过 **forms[0]** 使用 forms 数组访问表单，它返回数组中的第一个表单。类似地，如果页面上有几个表单，我们可以使用这个数组索引方法来获取它们。

![forms-3](img/8980a0300df7ec4fa968dfb66006d9ed.png)

我们可以使用提交事件监听器提交用户输入，如上面的代码所示。回调函数接受一个 **事件** 参数，例如 **(e)。** 事件参数有助于防止默认动作，即页面在提交时重新加载。事件参数也有助于获取表单字段中的值用户目标对象，例如**e . target[‘用户名’]。值**

在目标对象内部，我们传递与表单字段中的 name 属性相对应的值。 **。值** 有助于获得字段中填写的实际值/输入。我们将这些存储在单独的变量中，并将它们记录到控制台。然而，在真实的场景中，我们可以将它们发送到服务器进行验证。

## **创建 HTML 元素**

HTML 代码:

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Javascript and the DOM</title>
<style>
h1{
font-size: 60px;
}
</style>
</head>
<body>
<div id="app">

</div>

<script src="./script.js"></script>
</body>
</html>

```

JavaScript 代码:

```
var app = document.getElementById("app");

// creating new H1 tag
var H1 = document.createElement("H1");

// add some text to H1
H1.textContent = "I am a Heading";

// appendig H1 to ap div
app.appendChild(H1);

```

新的 HTML 元素可以通过**document . createelement()**创建，并将标签名作为值传递。例如**document . createelement(" DIV ")**

![Creating HTML Elements](img/1b42194bd0c043899f5ecce3abb06940.png)

在上面的代码中，我们获得了 id 为“app”的 div，并将其存储在变量 **app** 中。然后我们使用 **创建了一个新的 HTML H1 标签。在 **文档** 对象上创建元素【H1】**，并使用 **app.appendChild()将其作为子元素追加到 div 中。**

## **添加 CSS**

JavaScript 也可以用来添加 CSS 样式。

HTML 代码:

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Javascript and the DOM</title>
<style>
h1{
font-size: 60px;
}
</style>
</head>
<body id="body">
<h1 id="title">Watch me go Red!</h1>

<script src="./script.js"></script>
</body>
</html>

```

JavaScript 代码:

```
var title = document.getElementById("title");
// cgangin color to red
title.style.color = "red"

var body = document.getElementById("body")

// changing the background color to light blue
body.style.backgroundColor = "lightblue"

```

![Adding CSS](img/657ecaba9ea5e117bcadf26366802822.png)

我们使用 JavaScript 将标题的文本颜色从黑色改为红色。我们使用 **实现了这一点。样式** 属性随后将 **颜色** 的值改为等于 **红色** 。

现在让我们将 body 元素的背景色改为 **浅蓝色** 。

![Final-red-DOM-in-javascript](img/c889a433543848a1b892f3a212251c7a.png)

至此，我们结束了这篇 JavaScript 文章中的 DOM。我希望您理解了文档对象模型是如何工作的，以及如何用 JavaScript 实现相同的 DOM。

*既然你已经了解了 JavaScript 中的 DOM，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

有问题要问我们吗？请在“JavaScript 中的 DOM”的评论部分提到它，我们会回复您。