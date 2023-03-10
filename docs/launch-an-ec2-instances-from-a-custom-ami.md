# 如何从定制 AMI 启动 EC2 实例？

> 原文：<https://www.edureka.co/blog/launch-an-ec2-instances-from-a-custom-ami/>

[云](https://www.edureka.co/blog/how-to-become-a-cloud-engineer/)与敏捷性息息相关。快速创建各种规模的新服务器并在其上部署应用程序就是其中之一。以网飞为例，它由 AWS 托管。每当有受欢迎的节目或电影，网飞就会使用[自动缩放](https://www.youtube.com/watch?v=-hFAWk6hyZA&t=670s)来添加越来越多的 ec2，以满足客户需求。根据尝试访问网飞服务的用户数量，自动缩放功能可以自动添加或删除 EC2 实例。让我们看看如何从定制 AMI 启动 EC2 实例？

本文将涉及以下几点:

*   将应用程序放到 EC2 实例上有哪些不同的方法？
*   创建自定义 AMI 的演示？

那么，让我们从关于如何从定制 AMI 启动 EC2 实例的文章开始吧。

## 将应用程序放到 EC2 实例上有哪些不同的方法？

应用程序是如何自动安装在 EC2 上的？如下所述，有多种方法可以在 EC2 实例上获得应用程序和设置。

*   使用配置管理工具如 Puppet 和 Chef 来管理应用程序的生命周期。使用这些配置管理工具，可以在数千台机器上安装、升级和回滚应用程序。

*   通过将[用户数据](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html)传递给 EC2 实例。用户数据可以是安装应用程序的 shell 脚本，并将在 EC2 启动时执行。

最后一个选项是使用 EC2 AMI (Amazon 机器映像)，AMI 拥有所有信息，如操作系统、附加的 EBS 磁盘、应用程序和相应的设置。AMI 是启动 EC2 实例所需要的。与上述两种方法相比，使用 AMI 是启动 EC2 实例的最快方法，因为 AMI 已经拥有启动 EC2 实例的所有细节。本教程介绍了创建 AMI 的一系列步骤。

![Image - How to Launch an EC2 Instance From a Custom AMI - Edureka](img/b8776028abf0bc7c5abe796bcaa0b093.png) 现在让我们进入演示部分，

## 如何从定制 AMI 启动 EC2 实例:关于创建定制 AMI 的演示？

AWS 为我们提供了一套适用于 Windows 和 Linux 的 ami。根据需求，还可以用附加软件和配置设置创建定制的 AMI。下面是创建 AMI 的高级步骤序列。

**步骤 1:** 从一个现有的 AMI 启动一个 EC2 实例并登录到它。

**步骤 2:** 安装应用程序，并进行适当的配置更改。

**第三步:**创建一个新的 AMI。

**步骤 4:** 通过使用在**步骤 3** 中创建的 AMI 启动额外的 EC2 实例。

![Image - How to Launch an EC2 Instance From a Custom AMI - Edureka](img/2e42c46ec13475f23d6749d25fdd72ce.png)

以下是详细步骤:

**步骤 1:启动 EC2 实例**

使用现有的 AWS 提供的 AMI (Windows 或 Linux)来启动 EC2 实例，并登录到 Edureka 教程中提到的用于 [EC2](https://www.edureka.co/blog/ec2-aws-tutorial-elastic-compute-cloud/) 的实例。

**步骤 2:在 EC2 上安装应用程序**

登录到 EC2 实例后，按照您的要求安装任何应用程序。以下命令用于在 Ubuntu EC2 实例上安装 Apache Tomcat。Apache Tomcat 可用于使用 JSP 和 Servlets 构建动态网页。同样，可以安装任何其他软件。

*#成为根须藤苏*

*#获取软件和最新补丁列表 apt-get 更新& & apt-get 升级*

*#下载安装 Apache Tomcat apt-get 安装 tomcat8*

Tomcat 安装可以通过在浏览器中访问(ec2-ip:8080) URL 来验证，Tomcat 主页应该如下所示。确保用 ec2 实例的适当公共 ip 替换 ec2-ip。端口 8080 应该在安全组的入站规则中与端口 22 一起打开，如下面安全组的“入站规则”所示。端口 22 用于 SSH 访问，端口 8080 用于访问 Tomcat。

**![](img/ca73e2582510a3431125d9435bd3e30b.png)**

**![](img/36098635463d22777c272b1e98f20050.png)**

**步骤 3:创建自定义 AMI**

**步骤 3.1:** 选择 EC2 实例，转到“操作- >映像- >创建映像”。

**![](img/d6094deadd07919c449f36891639bf30.png)**

**步骤 3.2:** 指定图像名称和描述，并点击“创建图像”。请注意，在创建映像之前，EC2 实例被停止，AMI 被创建并重新启动。这是为了确保创建的映像处于一致的状态。EC2 重新启动，因此任何 Putty 或 EC2 的其他会话都将终止。

**![](img/8d4733b76696bea829fbf17e9b34a6f8.png)**

**![](img/1d8d6e9138eac54ffae05a8079dbe921.png)**

**步骤 3.3:** 单击左侧窗格中的 AMI 选项卡。最初，AMI 将处于“未决”状态，然后它将变为“可用”状态。根据 EC2 实例的大小，AMI 的创建可能需要一些时间。请注意，默认情况下，AMI 具有 Private 可见性，并且只有创建它的用户才能访问。通过进入“操作- >管理图像权限”，AMI 可被公开或供少数用户访问。

**![](img/b002ac6ea2cd553e060eff822e5a87a2.png)**

**![](img/7ee10f345cabc935ec29d2768c009ad8.png)**

**![](img/b00350edfea1630752191126dbafdec7.png)**

**步骤 4:从新 AMI 创建 EC2**

在 EC2 管理控制台中，单击“启动实例”，单击“我的 AMI ”,在这里应该可以看到在**步骤 3** 中创建的私有 AMI。选择 AMI 并像往常一样遵循 EC2 创建过程。创建 EC2 实例后，获取 EC2 的公共 IP 地址，并通过浏览器中的(ec2-ip:8080) URL 访问 Tomcat 主页。这次不需要登录 EC2 实例并安装 Tomcat，因为在**步骤 3** 中创建的 AMI 已经安装了 Tomcat。

![](img/4a415eced383e385a58bc871cd1914ad.png)

创建 EC2 后，确保以相同的顺序终止 EC2 并注销 AMI。如果 EC2 实例正在运行，那么相应的 AMI 不能被注销。AMI 占用存储空间，并且如果它没有被注销/删除，则存在与之相关联的成本。

**![](img/e62a1d52935e93cbe81aaf82332d32e2.png)**

伙计们，这就把我们带到了这篇关于如何从定制 AMI 启动 EC2 实例的文章的结尾。如果您希望获得这方面的专业知识，Edureka 已经提供了一套课程，该课程完全涵盖了您通过解决方案架构师考试所需的内容！可以看看 **[AWS 解决方案架构师认证](https://www.edureka.co/aws-certification-training)** 的课程详情。

*如果对本博客有任何疑问，请随时在下面的评论区提问，我们将非常乐意尽快回复您，或者今天就参加我们在霍巴特的 [AWS 培训。](https://www.edureka.co/aws-certification-training-hobart)*