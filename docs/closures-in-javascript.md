# JavaScript 中的闭包是什么&它们是如何工作的？

> 原文：<https://www.edureka.co/blog/closures-in-javascript/>

JavaScript 是一种面向函数的语言，给用户很大的自由。你可以动态地创建一个函数，将它复制到另一个变量中，或者作为一个参数传递给另一个函数，然后在不同的地方调用。JavaScript 中的闭包是在每次创建函数时创建的。在本文中，我们将按以下顺序理解闭包:

*   [JavaScript 中闭包的介绍](#introduction)
*   [实用瓶盖](#practical)
*   [范围链](#scope)
*   [循环内的闭合](#closure)

## **JavaScript 中闭包的介绍**

闭包是一个[函数](https://www.edureka.co/blog/javascript-functions/)与对其周围状态(即词法环境)的引用捆绑在一起的组合。换句话说，闭包提供了从内部函数到外部函数范围的访问。

![coder - closures in javascript - edureka](img/ac47dc84654a17950c4c730389795e67.png)

大多数开发人员有意识或无意识地在 JavaScript 中使用闭包。当使用它们时，它提供了对代码更好的控制。同样，这也是在任何 JavaScript 面试中最常被问到的问题。

**举例:**

```
function foo()
{
var x = 10;
function inner(){
return x;
}
return inner;
}
var get_func_inner = foo();

console.log(get_func_inner());
console.log(get_func_inner());
console.log(get_func_inner());
```

**输出:**

10 10 10

这里，您可以通过函数 inner()访问函数 foo()中定义的[变量](https://www.edureka.co/blog/javascript-variable/) x，因为后者在执行封闭函数时保留了封闭函数的作用域链。因此，内部函数通过它的作用域链知道 x 的值。这就是在 JavaScript 中使用闭包的方式。

## **实用瓶盖**

闭包允许您将词法环境与操作该数据的函数相关联。这与[面向对象编程](https://www.edureka.co/blog/javascript-object/)有明显的相似之处，在面向对象编程中，对象允许我们将对象的属性与一个或多个方法相关联。

因此，您可以在任何通常只使用一个方法的地方使用闭包。

**举例:**

```
function makeSizer(size) {
return function() {
document.body.style.fontSize = size + 'px';
};
}

var size12 = makeSizer(12);
var size14 = makeSizer(14);
var size16 = makeSizer(16);
```

上面的例子通常以回调的形式出现:一个响应事件而执行的函数。

## **范围链**

JavaScript 中的闭包有三个作用域，比如:

*   局部范围
*   外部功能范围
*   全球范围

一个常见的错误是没有意识到，在外部函数本身是嵌套函数的情况下，对外部函数范围的访问包括外部函数的封闭范围，这实际上创建了一个函数范围链。

```
// global scope
var x = 10;
function sum(a){
return function(b){
return function(c){
// outer functions scope
return function(d){
// local scope
return a + b + c + d + x;
}
}
}
}

console.log(sum(1)(2)(3)(4)); // log 20
```

也可以不用匿名函数来编写:

```
// global scope
var x = 10;
function sum(a){
return function sum2(b){
return function sum3(c){
// outer functions scope
return function sum4(d){
// local scope
return a + b + c + d + x;
}
}
}
}

var s = sum(1);
var s1 = s(2);
var s2 = s1(3);
var s3 = s2(4);
console.log(s3) //log 20
```

在上面的例子中，有一系列嵌套的函数，它们都可以访问函数的外部范围。因此，可以说闭包可以访问声明它们的所有外部函数范围。查看[网络开发者在线课程](https://www.edureka.co/masters-program/full-stack-developer-training)，了解更多关于 Javascript 函数的知识。

## **循环内的闭合**

您可以在 JavaScript 中使用闭包在一个[数组](https://www.edureka.co/blog/javascript-array/)的每个索引处存储一个匿名函数。让我们举一个例子，看看闭包是如何在循环中使用的。

**举例:**

```
function outer()
{
var arr = [];
var i;
for (i = 0; i < 3; i++)
{
// storing anonymus function
arr[i] = function () { return i; }
}

// returning the array.
return arr;
}

var get_arr = outer();

console.log(get_arr[0]());
console.log(get_arr[1]());
console.log(get_arr[2]());
```

**输出:**

3 3 3 3

说到这里，我们的文章就到此为止了。我希望您理解了 JavaScript 中的闭包是如何工作的，以及如何使用它们来更好地控制代码。

*既然你已经了解了 JavaScript 中的闭包，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 中的闭包”的评论部分提到它，我们会回复您。*