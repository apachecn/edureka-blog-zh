# JavaScript 中的数组方法:关于数组方法你需要知道的一切

> 原文：<https://www.edureka.co/blog/array-methods-in-javascript/>

当计划编写解决方案时，效率是非常重要的。 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 中的数组对象由各种方法组成。这些方法在代码中使用是为了它们的高效运行。本文将关注 JavaScript 中的各种数组方法。

本文将涉及以下几点:

*   [Concat 方法](#ConcatMethod)
*   [CopyWithin 方法](#CopyWithinMethod)
*   [每一种方法](#EveryMethod)
*   [ToString 方法](#ToStringMethod)
*   [加入方式](#JoinMethod)
*   [弹出推送方式](#PopAndPushMethod)
*   [换档和非换档方法](#ShiftAndUnshiftMethod)
*   [拼接方法](#SpliceMethod)
*   [切片法](#SliceMethod)
*   [ForEach 方法](#ForEachMethod)

让我们继续这篇文章的第一个主题，

## **JavaScript 中的数组方法**

## **Concat 方法**

concat()方法连接两个或多个数组，然后返回连接后的数组的副本。

```

<html>
<body>
<script type = "text/javascript">
var alphabet = ["r", "s", "t"];
var num = [5, 6, 7];
var AlphabetNum = alphabet.concat(num);
document.write("AlphabetNum : " + AlphabetNum );
</script>
</body>
</html>

```

在给出的示例中，concat 方法连接两个数组 alphabet 和 num，并返回一个新的连接数组:AlphabetNum。

**输出:**

字母数字:r，s，t，5，6，7

接下来是 CopyWithin 方法，

## **CopyWithin 方法**

JavaScript 中的 copyWithin()方法用于将数组的一部分复制到同一个数组中，然后返回它。

**语法:**

```
array.copyWithin(target, start, end)
```

该方法由三个参数组成:

*   Target:要复制元素的索引位置。必须指定目标。
*   Start:开始复制元素的索引位置。它是可选的。start 的默认值为 0。
*   End:结束复制元素过程的索引位置。这也是一个可选参数，默认值是*长度*。

```

<!DOCTYPE html>
<html>
<body>
<script>
var number = ["One", "Two", "Three", "Four", "Five", "Six", "Seven"];
document.write(number);
document.write("<br>"+number.copyWithin(3,0,4));
</script>
</body>
</html>

```

**输出:**

一，二，三，四，五，六，七

一，二，三，一，二，三，四

如示例所示，数组中的值被复制到同一个数组中。目标索引为:3，开始索引为:0，结束索引为:4。

javascript 中数组方法的下一位是，

## **每一种方法**

此方法检查数组中的所有元素是否都满足指定的条件。该方法的语法如下:

```
array.every(function[, This_arg])
```

这个函数的参数是另一个函数。它定义了必须检查的条件。它有以下论点:

*   Array:调用 every()函数的数组。这是一个可选参数。
*   Index:当前元素的索引。这也是可选的。
*   Element:函数正在处理的当前元素。必须使用该参数。

this_arg 用于告诉函数使用*这个*值。在下面的例子中，我们检查数组中的每个元素是否为正。

```

function positive(element, index, array)
{
return element > 0;
}
function func() {
var array = [ 11, 89, 23, 7, 98 ];
//check for positive number
var value = array.every(positive);
document.write(value);
}
func();
</script>

```

必须注意，该函数返回的值是真还是假。由于数组中的所有元素都是正的，因此输出将是:

真实的

接下来是 ToString 方法。

## **ToString 方法**

此方法将数字转换为字符串。也可以通过指定基值来转换这些数字。

```

<script type="text/javascript">
var number=569;
document.write("Output : " + number.toString());
</script>

```

在给出的示例中，调用 toString()方法时没有任何参数或基值。

**输出:**

Five hundred and sixty-nine

现在让我们来看看连接方法，

## **加入方式**

join()方法连接数组中的每个元素。此外，我们可以指定一个分隔符来分隔元素。

```

<html>
<body>
<script type = "text/javascript">
var a = new Array("I","Love","Music");
var string = a.join();
document.write("string : " + string );
var string = a.join(" * ");
document.write("<br />string : " + string );
var string = a.join(" + ");
document.write("<br />string : " + string );
</script>
</body>
</html>

```

在提供的示例中，第一个连接方法不包含任何分隔符，因此使用默认分隔符。在另外两种方法中，“*”和“+”是指定的运算符。

**输出:**

弦乐:我，爱，音乐

弦乐:我爱音乐

弦乐:我+爱+音乐

本文的下一个主题是 javascript 上的数组方法，

## **弹出推送方式**

pop()方法从数组末尾移除元素，就像堆栈一样。另一方面，push()方法将元素添加到数组的末尾。如需了解更多信息，请立即查看本[网络开发课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

这些方法实现了后进先出的概念。

```

["Rock", "Metal", "Blues", "Jazz"]
list.pop();
["Rock", "Metal", "Blues"]

```

代码删除数组中的最后一个元素，即“Jazz”。

push()方法将元素追加回数组。

```

["Rock", "Metal", "Blues"]
list.push("Jazz");
["Rock", "Metal", "Blues", "Jazz"]

```

让我们继续前进，

## **换档和非换档方法**

shift()方法从数组的开头移除元素。另一方面，unshift()方法将元素添加回数组的开头。

```

["Rock", "Metal", "Blues", "Jazz"]
list.shift();
["Metal", "Blues", "Jazz"]

```

代码从数组中删除第一个元素，即 Rock。

在使用 unshift()方法时，“Rock”将被添加回数组。

```

["Rock", "Metal", "Blues", "Jazz"]
list.unshift("Rock");
["Rock”, “Metal", "Blues", "Jazz"]

```

在 javascript 博客中，我们正在讨论这个数组方法的最后一点，

## **拼接方法**

splice()方法移除数组中特定的或选定的部分。事实证明，这是一种在数组中删除、替换或添加元素的有效方法。

```

["Rock", "Metal", "Blues", "Jazz"]
list.splice(2, 1);
// Starting at index position 2, remove one element
["Rock", "Metal", "Jazz"]
list.splice(2,2);
// Starting at index position 2, remove two elements
["Rock", "Metal"]

```

在上面的示例中，slice 方法根据指定的索引移除元素。

“Blues”从第一个示例中删除，因为它位于索引 2 处。

在第二个例子中，删除了两个元素，即“布鲁斯”和“爵士乐”，因为索引指定必须从索引 2 开始删除 2 个元素。

必须注意，在 JavaScript 中数组是零索引的。

## **切片法**

slice()方法从初始数组中分割出一个元素，并返回一个包含该元素的新数组。必须注意，slice()方法不会从初始数组中移除任何元素。

```

<html>
<body>
<script type = "text/javascript">
var array = ["Rock", "Pop", "Jazz", "Blues", "Metal"];
document.write("array.slice( 1, 2) : " + array.slice( 1, 2) );
document.write("<br />array.slice( 1, 3) : " + array.slice( 1, 3) );
</script>
</body>
</html>

```

以下代码的输出如下:

array.slice( 1，2):弹出

array.slice( 1，3):流行音乐、爵士乐

JavaScript 中这个数组方法的最后一个方法是，

## **ForEach 方法**

此方法为数组中的每个元素调用函数。

```

<script>
function funct() {
// Initial array
const items = [2, 18, 28];
const copy = [];
items.forEach(function(item){
copy.push(item*item);
});
document.write(copy);
}
funct();
</script>

```

在示例中，我们计算数组中每个元素的平方。

输出如下所示:

Four million three hundred and twenty-four thousand seven hundred and eighty-four

至此，我们结束了这篇关于“JavaScript 中的数组方法”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。

****