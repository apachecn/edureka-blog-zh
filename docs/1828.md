# 如何在 Angular JS 中实现表单验证？

> 原文：<https://www.edureka.co/blog/validation-in-angular-js>

验证是对 **用户进行** 身份验证的一种方法。它被用在所有的网络技术中，比如 HTML 和 JavaScript。但是今天我们的重点将是 Angular JS 中的验证，顺序如下:

*   [什么是表单验证？](#validation)
*   [角度 JS 中的表单验证](#angular)
*   [表单验证步骤](#steps)
*   [代码](#code)

## **什么是表单验证？**

表单验证是一种我们可以用来验证 HTML 表单的技术。让我们举一个简单的例子，假设一个用户有一个 HTML 表单，该 HTML 表单有不同的字段，这些字段由表单验证器验证。当我们想要验证表单时，我们只需要用验证器表达式检查特定字段的值。如欲了解更多信息，请立即查看此[全栈开发课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

如果正则表达式和字段值相同，那么我们可以说我们的表单是有效的。在 HTML 表单中，有不同类型的验证，如电子邮件、必填项、最小值、最大值、密码等。

## **角度 JS 中的表单验证**

让我们谈谈如何在 angular JS 中验证一个表单。Angular JS 提供了各种类型的表单验证属性，我们可以使用这些属性来验证表单或从表单中获取数据。

*   *$valid* :该属性通过应用适当的规则来判断字段是否有效。

*   *$invalid* :顾名思义 invalid 这种磁贴不管字段是否基于相应的规则无效。

*   *$质朴* :在表单输入字段未使用时返回 true。

*   *$dirty* :在表单输入字段使用时返回 true。

*   *$ touched*:boolean true 如果输入已经模糊。

***访问表单:*** `<form name>.<angular property>`

***访问一个输入:*** `<form name>.<input name>.<angular property>`

现在让我们用一个例子来解释 angular JS 中的表单验证，首先我们创建两个文件，一个是 app.js，另一个是 index.html。我们的 index.htm 文件包含一个具有角度验证的简单 HTML 表单，我们的 app.js 文件包含处理 index.html 页面上表单验证的后端代码。

带有`novalidate`属性的`index.html`页面内容表单，这到底是什么意思？

form 标签中的 novalidate 属性告诉 HTML 我们可以使用自定义的表单验证。如果我们不给出 novalidate 属性，那么 HTML 表单将使用 HTML5 默认的表单验证属性进行验证。

## **表单验证步骤**

在我们的表单中，我们创建了 6 个字段，分别是名字、姓氏、电子邮件、电话、密码和消息。

1.  首先，我们添加必填字段验证器，这个验证器告诉用户某个特定字段是必填的。

2.  接下来是电子邮件字段，如果用户没有给出任何有效的电子邮件，那么我们的电子邮件验证器会抛出一个电子邮件验证错误。

3.  我们在密码验证中设置了最小和最大长度。最小长度为 5，最大长度为 8，因此用户可以提供 5 到 8 个字符的有效密码。

4.  最后，我们设置所需的电话和消息字段，特别是在电话字段应用号码验证。

**Angular JS 中表单验证的代码**

**index.html**

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Angular scope example</title>
</head>
<body ng-app="ngValidApp">

<div ng-controller="ngValidController">

<form name="chkValidation" novalidate>
<label>First Name</label>
<input type="text" placeholder="Enter first name" name="firstName" ng-model="firstName" ng-required="true"><br>
<p style = "color:red" ng-show = "chkValidation.firstName.$error.required">This filed is required</p>

<label>Last Name</label>
<input type="text" placeholder="Enter last name" name="lastName" ng-model="lastName" ng-required="true"><br>
<p style = "color:red" ng-show = "chkValidation.lastName.$error.required">This filed is required</p>

<label>Email</label>
<input type="email" placeholder="Enter email" name="email" ng-model="email" ng-required="true"><br>
<p style = "color:red" ng-show = "chkValidation.email.$error.required">This filed is required</p>
<p style = "color:red" ng-show = "chkValidation.email.$error.email">Not a valid email</p>

<label>Phone</label>
<input type="text" required placeholder="Enter phone" name="phone" ng-model="phone" ng-required="true" ng-pattern="/^(+d{1,2}s)?(?d{3})?[s.-]?d{3}[s.-]?d{4}$/"><br>
<p style = "color:red" ng-show = "chkValidation.phone.$error.required">This filed is required</p>
<p style = "color:red" ng-show="chkValidation.phone.$error.pattern">This is not a valid phone</p>

<label>Password</label>
<input placeholder="******" type="password" name="password" ng-model="password" ng-required="true" ng-minlength="5" ng-maxlength="8"><br>
<p style = "color:red" ng-show = "chkValidation.password.$error.required">This filed is required</p>
<p style = "color:red" ng-show = "(!chkValidation.password.$valid)">Password between 5 to 8 characters</p>

<label>Message</label>
<textarea required placeholder="Enter your message" name="message" ng-model="message" ng-required="true"></textarea><br>
<p style = "color:red" ng-show = "chkValidation.message.$error.required">This filed is required</p>

<button type="submit">Submit</button>
</form>

</div>

<!--angular js library-->
<script src="assets/js/angular.js"></script>
<script src="app.js"></script>
</body>
</html>

```

**app.js**

```
var app = angular.module('ngValidApp', []);

app.controller('ngValidController', function($scope) {

});

```

让我们来谈谈表单中使用的一些验证指令:

*   ***-ng-必填*** **:** 用于提供必填字段
*   ***ng-显示*** **:** 根据条件显示错误信息(检查验证属性)
*   ***ng-minlength*****:**用于提供最小长度
*   ***ng-maxlength*****:**用于提供最大长度
*   ***-ng 模式*** **:** 匹配特定模式
*   ***ng-model*****:**用$error、$valid 等验证属性绑定字段。

至此，我们结束了 Angular JS 文章中的验证。我希望您理解了 Angular JS 中表单验证需要考虑的各种事情。

*如果您希望了解更多关于 Angular framework 的知识，请查看我们的 **[Angular 课程](https://www.edureka.co/angular-training)** ，该课程包含讲师指导的现场培训和真实项目体验。这个训练将帮助你深入了解 Angular，并帮助你掌握这个主题。*

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会给你回复。