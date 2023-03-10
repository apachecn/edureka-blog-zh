# 使用 AngularJS 进行水疗

> 原文：<https://www.edureka.co/blog/spa-using-angularjs>

今天，AngularJS 已经成为最受欢迎的开发框架之一，主要是因为它能够帮助开发人员轻松创建单页面应用程序(SPA)。在传统的 web 应用程序中，客户端(浏览器)通过请求页面来启动与服务器的通信通道。服务器通过处理请求并将页面的 HTML 发送回客户端来做出响应。如果用户请求一个新页面，服务器发送另一个 HTML 页面。即使客户端要求一个小的改变，比如说一个有基本细节的表单，整个页面都要被服务器重新加载并发送给客户端。

## HTML 和 Ajax 请求

在单页面应用程序中，一次加载整个页面，随后的通信由服务器使用 Ajax 请求来执行。浏览器只需更新页面中发生变化的部分，不需要每次用户发出新请求时都重新加载整个页面。由于 SPA 方法减少了服务器响应用户请求的时间，因此 web 应用程序运行速度更快，使用的计算能力更低，并且允许用户界面(UI)开发人员创建更有吸引力、更灵活的网页。

## 外壳页面的创建

SPA 中的“单个页面”是指以 HTML、CSS 或 JavaScript 形式响应查询的外壳页面。shell 页面与 HTML 异步呈现，消除了来回访问服务器的需要。shell 页面只需要一个对 AngularJS JavaScript 库的引用和一个 ng-view 指令(一个允许 UI 开发人员在视图之间切换的虚拟容器)来告诉 AngularJS 内容页面需要在 shell 页面上呈现在哪里。在同一个“单一”页面中，AngularJS 允许开发者提供包含在同一个 URL 中的多个视图。不同的视图集可以一个接一个地出现在同一个 shell 页面中，当用户滚动页面时，每个视图都会动态加载。

[![SPA-using-AngularJS-multiple-views](img/5d1c16be2d0b536a36c06f39827e8ad9.png "SPA-using-AngularJS-multiple-views")](https://www.edureka.co/angular-training)

内置的 AngularJS 指令(ng-app)允许开发人员初始化应用程序，也可以选择添加第三方指令。另一方面，ng-model 指令允许您将数据绑定表达式添加到内存中。请看这里:

[![ng-directive-SPA-using-AngularJS](img/a8fb335985520459ebd972fd0a22ab79.png "ng-directive-SPA-using-AngularJS")](https://www.edureka.co/angular-training)

在全球范围内，开发人员已经采用了使用 AngularJS 的 SPA，这种趋势很可能会持续一段时间。

有问题要问我们吗？请在评论区提出来，我们会尽快回复您，或者今天就加入我们的[角度认证](https://www.edureka.co/angular-training)课程。

**Related Posts:**[Deep Dive on AngularJS Javascript Framework](https://www.edureka.co/blog/videos/deep-dive-into-angularjs-javascript-framework/ "deep dive into angularjs javascript framework")[Are You Riding the AngularJS Wave Yet?](https://www.edureka.co/blog/videos/are-you-riding-the-angularjs-wave-yet/ "are you riding the angularjs wave yet")[Successful Web Development  Career with AngularJS](https://www.edureka.co/blog/successful-web-development-career-with-angularjs "successful web development career with AngularJS")