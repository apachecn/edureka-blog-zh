# 20 大 Javascript 字符串函数有哪些，如何使用？

> 原文：<https://www.edureka.co/blog/javascript-string-functions/>

Javascript 是一种高级编程语言，具有花括号语法，基于面向对象的动态类型&原型。在 [Java 编程](https://www.edureka.co/blog/java-tutorial/)中，字符串被当作文章处理。Java stage 提供了 String 类来创建和控制字符串。这个 **JavaScript 字符串函数**将列出一些最常用的字符串函数。

一些重要的 javascript 字符串函数包括:

*   [character(x)](#charAt(x))
*   [charCodeAt(x)](#charCodeAt(x))
*   [concat(v1，v2..)](#concat(v1,v2..))
*   [弗洛姆 Charcode(c1，c2)](#fromCharcode(c1,c2))
*   [indexOf(substr, [start])](#indexOf(substr,%5Bstart%5D))
*   [lastIndexOf(substr, [start])](#lastIndexOf(substr,%5Bstart%5D))
*   [![JavaScript - javascript string function- Edureka](img/d381545dc236a418e9576d797d97f1d6.png)【匹配(正则表达式)](#match(regexp))
*   [替换(regexp/substr，replacetext)](#replace(regexp/substr,replacetext))
*   [搜索(regexp)](#search(regexp))
*   [切片(开始，[结束])](#slice(start,%5Bend%5D))
*   [拆分(分隔符，[限制])](#split(delimiter,%5Blimit%5D))
*   [substr(开始，[长度])](#substr(start,%20%5Blength%5D))
*   [子串(从，[到])](#substring(from,%20%5Bto%5D))
*   [toLowerCase()](#toLowerCase())
*   [toUpperCase()](#toUpperCase())
*   [包括()](#includes)
*   [endsWith()](#endswith)
*   [重复()](#repeat)
*   [valueOf()](#linkValueOf)
*   [trim()](#trim)

现在让我们继续，看看字符串函数。

## **1.查尔特(x)**

这个函数将返回字符串中 x 位置的字符。

```
//charAt(x)
var myString = 'jQuery FTW!!!';
console.log(myString.charAt(7));
//output: F

```

继续这篇关于 [Javascript](https://www.edureka.co/blog/javascript-tutorial/) 字符串函数的文章，让我们看看下一篇。

## **2.charCodeAt(x)**

此函数将返回字符串中位置“x”处字符的 unicode 值。

```
//charAt(position)
var message="jquery4u"
//alerts "q"
alert(message.charAt(1)

```

## 3.concat(v1，v2..)

该函数将一个或多个字符串(argv1、v2 等)合并成一个现有的字符串。

```
//concat(v1, v2,..)
var message="Sam"
var final=message.concat(" is a"," hopeless romantic.")
//alerts "Sam is a hopeless romantic."
alert(final)

```

## **4.fromCharcode(c1，c2)**

函数将返回使用指定的 unicode 值序列(argc1，c2)创建的字符串。

```
//fromCharCode(c1, c2,...)
console.log(String.fromCharCode(97,98,99,120,121,122))
//output: abcxyz
console.log(String.fromCharCode(72,69,76,76,79))
//output: HELLO

```

## **5.indexOf(substr, [start])**

搜索并(如果找到)返回字符串中被搜索字符或[子字符串的索引号。如果没有找到，则返回-1。“Start”是一个可选参数，指定字符串中开始搜索的位置。默认值为 0。](https://www.edureka.co/blog/javascript-substring/)

```
//indexOf(char/substring)
var sentence="Hi, my name is Sam!"
if (sentence.indexOf("Sam")!=-1)
alert("Sam is in there!")

```

继续这篇关于 Javascript 字符串函数的文章

## **6.lastIndexOf(substr, [start])**

搜索并(如果找到)返回字符串中被搜索字符或子字符串的索引号。从末尾到开头搜索字符串。如果没有找到，则返回-1。“Start”是一个可选参数，指定字符串中开始搜索的位置。默认值为 string.length-1。

```
//lastIndexOf(substr, [start])
var myString = 'javascript rox';
console.log(myString.lastIndexOf('r'));
//output: 11

```

## 7 .匹配(正则表达式)

基于正则表达式在字符串中搜索匹配项。如果没有找到匹配，它返回一个信息数组或 null。

```
//match(regexp) //select integers only
var intRegex = /[0-9 -()+]+$/;  

var myNumber = '999';
var myInt = myNumber.match(intRegex);
console.log(isInt);
//output: 999

var myString = '999 JS Coders';
var myInt = myString.match(intRegex);
console.log(isInt);
//output: null

```

继续这篇关于 Javascript 字符串函数的文章，让我们了解一下替换函数。

## 8 .替换(regexp/substr，replacetext)

搜索并用替换的文本替换正则表达式(或子字符串)部分(匹配)。

```
//replace(substr, replacetext)
var myString = '999 JavaScript Coders';
console.log(myString.replace(/JavaScript/i, "jQuery"));
//output: 999 jQuery Coders

//replace(regexp, replacetext)
var myString = '999 JavaScript Coders';
console.log(myString.replace(new RegExp( "999", "gi" ), "The"));
//output: The JavaScript Coders

```

## 9 .搜索(正则表达式)

测试字符串中的匹配项。它返回匹配的索引，如果没有找到则返回-1。

```
//search(regexp)
var intRegex = /[0-9 -()+]+$/;  

var myNumber = '999';
var isInt = myNumber.search(intRegex);
console.log(isInt);
//output: 0

```

## **10.slice(开始，[结束])**

此函数根据“开始”和“结束”索引参数返回字符串的子字符串，不包括“结束”索引本身。“End”是可选的，如果没有指定，片段包括从“start”到字符串结尾的所有字符。

```
//slice(start, end)
var text="excellent"
text.slice(0,4) //returns "exce"
text.slice(2,4) //returns "ce"

```

继续这篇关于 Javascript 字符串函数的文章

## 11.split(分隔符，[限制])

这将根据指定的分隔符将一个字符串分成许多部分，并返回包含每个元素的数组。可选的“limit”是一个整数，允许您指定要返回的最大元素数。

```
//split(delimiter)
var message="Welcome to jQuery4u"
//word[0] contains "We"
//word[1] contains "lcome to jQuery4u"
var word=message.split("l")

```

12.substr(开始，[长度])

此函数返回从“start”开始到指定字符数“length”的字符串中的字符。“Length”是可选的，如果省略，则假定一直到字符串的末尾。

```
//substring(from, to)
var text="excellent"
text.substring(0,4) //returns "exce"
text.substring(2,4) //returns "ce"

```

## 13.substring(from，[to])

它返回“从”和“到”索引之间的字符串中的字符，不包括“到”本身。“To”是可选的，如果省略，则假定一直到字符串的末尾。

```
//substring(from, [to])
var myString = 'javascript rox';
myString = myString.substring(0,10);
console.log(myString)
//output: javascript

```

## 14.toLowerCase()

这将返回所有字符都转换成小写的字符串。

```
//toLowerCase()
var myString = 'JAVASCRIPT ROX';
myString = myString.toLowerCase();
console.log(myString)
//output: javascript rox

```

## toUpperCase()

这将返回所有字符都转换为大写的字符串。

```
//toUpperCase()
var myString = 'javascript rox';
myString = myString.toUpperCase();
console.log(myString)
//output: JAVASCRIPT ROX

```

## 16。包含()

它用于检查字符串是否包含指定的字符串或字符。

```
//includes()
var mystring = "Hello, welcome to edureka";
var n = mystring.includes("edureka");
//output: True

```

## **17。endsWith()**

这个函数检查一个字符串是否以指定的字符串或字符结尾。

```
//endsWith()
var mystr = "List of javascript functions";
var n = mystr.endsWith("functions");
//output: True

```

## 18。重复()

这将返回一个新字符串，它具有现有字符串的指定数量的副本。

```
//repeat()
var string = "Welcome to Edureka";
string.repeat(2);
//output: Welcome to Edureka Welcome to Edureka

```

## **19。valueOf()**

它用于返回字符串对象的原始值。

```
//valueOf()
var mystr = "Hello World!";
var res = mystr.valueOf();
//output: Hello World!

```

## 20。trim()

这个函数删除字符串两端的空格。

```
//trim()
var str = "     Hello Edureka!     ";
alert(str.trim());

```

这些是一些最常用的 JavaScript 字符串函数。说到这里，我们的文章就到此为止了。

*既然你已经了解了 JavaScript 字符串函数，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 字符串函数”的评论部分提到它，我们会回复您。*