# 如何创建自举按钮？

> 原文：<https://www.edureka.co/blog/bootstrap-buttons/>

[Bootstrap](https://getbootstrap.com/) 是一个基于前端框架的 web 开发平台。它用于使用 [、HTML](https://www.edureka.co/blog/what-is-html/) 和 [CSS](https://www.edureka.co/blog/what-is-css/) 创建卓越的响应式设计。这些模板用于表单、表格、按钮、排版、模型、表格、导航、传送带和图像。按钮是网站和应用程序不可或缺的一部分。在本文中，我们将按以下顺序了解不同类型的自举按钮:

*   [如何创建自举按钮？](#create)
*   [自举按钮样式](#style)
*   [按钮尺寸](#size)
*   [轮廓按钮](#outline)
*   [禁用按钮](#disabled)
*   [活动按钮](#active)

## **如何创建自举按钮？**

按钮有多种用途。您可以提交或重置 HTML 表单，执行交互式操作，如单击按钮显示或隐藏网页上的内容，将用户重定向到另一个页面等。Bootstrap 提供了一种快速简单的方法来创建和定制按钮。

使用这些按钮可以执行不同的操作。让我们继续深入了解引导按钮及其不同的活动。

## **自举按钮样式**

Bootstrap 中有不同的类用于设计按钮的样式。此外，它们表示不同的状态或语义。按钮样式可以应用于任何元素。但是，它通常应用于

以下是一个示例，向您展示如何在 Bootstrap 中创建不同样式的按钮:

```
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-link">Link</button>
```

**输出:**

![button style - bootstrap button - edureka](img/48c31209b9875b9262fb6769cad78891.png)

## **按钮尺寸**

你可以在 bootstrap 的帮助下放大或缩小一个按钮。因此，您可以通过添加一个额外的类**来放大或缩小按钮。btn-lg** 或**。btn-sm。**

让我们举个例子，看看它是如何工作的:

```
<button type="button" class="btn btn-primary btn-lg">Large</button>
<button type="button" class="btn btn-primary">Default</button>
<button type="button" class="btn btn-primary btn-sm">Small</button>
```

**输出:**

![output - bootstrap button - edureka](img/a8b9e0c92592f50b349ac6638d1bf48e.png)

## **轮廓按钮**

大纲按钮是一种不同的样式。还可以通过替换按钮修饰符类来创建轮廓按钮。

以下示例显示了大纲按钮的工作方式:

```
<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-outline-secondary">Secondary</button>
<button type="button" class="btn btn-outline-success">Success</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
<button type="button" class="btn btn-outline-light">Light</button>
```

**输出:**

![](img/375ee0088b0898a0d4d604d26bba85cd.png)

## **禁用按钮**

出于某种原因，我们可能需要禁用某个按钮。例如，如果用户没有资格执行此特定操作，或者我们希望确保用户在继续执行此特定操作之前应该执行所有其他必需的操作。

让我们举个例子，看看如何禁用按钮:

```
<button type="button" class="btn btn-primary btn-lg" disabled>Primary button</button>
<button type="button" class="btn btn-secondary btn-lg" disabled>Button</button>
```

**输出:**

![](img/478127b1e729d962d2bd81bfb420678d.png)

您也可以通过添加类**来禁用通过**

```
<a href="#" class="btn btn-primary btn-lg disabled">Primary link</a>
<a href="#" class="btn btn-secondary btn-lg disabled">Link</a>
```

**输出:**

![](img/52437fcef16548355e4409fd61499388.png)

## **活动按钮**

你可以使用类**。激活**强制按钮看起来像激活或按下。通常你不需要把这个类添加到按钮中，因为它们的活动状态是由引导程序使用 CSS :active 伪类自动设置的。

以下是激活按钮的示例:

```
<a href="#" class="btn btn-primary btn-lg active" role="button" aria-pressed="true">Primary link</a>
<a href="#" class="btn btn-secondary btn-lg active" role="button" aria-pressed="true">Link</a>
```

**输出:**

![output - bootstrap button - edureka](img/4a6b727e74241f4220a560b0d7c3c402.png)

这些是不同类型的引导按钮。就这样，我们来到了这篇文章的结尾。我希望你明白如何根据自己的需要设计不同的按钮样式。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“自举按钮”博客的评论部分提到它，我们将会回复您。