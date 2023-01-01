# 什么是 AngularJS Bootstrap，如何实际使用？

> 原文：<https://www.edureka.co/blog/angularjs-bootstrap/>

这篇 AngularJS Bootstrap 文章将通过一个实际的演示向您介绍 [AngularJS](https://www.edureka.co/blog/angular-tutorial/) 中的引导概念。本文将涉及以下几点:

*   [角度.自举](#Angular.bootstrap)
*   [例 1](#Example1)
*   [例 2](#Example2)

让我们开始吧！！

**Angular.bootstrap()**

核心 ng 模型中有一个功能组件，称为 angular.bootstrap()函数。它用于手动启动角度应用。

***语法:***

angular.bootstrap(元素，[模块]，[配置])

***参数:***

*   **元素**–DOM 元素是一个元素，被认为是角度应用的根。
*   **模块**–要加载的模块数组称为模块。它是可选指定的。
*   **Config**–用于配置选项的对象称为 Config。这也是可选的。

继续角度引导示例

***例如:***

```
<html>
<head>
<title>ANGULAR BOOTSTRAP EXAMPLE</title>
<script src=
"https://ajax.googleapis.com/ajax/libs/angularjs/1.5.6/angular.min.js">
</script>
<style>
.id 
{
font-size: 1.5em;
color:blue;
}
</style>
</head>
<body ng-app="app" style="text-align:Center">
<h1 style="color:blue">Bootstrap</h1>
<h2>angular.bootstrap()</h2>
<div ng-controller="Bootstrap">
<span class="id">{{name}}</span>
is easy to use.
</div>
<script>
var app = angular.module("app", []);
app.controller('Bootstrap', ['$scope', function ($scope) {
$scope.name = "Bootstrap";
}]);
angular.bootstrap(document, ['app']);
</script>
</body>

```

**输出:**

![Output - AngularJS Bootstrap - Edureka](img/298dd34e77fbc78b473fce8d7ef0cd3b.png)

继续角度引导示例

***例 2:***

```
</div>
<html>
<head>
<title>angular.bootstrap()</title>
<script src=
"https://ajax.googleapis.com/ajax/libs/angularjs/1.5.6/angular.min.js">
</script>
</head>
<body ng-app="app" style="text-align:Center">
<h1 style="color:blue">Bootstrap</h1>
<h2>angular.bootstrap()</h2>
<div ng-controller="Bootstrap">
<div class="col-md-3 well" ng-init="count=0">
Rock:
<input type="radio" ng-model="Music" value="Rock"
ng-change="layout(Music)" />
Metal:
<input type="radio" ng-model="Music" value="Metal"
ng-change="layout(Music)" />
<pre><b>You selected:</b> {{result}} </pre>
</div>
</div>
<script>
var app = angular.module("app", []);
app.controller('Bootstrap', ['$scope', function ($scope) {
$scope.layout = function (Music) {
$scope.result = Music;
}
}]);
angular.bootstrap(document, ['app']);
</script>
</body>
</html>

```

**输出:**

选择单选按钮后，将显示以下输出:

![Output - AngularJS Bootstrap - Edureka](img/25164a97202cb1f29f4b3cd50232a0d6.png)

angular.bootstrap()函数提供了对应用程序初始化的主要控制。

这就把我们带到了这篇关于 AngularJS Bootstrap 的文章的结尾。

如果你想了解更多，请查看 Edureka 提供的[](https://www.edureka.co/angular-training)角度训练，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。

随着 Angular 框架的广泛采用，应用程序的性能管理由社区驱动，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。查看这个[网络开发者在线课程](https://www.edureka.co/masters-program/full-stack-developer-training)，了解更多关于 Angular 的知识。

有问题要问我们吗？请在“AngularJS Bootstrap”的评论部分提到它，我们会回复您。