# 什么是 JavaScript 类，如何使用？

> 原文：<https://www.edureka.co/blog/javascript-classes/>

在面向对象编程中，类是用于创建对象的可扩展程序代码模板。JavaScript 类主要可以被认为是 JavaScript 现有的基于原型的继承的语法糖。在本文中，我们将深入探讨 JavaScript 类，并学习如何按以下顺序使用它们:

*   什么是 JavaScript 类？
*   [如何使用 JavaScript 类？](#howtouse)
    *   [定义一个类](#class)
    *   [定义方法](#method)
    *   [扩展一个类](#extend)

## 什么是 JavaScript 类？

在 JavaScript 中，类是一种函数类型，用 class 关键字声明。您需要使用函数表达式语法来初始化函数，使用类表达式语法来初始化类。

```

// Initializing a function with a function expression
const a = function() {}

```

```

// Initializing a class with a class expression
const b = class {}

```

在 JavaScript 中，我们不使用关键字函数来初始化它，而是使用关键字类。此外，属性是在 constructor()方法中分配的。

## **如何使用 JavaScript 类？**

用[函数](https://www.edureka.co/blog/javascript-functions/)和 class 声明的代码都返回一个函数[[Prototype]]。有了原型，任何函数都可以使用 new 关键字成为构造函数实例。例如:

```

const a = class {}

// Initialize a constructor from a class
const constructorFromClass = new a();

console.log(constructorFromClass);

```

**输出:**

```
a {}
constructor: class
```

现在，在 JavaScript 中有三种不同的使用 class 的方法。让我们通过一个例子来深入了解每种方法的细节。

## **定义一个类**

一个构造函数用多个参数初始化，这些参数被赋值为*‘this’*的属性，引用函数本身。按照惯例，标识符的首字母大写。要了解更多信息，请立即参加[全栈开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

```

// Initializing a constructor function
function employee(name, empid) {
this.name = name;
this.empid = empid;
}

```

现在，如果我们把它翻译成类语法，你会看到结构非常相似。

```

// Initializing a class definition
class employee{
constructor(name, empid) {
this.name = name;
this.empid = empid;
}
}

```

我们可以说 class 关键字以一种更直接的方式进行交流。初始化语法的唯一区别是使用 class 关键字而不是 function。此外，它在 constructor()方法中分配属性。

## **定义方法**

构造函数的另一个常见做法是将[方法](https://www.edureka.co/blog/javascript-array/)直接分配给原型，而不是在初始化时分配。我们将举一个例子，看看它是如何工作的:

```

function employee(name, empid) {
this.name = name;
this.empid = empid;
}

// Adding a method to the constructor
employee.prototype.greet = function() {
return `${this.name} says hello.`;
}

```

当您使用 class 编写相同的代码时，它会被简化并直接添加方法。

```

class employee {
constructor(name, empid) {
this.name = name;
this.empid = empid;
}

// Adding a method to the constructor
greet() {
return `${this.name} says hello.`;
}
}

```

虽然类允许更简单和简洁的语法，但有时你可能不得不在过程的清晰性上妥协。

## **扩展一个类**

构造函数和类的优点是它们可以扩展到基于父对象的新对象蓝图中。这有助于防止相似但需要一些额外的或更具体的特性的对象的代码重复。

可以使用 call()方法从父类创建新的构造函数。例如:

```

// Creating a new constructor from the parent
function info(name, empid, salary) {
// Chain constructor with call
employee.call(this, name, empid);

this.salary = salary;
}

```

现在，当我们使用 class 编写相同的代码时，使用 super 关键字代替 call 来访问父函数。

```

// Creating a new class from the parent
class info extends employee {
constructor(name, empid, salary) {
// Chain constructor with super
super(name, empid);

// Add a new property
this.salary = salary;
}
}

```

类为你提供了一种更简洁的创建[对象](https://www.edureka.co/blog/javascript-object/)蓝图的方式，构造函数以一种更具体的方式描述了正在发生的事情。

说到这里，我们的文章就到此为止了。我希望你明白如何使用 JavaScript 类。

*既然你已经了解了 JavaScript 类，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 类”的评论部分提到它，我们会给你回复。*