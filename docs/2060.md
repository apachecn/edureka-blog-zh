# 什么是角度 JS 的 Ng-change，如何给它赋值？

> 原文：<https://www.edureka.co/blog/angularjs-ng-change-directive/>

嗨，让我们了解一下 [AngularJS](https://www.edureka.co/blog/angular-tutorial/) 中提供的一个有趣的指令，即 ng-change 指令，这个名称本身就部分泄露了它所执行的工作。程序员通常会对 on-change 和 ng-change 事件感到困惑，让我们今天在这个博客中把所有事情都弄清楚。我们今天要讨论的主题是:

*   [什么是指令？](#directive)
*   [什么是 ng-change？](#ng-change)
*   [使用 ng-change 指令时的要点](#points)
*   [语法](#syntax)
*   [例如](#example)

在继续写博客之前，我们先快速浏览一下 AngularJS 中的指令。

## 什么是指令？

AngularJS 指令是带有前缀“ng-”的简单扩展 HTML 属性。AngularJS 提供了一组内置指令，为我们的应用程序提供各种功能。

AngularJS 还让我们定义自己的指令。

## **什么是 ng-change？**

Ng-change 是 AngularJS 中的一个[指令，用于在组件值或事件改变时执行操作。换句话说，](https://www.edureka.co/blog/angular-directive/) ng-change 指令告诉 AngularJS 当一个 HTML 元素的值改变时该做什么。

ng-change 指令需要一个 ng-model 指令。

## **使用 ng-change 指令时的要点:**

*   onChange 事件会发生什么？AngularJS 中的 ng-change 指令不会覆盖元素的原始 onchange 事件，将执行 ng-change 表达式和原始 onchange 事件。
*   ng-change事件在每次值改变时被触发。它不会等待所有的更改完成，也不会等待输入字段失去焦点。
*   ng-change事件只有在输入值发生实际变化时才会触发，而不是在 JavaScript 中发生变化时。
*   这个 ng-change 指令由 HTML 标签支持，如<输入>、<选择>和<文本区域>。
*   只有当输入值的变化导致新值提交给模型时，才会计算 ngChange 表达式。

不予评价:

1.  如果从$parsers 转换管道返回的值没有改变
2.  如果输入继续无效，自模式将保持为空
3.  如果不是通过输入值而是通过编程来改变模型。

**注意** ，该指令要求 ngModel 到场。

## **语法:**

**<** **元素**ng-change=“表情” **> < /** **元素** **>**

表达式:指定一个元素的值发生变化时执行的表达式。

## **举例:**

```
<!DOCTYPE html>  
<html>  
<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script>  
<body ng-app="App1">  
<div ng-controller="Cng1">  
  <p>Please type in the input field:</p>  
  <input type="text" ng-change="myFunc()" ng-model="Val" />  
  <p>The input field has changed {{count}} times.</p>  
</div>  

<script>  
  angular.module('App1', [])  
    .controller('cng1l', ['$scope', function($scope) {  
      $scope.count = 0;  
      $scope.myFunc = function() {  
        $scope.count++;  
      };  
    }]);  
</script>  
</body>  
</html>  

```

**输出(3 次改变后)**

请在输入框中输入:

输入字段已经改变了 3 次。

我希望，现在你可能已经对 ng-change 指令有了清晰的理解，试着在你的程序中使用它，看看你学到了多少。感谢阅读。 我会推荐你浏览这个 ***Angular 教程 [Edureka 视频播放列表](https://www.youtube.com/playlist?list=PL9ooVrP1hQOFyAdwmvyPgFlbiBKiDoTa_)*** 观看视频，学习如何使用 Angular 应用程序。

*既然你已经知道了 Angular 指令，那就来看看 Edureka 的 [**Angular 课程**](https://www.edureka.co/angular-training) 吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。随着 Angular 框架的广泛采用，应用程序的性能管理是由社区驱动的，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。*