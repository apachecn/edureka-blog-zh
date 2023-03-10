# 实现高可用性的 Docker 群

> 原文：<https://www.edureka.co/blog/docker-swarm-cluster-of-docker-engines-for-high-availability>

任何基于网络的应用程序最重要的特征是什么？有很多，但对我来说**高可用性**最重要。这就是 Docker Swarm 帮助我们实现的目标！这有助于提高应用程序的可用性。

在我之前的博客中，我解释了 Docker Compose 是如何工作的。这篇关于 Docker Swarm 的博客是前者的延续，这里已经解释了使用 Docker Swarm 容器化任何多容器应用程序的好处。

在这个博客中，它只是一个有角度的应用程序，会被 Docker 蜂拥而至。 ***注**:容器化 MEAN Stack app 的方法相同。*

## **那么，Docker Swarm 是什么？**

**Docker Swarm** 是一种创建和维护集群 **Docker 引擎**的技术。Docker 引擎可以托管在不同的节点上，这些位于远程位置的节点在以群模式连接时形成一个*集群*。

## **为什么要用 Docker 蜂群？**

由于已经提到的原因！实现**高可用性**而不出现任何宕机是每个服务提供商的首要任务。高可用性会给客户留下深刻印象吗？如果他们面临停机，他们不会被打动。这是显而易见的。

## **码头工人蜂拥而至的其他好处**

像许多其他服务一样，Docker Swarm 为我们做自动**负载平衡**。因此，当一个节点出现故障时，DevOps 工程师不需要将处理请求路由到其他节点。集群的管理器将自动为我们执行负载平衡。

**分散访问**是另一个好处。那是什么意思？这意味着可以从管理器轻松访问所有节点。管理器还会定期提示节点，并跟踪其健康/状态，以应对停机。但是，节点不能访问或跟踪在其他节点/管理器中运行的服务。

只需执行一条命令，您就可以根据我们的要求检查一个节点中运行的集装箱数量、**放大**集装箱数量或**缩小**集装箱数量。

即使应用程序已经部署，我们也可以发布**滚动更新**并确保实现 CI(持续集成)。滚动更新一个接一个地发布到一个节点，从而确保没有停机时间，并且负载在集群中的其他节点之间分布。

那么，接下来呢？做显而易见的事情。如果您已经使用过 Docker，或者您的组织希望将一个可靠的 web 服务容器化，那么就开始使用 Docker Swarm 吧。

***注** : Docker 引擎安装在独立的主机/服务器上或一台主机中的多个虚拟机中。*

**虫群模式入门**

Docker Swarm 是由管理器发起的，或者这么说吧，启动 Swarm 集群的实例成为管理器。启动集群的命令是:

```
$ docker swarm init --advertise-addr ip-address

```

这里，‘–advertise-addr’标志用于向想要加入集群的其他节点通告自身。管理器的 IP 地址需要与标志一起指定。下面是示例截图。

![docker init command - docker swarm - edureka](img/667942dae1e55078d161b581c613be07.png)

当 Swarm 集群启动时，在管理者端生成一个令牌。其他节点需要使用这个令牌来加入 swarm 集群。

到底是怎么回事？复制在管理器的 docker 引擎生成的整个令牌，将其粘贴到节点的 docker 引擎并执行它。上面截图突出显示的部分是一个令牌。当令牌在一个 worker 节点上执行时，它将看起来像下面的屏幕截图。

![docker swarm join worker - docker swarm - edureka](img/4cf319df7a9a4d384cdcbb4ed48c3376.png)

任何加入集群的节点都可以在以后升级为管理器。如果您希望 docker 引擎作为管理器加入，请在管理器端执行以下命令:

```
$ docker swarm join-token manager
```

![docker swarm join manager command - docker swarm - edureka](img/e5c69ae870dc8c5c13349a8d409f0399.png)

稍后，如果您希望某个节点的令牌加入集群，请运行以下命令:

```
$ docker swarm join-token node
```

继续，在你想要的每个节点上执行令牌，加入集群。当所有这些都完成后，您可以运行 docker node list 命令来检查有多少节点加入了集群以及它们的状态。命令是:

```
$ docker node ls
```

截图如下:

## **![docker node ls command - docker swarm - edureka](img/ac8f2de048ef7ff6281dea0b81d533e1.png)**

## **为 Angular App 创建 Docker 图像**

如果一切顺利，我们就可以开始我们的 Swarm 服务了，前提是 Docker 映像已经建立。Docker 映像可以从 Docker 文件中构建。用于构建应用程序的 Dockerfile 文件如下:

```
FROM node:6
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY package.json /usr/src/app
RUN npm cache clean
RUN npm install
COPY . /usr/src/app
EXPOSE 4200
CMD ["npm","start"]
```

Docker 文件用于一起执行一组命令，以从基础映像构建自定义 Docker 映像。如你所见，我使用的基本图像是“节点:6”。NodeJS 是来自 Docker Hub 的图像 I，标记为版本 6。

然后，我在容器内创建一个新的 Docker 目录，并将其作为我的容器内的工作目录。

我正在从我的本地机器复制‘package . JSON’文件到容器的工作目录。然后，我指定“运行 npm 缓存清理”和“运行 npm 安装”命令。 *npm install* 命令下载 package.json 文件中提到的依赖项版本。

然后，我将所有项目代码从本地机器复制到容器中，显示端口号 4200，以便在浏览器上访问 Angular 应用程序，最后，我指定 npm start 命令，该命令将应用程序打包。

现在，要基于这个 Docker 文件创建 Docker 映像，运行下面的命令:

```
$ docker build -t angular-image .
```

## **![command to build dockerfile - docker swarm - edureka](img/ecc7c367c41c34af7f0b17231b4726e5.png)**

***注意:** 集群中的所有节点都需要建立 Docker 镜像。没有它，容器不能在其他 Docker 引擎中旋转。*

## **启动 Docker 群服务**

给定我们的 Docker 映像，我们可以用这个映像旋转出一个容器。但是，我们会做得更好:用它创建一个 Docker Swarm 服务。创建群服务的命令是:

```
$ docker service create --name "Angular-App-Container" -p 4200:4200 angular-image
```

![docker service create command - docker swarm - edureka](img/6ca1be76dc0917eb08bbbf3b635271f4.png)

这里,‘name’标志用于给我的服务命名，而‘p’标志用于将容器端口暴露给主机端口。在 package.json 文件中，我已经指定了应该托管 Angular 应用程序的容器端口。这个命令中的 4200 帮助将容器的端口 4200 映射到主机的端口 4200。“角度图像”是我之前制作的图像的名字。

**记住**:当我们创建一个服务时，它可以托管在集群中的任何 docker 引擎上。蜂群的管理者将决定它将在哪里被托管。但是，无论应用程序驻留在哪个节点上，都可以从集群中连接的任何节点访问 localhost:4200 上的应用程序。

这怎么可能？因为 Swarm 在内部公开了可供集群中所有其他节点访问的端口号。这意味着，集群中任何节点/管理器上的端口号 4200 都会呈现 Angular 应用程序。

现在怎么办？容器是活动的吗？

您可以通过运行 docker service list 命令来验证服务是否被容器化。但是，部署容器可能需要一分钟的时间。下面是命令:

```
$ docker service ls
```

这个命令将列出所有由 Swarm 集群管理的服务。在我们的例子中，它应该显示一个活动容器。看下面截图做参考。

![docker service ls command - docker swarm - edureka](img/075ead8cb73bb2816f04ee4a71fd95fe.png)

这里，“REPLICAS=1/1”表示集群中该容器只有一个“服务”。“MODE=replicated”表示服务在集群中的所有节点上复制。

现在，为了确定应用程序托管在哪个节点/管理器上，我们可以运行 docker service ps 命令，后跟容器名称。命令是:

```
$ docker service ps Angular-App-Container
```

同样的截图如下。

![docker service ps command - docker swarm - edureka](img/7560794b31d01ec1e4f2e70ffab32dd0.png)

这提到了应用程序所在节点的详细信息，以及用于启动服务的命令。

“docker ps”命令揭示了活动容器的详细信息。命令是:

```
$ docker ps
```

看下面截图做参考。

![docker ps command - docker swarm - edureka](img/d8d2750b22509c8edfcd5ca1f26845d5.png)

但是，这个命令只能在集群管理器和实际托管服务的节点上运行。

要检查有多少节点正在运行，运行节点列表命令。命令是:

```
$ docker node ls
```

要检查在特定主机上运行的容器，运行 node ps 命令。命令是:

```
$ docker node ps
```

![docker node ps command - docker swarm - edureka](img/e6854e6e64aa189c4f64681d14eeb76e.png)

如果您还记得的话，我之前提到过该服务目前是以复制模式运行的。这意味着服务在集群中的所有节点上复制。你认为有其他选择吗？

绝对的！有一种东西叫做全局模式。在这种模式下，集群中的每个/ manager 上都运行着该容器的服务。记得在旋转另一组容器之前停止当前服务/容器。

该命令为:

```
$ docker service rm Angular-App-Container
```

在全局模式下旋转容器的命令是:

```
$ docker service create --name "Angular-App-Container" -p 4200:4200 --mode global angular-image
```

![docker swarm global mode - docker swarm - edureka](img/a59e49a7aeb2386be826982378a7d061.png)

这将在我们集群的 3 个节点上创建 3 个服务。您可以通过运行 docker 服务列表命令来验证它。下面是这个的截图。

![docker service list command - docker swarm - edureka](img/2e395e0e1106823946058796f75f3182.png)

当 docker 服务 ps 命令被执行时，你会看到这样的内容:

![](img/38c032d367ad5d9bf0c72192d88df072.png)

如你所见，它说模式是复制的，这个容器的副本是 3 个。现在是这个博客最精彩的部分。

为了在三个容器之间运行服务的两个副本，我们可以使用 replicas 标志。看下面这个命令:

```
$ docker service create --name "Angular-App-Container" -p 4200:4200 --replicas=2 angular-image
```

![docker swarm replicas command - docker swarm - edureka](img/5ba4cc634d93e5f7d8ff4a7c1329656b.png)

您会注意到这两个服务在集群中的三个节点之间实现了负载平衡。运行 docker 服务进程命令来验证容器在哪些节点上是活动的。看下面截图做参考。容器在一个管理器节点和一个工作者节点中是活动的。

![docker service ps command - docker swarm - edureka](img/72149c18fb6dcf37793c4aad49027ab1.png)

从 Worker 节点，您可以通过执行‘docker PS’命令来验证容器是否正在运行。

## **![docker ps command - docker swarm - edureka](img/7f98d232103eaed5dc5410cca7b347db.png)**

## **码头工人蜂拥而至**

现在，为了实际验证我们的集群中是否存在高可用性，我们需要体验一个场景，其中一个节点发生故障，集群中的其他节点会进行弥补。我们可以通过使用以下命令从其中一个节点手动停止容器来实现这个场景:

```
$ docker stop Angular-App-Container
```

在运行容器的节点 Worker-1 上运行上面的命令。 从管理器中，运行命令:

```
$ docker service ps Angular-App-Container
```

您会注意到容器现在运行在节点:Worker-2 和 Manager 中。但是，它已从节点 Worker-1 关闭。从下面的截图中可以看到同样的情况。

![docker swarm ps command - docker swarm - edureka](img/87f3737475945e47e1ad6bb3ef72c766.png)

***Docker 高可用性*** 就是这样实现的。I n 尽管容器在 Worker-1 中是不活动的，但是应用程序可以在该 Worker 节点上的端口号 4200 处呈现。这是因为它在内部连接到集群中的其他节点，并且能够在浏览器中呈现应用程序。

## **服务规模化后的高可用性**

无论是在复制模式还是全局模式下，我们都可以扩大集群中运行的服务数量。即使在扩展之后，我们也能够保持高可用性。太棒了，不是吗？

回到我们的主题，让我们看看在我们的集群中增加服务数量是多么容易。假设我们的集群中有 2 个或 3 个副本，让我们通过运行一个命令将服务扩展到 5 个。命令是:

```
$ docker service scale Angular-App-Container=5
```

下面是这个的截图。

![docker service scale up command - docker swarm - edureka](img/44f2ed1522003b9e963eb6a88c0430f3.png)

通过运行 docker 服务列表命令，您可以注意到副本的数量现在是 5。通过运行 docker service ps 命令和服务名，您可以看到这 5 个服务是如何在 3 个节点上实现负载平衡和分布的。命令有:

```
$ docker service ls
$ docker service ps Angular-App-Container
```

![docker service ps scaled up command - docker swarm - edureka](img/e234298b4da75920c0e7b0133e0d72f8.png)

最后，在 Docker Swarm 设置中，如果您不希望您的经理参与到流程中，并且只负责管理流程，那么我们可以让经理不再托管任何应用程序。因为这个世界就是这样运作的，不是吗？经理只是用来管理其他员工的。总之，这样做的命令是:

```
$ docker node update --availability drain Manager-1
```

![docker node update drain command - docker swarm - edureka](img/4f6f427f1c5b91cdc58dfbdf8780c97c.png)

您可以通过运行 docker node list 命令和 docker service ps 命令来验证管理器现在是否加入了集群:

```
$ docker node ls
$ docker service ps Angular-App-Container
```

![docker node ls command - docker swarm - edureka](img/62857468cf6b60b101984c95599b936b.png)

您现在可以注意到，容器服务已经在工作节点之间进行了划分，而管理节点实际上已经不再对任何服务进行容器化。截图如下。

![docker swarm ps command - docker swarm - edureka](img/bdc68c6a9b7ba9e01df9483a4bc579f7.png)

Docker Swarm 上的这篇博客到此结束。我希望这篇博客解释了实现群体模式对于实现高可用性的重要性。请继续关注 Docker 教程系列中的更多博客。

你也可以观看下面的视频，了解 Docker Swarm 是如何工作的。上面解释的所有概念在视频中都有涉及。

## **Docker 集群高可用性| Docker 教程| DevOps 教程**[https://www.youtube.com/embed/Ceqb53EXANk?rel=0&showinfo=0](https://www.youtube.com/embed/Ceqb53EXANk?rel=0&showinfo=0)

既然您已经了解了 Docker，请查看 Edureka 提供的Docker 培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。这个 Edureka Docker 认证培训课程帮助学习者获得实现 Docker 和掌握它的专业知识。

*有问题吗？请在评论区提到它，我们会给你回复。*