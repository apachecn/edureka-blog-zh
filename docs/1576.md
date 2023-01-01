# 如何在 angularjs 中执行 CRUD 操作？

> 原文：<https://www.edureka.co/blog/crud-operations-in-angularjs/>

嘿，如果你想了解 AngularJS 中的 CRUD 操作，那么这里是你的好去处。本文将带你浏览 AngularJS 中的 CRUD 操作，并解释如何使用它们。

本文将涵盖以下主题

*   [什么是 AngularJS？](#WhatisAngularJS)
*   [棱角的特征](#FeaturesofAngularJS)
*   [什么是 CRUD 操作？](#WhatisCRUDOperations)
*   [如何在 AngularJS 中实现 CRUD 操作？](#implementCRUD)

那么我们开始吧。

****什么是 AngularJS？**** AngularJS 是一个开源的前端开发框架，实现了 MVVM(模型-视图-视图模型)架构。AngularJS 基于 JavaScript。它由 Google 和 维护，可以说是最流行的框架之一。这主要是因为它得到了谷歌的全力支持，并融入了最新的市场趋势。AngularJS 主要用于开发单页面应用程序或 spa。

## 的特点

1.  ——MVVM(Model-View-ViewModel)架构模式基于 MVC (Model-View-Control)模型。这里，控制器被视图模型代替。由此，AngularJS 实现了[双向数据绑定](https://www.edureka.co/blog/angular-data-binding/#two-way)的概念。双向数据绑定允许通过模型和视图来管理数据。
2.  ****数据模型绑定****——无需编写特定代码将数据绑定到 HTML 控件。这可以通过 AngularJS 添加一些代码片段来实现。
3.  ****编写更少的代码****——更早的时候，对于 DOM 操纵，设计任何应用都需要编写大量的 JavaScript。但是使用 AngularJS，DOM 操作只需要很少的代码。
4.  ****单元测试** **就绪****——谷歌的开发人员还与 AngularJS 一起开发了一个名为“Karma”的测试框架，帮助设计 AngularJS 应用的单元测试。

## ****什么是 Crud 操作？****

CRUD 基本上代表 **从服务器或数据库创建读取更新删除** 数据。

## ****如何在 AngularJS 中实现 CRUD 操作？****

在本教程中，我们将学习为学生管理门户创建一个演示项目，该项目将允许用户使用 AngularJS 创建、读取(查看)、编辑(更新)和删除数据。 现在市场上有很多编辑器可以用于 angular 开发，比如 Webstorm、Aptana、Sublime Text、Eclipse IDE 等。你可以使用其中任何一个。

本教程中需要了解的基本术语:

*   控制器:这是一个常规的 javascript 对象，用于控制 AngularJS 应用程序的数据。
*   范围:是视图和控制器之间的绑定部分。它是一个具有已定义属性和方法的对象。

让我们开始编码吧。

**第一步:**创建 student.html 文件:

**student.html:**

*   在 html 文件的< head >标签内添加以下脚本。CDN 链接将有助于 Angular 的入门。

`<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>`

*   在同一个文件夹中创建一个 angularCrud.js 文件，并用脚本标签:引用它

`<script src="angularCrud.js"></script>`

*   创建一个注册学生的表单。

```
<div ng-app="myapp" ng-controller="myctrl"> 
<!--ng-app directive is used to initialize an angular application -->
        <label>Name</label>

        <input type="text" name="name" ng-model="newStudent.name"/>

        <label>Address</label>

        <input type="text" name="address" ng-model="newStudent.address"/>

        <label>Dept.</label>

        <input type="text" name="dept" ng-model="newStudent.dept"/>

        <input type="hidden" ng-model="newStudent.id" />

        <input type="button" value="Save" ng-click="saveRecord()" class="btn btn-primary"/>

```

注意:在这里点击按钮，我们调用 saveRecord()函数，我们将在定义控制器的 angularCrud.js 文件中创建该函数。

*   创建一个表格，显示学生的数据以及更新和删除学生的选项。

```

<table border="1" bordercolor="blue">

<tr style="color:blue">

<th style="width:150px">Name</th>

<th style="width:150px">Address</th>

<th style="width:150px">Dept</th>

<th>Action</th>

            </tr>

<tr style="color:pink" ng-repeat="student in students">

<td>{{ student.name }}</td>

<td>{{ student.address }}</td>

<td>{{ student.dept }}</td>

<td>

                    <a href="#" ng-click="edit(student.id)">edit</a> | 

                    <a href="#" ng-click="delete(student.id)">delete</a>

                </td>

            </tr>

        </table>

```

注:- 在第一行我们增加了一个标题，“行动”。在第二行中，我们增加了一列，其中使用了两个锚点。

第一个锚定链接用于“编辑”功能，第二个锚定链接用于“删除”功能。学生的 Id 是根据定位点传递的，换句话说，无论定位点放在哪里，Id 都会同时传递给函数。

*   **现在我们的视图模型例如 students.html 被更新了，它的代码是这样的:**

```
<!DOCTYPE html>
<html>
<head>

<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%20src%3D%22https%3A%2F%2Fajax.googleapis.com%2Fajax%2Flibs%2Fangularjs%2F1.6.9%2Fangular.min.js%22%3E%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%20src%3D%22angularCrud.js%22%3E%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />
<title>Student Management Portal</title>

</head>
<body>

<div ng-app="myapp" ng-controller="myctrl">

        <label>Name</label>

        <input type="text" name="name" ng-model="newStudent.name"/>

        <label>Address</label>

        <input type="text" name="address" ng-model="newStudent.address"/>

        <label>Dept.</label>

        <input type="text" name="dept" ng-model="newStudent.dept"/>

        <input type="hidden" ng-model="newStudent.id" />

        <input type="button" value="Save" ng-click="saveRecord()" class="btn btn-primary"/>

<table border="1" bordercolor="blue">

<tr style="color:blue">

<th style="width:150px">Name</th>

<th style="width:150px">Address</th>

<th style="width:150px">Dept</th>

<th>Action</th>

            </tr>

<tr style="color:pink" ng-repeat="student in students">

<td>{{ student.name }}</td>

<td>{{ student.address }}</td>

<td>{{ student.dept }}</td>

<td>

                    <a href="#" ng-click="edit(student.id)">edit</a> | 

                    <a href="#" ng-click="delete(student.id)">delete</a>

                </td>

            </tr>

        </table>

    </div>

</body>
 </html>

```

第二步:创建一个 angularCrud.js 文件，这将是我们的控制器。

*   **创建一个角度模块，并为其指定一个名称**

`var app=angular.module('myapp',[]);`

*   **创建一个控制器**

`app.controller('myctrl',function($scope){});`

****现在我们将逐一创建所有的 CRUD 函数****

*   **创建功能:**

```

$scope.saveRecord = function () {

if ($scope.newStudent.id == null) {

$scope.newStudent.id = empid++;

$scope.students.push($scope.newStudent);

} else {

for (i in $scope.students) {

if ($scope.students[i].id == $scope.newStudent.id) {

$scope.students[i] = $scope.newStudent;

}

}

}

$scope.newStudent = {};

}

```

saveRecord()函数做两件事。第一，如果是一个新学生，我们将从 newStudent 获取属性，即 来自模板，并将该对象推送到本地地址集合中。然后地址集合被分配给视图中的模型集合。

*   **编辑和删除功能:**

首先，我们提供了删除功能。为此，我们创建了一个名为“删除”的功能。在这个函数中，学生的 Id 被传递，如果 Id 正确地匹配一个现有的 Id，那么删除操作将被执行，该条目将被删除。

同样，我们已经创建了“编辑”功能。在此功能中，学生的 Id 也将被传递，但这一次与该 Id 相关的数据将不会被删除，而是被传递回相应的输入框，以便用户可以进行更改，当用户单击保存按钮时，数据将再次保存在与先前存储的 Id 相同的位置。

*   **现在更新后的 angularCrud.js 脚本是这样的—**

```

$scope.delete = function (id) {

for (i in $scope.students) {

if ($scope.students[i].id == id) {

$scope.students.splice(i, 1);

$scope.newStudent = {};

}

}

}

$scope.edit = function (id) {

for (i in $scope.students) {

if ($scope.students[i].id == id) {

$scope.newStudent = angular.copy($scope.students[i]);

}

}

}

```

**输出:**

至此，我们结束了这篇关于 AngularJS 中 CRUD 操作的博客。我希望阅读这篇博客能帮助你解决与 CRUD 操作相关的问题，并使你能够在 AngularJS 中使用 CRUD 操作。

继续参观， 继续学习！

*如果您希望了解更多关于 Angular framework 的知识，请查看我们的 **[Angular 课程](https://www.edureka.co/angular-training)** ，该课程包含讲师指导的现场培训和真实项目体验。这个训练将帮助你深入了解 Angular，并帮助你掌握这个主题。*

有问题要问我们吗？请在“**Angularjs 中的 crud 操作”的评论区提及？**“我会回来找你的。