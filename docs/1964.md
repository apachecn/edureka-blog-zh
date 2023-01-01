# JavaScript 中的 indexOf 是什么，它是如何工作的？

> 原文：<https://www.edureka.co/blog/indexof-in-javascript/>

对于不同的任务， [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 中有不同的内置函数。Indexof 函数用于返回单词的起始位置。它主要返回数组中特定元素的索引。它是 Array 的一个函数，返回数组中某个元素的索引。在本文中，我们将按照以下顺序理解 JavaScript 中的 indexOf:

*   [JavaScript 中的 indexOf 是什么？](#what)
*   [Javascript String indexOf](#string)
*   [JavaScript 中的数组 index of](#array)
*   [index of()和 search()的区别](#difference)

## **JavaScript 中的 indexOf 是什么？**

**IndexOf** 函数用于找出[字符串](https://www.edureka.co/blog/javascript-string-functions/)和[数组](https://www.edureka.co/blog/javascript-array/)中元素的索引。有两种变体，一种是 indexOf，用于给出搜索元素或第一个匹配元素的位置:

如果没有找到元素，它将返回-1。

第二个是 lastIndexOf 函数，用于从字符串或数组中的最后一个开始查找元素。

**举例:**

```
var string =’Welcome to Edureka’

string.indexOf(‘Welcome’)
```

**输出:**

```
0
```

对于 lastIndexof 函数，我们可以举以下例子:

```
var = ‘Welcome to edureka’

string.lastIndexOf(‘edureka’)
```

**输出:**

```
12
```

JavaScript 中的 indexOf 以类似的方式为[数组](https://www.edureka.co/blog/array-methods-in-javascript/)工作。现在让我们结合实例深入探讨一下[字符串](https://www.edureka.co/blog/javascript-string-functions/)和数组 indexOf 方法。

## **Javascript String indexOf **

**str.indexOf()** [函数](https://www.edureka.co/blog/javascript-functions/)在给定的字符串中查找参数字符串第一次出现的索引。返回值是从 0 开始的。此外，如果要搜索的值从未出现，它将返回-1。

**语法:**

```
string.indexOf(searchvalue, start)
```

第一个参数 searchValue 是要在基本字符串中搜索的字符串。函数 index 的第二个参数定义了在基本字符串中搜索 searchValue 的起始索引。

此函数返回第一次找到 searchValue 的字符串的索引(从 0 开始)。如果在字符串中找不到 searchValue，则函数返回-1。

**举例:**

```
var str = "Hello, welcome to edureka!";
var n = str.indexOf("e");
```

**输出:**

```
1
```

## **JavaScript 中的数组 index of**

arr.indexOf()函数用于查找作为函数参数提供的搜索元素的第一个匹配项的索引。

**语法:**

```
arr.indexOf(searchElement[,index])
```

第一个参数 searchElement 是要在数组中搜索的值。这个函数的第二个参数是可选的 index 参数，它定义了在数组中搜索元素的起始索引。如果未提供此参数，则将索引 0 作为开始搜索的起始索引，因为这是默认值。

该函数返回 searchElement 第一次出现的索引。如果在数组中找不到该元素，则该函数返回-1。

**举例:**

```
var cars = ["BMW", "Audi", "Ferrari"];
var arr = cars.indexOf("Ferrari");
```

**输出:**

```
2
```

## **index of()和 search()的区别**

indexOf()和 search()方法都用于检查字符串中是否存在子串。此外，如果字符串中不存在子字符串，则返回子字符串的索引或-1。但是 indexOf()和 search()方法是有区别的。让我们来看看这两种方法的语法。

**index of()方法的语法:**

```
String.indexOf(substring, [offset]);
```

**search()方法的语法:**

```
String.search(substring);
```

现在，您可以看到在 **indexOf()** 方法中，有一个可选参数(offset ),我们可以从这里开始搜索，但是 search()方法没有这个特性。它只是获取子串，并从第 0 个索引开始搜索。

这都是关于 JavaScript 的索引。说到这里，我们的文章就到此为止了。我希望您理解这个方法在 JavaScript 中是如何工作的。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“JavaScript 中的 indexOf”博客的评论部分提到它，我们会给你回复。