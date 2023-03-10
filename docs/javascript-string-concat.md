# JavaScript 中的字符串串联:关于 String concat()您所需要知道的一切

> 原文：<https://www.edureka.co/blog/javascript-string-concat/>

随着网络开发和应用的增长，对 JavaScript 的需求也在增长。它是设计网站最重要的语言之一。这篇关于 JavaScript 中的**字符串连接的文章**将解释字符串是如何按以下顺序操作的:

*   [JavaScript 中字符串连接的基础知识](#concatfundamentals)
*   [与微软 Excel 的类比](#microsoftexcel)
*   [与 C 编程的类比](#cprogramming)
*   [JavaScript 中字符串是如何操作的？](#stringmanipulation)
*   [字符串操作方法](#stringmethods)

## **JavaScript 中字符串连接的基础知识**

串联是构成连接两个字符串的基础的操作。合并字符串是编程中不可避免的一个方面。在进入“JavaScript 中的字符串连接”之前，我们需要先理清一些基础知识。当解释器执行操作时，一个新的字符串被创建。每种编程语言都有不同的连接操作语法。

```
edu.reka : Perl, PHP
```

```
edu & reka: Visual Basic, Visual Basic.NET and Ada
```

```
strcat(edu,reka): C, C++
```

```
edu+reka: Java
```

```
edu || reka: FORTRAN
```

此外，串联也适用于其他数据类型，如二进制、浮点、字符、整数等。但是要做到这一点，首先要将数据类型转换成字符串。此外，当我们处理对象时，只有当一个或两个对象属于同一个类时，字符串连接才是可能的。更多信息，请查看[网络开发者在线课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

**与微软 Excel 的类比**

让我们在我们最基本的平台上理解串联:微软 Excel。CONCATENATE/CONCAT 函数将两个或多个字符串连接在一起。它用作工作表函数，可以作为公式的一部分输入到单元格中。

**语法:**

```

CONCATENATE(edu1, [edu2,….edu_n])

```

**返回值:**

```
A string/Text
```

![string concatenation in excel](img/6fd3174ff2747ac47de0bcc3e9c51c0c.png)

有时用户可能想在结果中添加空格。在这种情况下，语法略有不同。

![Concatenate with Spaces](img/46f241ca16e4b7938324ea5ec438b122.png)

## **与 C 编程的类比**

因为我们都熟悉最基本的语言，即。c 编程，我们用 c 中的一个简单程序来理解拼接。

```

#include <stdio.h>
int main()
{
char edu1[100], edu2[100], i, j;
printf("Enter first string: ");
scanf("%s", edu1);
printf("Enter second string: ");
scanf("%s", edu2);
// calculate the length of string edu1
// and store it in i
for(i = 0; edu1[i] != ''; ++i);
for(j = 0; edu2[j] != ''; ++j, ++i)
{
edu1[i] = edu2[j];
}
edu1[i] = '';
printf("After concatenation: %s", edu1);
return 0;
}

```

**输出:**

```
Enter first string: edu
```

```
Enter second string: reka
```

```
After concatenation: edureka
```

**JavaScript 中字符串是如何操作的？**

我们先来了解一下 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 中的字符串对象。我们可以将字符串定义为在编程中用于存储字符序列的数据类型。整数和浮点单元也可以编码为字符串，但大多是文本形式，而不是数字。在进一步操作字符串之前，我们需要理解字符串对象的属性。

1.  **构造器:**返回一个由 JavaScript 实例的原型创建的引用。

**语法:**

```

array.constructor

```

**代码:**

```

<html>
<head>
<title>JavaScript Array constructor | Edureka</title>
</head>
<body>
<script type = "text/javascript">
var edu = new Array( 10, 20, 30 );
document.write("edu.constructor is:" + edu.constructor);
</script>
</body>
</html>

```

**输出:**

```
edu.constructor is:function Array() { [native code] }
```

2.  长度:它告诉我们数组中元素的数量

**语法:**

```

array.length

```

**代码:**

```

<html>
<head>
<title>JavaScript Array length | Edureka</title>
</head>
<body>
<script type = "text/javascript">
var edu = new Array( 10, 20, 30 );
document.write("edu.length is : " + edu.length);
</script>
</body>
</html>

```

**输出:**

```
edu.length is : 3
```

3.  **Prototype:**Prototype 属性允许我们向任何对象添加方法和属性(数字、布尔值、字符串和日期等)。这是一项全球性的财产

**语法:**

```

object.prototype.name = value

```

**代码:**

```

<html>
<head>
<title>Edureka Objects</title>
<script type = "text/javascript">
function Online(course, platform) {
this.course = course;
this.platform&nbsp; = platform;
}
</script>
</head>
<body>
<script type = "text/javascript">
var myOnline = new Online("R programming", "Edureka");
Online.prototype.price = null;
myOnline.price = 2400;
document.write("Online course is : " + myOnline.course + "<br>");
document.write("Online platform is : " + myOnline.platform + "<br>");
document.write("Online price is : " + myOnline.price + "<br>");
</script>
</body>
</html>

```

**输出:**

```
Online course is: R programming
Online platform is : Edureka
Online price is : 2400
```

**字符串操作方法**

| <u>序列号</u> | <u>方法</u> |
| one | **indexOf()**返回任何 string 对象第一次出现的索引值。 |
| <u>2</u> | **<u>slice()</u>**此方法用于从给定的字符串中提取特定的部分 |
| <u>3</u> | **split()**为了将一个字符串分成两个单独的字符串，使用了此方法 |
| <u>4</u> | **concat()**此方法用于合并两个不同的字符串，并返回合并后的字符串 |
| <u>5</u> | **valueOf()**若要返回字符串的主值，请使用此方法 |

从表中，我们将只关注 **concat()** 方法。正如我们所知，串联方法接受多个字符串，合并它们并返回一个新的单个字符串。下面给出了语法、参数和示例:

*   **语法:**

```

String.concat(edu1, edu2[, …, eduN]);

```

*   **方法中的参数:**

edu1，edu2，… eduN 是被传递用于连接的字符串。

*   **代码:**

```

<html>
<head>
<title>String Concatenation | Edureka</title>
</head>
<body>
<script type = "text/javascript">
var edu1 = new String( "If it's about learning, " );
var edu2 = new String( "Edureka is the right platform" );
var edu3 = edu1.concat( edu2 );
document.write("Result: " + edu3);
</script>
</body>
</html>

```

**输出:**

```
If it's about learning, Edureka is the right platform
```

此外，作为程序员，有时需要将多个字符串连接在一起，即。不止两个。让我们来看一段简单的代码，这段代码强调了 JavaScript 中字符串连接的使用:

```

<!DOCTYPE html>
<html>
<body>
<p>Let's join three strings</p>
<button onclick="myFunction()">Edureka Button</button>
<p id="edu"></p>
<script>
function myFunction() {
var edu1 = "Hello ";
var edu2 = "Edureka, " ;
var edu3 = "Let's code today !";
var con = edu1.concat(edu2, edu3);
document.getElementById("edu").innerHTML = con;
}
</script>
</body>
</html>

```

**输出:**

`![Join multiple strings](img/5872eb57e46bd12697d4840fe6ed36c2.png)`

因此，我们已经讨论了 JavaScript 中与字符串连接相关的所有内容，现在我们可以编写代码，看看我们是否可以实际实现连接方法。因此，在撰写文章之前，你可以做以下事情:

1.  可视化你的程序流程
2.  决定变量声明
3.  记下几个**字符串**
4.  遵循这里写的**例子**
5.  你可以在你的本地服务器上测试它。

至此，我们结束了 JavaScript 博客中的字符串连接。我希望您了解连接字符串的不同方式。

*既然你已经了解了 JavaScript，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 中的字符串连接”的评论部分提到它，我们会回复您。*