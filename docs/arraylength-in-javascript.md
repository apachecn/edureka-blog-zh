# JavaScript 中的 Arraylength:您需要知道的一切

> 原文：<https://www.edureka.co/blog/arraylength-in-javascript/>

变量用于存储用户定义的数据类型的值，但它只能存储一个值。数组是一种在单个变量中存储多个值的方法。在本文中，我们将按以下顺序讨论 [JavaScript 数组](https://www.edureka.co/blog/javascript-array/)以及 JavaScript 中的数组长度是多少:

*   [简介](#introduction)
*   [数组索引](#arrayindex)
*   JavaScript 中的 Arraylength 是什么？
*   [数组长度的属性](#properties)
*   [长度和分度之间的差异](#lengthindex)

## **简介**

数组用于在单个变量中存储几个相同类型的值。在技术术语中是一种线性数据结构。简而言之，数据是按照一个接一个的特定顺序存储的。数组是同一数据类型的数据值的连续内存分配。

![Array length - Arraylength in javascript - edureka](img/4abaa5a4d7350e43c3889734c5b7f32a.png)

## **数组索引**

数组索引在技术上表示元素的位置。元素是存储在数组中的数据值。数组索引从 0 开始，即第一个元素的位置号用 0 表示。

![Array Index - Arraylength in JavaScript - edureka](img/fbdc8e1f5f9bef7a953e9bb5d55f1f10.png)

Arr[0]=45。然后在数组 Arr 的第 0 个位置出现数据元素 45。

## JavaScript 中的 Arraylength 是什么？

Array.length 是 Array 类型的实例，其对象属性为 length。数组的长度属性返回数组中元素的个数。它还可以帮助更新数组的长度(即增加或减少元素的数量。属性 length 的值是一个正整数，范围从小于 2 到 2 的 32 次方(232)。如欲了解更多信息，请立即查看此 [全栈开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

**语法:**

```

array.length

```

**代码:**

```

<html>
<head>
<title>Array Length in JavaScript</title>
</head>
<body>
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%20type%20%3D%20%22text%2Fjavascript%22%3E%0Avar%20arr%20%3D%20new%20Array(%2010%2C%2020%2C%2030%2C%2040%2C%2050%20)%3B%0Adocument.write(%22arr.length%20is%20%3A%20%22%20%2B%20arr.length)%3B%0A%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />
</body>
</html>

```

**输出:**

```
arr.length is : 5
```

与 Array.length 相关的属性特性

| **属性** | **值** |
| **可写** | 是 |
| **可配置** | 不 |
| **可枚举** | 不 |

*   **可写:**如果该属性设置为 false，该属性的值保持不变。
*   **可配置:**如果该属性设置为 false，则任何删除该属性或更改其属性的尝试都将失败。
*   **可枚举:**如果该属性设置为 true，则该属性将在 for 循环中迭代。

## **长度和分度之间的差异**

*   索引是数组中元素的位置号，而长度是任何数组中元素的数量。
*   索引从 0 开始，而长度从 1 开始。
*   索引范围从 0 到 n-1，长度范围从 1 到 n。

说到这里，我们的文章就到此为止了。我希望你明白 JavaScript 中的 Arraylength 是什么，以及它是如何工作的。

*既然你已经了解了 JavaScript 中的 Arraylength，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 中的 Arraylength”的评论部分提到它，我们会回复您。*