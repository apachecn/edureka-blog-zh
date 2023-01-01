# angular . forEach:forEach 函数的实现

> 原文：<https://www.edureka.co/blog/angular-foreach-function/>

Angular 中的 ForEach 循环可用于对给定数组或对象中的每一项执行某些操作。这类似于其他语言中的 foreach 循环，如 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 、 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 等。其中循环用于数组或其他集合。在 AngularJS 中，它略有不同，因为它遍历给定数组或对象的每个元素。在这篇关于“Angular 中的 forEach”的博客中，你将按照以下顺序，通过例子学习如何实现 forEach 函数。

*   [角度中的每个循环](#foreach)
*   [使用 forEach 函数的语法](#syntax)
*   [使用角度 forEach 的演示](#demo)

## **角度中的每个循环**

Angular 中的 forEach 对 obj 集合中的每一项调用一次迭代器函数，可以是对象，也可以是数组。迭代器函数用 iterator(value，key，obj)调用，其中值是对象属性或数组元素，键是数组元素索引或对象属性键，obj 是 obj 本身。今天就来看看这个 [web 开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)，了解更多关于 Angular 的知识。

## **使用 forEach 函数的语法**

下面是使用 [AngularJS](https://www.edureka.co/blog/angular-tutorial/) 的 forEach 函数的方法:

**angular . foreach(object _ or _ Array，iterator，[context])；**

这里，第一个参数可以是对象或数组，第二个参数是为对象或数组中的每一项调用的迭代器函数。

## **使用角度 forEach 的演示**

```
<html> 
    <head> 
        <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%20src%3D%20%22%2F%2Fajax.googleapis.com%2Fajax%2Flibs%2Fangularjs%2F1.3.2%2Fangular.min.js%22%3E%20%0A%20%20%20%20%20%20%20%20%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" /> 
        <title>angular.forEach()</title> 
    </head> 

    <body ng-app="app" ng-cloak style="padding:30px">    
<h1 style="color:Blue">Learn with Edureka</h1>
<h2>Applying angular.forEach()</h2>

 Directives in Angular 

<div ng-controller="test">

<div ng-repeat="name in names">      
<ul>
<li>{{name}}</li>
</ul>
        </div>
        </div>
    <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%3E%20%0A%20%20%20%20%20%20%20%20var%20app%20%3D%20angular.module(%22app%22%2C%20%5B%5D)%3B%20%0A%20%20%20%20%20%20%20%20app.controller('test'%2C%20%5B'%24scope'%2C%20function%20(%24scope)%20%7B%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%24scope.names%20%3D%20%5B%5D%3B%20%0A%20%20%20%20%20%20%20%20%20%20%20%20var%20values%20%3D%20%5B%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%7Bname%3A%20'Component%20Directives'%7D%2C%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%7Bname%3A%20'Structural%20Directives'%7D%2C%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%7Bname%3A%20'Attribute%20Directives'%7D%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%5D%3B%20%0A%20%20%20%20%20%20%20%20%20%20%20%20angular.forEach(values%2C%20function%20(value%2C%20key)%20%7B%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%24scope.names.push(value.name)%3B%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%7D)%3B%20%0A%20%20%20%20%20%20%20%20%7D%5D)%3B%20%0A%20%20%20%20%20%0A%20%20%20%20%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" /> 
</body> 
</html> 

```

**输出:**

这就把我们带到了这篇关于“Angular 中的 ForEach 循环”的博客的结尾。我希望它能增长你的知识，增加你的知识。

*如果您希望了解更多关于 Angular framework 的知识，请查看我们的 [Angular 课程](https://www.edureka.co/angular-training)，该课程包含讲师指导的现场培训和真实项目体验。这个训练将帮助你深入了解 Angular，并帮助你掌握这个主题。*

有问题要问我们吗？请在“Angular 中的 ForEach 循环”的评论部分提到它，我们会回复您。