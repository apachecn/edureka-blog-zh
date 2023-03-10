# 关于 AngularJs 中的 MVC，您需要知道的是

> 原文：<https://www.edureka.co/blog/mvc-in-angularjs/>

MVC 的概念是一个伟大的概念，它的基本思想是拥有三个独立的实体，永远不要把它们混在一起。在本文中，我们将按照以下顺序理解 AngularJS 中的 MVC 是什么:

*   [什么是 MVC？](#what)
*   [MVC 在 AngularJS 中的工作](#working)

## **AngularJS 中的 MVC 是什么？**

AngularJs 支持 MVC 模式。MVC 即模型视图控制器是一种用于开发 web 应用程序的软件设计模式。它由以下部分组成:

*   **模型—**模式的最低层，模型由一个数据库组成。管理应用程序数据的责任交给了模型。简单来说，它管理应用程序的数据和逻辑。

*   **视图–**视图负责向用户显示部分数据或全部数据。为了显示来自控制器的数据，我们可以将角度表达式添加到视图中，这将协调模型和视图的任何修改。简单来说，视图就是用户界面，它展示了输出。

*   **控制器–**控制器提供对模型和视图的控制，即它控制数据的检索以及显示。更简单地说，控制器管理模型和视图部分之间的交互。

![MVC In AngularJs](img/9c4e64f5e47e960c7de43ebb65c28a41.png)

MVC 架构模式在软件工程中已经被高效地使用了很长时间。

## **在 AgularJS 中使用 MVC**

MVC 可以通过使用 JavaScript 和 HTML 在 AngularJs 中实现。模型部分可以通过 [HTML](https://www.edureka.co/blog/what-is-html/) 实现，而模型和控制器部分可以通过 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 实现。

下面的例子展示了 MVC 的工作方式:

`<!doctype html>`

`<html ng-app>`

`<head>`

`<title>Angular MVC Architecture </title>`

`<script src=”lib/Angular/angular.min.js”></script>`

`</head>`

`<body>`

`<div ng-controller = “address”>`

`<h1>{ {Person.Name} }</h1>`

`</div>`

`<script type=”text/javascript”>`

`function address($scope){`

`$scope.Person= {`

`'Name'      :   'Ari Jon ',`

`'Address'  :   'Park, NYC',`

`}`

`}`

`</script>`

`</body>`

`</html>`

输出的将是人名，即 **Ari Jon。**

至此，我们结束了 AngularJS 的这篇 MVC 文章。MVC 架构在 angular 中的实现是通过本文提到的方法来完成的。这种架构使得职责分离成为可能。模型由应用程序数据组成，而视图代表布局或用户界面。控制器充当视图和模型之间的连接。如需了解更多信息，请立即查看此[全栈开发人员课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

Edureka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。随着 Angular 框架的广泛采用，应用程序的性能管理是由社区驱动的，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。