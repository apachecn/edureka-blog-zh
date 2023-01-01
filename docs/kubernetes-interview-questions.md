# 2023 年 50 大 Kubernetes 面试问题及答案

> 原文：<https://www.edureka.co/blog/interview-questions/kubernetes-interview-questions/>

Kubernetes 已经成为当今市场的时髦词汇，是最好的编排工具。它吸引了许多有经验的专业人士，他们希望将自己的职业生涯提升一个档次。Huwaei、Pokemon、易贝、Yahoo Japan、SAP、Open AI 和 Sound Cloud 等跨国公司在其日常活动中使用 Kubernetes。但是市场上缺乏 Kubernetes 认证的专业人士。我相信你已经知道了这些事实，这些事实让你看到了这篇 Kubernetes 的面试问题文章，这篇文章将帮助你了解面试中最常被问到的问题。更多详情，请参考 [Kubernetes 认证](https://www.edureka.co/kubernetes-certification)。

## **顶级 Kubernetes 面试问题**

1.  [Kubernetes 和 Docker Swarm 有什么不同？](#one)
2.  [什么是 Kubernetes？](#two)
3.  [Kubernetes 和 Docker 有什么关系？](#three)
4.  [在主机和容器上部署应用程序有什么区别？](#four)
5.  [什么是容器编排？](#five)
6.  [容器编排的需求是什么？](#six)
7.  [Kubernetes 有什么特点？](#seven)
8.  【Kubernetes 如何简化容器化部署？
9.  你对 Kubernetes 的星团了解多少？
10.  [什么是谷歌容器引擎？](#ten)

在这篇关于 Kubernetes 面试问题的博客中，我将讨论你在面试中被问到的与 Kubernetes 相关的最常见问题。所以，为了让你更好的理解，我把这个博客分成了以下 4 个部分:

*   [Kubernetes 基本面试问题](#Basic%20Kubernetes%20Interview%20Questions)
*   [建筑类面试题](#Architecture-Based%20Interview%20Questions)
*   [情景式面试试题](#Scenario-Based%20Interview%20Questions)
*   [选择题](#Multiple%20Choice%20Questions)

所以让我们开始吧伙计们！！

## **基本 Kubernetes 面试问题**

这部分问题将包括你需要了解的与 Kubernetes 工作相关的所有基本问题。

### **Q1。Kubernetes 和 Docker Swarm 有什么不同？**

| **特征** |  | **码头工人群** |
| **安装&集群配置** | 安装非常复杂，但安装后的集群非常稳定。 | 安装非常简单，但是集群不够健壮。 |
| **桂** | GUI 是 [Kubernetes 仪表板](https://www.edureka.co/blog/kubernetes-dashboard/)。 | 没有图形用户界面。 |
| **扩展性** | 高度可扩展，快速扩展。 | 高度可扩展，扩展速度比 Kubernetes 快 5 倍。 |
| **自动缩放** | Kubernetes 可以自动缩放。 | Docker swarm 无法进行自动缩放。 |
| **负载均衡** | 不同集装箱和箱之间的负载平衡需要人工干预。 | Docker swarm 在集群中的容器之间进行流量的自动负载平衡。 |
| **滚动更新&回滚** | 可以部署滚动更新并执行自动回滚。 | 可以部署滚动更新，但不能自动回滚。 |
| **数据卷** | 只能与同一 pod 中的其他容器共享存储容量。 | 可以与任何其他容器共享存储卷。 |
| **记录&监控** | 用于记录和监控的内置工具。 | 应使用 ELK stack 等第三方工具进行记录和监控。 |

### **Q2。什么是 Kubernetes？**

![What is Kubernetes - Kubernetes Interview Questions - Edureka](img/0a3edb674580172735b1a76454d72094.png)

### **图 1:** 什么是 Kubernetes——Kubernetes 面试问题

Kubernetes 是一个开源的容器管理工具，它负责容器部署、容器缩放、负载平衡。作为谷歌的创意，它提供了优秀的社区，并与所有的云提供商合作愉快。因此，我们可以说 Kubernetes 不是*一个容器化平台，但它是一个多容器管理解决方案。*

### **Q3。Kubernetes 和 Docker 有什么关系？【T2**

众所周知，Docker 提供容器的生命周期管理，Docker 映像构建运行时容器。但是，由于这些单独的容器必须进行通信，因此使用了 Kubernetes。因此，Docker 构建容器，这些容器通过 Kubernetes 相互通信。因此，运行在多个主机上的容器可以使用 Kubernetes 手动链接和编排。

### **Q4。在主机和容器上部署应用程序有什么区别？**

![Deploying Applications On Host vs On Containers - Kubernetes Interview Questions - Edureka](img/33ceba4bb99304b17f32ee360b15244a.png)

### **图 2:** 在主机和容器上部署应用程序——Kubernetes 面试问题

参考上图。左侧架构表示在主机上部署应用程序。因此，这种架构将有一个操作系统，然后操作系统将有一个内核，该内核将在操作系统上安装应用程序所需的各种库。因此，在这种框架中，您可以有 n 个应用程序，并且所有应用程序将共享该操作系统中的库，而在容器中部署应用程序时，架构略有不同。

这种架构将有一个内核，这将是所有应用程序之间唯一的共同点。因此，如果有一个特定的应用程序需要 Java，那么这个特定的应用程序将可以访问 Java，如果有另一个应用程序需要 Python，那么只有这个特定的应用程序可以访问 Python。

您可以在图表右侧看到的各个模块基本上都是容器化的，并且与其他应用程序隔离开来。因此，应用程序拥有与系统其余部分隔离的必要库和二进制文件，不能被任何其他应用程序侵占。

### **Q5。什么是容器编排？**

考虑一个场景，您有 5-6 个微服务用于一个应用。现在，这些微服务被放在单独的容器中，但如果没有容器编排，将无法进行通信。因此，正如编排意味着所有乐器在音乐中和谐演奏的融合，类似地，容器编排意味着各个容器中的所有服务一起工作，以满足单个服务器的需求。

### **Q6。容器编排的需求是什么？**

假设您有 5-6 个微服务用于执行各种任务的单个应用程序，所有这些微服务都放在容器中。现在，为了确保这些容器相互通信，我们需要容器编排。

![Challenges without Container Orchestration - Kubernetes Interview Questions - Edureka](img/d3717c92d5370dea54249e94b950ae76.png)

### **图 3:** 没有容器编排的挑战——Kubernetes 面试问题

正如您在上图中看到的，在没有使用容器编排的情况下，也出现了许多挑战。因此，为了克服这些挑战，容器编排应运而生。

### **Q7。Kubernetes 有什么特点？**

库伯内特的特点如下:

![Kubernetes Features - Kubernetes Interview Questions - Edureka](img/a13751a11d29f9f82edfc00ba0680c92.png)

### **图 4:**Kubernetes 的特点——Kubernetes 面试问题

### **Q8。Kubernetes 如何简化容器化部署？**

由于一个典型的应用程序会有一个跨多个主机运行的容器集群，所有这些容器都需要相互通信。所以，要做到这一点，你需要一个大的东西来负载平衡，伸缩&来监控容器。由于 Kubernetes 与云无关，并且可以在任何公共/私有提供商上运行，因此简化容器化部署必然是您的选择。

### **Q9。你对 Kubernetes 的星团了解多少？**

Kubernetes 背后的基本原理是，我们可以实施所需的状态管理，我的意思是，我们可以提供特定配置的集群服务，并由集群服务在基础架构中运行该配置。

![Kubernetes Cluster - Kubernetes Interview Questions - Edureka](img/aca79fb8d678851d6fe3abc4172525db.png)

### **图 5:**Kubernetes 集群代表——Kubernetes 面试问题

因此，正如您在上面的图表中看到的，部署文件将包含所有需要提供给集群服务的配置。现在，部署文件将被提供给 API，然后由集群服务来决定如何在环境中调度这些单元，并确保正确数量的单元正在运行。

因此，位于服务前端的 API，工作节点&节点运行的 Kubelet 进程，共同组成了 Kubernetes 集群。

### **Q10。什么是谷歌容器引擎？**

**Google 容器引擎(GKE)** 是 Docker 容器和集群的开源管理平台。这个基于 Kubernetes 的引擎只支持那些运行在 Google 公共云服务中的集群。

[https://www.youtube.com/embed/S7JEPz6sY5g](https://www.youtube.com/embed/S7JEPz6sY5g)

## **立方面试问题**

### **Q11。Heapster 是什么？**

Heapster 是一个集群范围内的数据聚合器，由运行在每个节点上的 Kubelet 提供。这个容器管理工具在 Kubernetes 集群上得到本机支持，并作为一个 pod 运行，就像集群中的任何其他 pod 一样。因此，它主要通过机器上的 Kubernetes 代理发现集群中的所有节点，并从集群中的 Kubernetes 节点查询使用信息。

### **Q12。Minikube 是什么？**

Minikube 是一个让本地运行 Kubernetes 变得容易的工具。这在一个虚拟机内运行一个单节点 Kubernetes 集群。

### **Q13。什么是** **Kubectl？**

Kubectl 是一个平台，您可以使用它向集群传递命令。因此，它基本上提供了针对 Kubernetes 集群运行命令的 CLI，以及创建和管理 Kubernetes 组件的各种方法。

### **Q14。库伯莱是什么？**

这是一个代理服务，运行在每个节点上，使从节点能够与主节点通信。因此，Kubelet 处理 PodSpec 中提供给它的容器描述，并确保 PodSpec 中描述的容器是健康的和运行的。

### **Q15。你所理解的 Kubernetes 中的一个节点是什么？**T3T5![Kubernetes Node - Kubernetes Interview Questions - Edureka](img/fae7d6fdb47909f354ba4124e0734718.png)

### **图 6:**Kubernetes 中的节点——Kubernetes 面试问题

## **建筑类 Kubernetes 面试问题**

这部分问题将涉及与 Kubernetes 建筑相关的问题。

### **Q1。Kubernetes 建筑有哪些不同的组成部分？**

[Kubernetes 架构](https://www.edureka.co/blog/kubernetes-architecture/)主要有两个组件——主节点和工作者节点。正如您在下图中看到的，主节点和工作节点中有许多内置组件。主节点有 kube 控制器管理器、kube API server、kube 调度器等。而 worker 节点在每个节点上运行 kubelet 和 kube-proxy。

![Kubernetes Architecture Components - Kubernetes Interview Questions - Edureka](img/9b1e7ebfddf4539332f0336659bf1c11.png)

### **图 7:**Kubernetes 的建筑——Kubernetes 面试问题

### **Q2。你所理解的 Kube-proxy 是什么？**

Kube-proxy 可以在每一个节点上运行，并且可以跨后端网络服务进行简单的 TCP/UDP 数据包转发。所以基本上，它是一个网络代理，反映每个节点上 Kubernetes API 中配置的服务。因此，Docker 可链接的兼容环境变量提供了由代理打开的集群 IP 和端口。

### **Q3。你能简单介绍一下 Kubernetes 中主节点的工作吗？**

Kubernetes master 控制节点，并且在节点内部存在容器。现在，这些单独的容器包含在单元中，在每个单元中，您可以根据配置和要求拥有不同数量的容器。因此，如果必须部署 pod，那么可以使用用户界面或命令行界面进行部署。然后，在节点上调度这些 pod，并且基于资源需求，将 pod 分配给这些节点。kube-apiserver 确保在 Kubernetes 节点和主组件之间建立通信。

![Kubernetes Master - Kubernetes Interview Questions - Edureka](img/1bd210e580956b9be6bb1f960d80e403.png)

### **图 8:**Kubernetes 主节点表现——Kubernetes 面试问题

### **Q4。kube-apiserver 和 kube-scheduler 的作用是什么？**

kube–API server 遵循横向扩展架构，是主节点控制面板的前端。这公开了 Kubernetes 主节点组件的所有 API，并负责在 Kubernetes 节点和 Kubernetes 主组件之间建立通信。

kube 调度器负责在工作节点上分配和管理工作负载。因此，它会根据资源需求选择最合适的节点来运行未计划的 pod，并跟踪资源利用率。它确保不会在已满的节点上安排工作负载。

### **Q5。你能简单介绍一下 Kubernetes 控制器管理器吗？**

多个控制器进程在主节点上运行，但被编译在一起作为一个进程运行:Kubernetes 控制器管理器。因此，控制器管理器是一个守护进程，它嵌入控制器并进行命名空间创建和垃圾收集。它负责并与 API 服务器通信来管理端点。

所以，主节点上运行的不同类型的控制器管理器有: ![Types Of Controllers - Kubernetes Interview Questions - Edureka](img/b85618efcc3282bda23d33b5d72ea041.png)

### **图 9:** 控制人类型——Kubernetes 面试问题

### **Q6。什么是 ETCD？**

Etcd 是用 [Go 编程语言](https://www.edureka.co/blog/golang-tutorial/)编写的，是一个分布式键值存储，用于协调分布式工作。因此，Etcd 存储 Kubernetes 集群的配置数据，表示集群在任何给定时间点的状态。

### **Q7。Kubernetes 有哪些不同类型的服务？**

以下是所使用的不同类型的服务:

![Types Of Services - Kubernetes Interview Questions - Edureka](img/35ebf26e06793f56f8e8b88b83a69838.png)

### **图 10:** 服务类型——Kubernetes 面试问题

### **Q8。你对 Kubernetes 中负载均衡器的理解是什么？**

负载平衡器是公开服务的最常见和标准的方式之一。根据工作环境，使用两种类型的负载平衡器，即内部负载平衡器或外部负载平衡器。内部负载平衡器自动平衡负载并分配具有所需配置的单元，而外部负载平衡器将流量从外部负载导向后端单元。

## **立方面试问题**

### **Q9。什么是入口网络，它是如何工作的？**

入口网络是规则的集合，充当 Kubernetes 集群的入口点。这允许入站连接，可以将入站连接配置为通过可到达的 URL、负载平衡流量或通过提供基于名称的虚拟主机向外部提供服务。因此，Ingress 是一个 API 对象，它通常通过 HTTP 管理对集群中服务的外部访问，并且是公开服务的最强大的方式。

现在，让我用一个例子向你解释入口网络的工作原理。

有 2 个节点具有 pod 和根网络名称空间，并带有一个 Linux 桥。除此之外，根网络中还添加了一个名为 flannel0(网络插件)的新虚拟以太网设备。

现在，假设我们希望数据包从 pod1 流向 pod 4。请参考下图。

![Ingress Network - Kubernetes Interview Questions - Edureka](img/1ae1e97f3815494814975af21eebf345.png)

### **图 11:**Ingress 网络工作——Kubernetes 面试问题

*   因此，数据包在 eth0 离开 pod1 的网络，并在 veth0 进入根网络。
*   然后，它被传递到 cbr0，CB r0 发出 ARP 请求以找到目的地，结果发现该节点上没有人拥有目的地 IP 地址。
*   因此，网桥将数据包发送到 flannel0，因为该节点的路由表配置了 flannel0。
*   现在，法兰绒守护进程与 Kubernetes 的 API 服务器对话，以了解所有 pod IPss 及其各自的节点，从而创建 pod IP 到节点 IP 的映射。
*   网络插件将该数据包封装在 UDP 数据包中，并使用额外的报头将源和目的地 IP 更改为各自的节点，然后通过 eth0 将该数据包发送出去。
*   现在，由于路由表已经知道如何在节点之间路由流量，它将数据包发送到目的节点 2。
*   数据包到达 node2 的 eth0，回到 flannel0 解封装，在根网络命名空间中发出。
*   同样，数据包被转发到 Linux 网桥，发出 ARP 请求，以找出属于 veth1 的 IP。
*   数据包最终穿过根网络，到达目的地 Pod4。

### **Q10。你所理解的云控制器管理器是什么？**

云控制器管理器负责持久存储、网络路由、从核心 Kubernetes 特定代码中提取特定于云的代码，以及管理与底层云服务的通信。根据您运行的云平台，它可能会被拆分成几个不同的容器，然后它使云供应商和 Kubernetes 代码的开发没有任何相互依赖性。因此，云供应商开发他们的代码，并在运行 Kubernetes 时与 Kubernetes 云控制器管理器连接。

云控制器管理器的各种类型如下:

![Types Of Cloud Controller Manager - Kubernetes Interview Questions - Edureka](img/ea63a0f2d0ba9e0ab7feb8f2f63a911a.png)

### **图 12:** 云控制器经理的类型——Kubernetes 面试问题

### **Q11。什么是容器资源监控？**

对于用户来说，了解应用程序的性能和所有不同抽象层的资源利用率非常重要，Kubernetes 通过在不同级别(如容器、容器、服务和整个集群)创建抽象来考虑集群的管理。现在，每个级别都可以被监控，这就是容器资源监控。

各种容器资源监控工具如下:

![](img/b6264867b81a42df3e17bfdd4eaa56a3.png)

### **图 13:** 集装箱资源监控工具——Kubernetes 面试问题

### **Q12。副本集和复制控制器之间有什么区别？**

副本集和复制控制器做几乎相同的事情。两者都确保指定数量的 pod 副本在任何给定时间都在运行。不同之处在于使用选择器来复制 pod。副本集使用基于集合的选择器，而复制控制器使用基于股权的选择器。

*   **基于权益的选择器:** 这类选择器允许按标签键和值过滤。因此，通俗地说，基于股票的选择器只会寻找与标签短语完全相同的 pod。 **举例**:假设你的标签键说 app = nginx 然后，使用这个选择器，您只能查找那些标签 app 等于 nginx 的 pod。
*   **基于选择器的选择器:** 这种类型的选择器允许根据一组值过滤按键。因此，换句话说，基于选择器的选择器将寻找标签在集合中被提及的 pod。 **举例:**说你的标签键说 app in (Nginx，NPS，Apache)。然后用这个选择器，如果你的 app 等于 Nginx，NPS，或者 Apache 中的任何一个，选择器就会把它当成真结果。

### **Q13。什么是无头服务？**

Headless 服务类似于“普通”服务，但没有集群 IP。该服务使您能够直接访问 pod，而无需通过代理访问它们。

### **Q14。在使用 Kubernetes 时，你能采取的最好的安全措施是什么？**

以下是您在使用 Kubernetes 时可以遵循的最佳安全措施:

![Security Measures - Kubernetes Interview Questions - Edureka](img/2579f764f45f5873547a08883cd62f59.png)

### **图 14:** 最佳安保措施——Kubernetes 面试问题

### **Q15。什么是联合集群？**

在联合集群的帮助下，多个 Kubernetes 集群可以作为单个集群进行管理。因此，您可以在一个数据中心/云中创建多个 Kubernetes 集群，并使用联合在一个位置控制/管理它们。

联合集群可以通过以下两件事来实现这一点。请参考下图。

![Federated Clusters - Kubernetes Interview Questions - Edureka](img/24866a5caeeb5885c532dbc863d13dd7.png)

### **图 15:** 密集地——Kubernetes 面试问题

## **情景式面试试题**

这部分问题将由你在面试中可能会遇到的各种情景问题组成。

**场景 1:** 假设一家建立在整体架构上的公司处理众多产品。现在，随着该公司在当今扩展行业的扩张，他们的整体架构开始引发问题。

*你认为该公司如何从整体服务转向微服务并部署他们的服务容器？*

**解:**

由于该公司的目标是从他们的单片应用程序转移到微服务，他们可以并行地一件一件地构建，只需在后台切换配置。然后他们可以将这些内置的微服务放在 Kubernetes 平台上。因此，他们可以从迁移一次或两次服务开始，并监控它们以确保一切运行稳定。一旦他们觉得一切顺利，他们就可以将应用程序的其余部分迁移到他们的 Kubernetes 集群中。

**场景 2:** 假设一家跨国公司拥有非常分散的系统，有大量的数据中心、虚拟机和从事各种工作的员工。

*你认为这样一家* *的公司如何能和 Kubernetes 以一致的方式管理所有的任务？*

**解:**

众所周知，信息技术部门启动了数以千计的容器，任务在分布于世界各地的众多节点上运行。

在这种情况下，公司可以使用能够为他们提供敏捷性、横向扩展能力以及开发基于云的应用程序实践的产品。

因此，该公司可以使用 Kubernetes 定制他们的调度架构，并支持多种容器格式。这使得容器任务之间的密切关系成为可能，通过对各种容器网络解决方案和容器存储的广泛支持，提高了效率。

**场景 3:** 考虑这样一种情况，一家公司希望通过保持最低的成本来提高其效率和技术运营的速度。

你认为公司将如何努力实现这一目标？

**解:**

该公司可以通过构建 CI/CD 渠道来实施 DevOps 方法，但这里可能会出现一个问题，即配置启动和运行可能需要时间。因此，在实施 CI/CD 管道后，公司的下一步应该是在云环境中工作。一旦他们开始在云环境上工作，他们就可以在集群上调度容器，并可以在 Kubernetes 的帮助下进行编排。这种方法将有助于公司减少部署时间，并加快跨各种环境的速度。

**场景 4:** 假设一家公司希望修改其部署方法，并希望构建一个更具可扩展性和响应能力的平台。

您认为这家公司如何才能做到这一点来满足他们的客户？

**解:**

为了给数百万客户带来他们期望的数字体验，该公司需要一个可扩展且响应迅速的平台，以便他们能够快速将数据传输到客户网站。现在，要做到这一点，该公司应该从他们的私有数据中心(如果他们使用任何数据中心)转移到任何云环境，如 AWS。不仅如此，他们还应该实现微服务架构，以便可以开始使用 Docker 容器。一旦他们准备好基础框架，他们就可以开始使用最好的编排平台，即 Kubernetes。这将使团队能够自主地构建应用程序并快速交付它们。

**场景 5:** 假设一家跨国公司有一个非常分散的系统，希望解决单一代码库的问题。

你认为公司如何解决他们的问题？

**解**

为了解决这个问题，他们可以将他们的整体代码库转移到微服务设计，然后每个微服务都可以被视为一个容器。因此，所有这些容器都可以在 Kubernetes 的帮助下进行部署和编排。

Want to get Kubernetes Certified? [<button>View Batches Now</button>](https://www.edureka.co/kubernetes-certification)

## **立方面试问题**

**场景 6:** 我们都知道，从单片到微服务的转变解决了开发端的问题，但是增加了部署端的问题。

*公司如何解决部署端的问题？*

**解**

团队可以试验容器编排平台，如 Kubernetes，并在数据中心运行。因此，有了它，公司可以生成一个模板化的应用程序，在五分钟内部署它，并在那时将实际的实例容器化到登台环境中。这种 Kubernetes 项目将有几十个并行运行的微服务来提高生产率，因为即使一个节点出现故障，也可以立即重新调度，而不会影响性能。

**场景 7:** 假设一家公司想要通过采用新技术来优化其工作负载的分布。

*公司如何高效的实现这种资源分配？*

**解**

这个问题的解决方案不是别人，正是 Kubernetes。Kubernetes 确保资源得到有效优化，并且只使用特定应用程序所需的资源。因此，使用最好的容器编排工具，公司可以有效地实现资源的分配。

**场景 8:** 假设一家拼车公司希望通过同时扩展其平台来增加服务器数量。

您认为公司将如何处理服务器及其安装？

**解**

公司可以采用集装箱化的概念。一旦他们将所有应用程序部署到容器中，他们就可以使用 Kubernetes 进行编排，并使用 Prometheus 等容器监控工具来监控容器中的操作。因此，通过容器的这种使用，为他们提供了更好的数据中心容量规划，因为由于服务和运行它们的硬件之间的这种抽象，他们现在将受到更少的限制。

**场景 9:** 考虑一个场景，其中一家公司想要向其具有各种环境的客户提供所有需要的分发。

*你认为他们如何以动态的方式实现这一关键目标？*

**解**

该公司可以使用 Docker 环境，组建一个跨部门团队，使用 Kubernetes 构建一个 web 应用程序。这种框架将帮助公司实现在最短的时间内将所需的东西投入生产的目标。因此，随着这样一台机器的运行，公司可以向具有不同环境的所有客户分发资料。

**场景 10** :假设一家公司想要在从裸机到公共云的不同云基础设施上运行各种工作负载。

*在存在不同接口的情况下，公司将如何实现这一点？*

**解**

公司可以将其基础设施分解为微服务，然后采用 Kubernetes。这将使公司能够在不同的云基础设施上运行各种工作负载。

### **选择题面试题**

这部分问题将由多项选择题组成，这是面试中经常被问到的问题。

**Q1。Kubernetes 集群中有哪些爪牙？**

1.  它们是主节点的组件。
2.  它们是集群的工作马/工作者节点。【答案】
3.  他们正在监控在库伯内特广泛使用的发动机。
4.  他们是码头集装箱服务公司。

**Q2。Kubernetes 集群数据存储在以下哪个位置？**

1.  Kube-apiserver
2.  库伯莱
3.  Etcd【Ans】
4.  以上都不是

**Q3。他们中的哪一个是 Kubernetes 控制器？**

1.  复制集
2.  部署
3.  滚动更新
4.  复制集和部署[Ans]

**Q4。以下哪些是 Kubernetes 的核心对象？**

1.  豆荚
2.  服务
3.  卷
4.  以上所有【Ans】

**Q5。Kubernetes 网络代理运行在哪个节点上？**

1.  主节点
2.  工人节点
3.  所有节点【Ans】
4.  以上都不是

**Q6。**节点控制器**的职责是什么？**

1.  给节点分配一个 CIDR 块
2.  维护节点列表
3.  监控节点的健康状况
4.  以上所有【Ans】

**Q7。复制控制器的职责是什么？**

1.  用一个命令更新或删除多个 pods】
2.  有助于达到期望的状态
3.  如果现有 pod 崩溃，创建新的 pod
4.  以上所有【Ans】

**Q8。如何定义一个没有选择器的服务？**

1.  指定外部名称【Ans】
2.  用 IP 地址和端口指定一个端点
3.  只需指定 IP 地址
4.  指定标签和 api 版本

**Q9。1.8 版本的 Kubernetes 引入了什么？**

1.  污点和容忍【Ans】
2.  集群级日志记录
3.  秘密
4.  联合集群

**Q10。** **Kubelet 调用的检查一个容器的 IP 地址是否开放的处理程序是？**

1.  http 操作
2.  执行
3.  tcpsoketaction[ans]
4.  以上都不是

*被这些问题搞得不知所措？*

我们在 edureka！在这里帮助你成为认证 DevOps 专家的旅程中的每一步，因此除了这个 Kubernetes 面试问题博客，我们还推出了 **[DevOps 面试问题博客](https://www.edureka.co/blog/interview-questions/top-devops-interview-questions-2016/)** 来帮助你解决与 DevOps 相关的问题！

Want to learn the best orchestration tool? [<button>Learn Now</button>](https://www.edureka.co/kubernetes-certification)I hope you found this Kubernetes Interview Questions blog informative. The questions you learned in this Kubernetes Interview Questions blog are the most sought-after questions asked in the interview.

*有问题吗？请向我们的 edureka 社区提及，我们的专家将在第一时间回复。*