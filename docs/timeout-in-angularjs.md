# 如何在 AngularJS 中最好地实现$timeout？

> 原文：<https://www.edureka.co/blog/timeout-in-angularjs/>

AngularJs 中的$timeout 类似于 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 中的 window.setTimeout 函数。使用$timeout 服务允许开发人员根据需求设置一些时间延迟来执行方法和函数。在我们进一步讨论之前，本文将讨论以下几点。

*   [$timeout in AngularJS(语法)](#%24timeoutinAngularJS(Syntax))
*   [例子](#Example)

所以伙计们，让我们不要浪费任何时间，开始这篇文章

## **$角度超时**

简单来说，该服务可用于在指定的时间延迟后调用另一个函数。

***语法:***

```
var app = angular.module('firstApp', []);
ap
p.controller('firstCtrl', function ($scope, $timeout) {
$scope.msg="Ahoy!"
$timeout(function () {
$scope.msg = "Save the planet!";
}, 4000);
});

```

必须注意，在上面给出的代码中，我们在 4 秒钟后更改了消息。这是通过使用$timeout 服务来完成的。在上面给出的例子中，我们已经将$timeout 作为参数传递给了控制器。要在控制器中使用服务，必须将$timeout 作为参数传递。

继续举例。

**举例:**

```
<!DOCTYPE html>
<html>
<head>
<title>
$timeout Service Example
</title>
<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script>
<script type="text/javascript">
var app = angular.module('firstApp', []);
app.controller('firstCtrl', function ($scope, $timeout) {
$scope.msg="Ahoy!"
$timeout(function () {
$scope.msg = "Save the planet!";
}, 2000);
});
</script>
</head>
<body>
<div ng-app="firstApp" ng-controller="firstCtrl">
<p>$timeout Service Example</p>
<b>{{msg}}</b>
</div>
</body>
</html>

```

**输出:**

![$timeout In AngularJS](img/bdfee6c7fbdcc8fce1c28d346230fdc2.png)

在指定的两秒钟后，文本自动更改为:

![](img/b8518daa9222b7d94591ffc66f0784cc.png)

这是关于演示部分，这是你如何使$timeout 生效。

*这就把我们带到了本文的结尾$timeout In AngularJS。既然你已经了解了 JavaScript 中的方法，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

有问题要问我们吗？请在“$timeout in AngularJS”的评论部分提到它，我们会给你回复。