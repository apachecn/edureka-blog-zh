# 如何用 AngularJS 实现 DateFilter 并举例说明

> 原文：<https://www.edureka.co/blog/datefilter-in-angularjs/>

有时，我们需要检查任何特殊原因的日期。发生的情况是，有时它是我们想要的格式，有时不是。因此，在本文中，我们将按以下顺序讨论 [AngularJS](https://www.edureka.co/blog/what-is-angular-getting-started-with-angular/) 中的日期过滤器:

*   [AngularJS 中的 DateFilter 是什么？](#what)
*   [格式中使用的通用和预定义值](#format)

## **AngularJS 中的 DateFilter 是什么？**

我们可以使用 AngularJS 日期过滤器将日期转换成指定的格式。没有指定时，默认日期格式为“MMM d，yyyy”。

***语法:***

`{{ date | date : format : timezone }}`

必须注意，时区和格式参数是可选的。

## **格式中使用的常用值**

*   **‘YYYY’**–定义年份 ex。2018

*   **‘YY’**–定义年份 ex。18

*   **‘Y’**–定义年份 ex。2018

*   **‘MMMM’**–定义月 ex。三月

*   **‘嗯’**–定义月 ex。瑕疵

*   **‘MM’**–定义月 ex。03

*   **‘DD’**–定义日 ex。08

*   **‘d’**–定义日 ex。8

*   **‘hh’**–以 AM/PM 定义小时

*   **‘h’**–定义上午/下午的小时

*   **‘mm’**–定义分钟

*   **‘m’**–定义分钟

*   **‘ss’**–定义秒

*   **‘s’**–定义秒

## **格式**中使用的预定义值

*   **【短】**–相当于“米/日/年小时:毫米 a”

*   **【中】**–相当于“MMM d，y h:mm:ss a”

*   **“短日期”**–相当于“年月日”(2018 年 6 月 8 日)

*   **“中间日期”**–相当于“MMM d，y”(2018 年 4 月 7 日)

*   **“龙日期”**——相当于“MMMM d，y”(2019 . 4 . 7)

*   **“完整日期”**–相当于“EEEE，MMMM d，y”(2018 年 4 月 7 日，星期六)

*   **【短时】**–相当于“h:mm a”(凌晨 4:20)

*   **“中间时间”**–相当于“小时:分钟:秒钟”(上午 4:20:05)

**举例:**

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Date Filter</title>`

`<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js">`

`</script>`

`</head>`

`<body>`

`<div ng-app="firstApp" ng-controller="firstCntrl">`

`<p>{{ today | date : "dd.MM.y" }}</p>`

`</div>`

`<script>`

`var app = angular.module('firstApp', []);`

`app.controller('firstCntrl', function($scope) {`

`$scope.today = new Date();`

`});`

`</script>`

`</body>`

`</html>`

**输出:**

10.09.2019

**举例:**

为了以特定格式显示时间，我们使用以下代码:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Date Filter Ex</title>`

`<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js">`

`</script>`

`</head>`

`<body>`

`<div ng-app="firstApp" ng-controller="firstCntrl">`

`<p>{{ today| date : 'mediumTime'}}</p>`

`</div>`

`<script>`

`var app = angular.module('firstApp', []);`

`app.controller('firstCntrl', function($scope) {`

`$scope.today = new Date();`

`});`

`</script>`

`</body>`

`</html>`

**输出:**

上午 11 点 08 分 11 秒

**举例:**

为了以特定格式显示日期，我们使用了以下代码:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Date Filter Ex</title>`

`<script src=`

`"https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js">`

`</script>`

`</head>`

`<body>`

`<div ng-app="firstApp" ng-controller="firstCntrl">`

`<p>{{ today| date }}</p>`

`</div>`

`<script>`

`var app = angular.module('firstApp', []);`

`app.controller('firstCntrl', function($scope) {`

`$scope.today = new Date();`

`});`

`</script>`

`</body>`

`</html>`

**输出:**

2019 年 9 月 10 日

为了更好地理解，让我们看一下下面的例子:

**举例:**

`<!DOCTYPE html>`

`<html >`

`<head>`

`<title>`

`AngularJs Date Ex`

`</title>`

`<script`

`src="http://ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script>`

`<script>`

`var app = angular.module("firstApp", []);`

`app.controller("firstctrl", function ($scope) {`

`$scope.mydate = new Date();`

`});`

`</script>`

`</head>`

`<body ng-app="firstApp">`

`<div ng-controller="firstctrl">`

`Enter Number: <input type="text" ng-model="mydate" style="width:400px" /><br /><br />`

`Date with short expression:{{mydate | date:"short" }}<br /><br />`

`Date with mediumDate expression: {{mydate | date : "mediumDate"}} <br /><br />`

`Date with yyyy-mm-dd hh:mm:ss expression: {{mydate | date : "yyyy-mm-dd hh:mm:ss" : 0}} <br /><br />`

`Date with yyyy-mm-dd hh:mm:ss expression: {{mydate | date : "dd/mm/yyyy 'at' hh:mma" : 0}}`

`</div>`

`</body>`

`</html>`

**输出:**

![datefilter in angularjs](img/709ce7ed9d4c029512cb253544b38519.png)

至此，我们结束了 AngularJS 文章中的日期过滤器。我希望你理解日期过滤器的各个方面。

Edureka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。随着 Angular 框架的广泛采用，应用程序的性能管理是由社区驱动的，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。