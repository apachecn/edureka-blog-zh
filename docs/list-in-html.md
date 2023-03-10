# 如何在 HTML 中实现不同类型的列表？

> 原文：<https://www.edureka.co/blog/list-in-html/>

列表是表示数据&信息的重要方式之一，其中每条记录显示在一行中。有各种方式来表示列表中的数据，例如以有序的方式，或者以无序的方式。我将在这个列表中的 [HTML](https://www.edureka.co/blog/what-is-html/) 文章中涵盖以下主题:

*   [HTML 中的列表类型](#listtypes)
*   [无序的 HTML 列表](#unorderedlist)
*   [有序的 HTML 列表](#orderedlist)
*   [HTML 描述列表](#descriptionlist)
*   [HTML 中的嵌套列表](#nestedlist)

## **HTML 中的列表类型**

在我们开始创建列表之前，让我们先来看看 HTML 标签:

*   **< ul >** 用来定义一个无序列表
*   **< ol >** 用来定义一个有序列表
*   **<李>** 用来定义一个列表项
*   **< dl >** 用来定义一个描述列表
*   **< dt >** 用于定义描述列表中的术语
*   **< dd >** 用来描述描述列表中的术语

让我们来了解一下如何在 HTML 中创建不同类型的列表。

## **无序列表**

为了在 HTML 中定义一个无序列表，我们使用

 **<李>** 

```
<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ul> 
<li>Cricket</li>
<li>Football</li>  
<li>Baseball</li>
</ul>
</body> 
</html>

```

**输出:**

![Unordered List in HTML](img/bde3bdd77766bcbb11c3325ebdfbb307.png)

**无序的 HTML 列表:不同的项目标记**

你可以使用 CSS list-style-type 属性从标记列表中选择。让我们来看看不同的 CSS 列表样式类型属性，您可以使用它们来定义不同样式的标记:

*   **disc** :将列表项标记设置为 bullet
*   **圆形** :将列表项标记设置为圆形
*   **正方形** :将列表项标记设置为正方形
*   **无** :列表项不会被标记

**碟片:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ul style="list-style-type:disc;">
<li>Cricket</li>
<li>Football</li>
<li>Baseball</li>
</ul>
</body> 
</html>

```

**输出:**

**![Disc in HTML](img/1e2f70485c3d85d1124a798789acb22d.png)圆圈:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ul style="list-style-type:circle;">
<li>Cricket</li> 
<li>Football</li>
<li>Baseball</li>
</ul>
</body> 
</html>

```

**输出:**

**![Circle-List in HTML](img/87bfabea94c7adc6da1eb2e3a6ef0941.png)方:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ul style="list-style-type:square;"> 
<li>Cricket</li> 
<li>Football</li> 
<li>Baseball</li>
</ul>
</body> 
</html>

```

**输出:**

**![Square](img/7c373d9f8d21cf9784b0fd55ca5f9fd2.png)无:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ul style="list-style-type:none;"> 
<li>Cricket</li> 
<li>Football</li> 
<li>Baseball</li>
</ul>
</body> 
</html>

```

**输出:**

![None](img/ee6dcabf7ee96faa62fd3b6949161a36.png)现在了解了如何在 HTML 中创建一个无序列表之后，让我们来了解如何在 HTML 中创建一个有序列表。

有序列表

为了在 HTML 中定义有序列表，我们使用 **< ol >** 标签，然后在 **< li >** 标签中定义项目列表。默认情况下，物品列表标有数字。

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ol>  
<li>Cricket</li>
<li>Football</li>  
<li>Baseball</li>
</ol>
</body> 
</html>

```

**输出:**

![Ordered List in HTML](img/695dc359a1dabe6f548440892076a7c8.png)现在让我们看看有序列表的一些变体。

**有序 HTML 列表–类型属性**

有序列表有不同类型的项目标记:

*   **type = " 1"**列表项将用数字编号(默认)

*   **type="A"** 列表项将用大写字母编号

*   **type="a"** 列表项将用小写字母编号

*   **type="I"** 列表项将用大写罗马数字进行编号

*   **type="i"** 列表项将用小写罗马数字进行编号

**数字:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ol type="1">  
<li>Cricket</li>  
<li>Football</li>
<li>Baseball</li>
</ol>
</body> 
</html>

```

**输出:**

**![Numbers](img/695dc359a1dabe6f548440892076a7c8.png)大写字母:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ol type="A">  
<li>Cricket</li> 
<li>Football</li> 
<li>Baseball</li>
</ol>
</body> 
</html>

```

**输出:**

**![Uppercase Letter](img/3f378fae145299376d441b0863ab81a7.png)小写字母:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ol type="a">
<li>Cricket</li> 
<li>Football</li>
<li>Baseball</li>
</ol>
</body> 
</html>

```

**输出:**

**![Lowercase Letter](img/4f14297a965aee7d7808ed65cc1440c7.png)大写罗马 Nu**mbers:

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ol type="I"> 
<li>Cricket</li>
<li>Football</li> 
<li>Baseball</li>
</ol>
</body> 
</html>

```

**输出:**

![Uppercase Roman Number](img/3bb0e1334c9cdf757d01110afd194fc5.png)

**小写罗马数字:**

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ol type="i">
<li>Cricket</li>  
<li>Football</li> 
<li>Baseball</li>
</ol>
</body> 
</html>

```

**输出:**

![Lowercase Roman Numbers](img/db5057dd053c9df30225a10f1fb45d2d.png)

## **HTML 描述列表**

您也可以创建 HTML 格式的描述列表。描述列表用于创建术语列表，并向它们添加描述。你使用***<dl>***标签创建一个描述列表。 ***< dt >*** 标签定义了术语&***<DD>***标签给它们添加了描述。

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<dl> 
<dt>Cricket</dt> 
<dd> Cricket is a bat-and-ball game played between two teams of eleven players on a field at the centre of which is a 20-metre pitch with a wicket at each end, each comprising two bails balanced on three stumps.</dd>  
<dt>Table Tennis</dt>
<dd> Table tennis, also known as ping-pong, is a sport in which two or four players hit a lightweight ball back and forth across a table using small rackets. The game takes place on a hard table divided by a net.</dd>
</dl>
</body> 
</html>

```

**输出:**

![](img/479d06c532e96ff50f0323b1f50bd866.png)

## **HTML 中的嵌套列表**

您也可以在 HTML 中创建嵌套列表。

```

<!DOCTYPE html> 
<html> 
<body>
<h2>Sports</h2>
<ul> 
<li>Table Tennis</li>
<li>Cricket
<ul>   
<li>Virat Kohli</li>  
<li>Joe Root</li>
</ul>
</li></pre>
<pre><li>Basketball</li>
</ul>
</body> 
</html>

```

**输出:**

![Nested List in HTML](img/4f600ec37daa651246c161422f5091a6.png)

现在，在执行了上面的代码片段之后，你应该已经理解了如何在 HTML 中创建列表。我希望这篇博客能给你带来信息和附加值。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“HTML 列表”博客的评论部分提到它，我们将会回复您。