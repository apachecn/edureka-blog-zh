# Docker 网络——探索容器如何相互通信

> 原文：<https://www.edureka.co/blog/docker-networking/>

在当今世界，企业已经热衷于集装箱化，这需要强大的网络技能来正确配置集装箱架构，因此，这引入了 Docker 网络的概念。

在这篇关于 Docker Networking 的博客中，你将会看到以下主题:

*   [Docker 是什么？](#What%20is%20Docker?)
*   [联网中的](#Docker%20Networking)
*   [Docker 联网的目标](#Goals%20of%20Docker%20Networking)
*   [集装箱网络模型](#Container%20Network%20Model)
*   [网络驱动](#Network%20Drivers)
*   [动手](#Hands-On)

## **什么是 Docker？**

要理解 Docker，你需要了解应用程序以前是如何部署的历史，以及现在如何使用容器部署应用程序。

![Deployment Of Applications In Old Way And New Way - Docker Networking - Edureka](img/f6b70b108805d51151995f8181dc2d3a.png)

从上图中可以看出，旧方法在主机上也有应用。 因此，n 个应用程序共享该操作系统中的库。 但是，随着容器化，操作系统将拥有一个内核，这是所有应用程序之间唯一通用的东西。 所以，应用程序无法访问彼此的库。

因此， **[Docker](https://www.edureka.co/blog/docker-tutorial)** 简单来说就是一个开发、运输和运行应用的开放平台，使用户能够借助 **[容器](https://www.edureka.co/blog/docker-container/)** 将应用从基础设施中分离出来，快速交付软件。

那么，这些容器在各种情况下是如何相互通信的呢？

嗯，那是通过 Docker 联网来的。

## **Docker 联网**

在我深入研究 Docker 网络之前，让我向你展示一下 Docker 的工作流程。

![Docker Workflow - Docker Networking - Edureka](img/e7b014917d8d85e25100c7b8560477d2.png)

从上图中可以看出。开发者在易于编写的 Docker 文件中编写规定应用需求或依赖性的代码，并且该 Docker 文件产生 Docker 图像。因此，特定应用程序所需的任何依赖关系都会出现在此映像中。

现在，Docker 容器只不过是 Docker 映像的运行时实例。这些图像被上传到 Docker Hub(Docker 图像的 Git 存储库),其中包含公共/私有存储库。

因此，你也可以从公共存储库中提取你的图片，并将你自己的图片上传到 Docker Hub 上。然后，从 Docker Hub，各种团队(如质量保证或生产团队)将提取该图像并准备他们自己的容器。这些单独的容器通过网络相互通信以执行所需的操作，这就是 Docker 网络。

因此，您可以将 Docker 网络定义为一个通信通道，所有隔离的容器通过它在各种情况下相互通信，以执行所需的操作。

从这个在线 [Docker 课程](https://www.edureka.co/docker-training)中了解更多关于 Docker 网络的信息。

你认为 Docker 联网的目标是什么？

## **Docker 联网的目标**

![Goals Of Docker Networking - Docker Networking - Edureka](img/43bed295ca48a89049016bf1e5d7e052.png)

**灵活性**–Docker 通过支持各种平台上任意数量的应用程序相互通信来提供灵活性。

**跨平台**–借助 Docker Swarm 集群，Docker 可以轻松地用于跨平台，跨各种服务器工作。

**可扩展性**–Docker 是一个完全分布式的网络，支持应用在保证性能的同时单独增长和扩展。

**分散式**–Docker 使用分散式网络，这使得应用程序能够分散且高度可用。如果您的资源池中突然缺少一个容器或一个主机，您可以调用额外的资源或者转移到仍然可用的服务。

**用户友好的**–Docker 使服务的自动化部署变得容易，使它们在日常生活中易于使用。

**支持**–Docker 提供开箱即用的支持。因此，使用 Docker 企业版并获得所有功能的能力非常简单明了，使得 Docker 平台非常易于使用。

为了实现上述目标，你需要一种被称为容器网络模型的东西。

Want To Explore Various DevOps Stages? [<button>Explore now</button>](https://www.edureka.co/devops)

## **【CNM】**集装箱网络模型

在我告诉你到底什么是容器网络模型之前，让我简单介绍一下在你理解 CNM 之前所需要的 Libnetwork。

Libnetwork 是一个开源的 Docker 库，它实现了构成 CNM 的所有关键概念。

![Architecture of Container Networking Model - Docker Networking - Edureka](img/923717078518b598dc6cf92a28b4d001.png)

因此，**集装箱网络模型(CNM)** 标准化了使用多个网络驱动程序为集装箱提供网络所需的步骤。CNM 需要像控制台这样的分布式键值存储来存储网络配置。

CNM 有 IPAM 插件和网络插件的接口。

IPAM 插件 API 用于创建/删除地址池和分配/解除分配容器 IP 地址，而网络插件 API 用于创建/删除网络和从网络添加/移除容器。

CNM 主要建立在 5 个对象上:网络控制器、驱动程序、网络、端点和沙箱。

### **集装箱网络模型对象**

**网络控制器:**提供了 Libnetwork 的入口点，为 Docker 引擎提供了简单的 API 来分配和管理网络。由于 Libnetwork 支持多个内置和远程驱动程序，网络控制器使用户能够将特定的驱动程序连接到给定的网络。

**驱动:**拥有网络，并负责通过让多个驱动参与来管理网络，以满足各种使用案例和部署场景。

**网络:**提供属于同一网络并与其他网络隔离的一组端点之间的连接。因此，每当创建或更新网络时，相应的驱动程序都会收到事件通知。

**端点:**为网络中一个容器公开的服务提供与网络中其他容器提供的其他服务的连接。端点代表一个服务，而不一定是一个特定的容器，端点在集群中也具有全局范围。

**沙箱:**当用户请求在网络上创建端点时创建。一个沙箱可以有多个端点连接到不同的网络，代表容器的网络配置，如 IP 地址，MAC 地址，路由，DNS。

这些就是 CNM 的五个主要目标。

现在，我来告诉你 Docker 联网涉及的各种网络驱动。

Want To Take DevOps Learning To A Next Level? [<button>Learn Now</button>](https://www.edureka.co/devops)

## **网络驱动**

主要有 5 种网络驱动:网桥、主机、无、覆盖、Macvlan

**网桥:**网桥网络是由主机上的 docker 创建的私有默认内部网络。因此，所有容器都有一个内部 IP 地址，并且这些容器可以使用这个内部 IP 互相访问。当您的应用程序在需要通信的独立容器中运行时，通常使用桥接网络。

![Bridge Network - Docker Networking - Edureka](img/adac2c8c3a39c9ae7674574b35fb82e0.png)

**主机**:这个驱动去掉了 docker 主机和 docker 容器之间的网络隔离，直接使用主机的联网。这样，你就不能在同一个主机、同一个端口上运行多个 web 容器，因为这个端口现在是主机网络中所有容器的公共端口。

![Host Network - Docker Networking - Edureka](img/bf04ac6905f7d10a6a0e291d23fdebf5.png)

**【无】**:在这种网络中，容器不附属于任何网络，并且不具有对外部网络或其他容器的任何访问。因此，当想要完全禁用容器上的网络堆栈，而 只创建一个环回设备时，就使用这个网络。

![None Network - Docker Networking - Edureka](img/b68e3929942c47ac2c63221c9d6b6d3e.png)

**覆盖**:创建一个内部私有网络，跨越所有参与群集群的节点。因此，覆盖网络促进了群服务和独立容器之间的通信，或者不同 Docker 守护进程上的两个独立容器之间的通信。

![Overlay Network - Docker Networking - Edureka](img/388f6df2c496c88459d69d7a68de8e7e.png)

**Macvlan:** 允许你给一个容器分配一个 MAC 地址，使它在你的网络上表现为一个物理设备。然后，Docker 守护进程根据容器的 MAC 地址将流量路由到容器。当您希望直接连接到物理网络，而不是通过 Docker 主机的网络堆栈路由时，Macvlan 驱动程序是最佳选择。

![Macvlan Network - Docker Networking - Edureka](img/c8bbed697bb1a597d32c4b41ab1c626c.png)

好了，这就是理解 Docker 网络所需的全部理论。现在，让我继续向您实际展示网络是如何创建的，容器是如何相互通信的。

## **动手**

因此，假设你们所有人都在自己的系统上安装了 Docker，我将展示一个场景。

假设您想要存储课程名称和课程 ID，为此您将需要一个 web 应用程序。基本上，你需要一个 web 应用程序容器，你还需要一个后端 MySQL 容器，MySQL 容器应该链接到 web 应用程序容器。

我实际执行上面的例子怎么样。

### **涉及的步骤:**

*   初始化 Docker Swarm，形成 Swarm 集群。
*   创建覆盖网络
*   为 web 应用和 MySQL 创建服务
*   通过网络连接应用程序

我们开始吧！

**第一步:**初始化机器上的 Docker Swarm。

```
docker swarm init --advertise-addr 192.168.56.101

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/14f7f6068dbed7c7c1aa0a7ecb6d8ba3.png)

–advertise-addr 标志将管理中心节点配置为将其地址发布为 192.168.56.101。群中的其他节点必须能够通过 IP 地址访问管理器。

**第二步:**现在，如果你想把这个 manager 节点加入 worker 节点，复制你在 worker 节点上初始化 swarm 时得到的链接。 ![Snapshot Of Hands On - Docker Networking - Edureka](img/2ed2fe136abfe84abe61c942405527fd.png)   **第三步:**创建叠加网络。

```
docker network create -d overlay myoverlaynetwork

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/998913f01b3a5e4971e4938ca8b205f4.png)

其中 myoverlay 是网络名称，而-d 使 Docker 守护进程能够在后台运行。

**步骤 4.1:** 创建一个服务 webapp1，并使用您已经创建的网络在 swarm 集群上部署这个服务。

```
docker service create --name webapp1 -d --network myoverlaynetwork -p 8001:80 hshar/webapp

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/81bb372a16eb29b70285aa313162bc44.png)

其中-p 是端口转发， hshar 是 Docker Hub 上的账户名，webapp 是 Docker Hub 上已经存在的 web 应用的名称。

**步骤 4.2:** 现在，检查服务是否被创建。

```
docker service ls

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/10eaebd3d44e5f31050485f978297c98.png)

**步骤 5.1:** 现在，创建一个服务 MySQL，并使用您创建的网络在 swarm 集群上部署服务。

```
docker service create --name mysql -d --network myoverlaynetwork -p 3306:3306 hshar/mysql:5.5

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/0e23af6a62d1206695e5e0adc9672db7.png)  **步骤 5.2:** 现在，检查服务是否被创建。

```
docker service ls

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/c143bcef314fc9f17c6b1c3de5da627a.png)

**步骤 6.1:** 之后，检查你的主节点上运行的是哪个容器，进入 hshar/webapp 容器。

```
docker ps

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/229d5fb23aad08348f9e6eccc3486919.png)

**步骤 6.2:** 所以，你可以看到 manager 节点上只有 webapp 服务。因此，进入 webapp 容器。

```
docker exec -it container_id bash
nano var/www/html/index.php

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/0686e3460d456882ec38f8d388e3fecc.png)

docker ps 命令将列出两个容器及其各自的容器 id。第二个命令将在交互模式下启用该容器。

**第七步:**现在，将$servername 从 localhost 更改为 mysql，将$password 从"""更改为" edureka "，同时也更改所有需要填写的数据库详细信息，并使用键盘快捷键 Ctrl+x 保存您的 index.php 文件，之后使用 y 进行保存，并按 enter 键。

![Snapshot Of Hands On - Docker Networking - Edureka](img/73740a79a61380fe0e5fd6bd7213462b.png)

**第八步:**现在，进入另一个节点上运行的 mysql 容器。

```
docker exec -it container_id bash

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/4022d8c2c36e421615b1ecf4f8f8266d.png)

**第 9 步:**进入 mysql 容器后，输入以下命令使用 MySQL 中的数据库。

**步骤 9.1:** 获得使用 mysql 容器的权限。

```
mysql -u root -pedureka

```

其中-u 代表用户，-p 是您机器的密码。

**步骤 9.2:** 在 mysql 中创建一个数据库，该数据库将用于从 webapp1 中获取数据。

```
CREATE DATABASE HandsOn;

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/c8f6de47a51e8c6ac73bf08d8a52d98c.png)

**步骤 9.3:** 使用创建好的数据库。

```
USE HandsOn;

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/60cd99cf574da37ce2f93e175466fc84.png)

**步骤 9.4:** 在该数据库中创建一个表，该表将用于从 webapp1 获取数据。

```
CREATE TABLE course_details (course_name VARCHAR(10), course_id VARCHAR(11));

```

![Snapshot Of Hands On - Docker Networking - Edureka](img/f9e4e12e84cce4558bb59818a20eb00c.png)

**步骤 9.5:** 现在，使用命令 **exit** 退出 MySQL 和 container。

**第十步:**进入你的浏览器，输入地址为 **localhost:8001/index.php** 。这将打开您的 web 应用程序。现在，输入课程的详细信息并点击**提交查询**。

![Snapshot Of Hands On - Docker Networking - Edureka](img/abd1f0289f1a8402022b7ffe911ccca3.png)

**第 11 步:**点击提交查询后，转到运行 MySQL 服务的节点，然后进入容器。

```
docker exec -it container_id bash
mysql -u root -pedureka
USE HandsOn;
SHOW tables;
select * from course_details;

```

这将向您显示所有课程的结果，您已经填写了这些课程的详细信息。

![Snapshot Of Hands On - Docker Networking - Edureka](img/bf09c623798754935881bf6e8c0dad66.png)

在这里，我结束了我的 Docker 网络博客。我希望你喜欢这篇文章。你也可以看看这个系列中的其他博客，它们都是关于 Docker 的基础知识。

*如果您发现 Docker Container 博客相关，请查看 Edureka 的* *[**DevOps 培训**](https://www.edureka.co/devops-certification-training) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 450，000 名满意的学习者。Edureka DevOps 认证培训课程可帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Docker、Nagios、Ansible 和 GIT，用于自动化 SDLC 中的多个步骤。*

Looking For Certification in DevOps? [<button>View Batches Now</button>](https://www.edureka.co/devops)

*有问题问我吗？请在评论区提到它，我会回复你。*