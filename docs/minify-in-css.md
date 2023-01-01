# 如何在 CSS 中最好的实现 Minify？

> 原文：<https://www.edureka.co/blog/minify-in-css/>

这篇文章将向你介绍一个在 [CSS](https://www.edureka.co/blog/what-is-css/) 中被称为 Minify 的主题，并在过程中给你一个详细的实际演示。本文将涉及以下内容，

*   [什么是缩小化？【T2](#Whatisminification?)
*   [为什么需要缩小？【T2](#Whyisminificationneeded?)
*   [如何缩小 CSS、JS、HTML 代码？【T2](#HowdoyouminifyCSS,JS,HTMLcode?)
*   [你应该什么时候这样做？【T2](#Whenshouldyoudothat?)
*   [缩小化的好处？](#Benefitsofminification?)

顾名思义，缩小就是最小化文件的大小。在代码库中，我们可以自由地缩小 HTML、CSS 或 Javascript 文件。在这里，我们将讨论如何缩小一个 CSS 文件。

当一个开发人员编码时，他/她确保代码是以最好的可读格式来简化任何进一步修改的过程。因此，变量名采用了易于理解的格式，并且占用了大量的字符。然后，他们还增加了大量的空白，使其可读性更好。

但是在整个过程中，我们倾向于放松文件大小增加的限制，这反过来增加了网站的加载时间。特别是对于有大量功能和附加组件的网站，更长的代码库只会让网站变得更糟。

无论如何，谷歌都有一个受限的格式，根据网站提供的最佳用户体验，对其搜索页面上的网站进行排名。你的网站加载得越好，你的网站在搜索页面上的排名就越靠前。

有这么多的风险，你不希望你的用户因为糟糕的网站加载时间而受苦，然后转向下一个网站。因此，代码的精简极其重要。

事实上，在构建网站时，我们知道最大代码库由什么组成？ 都是关于 CSS、HTML、Javascript 的。今天，让你的网站看起来更吸引人的竞争强调了 CSS 文件，而没有意识到我们用大量代码来利用我们的网站。

进入，缩小..

继续这篇关于缩小 CSS 的文章

## **什么是**缩小版**？**

缩小允许你把你的代码分解成最小的文件大小，这不会影响代码，但会减小文件的大小。在这个过程中，你可以删除不必要的间距和字符，这些都不会影响你的网站的原创性。代码中应该避免的一些事情是:

*   空白字符
*   新行字符
*   块分隔符
*   评论
*   缩短变量名

这些因素并不影响你的网站运行，只是增加了文件的重量和网站的加载时间。

代码的可读性完全取决于机器能理解什么。网页浏览器不需要额外的字符间距来理解和运行。所以，试着减少它们，缩小 CSS 和 HTML 代码。

**我们来举个例子:**

```
<html>
<head>
<style>
#myContent
{
font-family: Montserrat
}
#myContent
{
font-size: 90%
}
</style>
</head>
<body>
<!-- start myDemo-->
<div id="myContent">
<p>Minify my CSS</p>
</div>
<!-- end myDemo -->
</body>
</html>

```

```
Almost a difference of 48% in the original and minified file. Reduced by 178 bytes.

After Minification
```

```
<html><head><style>#myContent{font-family:Arial;font-size:90%}</style></head>
<body><div id="myContent"><p>Hello world!</p></div></body></html>

```

继续这篇关于缩小 CSS 的文章

## 为什么需要缩小**？**

以缩短网站加载时间。没有人喜欢为了方便而等待网站加载。有这么多选择，人们倾向于换另一个。因此，最好减小文件大小。

继续这篇关于缩小 CSS 的文章

## **如何**缩小 **CSS，JS，HTML 代码？**

简而言之，网上有很多工具可以帮助你减少代码量。您也可以选择手动操作，但对于较大的代码库，建议使用以下任何工具来缩小您的 CSS 文件:

CSSminifier.com:一个非常简单的工具。只需复制左边的代码，生成缩小的文件，并下载它。缩小后的文件扩展名为. min。

缩小后的 CSS 文件的扩展名为 demo.min.css。

Smallseotools.com:复制您的代码或上传您的代码文件。它将缩小你的代码，让你复制或下载它。

自动优化:这是一个你可以添加到你的 WordPress 工具中的插件。作为一个插件，你可以选择缩小你的 CSS 代码。

开发者更容易理解文件何时被缩小，何时不被缩小。缩小文件的扩展名为. min。

继续这篇关于缩小 CSS 的文章

## 你应该什么时候这样做？

缩小应该主要在你写了代码，并且必须把它发送到服务器上以获得响应的时候进行。一旦文件被缩小，缩小的版本被用于分发给用户。

## 缩小的好处**？**

文件大小减少:通过删除多余的空格、减少变量名称和删除注释，文件大小几乎减少了 30-60%。加载速度更快:由于通过网络发送的数据更少，网站加载速度比以前更快。更低的带宽成本:当不必要的数据被删除时，所需的带宽更少，成本也更低。

**需要记住的事情:**

即使在尝试缩小之前，也要确保你的代码不会突破限制。流程不应该中断，功能应该保持匿名。您需要检查一下，即使在缩小后，您的代码也以类似的方式运行。事实上，作为一种最佳实践，你可以随时准备好一个模板。在内置模板中进行更改，这将为您节省大量时间。

**类似压缩吗？**

当然不是。缩小和压缩是不同的。压缩使缩小的文件减少更多，但不影响代码样式和结构。当客户请求访问网站时，文件被缩小，然后压缩成 zip 文件并通过网络发送出去。然后，该文件被解压缩并使用。

**例子:**

**缩小前:**

```
<!DOCTYPE html>
<html>
<head>
<title>Portfolio</title>
<meta charset="utf-8">
<meta name="viewpoint" content="width=device-width", initial-scale="1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.0/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
</head>
<body>
<nav>
<ul>
<li>Home</li>
</ul>
</nav>
</body>
</html>

```

**缩小后:**

```
<!DOCTYPE html><html><head><title>Portfolio</title><meta charset="utf-8">
<meta name="viewpoint" content="width=device-width", initial-scale="1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.0/jquery.min.js">
</script> <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js">
</script></head><body><nav><ul><li>Home</li></ul></nav></body></html>
```

对于人类来说，这些代码肯定更难阅读和理解，但对于机器来说，这些代码同样是可信的。一台机器并不真正关心代码和间距的美观，它理解要点并据此工作。

对缩小技术印象深刻吗？

那你自己试试。减轻你的文件负担，让你的网站为所有用户自由流动！

这就把我们带到了这篇关于 CSS 中的 Minify 的文章的结尾。

如果你有兴趣学习更多关于网络开发的知识，可以看看 Edureka 的 **[网络开发认证培训](https://www.edureka.co/complete-web-developer)** 。 *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

如果你仍然感兴趣，如果你有任何问题，你可以在这个“用 CSS 缩小”博客的评论区发表，我们会尽快回复你。