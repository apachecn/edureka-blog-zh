# 关于 AngularJS 中的 Stateprovider，您只需要知道

> 原文：<https://www.edureka.co/blog/stateprovider-in-angularjs/>

在使用 [AngularJS](https://www.edureka.co/blog/what-is-angular-getting-started-with-angular/) 创建单页面应用程序时，路由是必须记住的一个重要方面。在本文中，我们将通过使用 [UI-Router](https://ui-router.github.io/) 来熟悉路由的概念，并了解 AngularJS 中的 stateprovider 如何按以下顺序工作:

*   [在 AngularJS 中使用 Stateprovider 的方法](#methods)
*   [安古拉瑞路由器](#router)
    *   [启动项目](#project)
    *   [路由](#routing)
    *   [从 URL 获取参数](#param)

## **在 AngularJS 中使用 Stateprovider 的方法**

$stateProvider 用于定义一条路由的不同状态。你可以给状态一个名字，不同的控制器，不同的视图，而不必使用一个直接的 *href* 到一个路线。在 [AngularJS](https://www.edureka.co/blog/timeout-in-angularjs/) 中有不同的方法使用 stateprovider 的概念。

![Angular Logo - stateprovider in angularjs - edureka](img/7b62b131e39893f6fc01069f651cbd3f.png)

所以，让我们继续讨论不同的方法。

## **安古拉瑞路由器**

UI-Router 是 AngularUI 团队为 AngularJS 构建的一个路由[框架](https://www.edureka.co/blog/videos/angularjs-superheroic-javascript-mvw-framework-2/)。它用于为 [AngularJS 应用](https://www.edureka.co/blog/videos/angular-js-develop-responsive-single-page-application-2/)创建路线，并提供不同于 ngRoute 的方法。 **UI-Router** 拥有额外的功能，并被证明更适合复杂的项目和应用。

### **启动项目**

在这一步中，我们将角度文件嵌入头部。

```
<html ng-app="angularRoutingEx">
...
<script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.7.2/angular.min.js"></script>
<script src="https://unpkg.com/@uirouter/angularjs@1.0.19/release/angular-ui-router.min.js"></script>
<script src="app.js"></script>
...
// Navigation Menu
<ul class="uk-nav uk-nav-default">
<li class="uk-active">
<a ui-sref="main">Menu</a>
</li>
<li>
<a ui-sref="main" ui-sref-active="active">Main</a>
</li>
<li>
<a ui-sref="info" ui-sref-active="active">Info</a>
</li>
</ul>
// Content
<ui-view></ui-view>

```

我们应用程序的主要逻辑出现在 **app.js** : 中

```
var app = angular.module('angularRoutingEx', ['ui.router']);
```

### **路由**

为了管理路由，我们需要添加$stateProvider。在下面给出的代码中，显示了主页和信息页之间的路由。

```
// app.js
app.config(function($stateProvider, $urlRouterProvider){
var states = [
{
name: 'main',
url: '/',
template: '<h1>This is Main</h1>'
},
{
name: 'info',
url: '/info',
template: '<h1>This is Info</h1>'
}
];
states.forEach((state) => $stateProvider.state(state));
$urlRouterProvider.otherwise('/');
});

```

### **从 URL 获取参数**

在下面给出的代码中，该参数通过{{id}}动态填充。

```
// index.html
<ul class="uk-nav uk-nav-default">
<li class="uk-active">
<a ui-sref="main">Menu</a>
</li>
<li>
<a ui-sref="main" ui-sref-active="active">Main</a>
</li>
<li>
<a ui-sref="info" ui-sref-active="active">Info</a>
</li>
<li>
<a ui-sref="params({id: 1})" ui-sref-active="active">Params</a>
</li>
</ul>

```

为了在 app.js 中配置路由，我们使用 **ParamsController** 来获取参数:

```
// app.js
app.config(function($stateProvider, $urlRouterProvider){
var states = [
{
name: 'main',
url: '/',
template: '<h1>This is Main</h1>'
},
{
name: 'info',
url: '/info',
template: '<h1>This is Info</h1>'
},
{
name: 'params',
url: '/params/{id}',
template: '<h1>Param value: {{ paramId }}</h1>',
controller: function($scope, $stateParams) {
$scope.paramId = $stateParams.id;
}
}
];
states.forEach((state) => $stateProvider.state(state));
$urlRouterProvider.otherwise('/');
});

```

这些是利用$stateProvider 的一些概念。到此，我们的文章就结束了。

Edureka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。随着 Angular 框架的广泛采用，应用程序的性能管理是由社区驱动的，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。

有问题要问我们吗？请在“AngularJS 中的 Stateprovider”博客的评论部分提到它，我们将会回复您。