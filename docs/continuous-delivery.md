# 持续交付教程–使用 Jenkins 构建持续交付渠道

> 原文：<https://www.edureka.co/blog/continuous-delivery/>

## **连续交货:**

连续交付是一个过程，其中代码变更被自动构建、测试，并为产品发布做好准备。 我希望你喜欢我以前在 Jenkins 上的 **[博客。](https://www.edureka.co/blog/what-is-jenkins/)** 在这里，我将谈论以下话题::

*   什么是持续交付？
*   软件测试的类型
*   持续集成、交付和部署的区别
*   持续交付的需求是什么？
*   动手使用 Jenkins 和 Tomcat

让我们快速了解连续交付是如何工作的。

## **什么是连续交割？**

这是一个过程，在这个过程中，你以一种可以在任何时候发布到生产环境的方式来构建软件。考虑下图:

![Continuous Delivery - Continuous Delivery - Edureka](img/4b02746f8d4fc12a9a6e6900baa49104.png)

我来解释一下上图:

*   自动化构建脚本将会检测像 Git 这样的源代码管理(SCM)中的变化。
*   一旦检测到变更，源代码将被部署到专用的构建服务器，以确保构建不会失败，并且所有测试类和集成测试都运行良好。
*   然后，在测试服务器(预生产服务器)上部署构建应用程序，进行用户验收测试(UAT)。
*   最后，应用程序被手动部署到生产服务器上进行发布。

在我继续之前，为了公平起见，我向你解释一下不同类型的测试。

## **软件测试类型:**

从广义上讲，有两种类型的测试:

*   **黑盒测试:**是一种忽略系统内部机制，针对系统的任何输入和执行，专注于产生的输出的测试技术。它也被称为功能测试。它主要用于验证软件。
*   **白盒测试:**是一种考虑到系统内部机制的测试技术。它也被称为结构测试和玻璃盒测试。它基本上用于验证软件。

### **白盒测试:**

属于这一类的测试有两种。

*   **单元测试:**对单个单元或一组相关单元的测试。程序员经常测试他/她所实现的单元是否在给定的输入下产生预期的输出。
*   集成测试:将一组组件 组合起来产生输出的一种测试。此外，如果软件和硬件组件有任何关系，则测试软件和硬件之间的交互。它可能属于白盒测试和黑盒测试。

### **黑盒测试:**

有多种测试属于这一类别。我将重点介绍几个，这些对你了解很重要，以便理解这个博客:

*   **功能/验收测试:**确保系统需求中规定的功能正常工作。这样做是为了确保交付的产品符合要求，并如客户预期的那样工作
*   **系统测试:**它确保将软件放在不同的环境中(例如操作系统)它仍然能工作。
*   **压力测试:**评估系统在不利条件下的表现。
*   **Beta 测试:**由最终用户、开发团队之外的团队完成，或者公开发布产品的完整预版本，称为 beta 版本。测试的目的是覆盖意外的错误。

现在是我解释持续集成、交付和部署之间区别的正确时机。

## **持续集成、交付和部署的区别:**

视觉内容比文本信息更快、更容易理解地到达个人的大脑。所以我将从一张图开始，它清楚地解释了两者的区别:

![Continuous Integration vs Continuous Delivery vs Continuous Deployment - Continuous Delivery - Edureka](img/e35590e39031517e8f1ef4106114491d.png)

在持续集成中，每一个提交的代码都被构建和测试，但是并不处于发布的状态。我的意思是，构建应用程序不会自动部署在测试服务器上，以便使用不同类型的黑盒测试(如用户验收测试(UAT))来验证它。

在连续交付中，应用程序被持续部署在 UAT 的测试服务器上。或者，您可以说该应用程序随时可以发布到生产环境中。因此，显然持续集成对于持续交付是必要的。

连续部署是连续交付之后的下一步，在这一步中，您不仅仅是创建一个可部署的包，而是实际上以自动化的方式部署它。

让我用一个表格总结一下不同之处:

| **持续集成** | **连续交货** | **连续部署** |
| 自动构建，提交 | 自动构建和 UAT for every，commit | 自动构建、UAT 和发布到生产环境，提交 |
| 独立于连续交付和连续部署 | 持续集成后的下一步 | 这是更进一步的连续交货 |
| 最后，应用程序不具备发布到生产环境的条件 | 最后，应用程序处于可以发布到生产环境的状态。 | 应用程序持续部署 |
| 包括白盒测试 | 包括黑盒和白盒测试 | 它包括部署应用程序所需的整个过程 |

简单来说，持续集成是持续交付和持续部署的一部分。持续部署类似于持续交付，除了发布是自动发生的。

了解如何使用云上的 Jenkins 创建 CI/ CD 管道 [<button>立即成为认证 DevOps 工程师</button>](https://www.edureka.co/masters-program/devops-engineer-training)

但问题是，持续集成是否足够。

## **为什么我们需要连续交货？**

让我们用一个例子来理解这一点。

想象一下，有 80 名开发人员在一个大型项目上工作。他们使用持续集成管道来促进自动化构建。我们知道构建也包括单元测试。有一天，他们决定将通过单元测试的最新构建部署到测试环境中。

这肯定是一个漫长但受控的部署方法，由他们的环境专家来执行。然而，该系统似乎并没有发挥作用。

### **失败的明显原因可能是什么？**

嗯，大部分人会认为的第一个原因是配置有问题。像大多数人一样，即使他们也这样认为。他们花了很多时间试图找到环境的配置有什么问题，但是找不到问题。

### **![Why We Need Continuous Delivery - Continuous Delivery - Edureka](img/6d78300bf56f588721a739354f8928e1.png)**

### **一个有洞察力的开发者采取了一个聪明的方法:**

然后，一位高级开发人员在他的开发机器上试用了这个应用程序。在那里也行不通。

他回顾了越来越早的版本，直到他发现系统在三周前就停止了工作。一个微小的、不明显的错误阻止了系统正确启动。虽然，这个项目有很好的单元测试覆盖率。尽管如此，80 名通常只运行测试而不运行应用程序本身的开发人员在三周内没有发现问题。

### **问题陈述:**

没有在类似生产的环境中运行验收测试，他们对应用程序是否符合客户的规格一无所知，也不知道它是否能在现实世界中部署和生存。如果他们想要得到关于这些主题的及时反馈，他们必须扩展他们持续集成过程的范围。

我来总结一下看以上问题的经验教训:

*   单元测试只测试开发人员对问题解决方案的观点。从用户的角度来看，他们只有有限的能力来证明应用程序做了它应该做的事情。它们不足以识别真正的功能问题。
*   在测试环境中部署应用程序是一个复杂的手动密集型过程，很容易出错。这意味着每一次部署尝试都是一次新的尝试——一个手动的、容易出错的过程。

## **解决方案——连续交付管道(自动化验收测试):**

他们将持续集成(持续交付)推进到下一步，引入了几个简单的自动化验收测试，证明应用程序能够运行并执行其最基本的功能。验收测试阶段运行的大多数测试都是功能验收测试。

![Continuous Delivery Pipeline - Continuous Delivery - Edureka](img/c6417229ca49492d64df4bcc398632f3.png)

基本上，他们构建了一个连续的交付管道，通过确保应用在测试服务器(生产服务器的副本)上部署时运行良好，来确保应用在生产环境中无缝部署。

*理论到此为止，我现在将向您展示如何使用 Jenkins 创建一个连续的交付管道。*

## **连续输送管道使用詹金斯:**

在这里，我将使用 Jenkins 创建一个连续的交付管道，其中将包括以下任务:

### **演示中涉及的步骤:**

*   从 GitHub 获取代码
*   编译源代码
*   单元测试并生成 JUnit 测试报告
*   将应用程序打包成一个 WAR 文件，并将其部署在 Tomcat 服务器上

![Continuous Delivery Use Case - Continuous Delivery - Edureka](img/6ce24e98636dc2beaa949dbe5a5a0a06.png)

先决条件:

*   CentOS 7 机
*   詹金斯 2.121.1
*   码头工人
*   Tomcat 7

### **Step–1 编译源代码:**

让我们首先在 Jenkins 中创建一个自由式项目。考虑下面的截图:

![Jenkins New Project - Continuous Delivery - Edureka](img/b22bffc290541b89feb20c46610faac2.png)

为您的项目命名，并选择自由式项目:

![Freestyle Project Jenkins - Continuous Delivery - Edureka](img/e48883638307ee022338ab5732959191.png)

当你向下滚动时，你会发现一个添加源代码库的选项，选择 git 并添加库 URL，在该库中有一个 pom.xml fine，我们将使用它来构建我们的项目。考虑下面的截图:

![Git Jenkins Integration - Continuous Delivery - Edureka](img/75d209353d471ce84c8f54956296349f.png)

现在我们将添加一个构建触发器。选择轮询 SCM 选项，基本上，我们将配置 Jenkins 每隔 5 分钟轮询一次 GitHub 存储库的代码变化。考虑下面的截图:

![Build Trigger In Jenkins - Continuous Delivery - Edureka](img/a9fde551c103fbef8120bdffbed3fc26.png)

在我继续之前，让我简单介绍一下 Maven 的构建周期。

每个构建生命周期由不同的构建阶段列表定义，其中一个构建阶段代表生命周期中的一个阶段。

以下是构建阶段列表:

*   验证–验证项目是否正确，所有必要信息是否可用
*   编译——编译项目的源代码
*   测试——使用合适的单元测试框架测试编译后的源代码。这些测试不需要打包或部署代码
*   打包——将编译好的代码打包成可分发的格式，比如 JAR。
*   验证——对集成测试的结果进行检查，以确保符合质量标准
*   install——将包安装到本地存储库中，作为本地其他项目的依赖项使用
*   deploy——在构建环境中完成，将最终的包复制到远程存储库，以便与其他开发人员和项目共享。

我可以运行下面的命令，用于编译源代码、单元测试，甚至将应用程序打包到一个 war 文件中:

```
mvn clean package
```

你也可以将你的构建工作分解成许多构建步骤。这使得在干净、独立的阶段中组织构建变得更加容易。

所以我们将从编译源代码开始。在 build 选项卡中，单击 invoke top level maven targets 并键入下面的命令:

```
compile
```

考虑下面的截图:

![Compile Source Code - Continuous Delivery - Edureka](img/0e87ed56d811958394080ab9ea6ac67a.png)

这将从 GitHub 库中提取源代码，并且还会编译它(Maven 编译阶段)。

点击保存并运行项目。

![Build A Freestyle Project - Continuous Delivery - Edureka](img/1eec7f3c58137cfc9409cfd4cc0855ed.png)

现在，点击控制台输出来查看结果。

![Compile Output - Continuous Delivery - Edureka](img/91264d70da29d85fcbb63baf6bce46df.png)

### **第二步单元测试:**

现在我们将为单元测试再创建一个自由式项目。

在源代码管理选项卡中添加相同的存储库 URL，就像我们在之前的工作中所做的那样。

现在，在“Buid Trigger”选项卡中点击“在其他项目都构建好之后再构建”。在这里输入我们正在编译源代码的前一个项目的名称，你可以选择下面的任何一个选项:

*   仅当构建稳定时触发
*   即使构建不稳定也触发
*   即使构建失败也触发

我认为以上选项都是不言自明的，所以请选择任何一个。考虑下面的截图:

![Build Trigger, After Other Projects - Continuous Delivery - Edureka](img/1c134cfbfa17be672a204ad17082e4db.png)在构建选项卡中，点击调用顶级 maven 目标并使用下面的命令:

```
test

```

Jenkins 在帮助您显示测试结果和测试结果趋势方面也做得很好。

Java 世界中测试报告的事实标准是 JUnit 使用的 XML 格式。许多其他 Java 测试工具也使用这种格式，比如 TestNG、Spock 和 Easyb。Jenkins 理解这种格式，所以如果您的构建产生了 JUnit XML 测试结果，Jenkins 可以生成漂亮的图形化测试报告和测试结果的统计数据，还可以让您查看任何测试失败的细节。Jenkins 还跟踪您的测试运行了多长时间，包括全局的和每次测试——如果您需要跟踪性能问题，这将非常有用。

所以我们需要做的下一件事是让 Jenkins 关注我们的单元测试。

转到 Post-build Actions 部分，勾选“Publish JUnit test result report”复选框。当 Maven 在一个项目中运行单元测试时，它会在一个名为 surefire-reports 的目录中自动生成 XML 测试报告。所以输入“**/target/surefire-reports/*。“测试报告 xml”字段中的“XML”。路径开头的两个星号(“**”)是使配置更加健壮的最佳实践:它们允许 Jenkins 找到目标目录，不管我们如何配置 Jenkins 来检查源代码。

```
**/target/surefire-reports/*.xml
```

![XML Reports - Continuous Delivery - Jenkins](img/291f836e0dae30f534d6aef40b7b95e3.png)

再次保存并点击立即构建。

![Test Results - Continuous Delivery - Jenkins](img/de7f0023be8c1cf16e5a8ae199f7f6a1.png)

现在，JUnit 报告被写到/var/lib/Jenkins/workspace/TEST/gameoflife-core/target/surefire-reports/TEST-behavior。

![XML Reports Output - Continuous Delivery - Jenkins](img/147e88c7920dc36bf0390fcd7cb80f09.png)

在 Jenkins 仪表盘 中，您还可以注意到测试结果:

![est Results In UI- Continuous Delivery - Jenkins](img/fedb964c29b6c3f612e1da28184a183b.png)

![Further Test Results - Continuous Delivery - Edureka](img/4906591a467ad29b81cd6b9c9d6d31ab.png)

## **第三步创建 WAR 文件并部署在 Tomcat 服务器上:**

现在，下一步是将我们的应用程序打包到一个 WAR 文件中，并部署到 Tomcat 服务器上进行用户验收测试。

再创建一个自由式项目，并添加源代码库 URL。

然后在 build trigger 选项卡中，选择 build when other projects build，考虑下面的截图:

![Build When Other Projects Are Built - Continuous Delivery - Edureka](img/1ab9e7e9bb3bfa164d263e1b000d3a67.png)

基本上，测试工作结束后，部署阶段将自动开始。

在构建选项卡中，选择 shell 脚本。键入以下命令将应用程序打包到一个 WAR 文件中:

```
mvn package
```

![Package Application - Continuous Delivery - Edureka](img/f0736e7a222ee0d216b5447fa98601ec.png)

下一步是将这个 WAR 文件部署到 Tomcat 服务器上。在“后期构建操作”选项卡中，选择将 war/ear 部署到容器。在这里，给出 war 文件的路径，并给出上下文路径。考虑下面的截图:

![Deploy The WAR File To The Tomcat Server - Continuous Delivery - Edureka](img/3f444fda6eaf25f514d806f9eb019bb0.png)

选择 Tomcat 凭证，注意上面的屏幕截图。另外，您需要给出您的 Tomcat 服务器的 URL。

要在 Jenkins 中添加凭证，点击 Jenkins 仪表板上的凭证选项。

![Adding Jenkins Credentials - Continuous Delivery - Edureka](img/d6239204e9043de27f4aa808c8b76125.png)

点击系统并选择全局凭证。

![Global Credentials - Continuous Delivery - Edureka](img/caf1a3616e4f328f12f5343d426ff99a.png)

然后你会发现一个添加凭证的选项。点击它并添加凭证。

![Adding Credentials - Continuous Delivery - Edureka](img/7d9c56d7b8bf430bbbb280ae3f0f3961.png)

添加 Tomcat 凭证，考虑下面的截图。

![Tomcat Credentials In Jenkins - Continuous Delivery - Edureka](img/b0e425cc5af9bbddf4000e7d66ff703d.png)

点击确定。

现在，在您的项目配置中，添加您在上一步中插入的 tomcat 凭证。

![Deploy The WAR File To The Tomcat Server - Continuous Delivery - Edureka](img/3f444fda6eaf25f514d806f9eb019bb0.png)

点击保存，然后选择立即构建。

![Deploy Output - Continuous Delivery - Jenkins](img/d09a769c62c93c5c4518186db7859bce.png)

进入您的 tomcat URL，带有上下文路径，在我的例子中是 http://localhost:8081。现在在最后添加上下文路径，考虑下面的截图:

![Deployed Application - Continuous Delivery - Edureka](img/f06476dae2925dff8e17d08117cad42d.png)

```
Link - http://localhost:8081/gof
```

我希望你已经理解了上下文路径的含义。

现在创建一个管道视图，考虑下面的截图:

*![Pipeline-View-Continuous-Delivery-Edureka](img/6d5201559f1b4322d934423e71305a00.png)*

点击加号图标，创建一个新视图。

按照您想要的方式配置管道，考虑下面的截图:

![Build Pipeline Configuration - Continuous Delivery - Edureka](img/317c4703fa75acb6daedf6f44d052639.png)

除了选择最初的工作，我没有做任何改变。所以我的管道会从编译开始。基于我已经配置的其他作业的方式，编译后测试和部署将会发生。

最后，您可以通过点击 RUN 来测试管道。每五分钟后，如果源代码有变化，将执行整个管道。

*![Continuous Delivery Pipeline - Continuous Delivery - Edureka](img/fce10c87caebca6897db36c16051f54c.png)*

因此，我们能够在测试服务器上持续部署我们的应用程序，以进行用户验收测试(UAT)。T3T5

*我希望你喜欢阅读这篇关于连续交货的文章。如果你有任何疑问，请在下面的评论区提出，我会尽快给你答复。*

为了构建 CI/ CD 管道，您需要掌握各种各样的技能 [<button>现在就掌握所需的 DevOps 技能</button>](https://goo.gl/zQwzEz)