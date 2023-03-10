# 安装 Docker–在 Ubuntu 和 CentOS 上安装 Docker

> 原文：<https://www.edureka.co/blog/install-docker/>

在这篇博客中，我将指导你通过简单的步骤安装 Docker。如果你不熟悉 Docker，别忘了看看 [**这个博客**](https://www.edureka.co/blog/docker-explained/) 。安装 docker 只是小菜一碟，你只需要运行几个命令就可以了！

在这篇 Install docker 博客中，您将了解到:

所以，我们先从在 Ubuntu 操作系统上安装 Docker 开始吧。

## **【Ubuntu 上的坞站安装】**

**第一步:**要在 Ubuntu box 上安装 docker，首先让我们更新软件包。

```

sudo apt-get update

```

这将要求输入密码。参考下面的截图，以获得更好的理解。

![UpdatePackages - Install Docker - Edureka](img/466eed0be7873754ec026e4a63e917fd.png)

**第二步:**现在在安装 docker 之前，我需要安装推荐的软件包。为此，只需键入以下命令:

```
sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual

```

按“y”继续。

![Packages - Install Docker - Edureka.png](img/0f63e3da3b4917b89530749ecd50228c.png)

在此之后，我们完成了先决条件！现在，让我们继续安装 Docker。

**第三步:**输入下面的命令安装 docker 引擎:

```
sudo apt-get install docker-engine

```

有时候它会再次询问要求输入密码。按回车键，安装将开始。

![DockerEngine - Install Docker - Edureka.png](img/ef46b0cf42544246f07f9cdc7c8ec216.png)

一旦完成，你安装 docker 的任务就完成了！

**第四步:**所以让我们简单地启动 docker 服务。为此，只需键入以下命令:

```

sudo service docker start

```

![DocketService - Install Docker - Edureka](img/09620e2d2d3d5949ee5b5bd2cc2953aa.png)

它说你的工作已经在运行了。恭喜你！docker 已成功安装。

**第 5 步:**现在，为了验证 docker 是否成功运行，让我向您展示如何从 docker hub 提取 CentOS 映像并运行 CentOS 容器。为此，只需键入以下命令:

```
sudo docker pull centos

```

首先，它将检查 CentOS 映像的本地注册表。如果在那里没有找到，那么它将转到 docker hub 并提取图像。为了更好的理解，请参考下面的截图:

![PullImage - Install Docker - Edureka](img/2b6ded39499e1a1082f163e1f47c6c27.png) 所以我们已经成功地从 docker hub 拉了一个 centOS 映像。接下来，让我们运行 CentOS 容器。为此，只需键入以下命令:

```

sudo docker run -it centos

```

![Container - Install Docker - Edureka](img/2d842e3077004e5c7fdfefd8a3c4e01d.png)

正如你在上面的截图中看到的，我们现在在 CentOS 容器中！

总而言之，我们首先在 Ubuntu 上安装了 docker，之后我们从 docker hub 中提取了一个 CentOS 映像，并使用该映像成功构建了一个 CentOS 容器。要了解更多关于 docker 容器及其工作原理，你可以参考 Docker 容器上的这篇博客。

这就是你在 Ubuntu 上安装 docker 和构建容器的方法。

## **在 CentOS** 上安装 Docker

要在您的 CentOS 机器上安装 docker，我建议您浏览这段 docker 安装视频。本 Edureka Docker 安装教程将帮助您了解如何在 CentOS 操作系统上安装 Docker，以及如何使用 Docker Run 命令运行 Docker 容器。继续，欣赏视频，告诉我你的想法。

[https://www.youtube.com/embed/CPQUgDyTd6g?rel=0&showinfo=0](https://www.youtube.com/embed/CPQUgDyTd6g?rel=0&showinfo=0)

## Docker 安装|以 CentOS 为单位的 Docker 安装

*If you found this “**Install Docker****” blog, relevant, **check out the *[***DevOps training***](https://www.edureka.co/devops-certification-training)*by Edureka, a trusted online learning company with a network of more than 250,000 satisfied learners spread across the globe. You can get a better understanding with this Online [Docker Certification](https://www.edureka.co/docker-training) Course. The Edureka DevOps Certification Training course helps learners gain expertise in various DevOps processes and tools such as Puppet, Jenkins, Nagios and GIT for automating multiple steps in SDLC.*

<article class="maincontentblog">*Got a question for us? Please mention it in the comments section of this “Install Docker” blog and we will get back to you as soon as possible.*</article>