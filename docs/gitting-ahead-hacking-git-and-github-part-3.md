# Git'ting Ahead:破解 Git 和 GitHub 第 3 部分

> 原文：<https://www.edureka.co/blog/gitting-ahead-hacking-git-and-github-part-3>

这是“攻击 Git 和 GitHub”博客系列的第三篇也是最后一篇文章。在本系列的前几篇博客中，我们已经介绍了 Git 和 GitHub 的一些非常重要的特性，在本帖中，我们将通过介绍以下内容来完善它:

1.  克隆 GitHub 存储库
2.  派生 GitHub 存储库
3.  创建 GitHub Gist
4.  了解如何在网页上嵌入 Gist

在我们讨论如何克隆一个 GitHub 库之前，我们需要问的问题是为什么我们甚至需要克隆一个库。

## 为什么要克隆 GitHub 库？

假设您想使用 GitHub 上的一些代码作为公共存储库，您可以使用 GitHub 的克隆特性将该存储库的内容复制到您的本地系统。

## 如何克隆一个 GitHub 库？

假设我们想使用用户 curran 的截屏存储库的代码:

![curran-git-and-github](img/ffd0ee9c7d9c31dfd0ad7b6d26663661.png)

我们可以将所有的截屏存储库的代码克隆到我们的本地系统中，这是一个如何实现的例子。

我们创建一个本地文件夹 curranD3，将当前目录更改为 curranD3，并在 curranD3 下克隆远程存储库:

![local-folder-git-and-github](img/6871b71a7ca4dbaea691eda7c0147619.png)

将整个存储库克隆到本地系统后，您会注意到所有代码都被复制到了 screencasts 文件夹下，如下所示:

![screencasts-folder-git-and-github](img/8f0f3bb1c0d6cfe44c4b5e205b52ee95.png)

接下来，我们将讨论如何派生 GitHub 存储库，并了解何时需要这样做:

## 为什么要分叉 GitHub 库？

很多时候，您可能需要为已经可用的项目创建自己的 GitHub 存储库。为此，我们可以派生原始的 GitHub 存储库，在我们自己的 GitHub 帐户下创建一个。

在我们开始如何派生存储库之前，有一些关于派生的要点需要注意

1.  对原始存储库所做的任何更改都将反映到您的分叉存储库中。
2.  如果您对分叉的存储库进行任何更改，它将不会反映回原始存储库，除非您发出一个拉请求。

## 如何分叉一个 GitHub 库？

派生 GitHub 库非常简单。我们将使用相同的存储库(curran 的 screencasts 存储库),但这次我们将分叉它。要派生 GitHub 存储库，只需点击 GitHub 存储库右上角的 fork 链接。

![fork-a-GitHub-repository-git-and-github](img/b8ca24d1f22d161dc2bc587689975c4c.png)

请注意，柯伦的截屏回购已经被分叉 1507 倍。让我们通过单击 fork 链接来派生它，您将看到我们帐户下的存储库，如下所示:

![fork-link-git-and-github](img/a609f0b3071585e25a27b64b7d4d905c.png)

接下来我们要学习 Github Gist，了解它是什么，怎么用？

## 什么是 GitHub 要点？

Gists 是分享你作品的好方法。您可以共享单个文件、部分文件或整个应用程序。其他人可以搜索 gists。你可以在[https://gists.github.com](https://gist.github.com/)访问 gist。Gists 通常用于共享小块代码。有两种类型的 gists 公开和秘密。

公共 gist 出现在 Discover 中，人们可以浏览新创建的 gist。它们也是可搜索的，所以如果你想让其他人找到并看到你的作品，你可以使用它们。

秘密秘笈不会出现在 Discover 中，也不可搜索。但是请注意，秘密 gists 不是私人的。如果你把秘密要点的网址发给朋友，他们就能看到。

创建要点:创建要点非常简单。只需点击 GitHub 页面上的 Gist 链接。

![creating-a-gist-git-and-github](img/e04b6e2f91323c61d186ea47682878f2.png)

这里，我们创建了一个名为 age-dob.js 的 GitHub gist，它根据给定的出生日期计算年龄。请注意，我们会自动突出显示 JavaScript 语法，因为我们已经使用了扩展**。带有要点名称的 js** 。**点击创建公共要点，创建公共要点。**

![public-gist-git-and-github](img/2373779eb47a3149b5ae75ca34cc398a.png)

**访问您所有的积分:**您可以在【https://gist.github.com/GITHUB_USERNAME】的 **访问您所有的积分**

![access-gists-git-and-github](img/b958c859003f3677a8b1fd8f76e756f8.png)

## 如何在网站上使用 GitHub Gist？

假设你想在你的网站上展示 GitHub gist，你需要做的就是在你的网站上嵌入 GitHub gist，点击嵌入选项，如下所示:

![using-a-GitHub-gist-git-and-github](img/5c0fa912f49e6fdd592f7adb50c9d7e2.png)

复制链接，并在 HTML 文件中使用该链接将 GitHub gist 嵌入到网页中，如下所示:

![GitHub-gist-git-and-github](img/3a24dcc8013ea0036d0aff91e231a800.png)

这就是嵌入式 GitHub gist 的外观。要点。

![embedded-GitHub-gist-git-and-github](img/7ca545a0ebb4707cc81365b32446baef.png)

这就是这篇文章的全部内容，希望你喜欢它，并发现它有所帮助。万事如意！

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[入门掌握 Git 和 Github](https://www.edureka.co/git-github "get started with mastering git and github")

[《Git ' ting Ahead:黑客 Git 与 GitHub Part 1](https://www.edureka.co/blog/git-ting-ahead-hacking-git-and-github-part-1 "hacking Git and Github")

[《Git ' ting Ahead:黑客 Git 与 GitHub Part 2](https://www.edureka.co/blog/gitting-ahead-hacking-git-and-github-part-2 "hacking Git and Github")