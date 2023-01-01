# JavaScript 中的数组长度:关于 JavaScript 中的长度属性，您只需要知道

> 原文：<https://www.edureka.co/blog/array-length-in-javascript/>

在保存要编程的数据时，数组起着非常重要的作用。同样， **[JavaScript](https://www.edureka.co/blog/what-is-javascript/)** 是一种流行的脚本语言，拥有强大的市场份额。这篇关于“Java 中的数组长度”的文章将帮助你探索 JavaScript 中关于数组的“长度”函数。以下是本文将涉及的要点，

*   [JavaScript 中的数组长度](#ArraylengthinJavascript)
*   [使用长度显示元素](#Displayingtheelementsusinglength)
*   [使用长度](#Findingoutthenumberofwordspresentusinglength)找出当前单词的数量

让我们从讨论的第一个话题开始，

## **JavaScript 中的数组长度**

那么在 JavaScript 中我们如何计算数组的长度呢？JavaScript 中数组的长度可以通过使用 length 属性(也称为 JavaScript 数组长度属性)有条不紊地找到。length 属性可以做多项工作，包括返回或设置数组中元素的数量，因为它返回一个无符号的 32 位整数。

返回值是无符号整数。长度属性可以指定为:

```
array.length
```

为了更好的理解，我们可以参考下面的程序，先从[安装](https://developer.mozilla.org/en-US/docs/Web/JavaScript)开始:

**例子**

```

<script type="text/javascript">
var music = new Array();
music[0] = "Rock";
music[1] = "Pop";
music[2] = "Jazz";
music[3] = "Blues";
document.write(music.length);
</script>

```

**输出**

four

使用 length 属性的另一种方法如下:

**举例:**

```
</p>
<script>
//JavaScript to illustrate length property
function fun() {
// length property for array
document.write([9,2,4,8,1,7,6,3,5].length);
document.write("<br>");
// length property for string
document.write("HelloWorld".length)
}
fun();
</script>
<p style="text-align: justify;">
```

应该注意，在字符串的情况下，length 属性返回字符串中存在的字符数，而在数组的情况下，返回数组中存在的元素数。

**输出**

nine

Ten

现在让我们看看如何使用长度来显示元素。

## 使用长度显示元素

在下面的程序中，使用以下方法访问数组的最后一个元素:(music.length-1)，然后显示该元素。

**示例:**

```

<script type="text/javascript">
var music = new Array();
music[0] = "Rock";
music[1] = "Pop";
music[2] = "Jazz";
music[3] = "Blues";
document.write(music[music.length-1]);
</script>

```

**输出:**

布鲁斯音乐

让我们转到这篇文章的最后一点，看看我们如何在长度的帮助下找出单词的数量。

## **使用长度**找出当前单词的数量

长度可以用来找出一个字符串中的单词数。我们还利用 split 函数来创建一个数组。

```

<script type="text/javascript">
//creating a string
var str="Music is a great way to relax. And rejuvenate";
//creating an array
var arr = new Array();
//using the split function
arr=str.split(" ");
document.write("Total Number Of Words: "+ arr.length);
</script>

```

**输出:**

总字数:9

***求数组的长度不仅是一个基本要求，也是解决许多问题的整体方法。***

至此，我们结束了这篇关于“JavaScript 中的数组长度”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。