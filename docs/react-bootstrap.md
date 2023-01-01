# 什么是 React Bootstrap 以及如何使用它？

> 原文：<https://www.edureka.co/blog/react-bootstrap/>

React bootstrap 用于替代 Bootstrap [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 。它是从零开始构建的，不需要任何依赖项，比如 jQuery。 [React](https://www.edureka.co/blog/what-is-react/) 是最古老的库之一， react bootstrap 一直伴随着 React 发展壮大，使其成为 UI 设计和基础的优秀工具之一。

在这篇博客中，你将了解到以下几点:

*   [简介反应自举](#reactbootstrap)
*   [安装](#installation)
*   [样式表](#stylesheets)
*   [导入](#importing)
*   [浏览器全局](#browser)

**反应自举**简介

React Bootstrap 构建为兼容任何用户界面(UI)生态系统。在 bootstrap 样式表的帮助下， react bootstrap 对您喜欢使用的所有 Bootstrap 主题都产生了奇迹。每个组件的形式和功能都由反应组件控制。牢记可访问性，执行每个组件。让我们来学习如何安装！

## **安装**

在 npm 包的帮助下，你可以用最好的方式安装 反应引导 。当你不想使用 CDN 表或者你有一个定制的 reactBootstrapsass 文件时，Vanilla Bootstrap 就派上了用场。

```
npm install react-bootstrap bootstrap
```

**样式表**

由于 react bootstrap 是定制的，它不依赖于 bootstrap 的某个特定版本。但是一些样式表使用了这些点:

{ /*下面这一行可以包含在你的 src/index.js 或者 App.js 文件中*/ }

```
import 'bootstrap/dist/css/bootstrap.min.css';

```

无论您想添加什么风格，都由您自己决定，只需添加来自 CDN 的风格即可。为了使用高级用例，像 Webpack 这样的捆绑器将 CSS 文件作为构建过程的一部分。

## **导入**

这里，像 react-bootstrap/Button 这样的单个组件被导入，而不是整个库。完成后，只需调出特定的组件，这样就减少了代码的行数，也减少了将代码发送到客户端所需的时间。

```
import Button from 'react-bootstrap/Button';

// or less ideally
import { Button } from 'react-bootstrap';

```

## **浏览器**

提供 React-bootstrap.js 和 react-bootstrap.min.js 包，然后将这些组件导出到窗口。ReactBootstrap 对象。unpkg 和 npm 包中提供了必要的包

```
<script src="https://unpkg.com/react/umd/react.production.min.js" crossorigin />

<script
  src="https://unpkg.com/react-dom/umd/react-dom.production.min.js"
  crossorigin
/>

<script
  src="https://unpkg.com/react-bootstrap@next/dist/react-bootstrap.min.js"
  crossorigin
/>

<script>var Alert = ReactBootstrap.Alert;</script>
```

就这样，我们来到了这篇文章的结尾。我希望你明白什么是 react bootstrap 以及如何使用它。

*查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)****Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这个“React Bootstrap”博客的评论部分提到它，我们会给你回复。*