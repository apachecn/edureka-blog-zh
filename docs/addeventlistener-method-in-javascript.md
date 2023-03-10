# 如何在 JavaScript 中实现 addEventListener()方法？

> 原文：<https://www.edureka.co/blog/addeventlistener-method-in-javascript/>

事件是 [JavaScript](https://www.edureka.co/javascript-jquery-training) 的重要组成部分。网页根据发生的事件做出响应。有些事件是用户生成的，有些是 API 生成的。在本文中，我们将了解事件是如何发生的，以及 JavaScript 中的 addEventListener 方法是如何按以下顺序使用的:

*   [什么是事件监听器？](#what)
*   [JavaScript 中的 AddEventListener()](#method)
*   [参数值](#values)
*   [JavaScript 中的 AddEventListener:示例](#example)

## **什么是事件监听器？**

事件监听器是 JavaScript 中等待事件发生的过程。[事件](https://www.edureka.co/blog/event-bubbling-and-event-capturing/)的简单例子是用户点击鼠标或按下键盘上的键。

**addEventListener()** 是一个内置的 [JavaScript 函数](https://www.edureka.co/blog/javascript-functions/)，它获取要监听的事件，以及每当触发所描述的事件时要调用的第二个参数。可以在单个元素中添加任意数量的事件处理程序，而不会覆盖现有的事件处理程序。

## **JavaScript 中的 addEventListener()**

事件监听器方法的一些**特性**包括:

*   **addEventListener()** 方法将一个**事件处理程序**附加到指定的元素上。
*   这个方法将一个事件处理程序附加到一个元素上，而不需要**覆盖现有的**事件处理程序。
*   你可以在一个元素中添加许多事件处理程序。
*   一个**元素**可以添加多个**相同类型**的事件处理程序，即两个“点击”事件。
*   事件监听器可以添加到任何 **DOM** 对象，而不仅仅是 HTML 元素。即窗口对象。
*   addEventListener()方法使得**更容易**控制**事件如何对冒泡做出反应**。

使用 addEventListener()方法时，JavaScript 与 [HTML](https://www.edureka.co/blog/what-is-html/) 标记分离，以获得更好的可读性，并允许您添加事件侦听器，即使您不控制 HTML 标记。今天就来看看这个[网站开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)吧。

此外，您可以通过使用 **removeEventListener()方法**轻松移除事件监听器。

**语法:**

```

```
target.addEventListener(type, listener[, options]);
target.addEventListener(type, listener[, useCapture]);
target.addEventListener(type, listener[, useCapture, wantsUntrusted ]);
```

```

## **参数值**

| **参数** | **描述** |
| ***事件*** | 必需的。指定事件名称的字符串。注意:不要使用“on”前缀。比如用“click”代替“onclick”。关于所有 HTML DOM 事件的列表，请看我们完整的 HTML DOM 事件对象参考。 |
| ***功能*** | 必需的。指定事件发生时要运行的函数。当事件发生时，事件对象作为第一个参数传递给函数。事件[对象](https://www.edureka.co/blog/javascript-object/)的类型取决于指定的事件。例如，“click”事件属于 MouseEvent 对象。 |
| ***使用捕获*** | 可选。一个布尔值，它指定事件应该在捕获阶段还是在冒泡阶段执行。可能值:true–在捕获阶段执行事件处理程序 false- Default。事件处理程序在冒泡阶段执行 |

现在你知道了事件监听器是如何工作的，让我们看看 JavaScript 中的 addEventListener()的例子。

## **JavaScript 中的 addEventListener():示例**

```

```
&amp;lt;!DOCTYPE html&amp;gt;
&amp;lt;html&amp;gt;
&amp;lt;body&amp;gt;
&amp;lt;p&amp;gt;This example uses the addEventListener() method to execute a function when a user clicks on a button.&amp;lt;/p&amp;gt;
&amp;lt;button id="myBtn"&amp;gt;Try it&amp;lt;/button&amp;gt;
&amp;lt;p id="demo"&amp;gt;
&amp;lt;script&amp;gt;
document.getElementById("myBtn").addEventListener("click", myFunction);
function myFunction() {
document.getElementById("demo").innerHTML = "Hello World";
}
&amp;lt;/script&amp;gt;
&amp;lt;/body&amp;gt;
&amp;lt;/html&amp;gt;
```

```

![addEventListener in JavaScript](img/aa419203cf98011d1b8987eadcba863d.png)

至此，我们结束了这个 JavaScript 中的 addEventListener。我希望您理解了事件监听器[方法](https://www.edureka.co/blog/javascript-methods/)在 JavaScript 中是如何工作的。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“JavaScript 中的 addEventListener”博客的评论部分提到它，我们将会回复您。