# Kubernetes 教程——Kubernetes 综合指南

> 原文：<https://www.edureka.co/blog/kubernetes-tutorial/>

Kubernetes 是一个平台，它消除了部署容器化应用程序所涉及的手动流程。在 Kubernetes 教程的这篇博客中，您将浏览与这个多容器管理解决方案相关的所有概念。

本教程将涵盖以下主题:

*   [挑战无容器编排](#Challenges%20Without%20Container%20Orchestration)
*   [Docker Swarm 或](#Docker%20Swarm%20or%20Kubernetes)Kubernetes
*   [什么是 Kubernetes？](#What%20is%20Kubernetes?)
*   Kubernetes 特性
*   [Kubernetes 建筑](#Kubernetes%20Architecture)

*   [动手](#Hands-On)

现在，在继续这篇博客之前，让我简单介绍一下集装箱化。

因此，在容器出现之前，开发人员和测试人员之间总是会发生口角。这通常是因为在开发端起作用的东西，在测试端不起作用。两者存在于不同的环境中。现在，为了避免这种情况，引入了容器，这样开发人员和测试人员就在同一个页面上。

同时处理大量的集装箱也是一个问题。有时在运行容器时，在产品方面，很少出现开发阶段不存在的问题。这种场景引入了容器编排系统。

在我深入探讨编排系统之前，让我快速列出没有这个系统所面临的挑战。

## **Kubernetes 教程:没有容器编排的挑战**

**![Challenges Without Container Orchestration - Kubernetes Tutorial - Edureka](img/9de0907fba99b5a203ee052f85022b03.png)**

从上图中可以看出，当多个服务在容器中运行时，您可能想要扩展这些容器。在大规模工业中，这真的很难做到。这是因为这将增加维护服务的成本，以及并行运行这些服务的复杂性。

现在，为了避免手动设置服务&克服挑战，需要一些大的东西。这就是容器编排引擎发挥作用的地方。【T2

这个引擎让我们组织多个容器，以这种方式启动所有的底层机器，容器是健康的，并且分布在集群环境中。当今世界，这样的引擎主要有两个:**Kubernetes**&**Docker Swarm**。

## **【立方教程:****【立方 vs 码头群】**

**Kubernetes** 和 **Docker Swarm** 是当今市场上领先的容器编排工具。所以在 prod 中使用它们之前，您应该知道它们到底是什么以及它们是如何工作的。

此外，在博客中，我将深入探究 Kubernetes，但要了解 Docker，你可以点击[这里](https://www.edureka.co/blog/what-is-docker-container)。

![Docker Swarm vs Kubernetes - Kubernetes Tutorial - Edureka](img/f1ea1189d2b029ffcec6f0f838113178.png)

你可以参考上图，与 Docker Swarm 相比，Kubernetes 拥有一个非常活跃的社区，并在许多组织中实现了自动扩展。类似地，与 Kubernetes 相比，Docker Swarm 有一个易于启动的集群，但它受限于 Docker API 的功能。

好了，伙计们，这些顶级工具之间的区别不仅仅是这些。如果您想知道这两种容器编排工具之间的详细区别，您可以点击这里的[。](https://www.edureka.co/blog/kubernetes-vs-docker/)

Interested To Know More About Kubernetes? [<button>Learn Now</button>](https://www.edureka.co/kubernetes-certification)

![Kubernetes On Docker - Kubernetes Tutorial - Edureka](img/eec64c29bc07d81a839fa065df7871ac.png) 如果我可以在这两者中选择一个，那么我会选择 Kubernetes，因为容器需要被管理并与外部世界连接，以完成调度、负载平衡和分配等任务。

但是，如果你从逻辑上考虑，Docker Swarm 会是一个更好的选择，因为它运行在 Docker 之上，对吗？如果我是你，我肯定会对使用哪个工具感到困惑。但是，嘿，Kubernetes 是市场上无可争议的领导者，也确实运行在 Docker 容器之上，具有更好的功能。

现在，既然你已经理解了 Kubernetes 的必要性，那我就告诉你**什么是 Kubernetes 吧？**

## **Kubernetes 教程:** **什么是 Kubernetes？**

[Kubernetes](https://www.edureka.co/blog/what-is-kubernetes-container-orchestration) 是一个开源的系统，它处理将容器调度到计算集群上的工作，并管理工作负载，以确保它们按照用户的意图运行。作为谷歌的创意，它提供了优秀的社区，并与所有的云提供商出色地合作，成为一个*多容器管理解决方案。*

## **【立方教程】** **立方特征**

Kubernetes 的特点如下:

![Kubernetes Featues - Kubernetes Tutorial - Edureka](img/54b6810b89773984e9826f472d553baf.png)

*   **自动调度:** Kubernetes 提供高级调度程序，根据资源需求和其他约束在集群节点上启动容器，同时不牺牲可用性。
*   **自我修复能力:** Kubernetes 允许在节点死亡时替换和重新安排容器。它还杀死不响应用户定义的健康检查的容器，并且在它们准备好服务之前不向客户端通告它们。
*   **自动推出&回滚:** Kubernetes 推出对应用程序或其配置的更改，同时监控应用程序的健康状况，以确保它不会同时杀死所有实例。如果出现问题，使用 Kubernetes，您可以回滚更改。
*   **水平扩展&负载平衡:** Kubernetes 可以通过一个简单的命令，使用一个 UI，或者根据 CPU 的使用情况自动地根据需求扩展和缩小应用程序。

## **【立方教程:** **【立方建筑】**

Kubernetes 架构有以下主要组件:

*   主节点
*   工作/从节点

我将逐一讨论它们。所以，最初让我们从了解**主节点**开始。

### **主节点**

主节点负责管理 Kubernetes 集群。它主要是所有管理任务的入口点。集群中可以有多个主节点来检查容错能力。

![Kubernetes Master - Kubernetes Tutorial - Edureka](img/b3f8fbc456d5ef9a8551d6136866abf5.png)

从上图中可以看出，主节点有各种组件，如 API 服务器、控制器管理器、调度器和 ETCD。

*   **API 服务器:**API 服务器是所有用于控制集群的 REST 命令的入口点。
*   **控制器管理器:**是一个监控 Kubernetes 集群的守护进程，管理不同的非终止控制循环。
*   **调度器:**调度器将任务调度给从节点。它存储每个从节点的资源使用信息。
*   **ETCD:** ETCD 是一个简单的、分布式的、一致的键值存储。它主要用于共享配置和服务发现。

### **工人/奴隶节点**

工作节点包含所有必要的服务，用于管理容器之间的网络，与主节点通信，以及向调度容器分配资源。

![Kubernetes Worker Node - Kubernetes Tutorial - Edureka](img/99e6fa2578491c03fe3b59abc6d7689a.png)

从上图中可以看出，worker 节点有各种组件，如 Docker 容器、Kubelet、Kube-proxy 和 Pods。

*   **Docker 容器:** Docker 运行在每个 worker 节点上，运行配置好的 pod
*   **Kubelet:** Kubelet 从 API 服务器获取 Pod 的配置，并确保所描述的容器启动并运行。
*   **Kube-proxy:**Kube-proxy 在单个工作节点上充当服务的网络代理和负载平衡器
*   **pod:**pod 是逻辑上在节点上一起运行的一个或多个容器。

如果你想详细了解 Kubernetes 建筑的所有组成部分，那么你可以参考我们关于 [Kubernetes 建筑的博客。](https://www.edureka.co/blog/kubernetes-architecture/)

Want To Get Certified In Kubernetes? [<button>View Batches Now</button>](https://www.edureka.co/kubernetes-certification)

## **【立方教程】** **立方案例研究**

**![Yahoo Logo - Kubernetes Tutorial - Edureka](img/8ed5806bca5d352d2246a0db13eb55ba.png)Y****ahoo！** **日本** 是一家网络服务提供商，总部位于加利福尼亚州森尼韦尔。由于公司的目标是虚拟化硬件，公司于 2012 年开始使用 ** OpenStack ** 。他们的内部环境变化很快。然而，由于云和容器技术的进步，该公司希望能够在各种平台上推出服务。

**问题:**如何从一个应用程序代码为所有需要的平台创建映像，并将这些映像部署到每个平台上？

为了更好地理解，请参考下图。当在代码注册处更改代码时，持续集成工具会创建裸机映像、Docker 容器和 VM 映像，并将其推入映像注册处，然后部署到每个基础架构平台。

![Problem Statement of Case Study - Kubernetes Tutorial - Edureka](img/f0a3649f31507fdc0f474e447eec00a0.png)

现在，让我们关注容器工作流，了解他们如何使用 Kubernetes 作为部署平台。参考下图，先睹为快平台架构。

![Solution of Case Study - Kubernetes Tutorial - Edureka](img/9730030eff3235c388f70a78fda0bef7.png)

使用 OpenStack 实例，在其上使用 Docker、Kubernetes、Calico 等来执行各种操作，如容器联网、容器注册等。

当你有许多集群时，管理它们就变得很困难，对吗？

因此，他们只想创建一个简单的基本 OpenStack 集群，以提供 Kubernetes 所需的基本功能，并使 OpenStack 环境更易于管理。

通过图像创建工作流和 Kubernetes 的结合，他们建立了下面的工具链，使得从代码推送到部署变得容易。

![Solution of Case Study - Kubernetes Tutorial - Edureka](img/d0d4ebe8e4655f06074ede63a0b6d7d2.png)

这种工具链确保了多租户、身份验证、存储、联网、服务发现等生产部署的所有因素都得到考虑。

乡亲们就是这样，**雅虎！日本**在**谷歌**和 **Solinea** 的帮助下，为运行在 OpenStack 上的 Kubernetes“一键式”代码部署建立了一个自动化工具链。

## **【立方教程:手放在**

在本次实践中，我将向您展示如何创建部署和服务。我使用一个 Amazon EC2 实例来使用 Kubernetes。嗯，亚马逊已经为 **Kubernetes(亚马逊 EKS)** 提供了 **亚马逊弹性容器服务**，这使得他们可以非常快速和轻松地在云中创建 Kubernetes 集群。如果你想了解更多，你可以参考这里的博客[。](https://www.edureka.co/blog/amazon-eks/)

**第一步:** 首先**创建一个文件夹**，您将在其中创建您的部署和服务。之后，使用编辑器和**打开一个部署文件**。

```
mkdir handsOn
cd handsOn
vi Deploy.yaml

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/b0b66d8bbf794333a90cb46728a8788e.png)**

**第二步:** 打开部署文件后，提及您想要部署的应用程序的所有规范。在这里，我试图部署一个 **httpd** 应用程序。

```
apiVersion: apps/v1  #Defines the API Version
kind: Deployment     #Kinds parameter defines which kind of file is it, over here it is Deployment
metadata:
  name: dep1        #Stores the name of the deployment
spec:               # Under Specifications, you mention all the specifications for the deployment
  replicas: 3       # Number of replicas would be 3
  selector:
   matchLabels:
     app: httpd     #Label name which would be searched is httpd
  template:
    metadata:
    labels:
      app: httpd   #Template name would be httpd
  spec:            # Under Specifications, you mention all the specifications for the containers
   containers:
   - name: httpd   #Name of the containers would be httpd
     image: httpd:latest  #The image which has to be downloaded is httpd:latest
     ports:
     - containerPort: 80 #The application would be exposed on port 80

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/820300b2c1747cf2ab76079ad1a8ed5c.png)第三步: ** 编写完部署文件后，使用以下命令应用部署。

```
kubectl apply -f Deploy.yaml

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/dbf673442852cc84a67008680bc08832.png)**

这里-f 是一个旗帜名称，用于 t he 文件 名称。

**第四步:** 现在，一旦应用了部署，就可以获得正在运行的 pod 列表。

```
kubectl get pods -o wide

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/49b43d3a98cfb2757ba45012c1b27bb1.png)**

这里，-o wide 用于了解部署在哪个节点上运行。

**第 5 步:** 创建了部署之后，现在要创建服务了。再次使用编辑器并打开一个空白的**服务。** **yaml 文件**。

```
vi service.yaml

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/a8dfda88577909bc8f4b5865e9361766.png)第六步: ** 一旦你打开了一个服务文件，提到了服务的所有规格。

```
apiVersion: v1  #Defines the API Version
kind: Service   #Kinds parameter defines which kind of file is it, over here it is Service
metadata:
  name: netsvc   #Stores the name of the service
spec:            # Under Specifications, you mention all the specifications for the service
  type: NodePort
  selector:
    app: httpd
ports:
-protocol: TCP
 port: 80
 targetPort: 8084    #Target Port number is 8084

```

**![](img/815f25a7dedc1996b9c42af278df000b.png)第 7 步: ** 编写完服务文件后，使用以下命令应用服务文件。

```
kubectl apply -f service.yaml

```

**![](img/e521f819cca71ecc332e07cfaa3efcd5.png)步骤 8:  ** 现在，一旦您的服务被应用，使用下面的命令检查服务是否正在运行。

```
kubectl get svc

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/881cd5dcc5b8afd98c7d417338d187a4.png)步骤 9:  ** 现在，要查看服务的规范，并检查它绑定到哪个端点 ，使用下面的命令。

```
kubectl describe svc <name of the service>

```

**![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/46d9972ccc81d65eabc8a6d57e92e9ff.png)第十步: ** 现在既然我们在使用 amazon ec2 实例，要获取网页并检查输出，使用下面的命令。

```
curl ip-address

```

*![Snapshot of Demo - Kubernetes Tutorial - Edureka](img/c7cad558875c27ca16f4bedbac0ed867.png)*

*如果你发现这个 Kubernetes 教程博客相关，请查看 Edureka 的* *[**Kubernetes 认证**](https://www.edureka.co/kubernetes-certification) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“ **Kubernetes 教程**的评论区提出来，我会回复你或者今天就参加我们在查谟的 [Kubernetes 培训..](https://www.edureka.co/kubernetes-certification-training-course-jammu)*