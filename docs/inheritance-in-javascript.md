# 关于 JavaScript 中的继承，你需要知道的一切

> 原文：<https://www.edureka.co/blog/inheritance-in-javascript/>

继承是面向对象编程中的一个重要概念。在传统继承中，基类的方法被复制到派生类中。所以让我们以下面的方式来理解 JavaScript 中的继承:

*   [JavaScript 中的继承](#inheritance)
*   [原型继承](#prototypal)
*   [代码](#code)

## **JavaScript 中的继承**

在 JavaScript 中，通过使用原型对象来支持继承。有人称之为“原型遗传”，有人称之为“行为委托”。

## **![Inheritance in JavaScript](img/1a439bdd1232bc3090d2f1112860b977.png)**

## **原型遗传(行为委托模式)**

*   v1 和 v2 链接到vehicle . prototype，因为它是使用*new*关键字创建的。

*   同样， c1 和 c2 链接到 Car.prototype 和car . prototype链接到vehicle . prototype。

*   在 JavaScript 中，当我们创建对象时，它并不复制属性或行为，而是创建一个链接。在类扩展的情况下，也会创建类似的链接。

*   与传统的非 js 继承相比，所有的箭头都指向相反的方向，因为这是一个行为委托链接。这些环节被称为原型链。

*   这种模式被称为 *行为委托模式* 也就是 JavaScript 中俗称的 ***原型继承*** 。

## **代码:JavaScript 中的继承**

`!DOCTYPE html>`

`<html>`

`<body>`

`<h1>Demo: Inheritance</h1>`

`<script>    `

`function Person(firstName, lastName) {`

`this.FirstName = firstName || "unknown";`

`this.LastName = lastName || "unknown";            `

`}`

`Person.prototype.getFullName = function () {`

`return this.FirstName + " " + this.LastName;`

`}`

`function Student(firstName, lastName, schoolName, grade)`

`{`

`Person.call(this, firstName, lastName);`

`this.SchoolName = schoolName || "unknown";`

`this.Grade = grade || 0;`

`}`

`//Student.prototype = Person.prototype;`

`Student.prototype = new Person();`

`Student.prototype.constructor = Student;`

`var std = new Student("James","Bond", "XYZ", 10);`

`alert(std.getFullName()); // James Bond`

`alert(std instanceof Student); // true`

`alert(std instanceof Person); // true`

`</script>`

`</body>`

`</html>`

这段代码将产生以下输出。

**输出:**

![Output-1](img/eb798f0686a9362af693746d65ff9023.png) ![Output-2](img/7d9608189db02c656ead6bd698fa9843.png)

到此，我们来结束这篇文章。欲了解更多信息，您可以参考以下博客:

*   [角度教程](https://www.edureka.co/blog/angular-tutorial/)
*   [角度入门](https://www.edureka.co/blog/what-is-angular-getting-started-with-angular/)
*   [AngularJS 真的是基于 MVC 架构吗？](https://www.edureka.co/blog/angular-mvc-architecture/)
*   [学习如何使用 Angular 中的指令](https://www.edureka.co/blog/angular-directive/)

*查看 Edureka 提供的 **[角度训练](https://www.edureka.co/angular-training)** ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。随着 Angular 框架的广泛采用，应用程序的性能管理是由社区驱动的，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。*

*有问题吗？请在这篇文章的评论部分提到它，我们会给你回复。*