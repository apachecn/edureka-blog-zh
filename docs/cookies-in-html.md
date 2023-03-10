# 在 HTML 中设置 Cookies:您需要了解的所有内容

> 原文：<https://www.edureka.co/blog/cookies-in-html/>

Cookies 是利用你以前数据的好方法。在这篇文章中，我们将按照以下顺序来理解 HTML 中的 Cookies:

*   [HTML 中的 Cookies 是什么？](#what)
*   [cookie 的工作方式](#working)
*   [HTML 中的 Cookies:代码](#code-1)
*   [设置作者姓名](#code-2)

## **HTML 中的 Cookies 是什么？**

这些是储存在计算机小文本文件中的数据。发明 cookies 是为了记住用户的信息。因为当一个网络服务器发送一个网站给浏览器时，如果它由于任何外部因素而关闭，那么服务器就会忘记关于用户的一切。

![Cookies-in-HTML](img/897c9958feab6c55be36d01ee1d219c2.png)

为了克服这个问题，创建了这些 cookies 来存储这些信息。

## **cookie 的工作方式**

当用户访问一个网页时，他的名字将被存储在 cookie 中。如果同一用户再次访问该网页，则该网页记住该用户并提供与先前搜索的项目相关的相关提要。这些 cookies 在 web 浏览器和 web 服务器之间交换，以根据 web 应用程序的需要跟踪不同的信息。Cookies 以名称-值对的形式保存，如:

`username = Edureka don`

当浏览器向服务器请求网页时，属于该网页的 cookies 会被添加到请求中。通过这种方式，服务器可以获得必要的数据来“记住”用户的信息。

标签可以用来在客户端存储 cookies。服务器使用这些 cookies 来跟踪网站访问者。因此，在一些网站上总会弹出一个窗口，询问你使用 cookies 的政策。

## HTML 格式的 Cookies:代码

5 秒钟后将当前页面重定向到另一个页面的示例:

```
<!DOCTYPE html>
<html>
		<head>
			<title>Meta tags </title>
			<meta name="keywords" content="HTML, Meta Tags, Metadata" />
			<meta name="description" content="Learning about Meta Tags." />
			<meta name="revised" content="tutorialpoint, 24/8/2019" />
			<meta http-equiv="cookie" content="useri8d=xyz; expires=sunday, 24-Sep-19 3:59:59 GMT;" />

		</head>
		<body>

Style is done to this text.

		</body>
</html>

```

如果未包含到期日期和时间，cookie 将被视为会话 cookie ，并将在用户退出浏览器后立即删除。这是一种信息的临时存储。

## **设置作者姓名**

```
<!DOCTYPE html>
<html>
		<head>
			<title>Meta tags </title>
			<meta name="keywords" content="HTML, Meta Tags, Metadata" />
			<meta name="description" content="Learning about Meta Tags." />
			<meta name="author" content="Avinash" />

		</head>
		<body>

Hello HTML5!

		</body>
</html>

```

至此，我们结束了这篇 HTML 格式的 Cookies 文章。C *查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“什么是 HTML？”的评论部分提及。我们会回复你的。*