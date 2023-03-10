# JavaScript 中的数组排序:JavaScript 中关于数组排序的所有内容

> 原文：<https://www.edureka.co/blog/array-sort-in-javascript/>

排序使您能够以所需的形式排列数据。这意味着访问和处理这些数据变得更加容易。在这篇关于“JavaScript 中的数组排序”的文章中，我们将探索 JavaScript 中不同的数据排序方式。我们将关注以下几点:

*   [JavaScript 中的排序方法](#SortMethodInJavaScript)
*   [排序数值](#SortingNumericalValues)
*   [按升序排列数组](#SortingArrayInAscendingOrder)
*   [按降序排列数组](#SortingArrayInDescendingOrder)
*   [排序对象数组](#SortingArrayOfObjects)

让我们从 JavaScript 文章中数组排序的第一个主题开始

## **JavaScript 文章中的数组排序**

## **JavaScript 中的排序方法**

sort()方法相应地对数组中的元素进行排序，并将排序后的数组作为输出返回给用户。内置方法将数组中的每个元素转换成一个*字符串*，并按照 Unicode 码位顺序对它们进行比较。不过先从[安装](https://developer.mozilla.org/en-US/docs/Web/JavaScript)开始。

下面的代码遵循最基本的数组排序:

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">  
</head>
<body>
<script>
var music = ["Pop", "Rock", "Jazz", "Blues", "Metal"];
var sorted = music.sort();
document.write(music + "<br>");  
</script>
</body>
</html>

```

**输出:**

蓝调、爵士、金属、流行、摇滚

现在让我们继续“JavaScript 中的数组排序”,看看如何对数值进行排序，

## **排序数值**

将数字作为字符串排序会产生错误的结果。

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">  
</head>
<body>
<script>
var music = ["Pop", "Rock", "Jazz", "Blues", "Metal"];
var sorted = music.sort();
document.write(music + "<br>");  
</script>
</body>
</html>

```

**输出:**

10,100,34,45,69,87

结果似乎绝对不准确。这是因为 sort()方法将数值数组转换为字符串。这个问题可以通过使用*比较*功能来解决。

该函数的语法如下:

```
array.sort([compareFunction])
```

compare 函数根据不同的属性和不同的顺序对数组中的元素进行排序。sort()函数比较两个值，并将值发送给 compare 函数。比较功能遵循以下给出的测试案例:

*   如果两个值(a & b)的比较结果是 ***负*** ，则 a 排在 b 之前
*   如果结果显示为 ***正*** ，则 b 排在 a 之前
*   如果结果是 **0** ，那么**T3【无变化】出现在值 a & b 的排序顺序中**

在 JavaScript 的数组排序中，我们将按升序对数据进行排序，

## **按升序排列数组**

下面的示例演示了按升序对数组进行排序的过程。

```
<!DOCTYPE html>
<html>
<body>
<script>
var num = [45, 34, 69, 87, 100, 10];
num.sort(); // Sorts numbers array
document.write(num);
</script>
</body>
</html>                            

```

**输出:**

3,18,25,28,29,69

进一步让我们检查如何按降序排列数组

## **按降序排列数组**

可以按以下方式按降序对数组进行排序:

```
<!DOCTYPE html>
<html>
<body>
<script>
var num = [3, 25, 18, 28, 69, 29];
//Sorting an array using compare function
num.sort(function(a, b) {
return a - b;
});
document.write(num);
</script>
</body>
</html> 

```

**输出:**

69,29,28,25,18,3

我们甚至可以对对象的数组进行排序，让我们看看如何去做，

## **排序对象数组**

compare 函数可用于以高效的方式对对象数组进行排序。

```
<!DOCTYPE html>
<html>
<body>
<script>
var people = [
{ name: "Jeremy"},
{ name: "Ari" },
{ name: "Jonathan"},
{ name: "Alec"},
{ name: "Stephen"}
];
//Sort by name
people.sort(function(a, b) {
var x = a.name.toLowerCase(); // ignore upper and lowercase
var y = b.name.toLowerCase(); // ignore upper and lowercase
if(x < y) {
return -1;
}
if(x > y) {
return 1;
}
//names should be equal
return 0;
});    
//Loop through all the elements in the array 
for(var i in people)  {  
//Loop through all the properties in the object  
for(var prop in people[i]) {  
document.write(prop + ": " + people[i][prop] + "<br>"); 
}
document.write("<hr>");
}

```

**输出:**

姓名:亚历克

姓名:Ari

姓名:杰里米

姓名:乔纳森

姓名:斯蒂芬

文章中解释的方法细致地证明了这样一个事实，即与比较函数相关联的排序函数在脚本语言中起着至关重要的作用。要了解更多信息，请立即参加[全栈开发人员课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

至此，我们结束了这篇关于“JavaScript 中的数组排序”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。