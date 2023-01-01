# Jenkins vs Jenkins X–了解 Jenkins X 与 Jenkins 的区别

> 原文：<https://www.edureka.co/blog/jenkins-vs-jenkins-x/>

Jenkins 一直是当今行业在日常 [DevOps 生命周期](https://www.edureka.co/blog/devops-lifecycle/)中使用的最受欢迎的[持续集成服务器](https://www.edureka.co/blog/continuous-integration/)之一。另一方面，Kubernetes 在容器编排领域不断发展。[开发人员](https://edureka.co/devops-certification-training)需要一种方法，通过减少生产时间和运营成本来实现利益最大化。嗯，Jenkins X 通过为 Kubernetes 上的现代云应用程序提供自动化的 CI/CD 解决方案，服务于开发人员的这一目的。在这篇关于 Jenkins vs Jenkins X 的文章中，我将按以下顺序讨论这两者的不同之处:

*   ***[詹金斯是什么？](#whatisjenkins)***

*   ***[詹金斯 X 是什么？](#whatisjenkinsx)***

*   ***[需要詹金斯 X](#needofjenkinsx)T5***

*   ***[詹金斯 vs 詹金斯 X](#differences)***

## **詹金斯是什么？**

Jenkins 是当今市场上最受欢迎的工具之一，是为持续集成目的而构建的。Jenkins 用  [Java](https://www.edureka.co/blog/java-tutorial/) 编写，用于构建和测试软件项目，并使开发人员可以轻松地将所需的更改集成到项目中。这个工具还旨在通过集成大量的  [测试](https://www.edureka.co/blog/software-testing-tutorial/) 和部署软件来持续交付软件。

![Jenkins Logo - Jenkins vs Jenkins X - Edureka](img/57defc5526eb73ce21e3b2c5fd5f600f.png)

通过使用  [詹金斯](https://www.edureka.co/blog/what-is-jenkins/)，初创公司到高速增长的公司可以通过自动化加速软件开发过程。另外，  [Jenkins](https://www.edureka.co/blog/jenkins-tutorial/) 集成了不同种类的开发生命周期过程，如构建、  文档、测试、打包、阶段、部署、静态分析等等。它提供了各种插件，允许集成各种 DevOps 阶段。例如，如果你想使用一个特定的工具，那么你只需要为这个特定的工具安装所需的插件。

## **詹金斯 X 是什么？**

詹姆斯·斯特拉坎(James strach an)，詹金斯 X 的首席架构师将其定义为一种开源的固执己见的方式，用 [Kubernetes](https://www.edureka.co/blog/kubernetes-tutorial/) 在本地进行[连续交付](https://www.edureka.co/blog/continuous-delivery/)，而不用太担心底层基础设施。它是 Jenkins 的扩展或子项目，由流行的云平台支持，如 [Amazon](https://www.edureka.co/blog/amazon-aws-tutorial/) 、 [Azure](https://www.edureka.co/blog/microsoft-azure-tutorial) 、Google IBM Cloud、OpenShift 和 Pivotal。Jenkins X 使用 DevOps 的最佳实践，为开发人员提供更快的速度并减少生产时间。

![Jenkins X Logo - Jenkins vs Jenkins X - Edureka](img/b96bd3f756504863c2e69d01565f6ff3.png)

除此之外，Jenkins X 还确保降低复杂性，因为只需一个命令就可以创建一个 [Kubernetes 集群](https://www.edureka.co/blog/logging-monitoring-elasticsearch-fluentd-kibana/)，安装工具来管理应用程序，创建和构建部署管道，设置 webhooks，还可以将应用程序部署到各种环境中。它还确保当项目开始时，不会花费大量时间来创建结构和收集所需的文件。

简而言之，Jenkins 提供了 Jenkins 所需的所有配置，你不必知道构建一个 [CI/CD 管道](https://www.edureka.co/blog/ci-cd-pipeline/)需要哪些插件。在这篇关于詹金斯 vs 詹金斯 X 的文章中，让我们了解詹金斯 X 的需求

## **詹金斯 X 的需求**

毫无疑问，在过去的几年中，软件开发的方式已经发生了变化。随着 DevOps 越来越受欢迎，公司正在使用这种方法快速交付他们的软件。这是因为，DevOps 确保了开发速度的降低，停机时间的减少，但与此同时，业界也看到了许多其他的变化。

*   [**微服务**](https://www.edureka.co/blog/microservices-tutorial-with-example) 是最受欢迎的部署模式之一，如今正被当今高速增长的市场所吸纳。与单片应用不同，[微服务应用](https://www.edureka.co/blog/what-is-microservices/)是更小粒度和独立的服务。这些提供了各种好处，导致这些公司将微服务与 DevOps 结合使用。

*   第二个是**容器生态系统**，与[微服务架构](https://www.edureka.co/blog/microservice-architecture/)齐头并进。在当今的行业中，同一主机上的各种容器可以部署使用不同技术/框架构建的微服务。这让开发人员可以自由地使用他们想使用的任何技术，并进一步编排这些容器。

*   最后来看**容器编排**， [Kubernetes](https://www.edureka.co/blog/what-is-kubernetes-container-orchestration) 正在当今市场崛起。它为世界上一些最大和最复杂的部署提供动力，著名的云服务提供商如 [GCP](https://www.edureka.co/blog/google-cloud-services/) 、 [AWS](https://www.edureka.co/blog/what-is-aws/) 、 [Azure](https://www.edureka.co/blog/what-is-azure/) 和 Oracle Cloud 已经宣布在其云平台中集成 Kubernetes。它的开源安装简化了优化操作，并升级了容器的编排。

有了所有这些变化，开发人员可以使用许多选项，用各种 CI/CD 工具来分割和修改他们的开源系统。在使用 Kubernetes 时，企业可能需要花费大量时间来理解必须使用哪些工具来开发成功的 CI/ CD 管道。这是因为没有一种直接的方法来管理具有插件和配置的正确组合的 Kubernetes 集群。

为了避免这种情况，开发人员社区希望找到一种解决方案，利用 Jenkins 在云中实现 CI/CD 的自动化，以帮助那些苦于使用 Kubernetes 或者以前没有使用过它的人。詹金斯 X 是这个问题的解决方案，这就是詹金斯 X 如何进入市场。

现在你知道了什么是 Jenkins 和 Jenkins X，让我们来了解一下它们之间的区别。

## **詹金斯 vs 詹金斯 X**

Jenkins X 坚持自己的观点，习惯于更好地使用容器化和编排工具，如 Docker 或 Kubernetes。另一方面，詹金斯持不赞同的观点，但他们两人是相互关联的，因为用詹金斯 X 可以做的事情也可以用詹金斯做。然而，要用 Jenkins 完成同样的任务，您将需要几个插件和集成。因此，Jenkins X 用于简化配置，并让您利用 Jenkins 2.0 的强大功能。它还允许您使用 Helm、Draft、simmono、ChartMuseum、Nexus 和 Docker Registry 等开源工具轻松构建云原生应用。

除此之外，Jenkins X 定义了过程，而 Jenkins 则适应了要求或需要的过程。Jenkins X 还采用了 CLI/API 优先的方法，并依赖配置作为代码来包含外部工具(例如，单目、头盔等)。相反，Jenkins 使用第一种 GUI 方法，通过 UI 进行配置，并且严重依赖插件。

所以，如果要我总结詹金斯和詹金斯 X 的区别，参考下表:

| 詹金斯 | 詹金斯 X |
| 詹金斯持不赞成的观点 | 詹金斯 X 采取了固执己见的观点 |
| 在 Jenkins 中，您需要几个集成和插件来配置 | 它简化了配置 |
| 詹金斯适应被要求或需要的过程 | 定义流程 |
| Jenkins 使用第一种 GUI 方法，通过 UI 进行配置，并且严重依赖插件。 | 它采用 CLI/API 优先的方法，并依赖配置作为代码来包含外部工具 |

至此，我们结束了这篇关于 Jenkins vs Jenkins X 的文章。如果您发现这篇关于“Jenkins vs Jenkins X”的文章相关，请查看 Edureka 的 [***DevOps 培训，这是一家值得信赖的在线学习公司，拥有遍布全球的 450，000 多名满意的学习者。Edureka DevOps 认证培训课程可帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Docker、Nagios、Ansible 和 GIT，用于自动化 SDLC 中的多个步骤。***](https://www.edureka.co/devops-certification-training)