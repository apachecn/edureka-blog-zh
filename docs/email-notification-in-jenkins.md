# 如何通过 6 个简单的步骤在 Jenkins 中配置电子邮件通知？

> 原文：<https://www.edureka.co/blog/email-notification-in-jenkins/>

詹金斯无疑是***[devo PS](https://www.edureka.co/devops)***中最受欢迎的工具之一。它可以以更快的速度自动构建和测试代码，因此软件公司可以加快他们的开发过程。Jenkins 为您提供了电子邮件通知服务，您可以通过它向团队报告构建状态和测试结果。在这篇关于 Jenkins 中的电子邮件通知的文章中，我们将要涉及的要点如下:

*   **[为什么我们在 Jenkins 中需要邮件通知？](#whyemail)**
    *   **[詹金斯面前的问题](#problem)**
    *   **[解与詹金斯](#solution)**
*   **[如何在 Jenkins 中使用电子邮件服务？](#howemail)T3**

在我开始这篇关于 Jenkins 中的电子邮件通知的文章之前，这里有几个涵盖 Jenkins 基本知识的博客:

1.  **[詹金斯是什么？](https://www.edureka.co/blog/what-is-jenkins/)**
2.  **[使用詹金斯](https://www.edureka.co/blog/continuous-delivery/)连续交货**

让我们从第一个话题开始。

## **为什么我们在 Jenkins 中需要电子邮件通知？**

### **问题陈述:**

*   假设应用程序的发布安排在午夜。现在，测试服务器或生产服务器上的应用程序出现了问题。此外，可能会有这样的情况，应用程序发布后几个小时就关闭了。如果应用程序(例如网飞)宕机几分钟，就可能导致数百万美元的损失。同样由于这样的错误，项目的最后期限可能会延长。

### **解决方案**

![architecture - Email notifications in Jenkins - Edureka](img/9c6397eed08bdad47b377b158fca8b31.png)

*   这个问题被一个叫做[詹金斯](https://jenkins.io/)的自动化工具解决了。Jenkins 提供电子邮件通知服务来处理这种情况。

*   如果构建不成功，那么开发团队会被告知构建的状态。这可以在 Jenkins 的电子邮件插件的帮助下完成。**插件** 是增强 **詹金斯** 环境功能以适应组织或用户特定需求的主要手段。

*   使用电子邮件插件，您可以配置在构建失败时应该通知的相关人员的电子邮件详细信息。

*   一旦开发人员得到错误通知，他就修复错误并再次将代码提交给 GitHub。在这之后，Jenkins 再次从 GitHub 中取出代码并准备一个新的构建。

*   类似地，Jenkins 可以通过电子邮件通知相关团队来解决发布后应用程序宕机的问题。

现在让我们看看如何在 Jenkins 中发送电子邮件通知。

## **如何在 Jenkins 中发送邮件通知？**

在 Jenkins 中配置电子邮件通知基本上有两种方式。

1.  **使用电子邮件扩展插件**–这个[插件](https://plugins.jenkins.io/)可以让你配置电子邮件通知的方方面面。您可以自定义诸如何时发送电子邮件、由谁接收以及电子邮件内容等内容。

2.  **使用默认电子邮件通知程序**–这是 Jenkins 默认提供的。它有一个由内部版本号和状态组成的默认消息。

### **电子邮件扩展插件**

#### **第一步:登录詹金斯主页**

使用 URL localhost:8080 转到 Jenkins 主页。默认端口号是 8080。我的情况是 9191。使用您的用户名和密码登录。

#### **第二步:安装电子邮件扩展插件**

之后在 Jenkins 主页上点击**管理 Jenkins- >管理插件**。在可用选项卡中搜索电子邮件扩展插件。如果在那里找到它，就安装它。如果没有找到，请在“已安装”选项卡中查找。![](img/30f759e013d0d908818e642daa86cf92.png)

#### **第三步:配置系统**

现在进入**管理詹金斯- >配置系统**。在这里向下滚动到电子邮件通知部分。如果您使用的是 Gmail，请为 SMTP 服务器键入 smtp.gmail.com。点击高级并选择使用 SMTP 认证。输入您的 Gmail 用户名和密码。选择使用 **SSL** 选项，输入端口号为 **465** 。单击应用，然后单击保存。

![](img/fc89189a29a0656bab9b7502cdf912b7.png)

#### **步骤 4:创建 Jenkins 管道作业**

现在转到 Jenkins 主页，创建一个新工作。使用您想要的任何名称命名作业，然后选择“管道”。点击确定。![](img/07d1f49389841ba2113045d78450cb6f.png)

现在，在管道部分键入以下代码。

```
pipeline {
    agent any

    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
    }
    post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
        }
    }
}

```

任何詹金斯特工都有这条管道。它有一个取样的阶段。在 post 步骤中，您可以运行任何想要的脚本。我们有邮件发送者在里面。保存并运行点击“工作”菜单上的“立即构建”。该构建将出现在舞台视图中。

![build output - Email Notifications in Jenkins - Edureka](img/f7262c1ec1be84506ed3b9340441729f.png)

#### **步骤 5:查看控制台输出**

单击内部版本号“#1”，然后单击“内部版本”菜单上的“控制台输出”。输出将是这样的:![console output - Email Notifications in Jenkins - Edureka](img/7a4b1f2b19cdb579169d31a46ab75590.png)

#### 第六步:查看电子邮件。

之后，进入你的 Gmail 收件箱，应该能看到这样一封邮件。![Test Email - Email Notifications in Jenkins - Edureka](img/e3cabe38d3df385b49bc196e1214809d.png)

### **默认电子邮件通知程序**

#### **第一步:登录詹金斯主页**

去詹金斯主页。

#### **第二步:配置系统**

点击**管理詹金斯- >配置系统**。在这里向下滚动到电子邮件通知部分。现在输入细节如下图![](img/2a42e50fbadf70277de1150fe574931f.png)

一旦设置好邮件配置，您可以通过发送测试邮件检查  **测试配置来测试它是否工作正常。**

#### **步骤 3:在项目中添加后期生成操作**

要允许您的项目发送电子邮件，您需要添加  **Post Build Action** ，并从下拉列表中选择**电子邮件通知**。这将为您提供下面的界面，在这里您可以添加一个电子邮件地址的列表，电子邮件需要发送到。![](img/e3c8e74839f96314b964bb0cb34effbf.png)

#### **步骤 4:构建项目并检查您的电子邮件**

现在尝试运行您添加了电子邮件的项目。如果构建失败，您将收到一封关于构建失败的电子邮件。![](img/727898c8a11d794a9f4267415a2e819f.png)

这就是在 Jenkins 中设置电子邮件通知的方式。这是我在这篇文章中的观点。我希望你喜欢它，并理解我在这里解释的一切。

*如果您在 Jenkins 中找到了这个“**电子邮件通知”*** *相关信息，请查看 Edureka 的* [***DevOps 培训***](https://www.edureka.co/devops/) *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka DevOps 认证培训课程可帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Nagios 和 GIT，用于自动化 SDLC 中的多个步骤。*

*有问题吗？请在评论区提到它，我们会给你回复。*