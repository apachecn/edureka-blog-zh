# 如何在 Javascript 中实现 Splice 方法()。

> 原文：<https://www.edureka.co/blog/splice-method-in-javascript/>

替换和添加元素是 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 最重要的方面之一。在本文中，我们将以如下方式理解 Javascript 中的 Splice 方法()。

*   [JavaScript 中的 Splice 方法()是什么？](#what)
*   [拼接方法参数()](#parameters)
*   [示例代码](#code)

## **JavaScript 中的 Splice 方法()是什么？**

JavaScript 中的 splice()方法通过移除或替换现有元素和/或添加新元素来改变数组的内容。

![Splice Method() in JavaScript](img/e7082dba2661bc6bfce4aa16f2459bbe.png)

## **语法**

`array.splice(index, howMany, [element1][, ..., elementN]);`

`Array.splice( index, remove_count, item_list )`

## **JavaScript 中拼接方法()的参数**

该方法接受许多参数，其中一些参数描述如下:

*   **指标:** 必要参数。此参数是开始修改数组的索引(原点为 0)。这也可以是负的，从末尾开始计算。

*   **remove_count:** 要从起始索引中删除的元素个数。

*   **items_list:** 由逗号运算符分隔的新项目列表，将从起始索引插入。

**返回值:** 虽然它就地改变了原始数组，但它仍然返回被删除项的列表。如果没有移除的数组，则返回一个空数组

## **示例代码**

**例 1:**

`<!DOCTYPE html>`

`<html>`

`<body>`

`<p>Click the button to add and remove elements.</p>`

`<button onclick="myFunction()">Try it</button>`

`<p id="demo"></p>`

`<script>`

`var fruits = ["Banana", "Orange", "Apple", "Mango"];`

`document.getElementById("demo").innerHTML = fruits;`

`function myFunction() {`

`  fruits.splice(2, 1, "Lemon", "Kiwi");`

`  document.getElementById("demo").innerHTML = fruits;`

`}`

`</script>`

`</body>`

`</html>`

**例 2:**

向现有数组中添加一个元素，同时移除其他元素。

`<script>  ``var arr=["Monday","Tuesday","Saturday","Sunday","Thursday","Friday"];  ``var result=arr.splice(2,2,"Wednesday")  ``document.writeln("Updated array: "+arr+"<br>");  ``document.writeln("Removed element: "+result);  `

![Splice method() Output](img/802f4c15a86c0eeaa64e247665442e3b.png)

**例 3:**

向现有数组中添加一个元素，同时移除其他元素。

`<script>  ``var arr=["Monday","Tuesday","Saturday","Sunday","Thursday","Friday"];  ``var result=arr.splice(2);  ``document.writeln("Updated array: "+arr+"<br>");  ``document.writeln("Removed element: "+result);  `

![Splice method() in Javascript](img/9d8d660ac2e5cf9dacb01f1f8ee7f7e9.png)

至此，我们结束了 Javascript 文章中的拼接方法()。我希望您了解了如何使用拼接方法()。

*查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这篇文章的评论部分提到它，我们会给你回复。*