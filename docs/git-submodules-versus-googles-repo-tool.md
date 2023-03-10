# Git 子模块与 Google 的回购工具

> 原文：<https://www.edureka.co/blog/git-submodules-versus-googles-repo-tool>

最近，一位客户问我使用 [git 子模块](https://git-scm.com/book/en/v2/Git-Tools-Submodules) 与 [google repo](https://code.google.com/p/git-repo/) 工具管理 git 中的多存储库集成的利弊。

互联网上有很多抨击每种工具的文章，但在我们看来，大部分都来自对工具设计的误解，或者试图在不恰当的环境中应用它。

这篇文章总结了我们在 Otomato 为这种公认的重要情况选择解决方案时遵循的一般经验法则。

首先——只要有可能——我们建议在二进制包级别上集成您的组件，而不是每次都从源代码编译所有内容。即:将组件打包到 jar、NPM、eggs、rpms 或 docker 映像，上传到二进制 repo，并在构建期间作为版本依赖关系拉入。

尽管如此——有时这并不是一个最优的解决方案，尤其是如果你做了大量的特性分支开发(这本身就是经典连续交付方法中的一个反模式——例如，参见 [这里的](https://www.thoughtworks.com/insights/blog/enabling-trunk-based-development-deployment-pipelines) )。

对于这些情况，我们坚持以下原则。

## Git 子模块:

**优点:**

1.一个集成的解决方案，从 1.5 版开始就是 git 的一部分

2.确定性关系定义(父项目总是指向子模块中的特定提交)

3.集成点记录在父回购中。

4.易于重建历史配置。

5.父模块和子模块之间生命周期的完全分离。

6.由 jenkins git 插件支持。

**缺点:**

1.管理开销。(需要单独的克隆来引入子模块的变化)

2.如果开发人员不了解内部机制，他们会感到困惑。

3.需要附加命令(“克隆递归”和“子模块更新”)

4.外部工具支撑不完善(、源树、ide 插件】

## 谷歌回购:

**优点:**

1.跟踪同步开发工作更加容易。

2.Gerrit 集成(？)

3.一个独立的 jenkins 插件。

**缺点:**

1.外部模糊机制

2.需要额外的存储库进行管理。

3.非确定性关系定义(每个回购版本可定义为浮动头)

4.很难重建旧版本。

5.不支持 bitbucket 或 gui 工具。

总的来说:每当我们想要集成具有不同生命周期的分离的组件时，我推荐*子模块*而不是*报告*，但是它们的实现必须伴随着关于它们需要的特殊工作流程的适当教育。从长远来看，这是值得的，因为集成点可以用确定性的方式来管理，并且随着知识而来的是工具的确定性。

如果您发现您的组件耦合得太紧，或者您需要在多个回购中同时进行持续的密集开发，那么您可能应该使用 git 子树，或者干脆将所有内容放入一个大的 monorepo 中。(当然，这取决于你的代码库有多大。)

要阅读更多关于 git 子树的内容，请点击[。](http://blogs.atlassian.com/2013/05/alternatives-to-git-submodule-git-subtree/)

需要理解的重要一点是，软件集成从来都不是完全没有痛苦的，也没有治愈痛苦的完美方法。选择让您的生活更轻松的解决方案，并承担学习相关工作流程的责任。正如他们所说:“重要的不是工具，而是你如何使用它。”

我很高兴听到你的想法，因为这是一个有争议的问题，在互联网上有许多不同的观点。

继续送！

*本博客最早出现在 http://otomato.link/git-submodules-vs-googles-repo-tool/*

Edureka 有一个专门策划的 Git 和 Github 课程，由行业专家共同创建。

**相关帖子:**

[【Git’ting Ahead:黑掉 Git 和 GitHub](https://www.edureka.co/blog/git-ting-ahead-hacking-git-and-github-part-1)