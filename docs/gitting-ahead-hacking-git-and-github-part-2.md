# Git'ting Ahead:破解 Git 和 GitHub 第 2 部分

> 原文：<https://www.edureka.co/blog/gitting-ahead-hacking-git-and-github-part-2>

这是黑客攻击 Git 和 GitHub 系列的第二篇文章。在这篇文章中，我们将深入 GitHub markdown 来创建自述文件，添加一个 ***。gitignore*** 文件，了解 Git 最重要的特性:分支。

以下是我们在本系列第一篇文章中涉及的主题的快速回顾:

*   下载和安装 Git
*   在 GitHub 上创建远程存储库
*   暂存文件
*   提交文件
*   将更改推送到远程存储库

在这篇文章中，我们将讨论以下主题:

*   添加自述文件
*   何时使用。gitignore 文件以及如何创建文件
*   为什么使用 Git 分支以及如何使用它

将一个 **README** 文件添加到您的存储库中总是一个好主意，这样其他团队成员可以很容易地识别他们各自存储库中的内容。GitHub 提供了在创建新的存储库时添加一个 **README** 文件的选项。你可以在 **README** 文件中放入纯文本，或者编写一个 [GitHub markdown](https://help.github.com/articles/github-flavored-markdown/ "GitHub Markdown") 来创建一个漂亮的 **README** 文件，包含图片、列表、表格等。

那么如果不添加一个 **README** 文件会怎么样呢？嗯，您必须猜测您的存储库中包含了什么。简而言之，好的存储库总是有很好的文档记录！

现在让我们将一个 **README** 文件添加到我们的 **LiveProject** 存储库中

[![LiveRepo](img/6f10b26aa257439357aa645a6cb382e0.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/LiveRepo.jpg)

这里有一个简单的 **README** 文件。我们需要确保它以 ***< b >结束。MD</b>*分机。**

[![README](img/bd8b406ac9ceec7cc0cb8dd256840b0e.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/README.jpg)

接下来，将 README 更改提交到我们的远程 GitHub 存储库:

[![commiting README changes](img/a29865f6276fe81b4dc0119f4a18c786.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/commiting-README-changes.jpg)

一旦您将 **README** 文件更改推送到远程存储库，这就是您的存储库的外观。

[![README Image](img/2a80a2880fcbc4c244eb9e89fe89fad2.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/README-Image.jpg)

以下是 GitHub 降价的快速备忘单:

***<前置> #*** 为 H1 表头

***#*#**为 H2 表头

…

***# # # # #***为 H6 表头

****此文本将被加粗****

***该文本将为斜体***

–或无序列表的

**1。2.3.对于有序列表**

对于链接换行，链接括号***[]***中的文本，并在括号 ***() < /pre >*** 中提供链接

接下来，我们要学习一下 ***。gitignore*** 文件，我们为什么需要它们以及如何使用它们。

**是什么。gitignore 文件以及我们为什么需要它**

在开发真实项目时，您的项目几乎肯定会包含第三方库作为依赖项，或者包含机密信息的配置文件。您肯定不希望这些文件出现在远程 GitHub 存储库中。为了防止某些文件/文件夹被推送到远程 GitHub 仓库，我们使用了 ***。gitignore*** 文件。

**创建一个. gitignore 文件**

这是一个用 Java 编写的测验应用程序的快照。在这里，我们不希望在 ***下建立******的任何东西。设置*** 文件夹被推送到远程 GitHub 库。为了实现这一点，我们将在我们的 ***中提到这两个文件夹名。git ignore*文件。**

[![quiz-project](img/f2b34f09cc14eea6b6dce4a7d3fe1a0d.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/quiz-project1.jpg)

创建一个**T1。gitignore 从 Git shell 中取出**文件，可以使用如下所示的 touch 命令:

[![touch gitignore](img/c938b87f3f28c8b59d92fd0c2ed03eca.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/touch-gitignore.jpg)

我们只是添加了两行来忽略 ***构建*** 和 ***下的所有内容。设置我们项目目录中的*** 文件夹。

< ***前>。*设置/***

***/</>/前期***

现在让我们添加并提交更改，并将其推送到 GitHub 存储库:

[![committing gitignore file](img/167be76a9c2e986a559755e0d60b3a3d.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/committing-gitignore-file.jpg)

***下没有文件建立******。设置*** 文件夹将被推送到远程资源库，如下所示:

[![poc gitignore](img/9e25553655490fdade439100ac77c98b.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/poc-gitignore.jpg)

接下来，我们将进一步了解 Git 最重要的特性之一:分支。

**为什么分支？**

**问题:**

假设您想要添加/更新***【courses.html】***文件以添加新特性，但是您不想弄乱原来的***【courses.html】***文件。你会怎么做？

[![branching need](img/e02fc6e27f4fc1287c368defa78bad25.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/branching-need.jpg)

传统方法:

很可能你会复制***【courses.html】***文件，并将其重命名为其他名称(在本例中为***【courses2.html】***)。一旦您对***【courses2.html】***中的更改感到满意，您就可以删除***courses.html***文件，并将***courses2.html***重命名为***courses.html***。Git 可以轻松解决这个繁琐的工作流程:

[![courses 2](img/c10a6f83a5fc534c7f457d59637f79da.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/courses-2.jpg)

Git 使用它的分支特性很好地解决了这个问题。现在让我们来看看如何实现这一点。

注意，默认情况下，当我们将任何目录初始化为 Git 存储库时，Git 都会创建主分支。你可以看到使用 **git branch** 命令如下所示:

[![branch1](img/30f301cd234c166ac0a727d3ce775fd8.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/branch1.jpg)

接下来，我们将创建一个新的分支(**新功能**)来进行新的更改，而**一旦我们完成了更改，我们将把新功能分支合并到主分支**。这样，我们可以轻松地进行代码实验，而不会破坏工作代码。

**创建新的分支:**那么让我们创建新的功能分支

[![git new branch](img/23cc9b29379cc11e9fe9a7b834c96a04.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/git-new-branch.jpg)

即使我们已经创建了新分支(newFeature)，git 也不会在分支创建时自动更改工作分支。为了将工作分支更改为 **newFeature** ，我们使用**git check out**命令。

[![git checkout](img/c906269d7e912135509746e42f6699fe.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/git-checkout.jpg)

对于演示，我们刚刚在 courses.html 文件中添加了 h2 头

[![change](img/dc3ddbd7623ed2bbe6edb0a0ffec0228.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/change.jpg)

让我们检查一下状态:

[![change 2](img/a600c08a631bfd1352c1801eba0a8ec0.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/change-2.jpg)

如上所示，我们已经修改了分支新功能上的 courses.html。现在让我们添加一个新文件，因为我们在新功能分支。

[![change5](img/0d705c13d20caa595dac0dc6b62105fe.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/change5.jpg)

现在我们准备好提交变更了。

[![change8](img/90200906de90e9caa12d97759ebbee35.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/change8.jpg)

注意:如果我们切换到主分支，您会看到***【courses.html】***将和以前一样，而***【sitemap.html】***将会缺席。正如我们在 ***newFeature*** 分支而不是 ***master*** 分支中所做的更改。

[![change9](img/f6643b2831a3344b3a8355c373139c45.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/change9.jpg)

现在让我们将更改合并到主分支。为此，切换到主分支并使用如下所示的 **git merge** 命令:

[![merge](img/81eb6e002c09235e1a3073f58eac567d.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/merge.jpg)

在 ***合并*** 操作后，您将能够查看 ***newFeature*** 分支中的变化在 ***master*** 分支中的反映。

[![after merge](img/614f7f62f3613efdf3a3c329f7502627.png)](https://www.edureka.co/blog/wp-content/uploads/2015/12/after-merge.jpg)

这就是关于 Git 的 ***分支*** 特性的所有信息。在下一篇文章中，我们将讨论 ***Git Gists*** 以及如何将 ***GitHub Gists*** 添加到网页中。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[入门掌握 Git 和 Github](https://www.edureka.co/git-github "get started with mastering git and github")

[《Git ' ting Ahead:黑客 Git 与 GitHub Part 1](https://www.edureka.co/blog/git-ting-ahead-hacking-git-and-github-part-1 "Gitting ahead: hacking git and github part 1")