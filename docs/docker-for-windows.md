# Docker For Windows |在 Windows 上设置 Docker

> 原文：<https://www.edureka.co/blog/docker-for-windows/>

如果您正在寻找简单、轻松的软件部署，Docker 是您的合适工具。它是最好的容器化平台，在这篇关于 Docker for Windows 的博客中，我们将特别关注 Docker 如何在 Windows 上工作。

要深入了解 Docker，您可以报名参加 Edureka 提供的全天候支持和终身访问的现场 ***[DevOps 认证培训](https://www.edureka.co/devops)*** 。

我将在这个博客中谈论以下话题:

1.  [为什么要用 Docker For Windows？](#Why%20use%20Docker%20For%20Windows)
2.  [Docker for Windows 必备](#Docker%20for%20Windows%20prerequisites)
3.  [组件安装有](#Components%20installed%20with%20Docker)
4.  [Docker 是什么？](#What%20is%20Docker)
5.  [码头工人术语](#Docker%20Terminologies)
6.  [动手](#Hands-On)

## **为什么要用 Docker for Windows？**

![Why use Docker for Windows - Docker for Windows - Edureka](img/49108d4e1f801ac874b1c3313994a848.png)

*为什么要用 Docker for Windows——Docker for Windows*

*   **避免了在我的机器上工作却不能在生产上工作的问题:** 这个问题是由于整个软件开发工作流程中的环境不一致而出现的。使用 Docker，您可以在包含应用程序所有依赖项的容器中运行应用程序，并且该容器可以在整个软件开发周期中运行。这种实践在整个软件开发生命周期中提供了一致的环境
*   **提高生产力:**通过在 windows 上安装 Docker，我们在本机运行 Docker。如果您已经关注 Docker 有一段时间了，您会知道 Docker 容器最初只支持 Linux 操作系统。但由于最近的发布，Docker 现在可以在 windows 上运行，这意味着不需要 Linux 支持，相反 Docker 容器将在 windows 内核本身上运行
*   **支持原生联网:**不仅是 Docker 容器，整个 Docker 工具集现在都兼容 windows。这包括 Docker CLI(客户端)、Docker compose、数据卷和 Docker 化基础架构的所有其他构建模块现在都与 windows 兼容。但是这有什么好处呢？由于所有 Docker 组件都与 windows 本地兼容，它们现在可以以最小的计算开销运行。你可以通过这个在线[码头工人课程](https://www.edureka.co/docker-training)更好的理解. .

## **Docker For Windows 必备**

![Docker for Windows - Prerequisites - Edureka](img/7c427e5fdb57cefff41185fbeae72243.png)

*Windows Docker–先决条件*

在 windows 上安装 Docker 需要满足以下要求:

1.  检查你用的是不是 Windows 10，无论是 pro 版还是企业版，64 位系统。Docker 不会在任何其他 windows 版本上运行。因此，如果你运行的是旧版本的 windows，你可以安装 Docker 工具箱。
2.  Docker for windows 需要一个类型 1 的虚拟机管理程序，在 windows 中，它被称为 Hyper-V。Hyper-V 基本上是一个基于虚拟机管理程序框架构建的轻量级虚拟化解决方案。因此，您不需要虚拟设备，只需启用虚拟机管理程序。
3.  此外，您还需要在 BIOS 中启用虚拟化。现在当你安装 Docker for windows 时，默认情况下这是启用的。但如果你在安装过程中遇到任何问题，请检查你的 Hyper-V 和虚拟化是否已启用。

## **组件安装有**

![Components installed with Docker - Docker for Windows - Edureka](img/7bce6f2cc2c972798b21979ae0da337d.png)

*安装有 Docker 的组件——Docker for Windows*

1.  Docker 引擎:当我们说 Docker 时，我们实际上是指 Docker 引擎。Docker 引擎包含 Docker 守护进程、用于与 Docker 守护进程交互的 REST API 以及与守护进程通信的命令行界面客户端。Docker 守护程序从 Docker 客户端接受 Docker 命令，如 Docker run、Docker build 等。
2.  Docker Compose: Docker compose 用于通过使用一个命令一次运行多个 Docker 容器，这个命令就是 docker-compose up。
3.  Docker 机:Docker 机用于安装 Docker 引擎。它基本上就是您在本地系统上安装的内容。Docker 机器有自己的 CLI 客户机，称为 Docker 机器，还有一个 Docker 引擎客户机，称为 Docker。
4.  Kitematic: Kitematic 是一个开源项目，旨在简化 Docker 在 Windows 上的使用。它有助于自动安装 Docker，并为运行 Docker 容器提供了一个非常交互式的用户界面。

如果您想了解更多关于 Docker for Windows 的信息，请观看我们的 DevOps 专家制作的视频。

## **Docker For Windows |在 Windows 上设置 Docker | Docker 初学者教程| edu reka**



[https://www.youtube.com/embed/iJeL2tOFfvM?rel=0&showinfo=0](https://www.youtube.com/embed/iJeL2tOFfvM?rel=0&showinfo=0)*This Edureka video on Docker For Windows we’ll discuss Docker which is one of the best containerization platforms out there.*

## **Docker 是什么？**

Docker 是一个容器化平台，它在称为 Docker 容器的容器中运行应用程序。与虚拟机相比，Docker 容器是轻量级的。当您在系统上安装虚拟机时，它会在您的主机操作系统上使用客户机操作系统。这显然会占用大量资源，如磁盘空间、RAM 等。另一方面，Docker 容器利用主机操作系统本身。

![What is Docker - Docker for Windows - Edureka](img/9d7a00d5c3770e92c7e3b62a2572883b.png)

*什么是 Docker–Docker for Windows*

在上面的图中，你可以看到，有一个主机操作系统，Docker 引擎安装在其上。Docker 引擎运行容器#1 和容器#2。这两种容器都有不同的应用程序，每个应用程序都有自己的库和包安装在容器中。

我希望你对 Docker 有一个很好的了解，如果你仍然有疑问，查看[这个](https://www.edureka.co/blog/docker-explained/)博客了解更多！

现在我们来讨论一些 Docker 术语:

*   **码头工人图片**

Docker 映像是用于构建 Docker 映像的只读模板。Docker 图像是从名为 Dockerfile 的文件中创建的。在 docker 文件中，您定义了应用程序所需的所有依赖项和包。

*   **码头工人集装箱**

每次你运行一个 Docker 镜像，它就作为一个 [Docker 容器](https://www.edureka.co/blog/docker-container/)运行。因此，Docker 容器是 Docker 映像的运行时实例。

*   **【码头工人登记册】**

Docker 的注册表被称为 DockerHub，用于存储 Docker 图像。这些图像可以从远程服务器上获取，也可以在本地运行。DockerHub 允许您拥有公共/私有存储库。

*   [**码头工人群**](https://www.edureka.co/blog/docker-swarm-cluster-of-docker-engines-for-high-availability)

Docker swarm 是一种创建和维护 Docker 引擎集群的技术。对接引擎集群包括多个相互连接的对接引擎，形成一个网络。这个 Docker 引擎网络被称为 Docker swarm。一个 Docker 管理器启动整个集群，其他 Docker 节点上运行服务。Docker 管理器的主要目标是确保应用或服务在这些 Docker 节点上有效运行。

*   [**坞站组成**](https://www.edureka.co/blog/docker-compose-containerizing-mean-stack-application/)

Docker compose 用于一次运行多个容器。假设您在 3 个不同的容器中有 3 个应用程序，并且您想一次执行它们。这就是 Docker compose 的用武之地，你可以一次在不同的容器中运行多个应用程序，只需一个命令，即 docker-compose up。

## **动手**

我们将从安装 Docker for windows 开始演示。但是在我们这样做之前，检查一下你是否满足了[先决条件](#prereq)。

还有一点需要注意的是，由于 Docker for Windows 需要微软的 Hyper-V，一旦启用，VirtualBox 将无法再运行虚拟机。所以你不能在同一个系统上同时运行 Docker for Windows 和 VirtualBox。

## **在 Windows 上安装 Docker:**

1.  从[官网](https://docs.docker.com/docker-for-windows/install/)下载 Docker for Windows installer
2.  双击安装程序运行它
3.  通过安装向导，接受许可并继续安装
4.  安装完成后，打开 Docker for Windows app，等待状态栏上的鲸鱼图标稳定下来
5.  打开任何终端，如 Windows PowerShell，并开始运行 Docker

*![Installation - Docker for Windows - Edureka](img/3ceff991e3b33d33f609e82a13ff964d.png)安装——Windows Docker*

理论讲得够多了，让我们动手使用 Docker Compose 创建一个简单的 [Python](https://www.edureka.co/blog/python-tutorial/) web 应用程序。这个应用程序使用 Flask 框架，并在 Redis 上维护一个点击计数器。

Flask 是一个 web 开发框架，用 Python 写的，Redis 是一个内存存储组件，用作数据库。您不必安装 Python 或 Redis，我们只需为 Python 和 Redis 使用 Docker 映像。

在本演示中，我们将使用 Docker compose 运行两个服务，即:

1.  网络服务
2.  再服务。

应用程序是做什么的？每当你访问一个网页时，它都会维护一个点击计数器。所以每次你访问这个网站，点击数就会增加。这是一个简单的逻辑，当网页被访问时，只需增加点击计数器的值。

对于这个演示，您需要创建四个文件:

1.  Python 文件
2.  Requirements.txt
3.  Dockerfile
4.  坞站复合文件

下面是 Python 文件(webapp.py ),它使用 Flask 框架创建了一个应用程序，并在 Redis 上维护了一个点击计数器。

```
import time
import redis
from flask import Flask
app = Flask(__name__)
cache = redis.Redis(host='redis', port=6379)
def get_hit_count():
retries = 5
while True:
try:
return cache.incr('hits')
except redis.exceptions.ConnectionError as exc:
if retries == 0:
raise exc
retries -= 1
time.sleep(0.5)
@app.route('/')
def hello():
count = get_hit_count()
return 'Hello World! I have been seen {} times.
'.format(count)
if __name__ == "__main__":
app.run(host="0.0.0.0", debug=True)

```

requirements.txt 文件具有两个依赖项的名称，即我们将在 Dockerfile 文件中安装的 Flask 和 Redis。

```
flask
redis

```

Docker file 用于创建 Docker 图像。在这里，我正在安装 python 和 requirements.txt 文件中提到的需求。

```

FROM python:3.4-alpine 
ADD . /code 
WORKDIR /code 
RUN pip install -r requirements.txt 
CMD ["python", "webapp.py"] 
```

Docker 撰写文件或 YAML 文件包含两个服务:

1.  Web 服务:在当前目录下构建 Dockerfile 文件
2.  再入服务:从坞站拉出再入图像

```
version: '3'
services:
web:
build: .
ports:
- "5000:5000"
redis:
image: "redis:alpine"

```

您现在可以使用下面的命令运行这两个服务或容器:

```
docker-compose up

```

要查看输出，您可以使用 Kitematic。要打开 Kitematic，右击状态栏上的鲸鱼图标。

![Kitematic -Docker For Windows - Edureka](img/7aefb474cd96c30581899f4843834af1.png)

*Kitematic–Docker for Windows*

在左上角，你可以看到两个服务正在运行。

![Kitematic -Docker For Windows - Edureka](img/5c5a8959443d43454a11fba631040848.png)

*Kitematic–Docker for Windows*

这是输出的样子。当您刷新页面时，点击次数会增加。

*![Output -Docker For Windows - Edureka](img/9b65f067bdf826fa42be7642fbc6f7e3.png)输出–Docker for Windows*

到此，我们结束了这篇博客。 希望你对 Docker 在 Windows 上的工作方式有更好的了解。敬请关注更多关于最热门技术的博客。

*如果您发现此 Docker for Windows 博客相关，请查看 Edureka 的 [**DevOps 培训**](https://www.edureka.co/devops/) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的超过 45 万名满意的学习者。Edureka DevOps 认证培训课程可帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Docker、Nagios、Ansible 和 GIT，用于自动化 SDLC 中的多个步骤。*