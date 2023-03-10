# 关于应用程序负载平衡器，您需要知道的一切

> 原文：<https://www.edureka.co/blog/application-load-balancer>

侦探掌握的线索越多，破案就越容易。这正是负载平衡器的工作方式。负载平衡器拥有的信息越多，它的工作就越好。在这篇博客中，我将讨论应用程序负载平衡器，以及它如何通过更好地访问数据包报头、HTTPS 和 HTTPS 细节来分配传入流量。

涵盖的主题:

*   [什么是应用负载均衡器？](#WhatisApplicationLoadBalancer?)
*   [应用负载均衡器的工作](#WorkingOfApplicationLoadBalancer)
*   [优于传统负载平衡器的特性](#FeaturesWhichMakeItBetterThanClassicLoadBalancer)
*   [演示:创建一个应用程序负载平衡器并演示它的工作](#Demo)

## **什么是应用负载平衡器？**

我相信你们都听说过 OSI 模型。这是一个 7 层架构，每一层都执行一项特殊的任务，在全球范围内传输数据。这些层包括物理层、数据链路层、网络层、传输层、会话层、表示层和应用层。顾名思义，应用程序负载平衡器运行在 OSI 模型的第 7 层。It 能够检查应用级内容，并根据获得的信息路由流量。应用层内容包括数据包详细信息、HTTP 和 HTTPS 详细信息。这使得路由更容易，更快，更有效。这是应用最广泛的 [ELB](https://www.edureka.co/blog/elastic-load-balancer-tutorial-application-load-balancer) 。

## **应用负载均衡器工作**

应用负载均衡器由**监听器**和**规则**组成。当客户端发出请求时，监听器会对其进行确认。这些规则是指导方针，一旦侦听器听到每个客户端请求，就控制其路由。规则由三部分组成——**目标组**、**优先级**和**条件**。目标组由**注册目标**(流量将被路由到的服务器)组成。每个目标组使用您指定的协议和端口号将请求路由到一个或多个注册的目标，如 EC2 实例。因此，基本上，当侦听器收到请求时，它会按照优先级顺序确定要应用的规则，分析规则，并根据条件决定哪个目标组收到请求。

![ALB - Application Load Balancer - Edureka](img/68798eda4733b6126c46f07c6d688275.png)

您可以随时根据需要在负载平衡器中添加或删除目标，而不会中断应用程序的整体请求流。ELB 可动态扩展您的负载均衡器，即当您的应用程序上的流量随时间变化时，让您的应用程序为各种情况做好准备。

## **优于传统负载平衡器的特性**

**基于内容的路由:**应用负载均衡器必须访问 HTTP 报头，并据此路由流量。

**支持基于容器的应用:**借助强大的容器化概念，大多数用户将他们的微服务打包到容器中，并在 EC2 实例上托管它们。这允许一个 EC2 实例运行多个服务。应用程序负载平衡器支持这些基于容器的应用程序。一个实例可以在同一个目标组后面托管多个容器并监听多个端口。它还执行细粒度的端口级运行状况检查。

**更好的指标:**应用程序负载平衡器对每个端口执行健康检查，并生成报告。健康检查指定了一系列可接受的 HTTP 响应。这些健康检查还伴随有详细的错误代码。

**基于路径的路由:**应用负载均衡器支持基于路径和基于主机的路由，这与传统负载均衡器不同。Y 你可以使用一个负载均衡器将请求路由到多个域。

**注册 IP 地址和 Lambda 函数:**除了注册 EC2 实例，还可以向你的目标注册 IP 地址和 Lambda 函数。因此你也可以注册 VPC 以外的目标。

**提供附加协议和工作负载:**

应用负载平衡器提供了两种附加协议——HTTP/2 和 WebSocket

**HTTPS/2:** 该协议支持单个连接上的多路复用请求。这减少了网络流量。

**WebSocket:** 这个协议允许你在客户端和服务器之间建立一个持久的 TCP 连接。与旧的方法相比，这个协议更有效。

## **演示:创建一个应用程序负载平衡器并演示它的工作**

让我们通过创建和使用应用程序负载平衡器来更好地理解它。在本演示中，我将创建两个 EC2 实例，在这两个实例上部署具有不同 HTML 输出的 Nginx web 服务器(很容易区分它们)，创建一个应用程序负载平衡器，将这两个实例注册到该负载平衡器，并检查是否可以从负载平衡器 DNS 访问部署在实例上的 web 服务器。让我们开始吧。

**步骤 1:** [创建两个 EC2 实例](https://www.edureka.co/community/37968/how-to-create-an-ec2-instance-in-aws-console?)，并将您的实例连接到 Putty 或 cmder。

**步骤 2:** 在两个实例上安装 Nginx web 服务器。执行以下命令安装 Nginx:

```
$ sudo apt-get update
$ sudo apt install nginx
$ sudo ufw app list
$ sudo ufw allow 'Nginx HTTP'
$ sudo ufw status
```

复制实例的公共 IP，像 URL 一样粘贴在浏览器上，检查 Nginx 是否安装成功。

**步骤 3** :更改 Nginx web 服务器的 HTML 输出，以避免两个实例上的部署混淆。

```
$ cd /var/www/html
$ sudo vi index.nginx-debian.html
```

将 H1 标签的内容改为“欢迎使用 Nginx！–服务器 1”。在另一个实例上做同样的操作，除了将它改为“欢迎使用 Nginx！–服务器 2”。

![nginxdebianhtml - Application Load Balancer - Edureka](img/6806f5a0b39486da40e60c80b5785c47.png)

**第四步:**创建一个应用负载均衡器。在导航窗格中，在**负载平衡**下，选择**负载平衡器**并点击应用负载平衡器下的**创建**。

![createlb1 - Application Load Balancer - Edureka](img/ae9ade3285884646d912877ebbfd8eb4.png)

你将被导航到另一个页面，在那里选择**创建负载平衡器**。

![createlb2 - Application Load Balancer - Edureka](img/b15228c87fc5097a012c6adb2a690c39.png)

让我们来配置负载平衡器。对于名称，键入您希望负载平衡器使用的名称。对于方案，选择面向 Internet 或内部。在这种情况下，我选择了面向互联网。面向互联网基本上是通过互联网将来自客户端的请求路由到目标。

![configurelb1 - Application Load Balancer - Edureka](img/cca4731bd4817395cc15045b6f8b805e.png)

对于监听器，默认是接受端口 80 上的 TCP 流量，我继续使用相同的默认监听器配置。如果您想添加另一个监听器，您可以选择**添加监听器**。

**![configurelb2 - Application Load Balancer - Edureka](img/43dc28be38b846469b139c45bbb8865a.png)**

对于可用性区域，选择您用来创建 EC2 实例的 VPC。为用于创建 EC2 实例的每个可用性区域选择一个可用性区域以及该可用性区域的子网。

![configurelb3 - Application Load Balancer - Edureka](img/177f01badb0cb4f176a73adbb69c31a7.png)

您可以根据需要向负载平衡器添加标签。当您有多个负载平衡器时，标签特别有用。

![configurelb4 - Application Load Balancer](img/9535bef8bb2b90423d121900d5bdabe5.png)

点击**下一步:配置安全设置**。你可能会看到一个警告，但你可以忽略它。

![configuresecurity1 - Application Load Balancer - Edureka](img/27e977d3c833442b97e74a5b18ff6212.png)

在这一步，您可以配置您的负载平衡器的安全性，您可以**创建一个新的安全组**或者**选择一个现有的安全组**。在本例中，我选择了一个现有的安全组。

![configuresecurity3 - Application Load Balancer - Edureka](img/932f642a80668b11c5d4f38e17e92c82.png)

完成安全配置后，点击**下一步:配置路由**。选择一个**新的目标组。**添加您想赋予您的**目标群体**的**名称**。选择**目标类型**作为实例，因为我们正在附加实例。应用程序负载平衡器还允许您附加 IP 地址和 Lambda 函数。将**协议**和**端口**设为默认。

![configurerouting1 - Application Load Balancer - Edureka](img/c1697594b8a9f2167d9c413cd3e764ab.png)

我在**健康检查**和**高级健康检查**也没有改变什么。默认设置对我们来说已经足够好了。

![configurerouting2 - Application Load Balancer - Edureka](img/4872adb16d976dbdfd3914458ddd5703.png)

![](img/1fe2f084c5b6b16b89f4d08839e55200.png)

单击 **Next: Register targets** 将您的目标(在本例中是实例)添加到您的负载均衡器中。

选择您希望添加为目标的实例，然后点击**添加以注册。**

![registertarget1 - Application Load Balancer](img/c89c2613f0c9fda56ba24050ae671152.png)

您的目标(实例)现在已经注册到负载平衡器。

![](img/68667947c6d3193bc52fbeeb0c0cd8ea.png)

点击**下一步:回顾**。检查您的负载平衡器，然后最后点击**创建**。

![lbreview - Application Load Balancer - Edureka](img/62c4f3b6a188b6d04308b52c423140fa.png)

您的负载平衡器现在已经创建，您可以检查它的状态。

![lbstatus - Application Load Balancer - Edureka](img/dd899cc1cd4937337f72bf007da1abc9.png)

![lb - Application load Balancer - Edureka](img/12ab6a133341ffef7e810bee8b8440ad.png)

耶！！您已经成功创建了一个应用程序负载平衡器。现在让我们检查一下它是否真的在工作。

**第五步:**复制你的负载均衡器的 DNS 名称，像 URL 一样粘贴在浏览器上。您应该会看到第一个实例的输出。

![op1 - Application Load Balancer - Edureka](img/9bb7a42d29a2fe8ee885adf6032466a4.png)

现在转到另一个浏览器，粘贴相同的 DNS 名称，您应该会看到第二个实例的输出。

![op2 - Application Load Balancer - Edureka](img/e62b0f387e908f04a8dd237cce67ddff.png)

这表明负载平衡器正在平衡其上两个实例的负载。两个 EC2 实例上的负载将由这个负载平衡器处理。测试负载平衡器工作情况的另一种方法是关闭一个实例，并检查它的部署是否部署在负载平衡器的 DNS 上。

这个应用负载平衡器博客到此结束。我希望你们已经理解了亚马逊提供的这项令人惊叹的服务背后的概念。更多这样的博客，请访问“ [Edureka |博客](https://www.edureka.co/blog/)”。

如果您希望了解更多关于云计算的知识，并在云计算领域建立自己的事业，那么请查看我们的[云计算课程](https://www.edureka.co/cloud-computing-certification-courses)，该课程提供有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解云计算，并帮助您掌握这门学科。

有问题要问我们吗？请在评论区提出来，我们会回复您或者将您的问题发布到 [Edureka | Community](https://www.edureka.co/community/) 。在 Edureka 社区，我们有超过 100，000 名技术狂热分子随时准备提供帮助。