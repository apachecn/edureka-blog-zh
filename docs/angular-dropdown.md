# 如何使用 Angular 创建下拉框？

> 原文：<https://www.edureka.co/blog/angular-dropdown/>

学习和完善如何使用 Angular 完成某些日常任务可以快速提升你的职业生涯，尤其是如果你是网络开发职业的新手。在这篇文章中，我们将讨论这样一个任务，一个开发人员必须做成千上万次:创建一个不起眼的下拉框。本博客将涵盖以下主题:

*   [什么是棱角分明？](#what-is-angular)
*   什么是下拉框？
*   使用 Angular 创建下拉框。

## **什么是棱角分明？**

![Angular Logo - Angular MVC - edureka](img/7906932a952cda9058fcecf024d5dcc6.png)好吧，如果你正在阅读一篇关于如何使用 Angular 制作下拉框的博客，可以假设你已经对 Angular 有了一个大致的概念。对于那些不了解这个博客并且由于互联网的突发奇想而偶然发现它的人来说， [Angular](https://www.edureka.co/blog/angular-tutorial/) 是一个前端开发框架。它由科技巨头谷歌开发和维护。它提供了一种模块化的方式来开发 Gmail、PayPal 和 Lego 等单页面网络应用程序。使用 Angular 构建的应用程序实现了模型-视图-视图-模型方法。

## 什么是下拉框？

下拉框是一种显示选项数组的简洁方法，因为在用户激活下拉框之前，最初只显示一个选项。要在网页上添加一个下拉框，你可以使用一个*选择*元素或者一个*列表项*。select 元素中的第一个<选项>标签需要将 selected 选项设置为 selected 的值。这里有一小段代码向您展示我的意思。

```
<select name="demo" id="#">
<option selected="selected" value="one">Option 1</option>
<option value="two">Option 2</option>
<option value="three">Option 3</option>
</select>
```

当然，上面的代码需要特定的 javascript 来实现预期的行为，但是下拉菜单的基本框架是一样的。现在让我们看看如何在 Angular 中实现这一点。

## **使用角度**的下拉框

老实说，在 angular 中演示所有可能实现下拉框的方法是相当令人畏惧的。每个开发人员的大脑都以自己独特的方式处理逻辑，在我的职业生涯中，我见过一些疯狂的下拉菜单。我将谦虚地向你们展示一个相当基本的下拉菜单方法。查看此[全栈开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)以了解更多关于 Angular 的信息。

### **方法 1:使用 ng 选项制作下拉列表**

您可以使用 ng-options [指令](https://www.edureka.co/blog/angular-directive/)从一个数组或一个项目列表中创建一个下拉菜单。

```
<div ng-app="demo" ng-controller="myCtrl">

<select ng-model="selectedName" ng-options="x for x in names">
</select>

</div>

<script>

var app = angular.module('demo', []);
app.controller('myCtrl', function($scope) {
$scope.names = ["Demavand", "Pradeep", "Ashutosh"];
});
</script>

```

### **方法 2:使用 ng-repeat 制作下拉列表**

Angular 是一个通用的[框架](https://www.edureka.co/blog/top-10-javascript-frameworks/)，显然有多种方法来创建一个基本的下拉菜单。ng-repeat 指令为数组中的每一项重复一段 HTML 代码，它可用于在下拉列表中创建选项，但 ng-options 指令是专门为用选项填充下拉列表而设计的，它有一个重要的优点，即用 ng-options 制作的下拉菜单允许选定的值是一个对象，而用 ng-repeat 制作的下拉菜单必须是一个字符串。

这个特殊的代码片段使用 ng-repeat 实现了相同的列表

```
<div ng-app="demo" ng-controller="myCtrl">

<select>
<option ng-repeat="name in names">{{name}}</option>
</select>

</div>

<script>
var app = angular.module('demo', []);
app.controller('myCtrl', function($scope) {
$scope.names = ["Demavand", "Pradeep", "Ashutosh"];
});
</script>

```

这就把我们带到了这篇相当短的博客“使用 angular 的下拉列表”的结尾。我希望现在你已经知道如何在自己的项目中实现下拉菜单了。如果你对这个博客有任何疑问，你可以在下面的评论区发表评论。你也可以分享自己制作下拉框的创意方式。

*如果您希望了解更多关于 Angular framework 的信息，请查看我们的**[Angular Certification](https://www.edureka.co/angular-training)**，它附带有讲师指导的现场培训和实际项目经验。这个训练将帮助你深入了解 Angular，并帮助你掌握这个主题。*

有问题要问我们吗？请在“角度下拉”的评论部分提到它，我会回复你。