# 如何用 JavaScript 创建提醒？

> 原文：<https://www.edureka.co/blog/javascript-alert/>

当您打开任何网站时，有时可能会看到弹出警告。这些 JavaScript 警告框对于提醒用户一些重要的事情非常有用。当 JavaScript 警告框被触发时，会弹出一个小框，显示您在 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 代码中指定的文本。在本文中，我们将按照以下顺序来看看 JavaScript 中的警报是如何工作的:

*   [JavaScript 中的弹出框](#popup)
*   [JavaScript 中的警报](#alert)
*   [如何用 JavaScript 创建提醒？](#example)

我们开始吧。

## **JavaScript 中的弹出框**

在 JavaScript 中，您可以找到三种弹出框:

*   **警告框-** 警告框主要用于确保信息传递给用户。当弹出一个警告框时，你需要点击“确定”来继续。

*   **确认框-** 确认框主要用于**验证**或者为用户接受某些东西。当弹出确认框时，用户需要单击“确定”或“取消”来继续。如果用户单击“确定”，框返回 true。如果用户单击“取消”，该框返回 false。

*   **提示框-** 提示框是用户在进入页面前**输入数值**的地方。当弹出提示框时，用户需要在输入值后点击“确定”或“取消”继续。如果用户点击“确定”,该框将返回输入值。如果用户点击“取消”,该框返回 null。

这些是不同类型的弹出框。因此，让我们深入到警告框中，看看如何用 JavaScript 创建警告框。

## **JavaScript 中的警告**

[JavaScript](https://www.edureka.co/blog/javascript-methods/) 中的 **alert()** 方法显示一个带有指定消息和 OK 按钮的警告框。它通常用于确保信息传递给用户。

警告框将焦点从当前窗口移开，并强制浏览器阅读消息。因此，您应该避免过度使用该方法，因为它会阻止用户在关闭盒子之前访问页面的其他部分。

**语法:**

```
alert(message)
```

这里，消息是一个[字符串](https://www.edureka.co/blog/javascript-string-functions/)类型，指定显示在警告框中的文本，或者是一个[对象](https://www.edureka.co/blog/javascript-object/)转换成一个字符串并显示。它是可选的。

**举例:**

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%3E%0Afunction%20myFunction()%20%7B%0Aalert(%22This%20is%20an%20Alert!%22)%3B%0A%7D%0A%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />
```

**输出:**

![Alert box - alert in javascript - edureka](img/8741c28fcd793493eff172ac7932a7a7.png)

## **如何用 JavaScript 创建提醒？**

JavaScript 中的 **alert()** 方法显示一个警告框。它显示一条指定的消息以及一个 **OK** 按钮，通常用于确保用户获得信息。它返回一个 string 类型的值，该值代表要在警告框中显示的文本。让我们举个例子，看看如何用 JavaScript 创建一个警告:

```
<!DOCTYPE html>
<html>

<head>
<title>
Alert() Method in JavaScript
</title>
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cstyle%3E%0Ah1%20%7B%0Acolor%3A%20Blue%3B%0A%7D%0A%0Ah2%20%7B%0Afont-family%3A%20Impact%3B%0A%7D%0A%0Abody%20%7B%0Atext-align%3A%20center%3B%0A%7D%0A%3C%2Fstyle%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;style&gt;" title="&lt;style&gt;" />
</head>

<body>

<h1>Welcome to Edureka</h1>
<h2>Alert in JavaScript</h2>

<p>
To Display the alert message,
click on the "Show Alert Message" button:
</p>

<button ondblclick="myalert()">
Show Alert Message
</button>

<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%3E%0Afunction%20myalert()%20%7B%0Aalert(%22This%20is%20the%20Alert%20Message!%22)%3B%0A%7D%0A%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />

</body>

</html>
```

**输出:**

![](img/f8510fc323750c017ef2d279dd1db466.png)

双击该按钮后，您将获得以下输出:

![Output 2- Alert in JavaScript - edureka](img/6485aaddb659b39be88c695e73ae01f4.png)

说到这里，我们的文章就到此为止了。我希望您了解 JavaScript 中的警告是什么，以及如何创建警告框。如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*查看我们的 [网络开发人员在线课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“JavaScript 中的警告”博客的评论部分提到它，我们会回复您。