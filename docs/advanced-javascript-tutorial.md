# 高级 JavaScript 教程:高级方面的最佳指南

> 原文：<https://www.edureka.co/blog/advanced-javascript-tutorial/>

网络的崛起已经把 JavaScript 的带到了它从未想到的地方。它已经成为当今世界最重要的语言之一。在我们之前的 [JavaScript 教程](https://www.edureka.co/blog/javascript-tutorial/)中，我们讨论了该语言的所有基础和基本原理。在这篇高级 JavaScript 教程中，我们将按以下顺序学习编程语言的一些高级方面:

*   [JavaScript 概述](#overview)
*   [高级功能操作](#functions)
*   [JavaScript 名称空间](#namespace)
*   [原型](#prototypes)
*   [错误处理](#error)
*   [JavaScript 中的模块](#module)
*   [链接 JavaScript 方法](#chaining)
*   [发电机](#generators)

## **JavaScript 概述**

[JavaScript](https://www.edureka.co/blog/what-is-javascript/) 是一种高级的、解释性的编程语言，用于使网页更具交互性。这是一个非常强大的客户端脚本语言，使你的网页更加生动和互动。

![Overview of JavaScript](img/862aa40faa227e3fc4931d8e80a54032.png)

它是一种编程语言，可以帮助你在网页上实现复杂而漂亮的设计。如果你想让你的网页看起来活灵活现，不只是呆呆地看着你，JavaScript 是必须的。

### **JavaScript 的特性:**

![features of javascript - advanced javascript tutorial- edureka](img/572e98527e74282ea9c099f24146ea8f.png)

*   它是一种脚本语言，与 Java 无关。最初命名为  **摩卡**，后改为**LiveScript**最后命名为 **JavaScript** 。

*   JavaScript 是一种  **基于对象的** 编程语言，支持多态、封装和继承。

*   你不仅可以在**浏览器**中运行 JavaScript ，还可以在**服务器**和任何有 JavaScript 引擎的设备上运行。

在之前的 JavaScript 教程中讨论的一些基础知识和基本原理是:

*   [变量](https://www.edureka.co/blog/javascript-tutorial/#variables)
*   [常数](https://www.edureka.co/blog/javascript-tutorial/#constants)
*   [数据类型](https://www.edureka.co/blog/javascript-tutorial/#datatypes)
*   [物体](https://www.edureka.co/blog/javascript-tutorial/#objects)
*   [数组](https://www.edureka.co/blog/javascript-tutorial/#arrays)
*   [功能](https://www.edureka.co/blog/javascript-tutorial/#functions)
*   [条件语句](https://www.edureka.co/blog/javascript-tutorial/#conditionalstatements)
*   [循环](https://www.edureka.co/blog/javascript-tutorial/#loops)
*   [开关盒](https://www.edureka.co/blog/javascript-tutorial/#switchcase)

在这篇高级 JavaScript 教程中，我们将深入探讨 JavaScript 的高级方面。

## **高级功能操作**

[功能](https://www.edureka.co/blog/javascript-functions/)是一个有组织的、可重用的代码块，用于执行单个相关的动作。一些高级功能包括:

*   **递归**
*   **关闭**
*   **【新功能】**
*   **箭头功能**
*   **剩余参数&传播算子**
*   **全局对象**
*   **功能对象**
*   **设置超时&设置间隔**
*   **功能绑定**

### **递归**

[递归](https://www.edureka.co/blog/recursion-in-python/)是一种编程模式，在一个任务可以自然地分成几个同类但更简单的任务的情况下很有帮助。或者当一个任务可以简化为一个简单的动作和同一任务的一个更简单的变体时。

![recursion - advanced javascript tutorial - edureka](img/f9c182e42dc3a1885472510726804ae9.png)

在解决任务的过程中，一个函数可以调用许多其他函数。这种情况的一部分是当一个函数调用它自己的时候。因此，它被称为递归。

**举例:**

```
function pow(x, n) {
if (n == 1) {
return x;
} else {
return x * pow(x, n - 1);
}
}

alert( pow(2, 4) ); // 16
```

在上面的例子中，递归函数简化了任务并调用自身。

### **关闭**

JavaScript 是一种面向函数的语言。你可以动态地创建一个函数，复制到另一个变量或者作为参数传递给另一个函数，然后从一个完全不同的地方调用。

一个[闭包](https://www.edureka.co/blog/closures-in-javascript/)是一个记住它的外部变量并能访问它们的函数。在某些语言中，这是不可能的，或者应该用特殊的方式编写一个函数来实现它。但是在 JavaScript 中，所有的函数自然都是闭包。

**举例:**

```
var add = (function () {
var counter = 0;
return function () {counter += 1; return counter}
})();

add();
add();

// the counter is now 2
```

### **【新功能】**

“new function”语法是创建函数的另一种方式。很少使用，但有时别无选择。

**语法:**

```
let func = new Function ([arg1, arg2, ...argN], functionBody);
```

该函数由 arg1…argN 参数和给定的 functionBody 组成。

**举例:**

```
let sum = new Function('a', 'b', 'return a + b');
alert( sum(1, 2) ); // 3
```

这里，函数是从运行时传递的字符串创建的。您需要在脚本中编写功能代码。但是“新函数”允许将任何字符串转换成函数。

### **箭头功能**

箭头函数是匿名的，它改变了函数绑定的方式。它使我们的代码更加简洁，简化了函数作用域和这个关键字。

![](img/35d9bdd8b0715716f3f50beee4fa2462.png)

但是箭头函数不仅仅是写小东西的简写。他们也有一些非常具体和有用的功能。JavaScript 包括需要编写一个在其他地方执行的小函数的情况，例如:

*   **arr . forEach(func)**–func 由 forEach 对每个数组项执行。
*   **setTimeout(func)**–func 由内置调度程序执行。

而在这样的函数中，我们通常不想离开当前的上下文。这就是箭头函数派上用场的地方。

**举例:**

```
//Arrow Function:
hello = () =&gt; {
document.getElementById("demo").innerHTML += this;
}
//The window object calls the function:
window.addEventListener("load", hello);
//A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);
```

### **剩余参数&传播算子**

许多 JavaScript 内置函数支持任意数量的参数，例如:

*   **Math.max(arg1，arg2，…，argN)**–返回最大的参数。

*   **Object.assign(dest，src1，…，srcN)**–从 src1 复制属性..n 到目的地

**Rest 参数**是处理函数参数的一种改进方式，允许我们更容易地处理函数中作为参数的各种输入。rest 参数语法允许我们将不定数量的参数表示为一个数组。

**举例:**

```
// es6 rest parameter
function fun(...input){
let sum = 0;
for(let i of input){
sum+=i;
}
return sum;
}
console.log(fun(1,2)); //3
console.log(fun(1,2,4)); //4
console.log(fun(1,2,4,6)); //13
```

**扩展运算符**允许 iterable 在应该有 0+个参数的地方扩展。它主要用于需要 1 个以上值的变量数组。它允许我们从数组中获取参数列表。

**举例:**

```
// spread operator doing the concat job
let arr = [1,2,3];
let arr2 = [4,5,6];

arr = [...arr,...arr2];
console.log(arr); // [ 1, 2, 3, 4, 5,6 ]
```

### **全局对象**

全局对象提供了在任何地方都可用的变量和函数。默认情况下，那些内置于语言或环境中的。最近，globalThis 被添加到语言中，作为一个全局对象的标准化名称，应该在所有环境中都得到支持。

可以直接访问全局对象的所有属性:

```
alert("Hello");
// is the same as
window.alert("Hello");
```

### **功能对象**

在 JavaScript 中，函数是对象。不同的属性包括:

*   **名称**–功能名称。通常取自函数定义，但如果没有，JavaScript 会尝试从上下文中猜测(例如赋值)。

*   **length**–函数定义中的参数个数。其余参数不计算在内。

如果函数被声明为函数表达式，并且它带有名称，那么它被称为命名函数表达式。该名称可以在内部引用自身，用于递归调用等。

**举例:**

```
function sayHi() {
alert("Hi");
}

alert(sayHi.name); // sayHi
function f2(a, b) {}
function many(a, b, ...more) {}
alert(f2.length); // 2
alert(many.length); // 2
```

### **设置超时&设置间隔**

如果你想在以后的某个时间执行某个功能，这就叫做调度呼叫。有两种方法:

![](img/12573d7fee925c96e9c3eda29a4a295c.png)

*   **setTimeout** 允许我们在间隔时间后运行一次功能。

*   **setInterval** 允许我们重复运行一个函数，在该时间间隔之后开始，然后在该间隔连续重复。

这些方法不是 JavaScript 规范的一部分。但是大多数环境都有内部调度程序并提供这些方法。

**设置超时**

**语法:**

```
let timerId = setTimeout(func|code, [delay], [arg1], [arg2], ...)
```

**举例:**

```
function sayHi() {
alert('Hello');
}

setTimeout(sayHi, 1000);
```

**设定间隔**

**语法:**

```
let timerId = setInterval(func|code, [delay], [arg1], [arg2], ...)
```

**举例:**

[/JavaScript]//间隔 2 秒重复 let time rid = setInterval(()=>alert(' tick ')，2000)；

//5 秒后停止 setTimeout(()=>{ clear interval(time rid)；alert(“停止”)；}, 5000);[/javascript]

### **功能绑定**

当将对象方法作为回调函数传递时，例如传递给 setTimeout，有一个已知的问题是“丢失这个”。函数提供了一个内置的方法绑定来修复这个问题。

**语法:**

```
// more complex syntax will come a little later
let boundFunc = func.bind(context);
```

func.bind(context)的结果是一个特殊的类似函数的“外来对象”，可以作为函数调用，并透明地将调用传递给 func 设置 this=context。

**举例:**

```
let user = {
firstName: "John"
};

function func() {
alert(this.firstName);
}

let funcUser = func.bind(user);
funcUser(); // John
```

这些是使用函数进行高级工作的一些例子。现在，让我们继续学习这个高级 JavaScript 教程，了解名称空间。

## **JavaScript 名称空间**

JavaScript 不支持名称空间。但是名称空间很重要，因为它们有助于减少添加到应用程序全局范围的变量、对象和函数的标识符数量。JavaScript 是一种灵活的语言，有很多方法可以绕过这个限制，实现自己的名称空间。

那么，我们为什么需要名称空间呢？在 JavaScript 中，代码共享一个全局名称空间，这个名称空间只是一个全局对象，它将所有全局变量和函数作为属性保存。在浏览器中，这是一个窗口对象，如果对象太多，它会污染全局范围。

**举例:**

```
let num = 5;
var obj = {};
var str = "Hello Edureka!";
function sum(x, y){
total = x + y;
return total;
}
numr = sum(3,3);
```

在上面的例子中，标识符 num、obj、str 和 sum 是使用 var 和 let 关键字正确声明的。但是函数作用域变量 total 缺少一个 var，numr 是 num 的拼写错误。这里，JavaScript 将 total 和 numr 都添加到全局名称空间中，这很可能不是您想要的。

## **高级 JavaScript 教程:原型**

在 JavaScript 中，对象有一个特殊的隐藏属性，称为 Prototype，它描述空值或引用另一个对象。现在，这个物体被称为原型。在这篇高级 JavaScript 教程中，我们将讨论 prototype 的两个重要特性:

*   **原型遗传**
*   **原型方法，没有 __proto__ 的对象**

### **原型遗传**

在编程中，我们经常想要获取一些东西并对其进行扩展。假设您有一个用户对象及其属性和方法，并且您想将 admin 和 guest 作为它的稍微修改的变体。在这里，您希望重用用户中的内容，而不是复制它的方法，只是在它的基础上构建一个新的对象。

原型[继承](https://www.edureka.co/blog/inheritance-in-javascript/)是在这方面有所帮助的语言特性。

**举例:**

```
let pet = {
eats: true
};
let dog = {
jumps: true
};

dog.__proto__ = pet; // (*)

// we can find both properties in dog now:
alert( dog.eats ); // true (**)
alert( dog.jumps ); // true
```

在这里，如果您在 dog 中寻找一个属性，并且它丢失了，JavaScript 会自动从 pet 中获取它。

### **原型方法，没有 __proto__ 的对象**

在原型继承中，我们使用 __proto__ 但这是一个过时的方法。在这个高级 JavaScript 教程中，我们将看看建立原型的现代方法:

*   **Object.create(proto[，descriptors])**–它用给定的 proto as [[Prototype]]和可选的属性描述符创建一个空对象。

*   **object . getprototypeof(obj)**–这将返回 obj 的[[Prototype]]。

*   **Object.setPrototypeOf(obj，proto)**–该方法将 obj 的[[Prototype]]设置为 proto。

**举例:**

```
let pet = {
eats: true
};

// create a new object with pet as a prototype
let dog = Object.create(pet);

alert(dog.eats); // true

alert(Object.getPrototypeOf(dog) === pet); // true

Object.setPrototypeOf(dog, {}); // change the prototype of dog to {}
```

现在让我们继续这个高级 JavaScript 教程，学习错误处理。

## **错误处理**

无论你多么擅长编程，你的脚本都可能包含错误。它们可能因为我们的错误、意外的用户输入、错误的服务器响应或任何其他原因而发生。

通常，如果出现错误，脚本会立即停止，并将其打印到控制台。现在，有一个语法结构 [**试试..捕捉**](https://www.edureka.co/blog/javascript-try-catch/) 允许捕捉错误，而不是死亡，做一些更合理的事情。

### **该试试了..Catch 语法**

尝试..catch 构造有两个主要块:

*   **试试**
*   **接住**

```
try {

// code...

} catch (err) {

// error handling

}
```

*   首先执行 **try {…}** 中的代码。

*   如果没有错误，那么 **catch(err)** 被忽略。执行到达 try 的结尾并继续，跳过 catch。

*   如果出现错误，try 执行将停止，控制将转到 catch(err)的开头。

**举例:**

```
try {
alert('Begin try runs'); // (1) &lt;--
// ...no errors here
alert('End try runs'); // (2) &lt;--
} catch(err) {
alert('Catch is ignored as there are no errors'); // (3)
}

```

这个高级 JavaScript 教程的下一个方面是关于 JavaScript 中的模块。

## **JavaScript 中的模块**

模块是一段自包含的代码，它将语义相关的变量和函数组合在一起。模块不是 JavaScript 中的内置结构。但是 JavaScript 模块模式提供了一种创建模块的方法，这些模块具有明确定义的接口，并向模块的客户端公开。

模块的一个重要优点是，您可以在任何需要的时候修改内部功能，而不会影响程序的其余部分。这促进了封装和信息隐藏。要在 JavaScript 中定义一个模块，可以通过创建一个匿名即时函数来利用匿名闭包。

**举例:**

```
var MODULE = (function () {
var module = {};
var privateVariable = 7;

function privateMethod() {
// ..
}

module.moduleProperty = 1;
module.moduleMethod = function () {
// ...
};
return module;
}());
```

现在让我们继续这个高级 JavaScript 教程，学习链接 JavaScript 方法。

## **链接 JavaScript 方法**

JavaScript 允许您在一个表达式中对一个对象调用多个[方法](https://www.edureka.co/blog/javascript-methods/)。为了调用多个方法，我们有链接。链接是用点将方法调用串在一起的过程。

**语法:**

```
object.method1().method2().method3();
```

构建链时，对象只命名一次，然后对它调用多个方法。为此，您的方法必须返回它们所操作的对象。每个方法都作用于对象，当它完成时，它返回给下一个调用。

**举例:**

```
account.number("11324567").setBalance(15000).applyCredit(200);
```

在上面的示例中，您将学习设置一个银行帐户，该帐户由帐号、余额和信用额度组成。

JavaScript 中的链接可以提高性能和可读性。这里，jQuery 库大量使用了链接。让我们举一个例子，看看如何链接 jQuery 选择器方法:

`$("#myDiv").removeClass("off").addClass("on").css("background": "red");`

现在让我们继续学习这个高级 JavaScript 教程，了解什么是生成器。

## **发电机**

生成器是一类特殊的函数，它简化了编写迭代器的任务。因此，该函数产生一系列结果而不是单个值，并生成一系列值。

因此，在 JavaScript 中，生成器是一个返回对象的函数，您可以在该对象上调用 next()。因此，每次调用 next()都会返回一个 shape 对象。

**举例:**

```
{
value: Any,
done: true|false
}
```

value 属性将包含值。done 属性为 true 或 false。当 done 为真时，生成器停止，不再生成任何值。

以上是 JavaScript 涉及的一些高级技术和方法。至此，我们已经结束了高级 JavaScript 教程。我希望你理解了高级 JavaScript 的概念。

*查看由 Edureka 提供的[全栈网络开发者硕士项目](https://www.edureka.co/masters-program/full-stack-developer-training)。* *有问题吗？请在“高级 JavaScript 教程”的评论部分提到它，我们会回复您。*