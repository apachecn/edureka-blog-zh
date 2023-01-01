# JavaScript Substring()–它与 Substr() & slice()有什么不同？

> 原文：<https://www.edureka.co/blog/javascript-substring/>

操作数据是任何 web 应用程序不可或缺的一部分。 [JavaScript](https://www.edureka.co/javascript-jquery-training) 提供了不同的解析和提取数据的方式。JavaScript Substring、Substr 和 Slice 方法用于从较大的字符串中提取字符串。这篇 **JavaScript Substrig** 文章将按以下顺序提供关于这方面的深入知识:

*   [什么是子串？](#substring)
*   [如何获取一个 JavaScript 子串？](#javascriptsubstring)
*   [使用带有长度属性的子串](#substringlength)
*   [子串 vs 子串 vs 切片](#substringvssubstrvsslice)

## **什么是子串？**

子字符串是另一个字符串的子集。它是字符串中连续的字符序列。

![substring-javascript substring - edureka](img/3a35fbc32b2b52d8aea6a337aef89ff5.png)

例如，“*欢迎来到 Edureka* ”是字符串“*欢迎来到 Edureka 在线课程*”的子字符串。但是，“ *Edureka Courses* ”不是子串，因为它是子序列或字符串的推广。

## **如何获取一个 JavaScript 子串？**

**substring()** 是 JavaScript 中的内置函数，它返回从**开始索引**到**结束索引**的给定**字符串**的一部分。索引从零开始。它用于返回字符串的一部分，从指定的索引开始，延伸到后面给定数量的字符。

**语法:**

```
string.substring(indexA, [indexB])

```

在哪里，

*   **indexA** (起始索引)-介于 0 和字符串长度减 1 之间的整数。
*   **indexB** (结束索引)-介于 0 和字符串长度之间的整数。它是可选的。

这个子串方法**根据给定的参数返回**新的子串**。**

我们举个例子，看看 **substring()** 函数是如何工作的。

**输入:**

```
<html>
<head>
<title>JavaScript String substring() Method</title>
</head>
<body>
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%20type%20%3D%20%22text%2Fjavascript%22%3E%0Avar%20str%20%3D%20%22Welcome%20to%20Edureka%20JavaScript%20Training%22%3B%0Adocument.write(%22(3%2C7)%3A%20%22%20%2B%20str.substring(3%2C7))%3B%0Adocument.write(%22(0%2C10)%3A%20%22%20%2B%20str.substring(0%2C10))%3B%0Adocument.write(%22(11)%3A%20%22%20%2B%20str.substring(11))%3B%0A%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />
</body>
</html>

```

**输出:**

```
(3,7): come
(0,10): Welcome to
(11): Edureka JavaScript Training
```

## **使用带有长度属性的子串**

length 属性用于获取一个[字符串](https://www.edureka.co/blog/javascript-string-concat/)的长度。 **substring()** 方法和 **length** 属性一起用于提取特定字符串的最后几个字符。这种方法更容易记忆，因为你不需要知道开始和结束的索引。

**举例:**

```

var anyString = 'Edureka';
var anyString1 = anyString.substring(anyString.length - 5); //Displays last 5 characters
console.log(anyString1);

```

**输出:**

```
ureka
```

现在你知道了什么是 substring 以及它是如何工作的，让我们继续我们的 JavaScript Substring 文章，讨论 Substring、substr 和 slice 之间的区别。

## **Substring()vs Substr()vs Slice()**

这些方法用于**提取一个字符串的部分**，并将提取的部分返回到一个**新字符串**中。所有这些都不会改变原来的字符串。

| **子串()** | **Substr()** | **切片()** |
| JavaScript **substring()** 方法返回 startIndex & endIndex 之间的部分字符串。它排除 endIndex 字符或直到字符串的末尾。 | JavaScript **substr()** 方法返回从一个索引开始的字符串的一部分，以及起始索引之后的字符数。它有两个参数，如 **startIndex** 和 **Length** | **slice()** 方法类似于 substring。它返回开始索引&和结束索引之间的部分字符串。如果没有提供结束索引，它将排除结束索引字符或直到字符串的结尾 |

**子串()** **语法:**

```

string.substring(startIndex[, endIndex])

```

**举例:**

```

var string = "Edureka JavaScript";
var substring = string.substring(0,7);
console.log(substring);

```

**输出:**

```
Edureka
```

**Substr()**语法:

```

string.substr(startIndex[, length])

```

**举例:**

```

var string = "Edureka JavaScript";
var substr = string.substr(8,10);
console.log(substr);

```

**输出:**

```
JavaScript
```

**Slice()** **语法:**

```

string.slice(startIndex[, endIndex])

```

**举例:**

```

var string = "Edureka JavaScript";
var substr = string.slice(8,12);
console.log(substr);

```

**输出:**

```
Java
```

至此，我们的 JavaScript Substring 博客到此结束。我希望你理解了它是如何被用来提取字符串的任何部分的。

*既然你已经了解了 JavaScript Substring，那就去看看 Edureka 的 [**Web 开发者课程**](https://www.edureka.co/complete-web-developer) 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript Substring”的评论部分提到它，我们会回复您。*