# 基础设施即代码——它是什么？为什么它很重要？

> 原文：<https://www.edureka.co/blog/infrastructure-as-code/>

如果您能够像编写软件一样编写您的基础架构，这不是很好吗？当然，那就太好了。这是基础设施即代码(IaC)这一术语的核心思想。IaC 是整个[***devo PS***](https://www.edureka.co/devops-certification-training)建立的基础。所以在这篇博客中，我将详细讨论 IaC。我们将要讨论的主题如下

*   [什么是基础设施即代码？](#what)
*   [IaC 是如何工作的？](#how)
*   [基础设施作为代码的优势](#benefits)
*   [基础设施即代码工具](#tools)

所以让我们开始讨论吧。首先，让我们试着了解一下传统的基础设施管理方式。

过去，管理 IT 基础架构是一个手动过程。人们会将服务器放在适当的位置并进行配置。只有在将机器配置为操作系统和应用程序所需的正确设置后，才能部署应用程序。不出所料，这种手动流程通常会导致如下几个问题

*   费用
*   可量测性
*   有效性
*   不一致

## **什么是基础设施即代码？**

基础设施即代码(IaC)是通过机器可读的定义文件，而不是物理硬件配置或交互式配置工具来管理和配置计算机数据中心的过程。由此管理的 IT 基础架构包括物理设备(如裸机服务器)以及虚拟机和相关的配置资源。

## **![What-is-Infrastructure-as-Code-Infrastructure-as-Code-Edureka](img/ef986fabd4fa7d15757a6917d3de1122.png)IaC 是如何工作的？**

IaC 工具的具体工作方式各不相同，但我们通常可以将它们分为两种主要类型:遵循 ***命令式*** 方法的工具，以及遵循 ***声明式*** 方法的工具。如果你认为上面的类别与编程语言范例有关，那么你绝对是正确的。

*   命令式方法“发号施令”。它定义了一系列命令或指令，这样基础设施就可以得到最终结果。
*   另一方面，声明式方法“声明”期望的结果。声明性方法显示了最终结果的样子，而不是显式地概述基础设施达到最终结果所需的步骤序列。

## **基础设施作为代码的优势**

### **速度**

![Speed](img/df2fa2c091a18bbf22394802cbb728b9.png)IaC 提供的第一个重要优势是速度。将基础设施作为代码，您可以通过运行脚本快速设置完整的基础设施。您可以对每个环境都这样做，从开发到生产，经过试运行、QA 等等。

### **一致性**

手动流程有时会导致错误。无论您如何努力，手动基础架构管理都会导致差异。IaC 通过让配置文件本身成为事实的唯一来源来解决这个问题。这样，您可以保证相同的配置会被反复部署，不会有差异。

### **问责**

这个又快又简单。因为您可以像任何源代码文件一样对 IaC 配置文件进行版本控制，所以您可以完全跟踪每个配置所遭受的更改。不再有猜谜游戏，谁做了什么，什么时候。

### **效率提高**

![](img/f8f0a027b4c5aa5e8de1484532edb86a.png)

IaC 可以让整个软件开发生命周期更加高效。通过将基础设施用作代码，您可以在许多阶段部署您的基础设施架构。这使得整个软件开发生命周期更加有效，将团队的生产力提升到新的水平。

### **降低成本**

毫无疑问，IaC 的主要优势之一是降低基础设施管理成本。通过将云计算与 IaC 结合使用，您可以大幅降低成本。这是因为你不必花钱购买硬件、雇人操作硬件、建造或租用物理空间来存储硬件。

## **基础设施即代码工具**

### **AWS 云组**

![](img/af93f07554212f017532bf5850fccada.png)

CloudFormation 允许用户在 JSON 或 YAML 模板文件中建模他们的基础设施。该服务还增加了自动化功能，以可重复和可管理的方式帮助您部署资源，并且您只需为自己使用的资源付费。根据您的应用程序规范配置模板后，CloudFormation 将为您处理剩下的任务。

明文的使用非常方便。YAML 或 JSON 都受支持，而且从 CloudFormation 提供的许多模板中很容易建立任何复杂程度的安全基础设施模型。

### **Azure 资源管理器**

![](img/36d3874d376dc21ad027d6ff0a09f7ae.png)

使用该工具，用户能够通过 Azure 资源管理器模板(ARM 模板)在一个无缝周期中供应基础设施和处理依赖关系。您的模板使用的资源在 JSON 中以声明方式描述，您也可以在一个 ARM 模板中声明多个 Azure 资源，以建立整个项目环境。

因为 ARM 模板也是幂等的，所以您可以无限次地重用同一个模板，并且总是得到相同的结果。使用 VSTS 仪表板直观地监控您的所有构建和发布，并快速了解您的环境的整体健康状况和模板的质量。资源管理器还支持服务器实例的分组以及组的统一管理。

### **谷歌云部署管理器**

![](img/03df1dfbfae1611a61f6b4030040d618.png)

该工具的执行基于配置文件，如 YAML 和模板(JINJA2 或 PYTHON ),所有这些都在 Google 云平台内。它还允许您定义您的资源并同步部署它们。您可以访问 Beta 和 Alpha 功能，并且可以使用自动扩展和负载平衡功能完全编写所有部署的脚本。

Google CDM 也支持预览；这意味着您不必直接提交变更，而是可以预先了解部署和变更将会产生的影响。该功能可以避免人为错误，并从整体上加强和稳定您的基础架构。

### **地形**

![](img/07df80361184aadff15778e6a684bbf9.png)

Terraform automation 有各种形式，并在不同程度上与核心计划/应用周期相协调。一些团队在本地运行 Terraform，但是他们使用包装器脚本来为 Terraform 运行建立一个一致的工作目录。其他开发团队也可能完全在另一个编排工具(如 Jenkins)中运行 Terraform。到目前为止，它是这个列表中适应性最强的工具，但至少从一开始，它就具有潜在的威胁性。

与 Google CDM 类似，Terraform 也支持变更和供应预览，此外，它还具有一组用于复制部署和单个服务器实例的功能。Terraform 还进一步发展了它的版本控制和远程状态，为远程团队的协作提供了一个集中的事实来源。

### **厨师**

![](img/b7a170151bc0dc76064b37240cdc4693.png)

Chef 是 CI/CD 从业者中非常流行的 IaC 工具。它使用基于 Ruby 的 DSL，这无疑是一个巨大的优势。它从一开始就有“食谱”版本，并允许您维护一致的配置。即使基础设施需要跟上其托管的应用程序的快速增长，这也是可能的。

Chef 在其配置的核心提供食谱和烹饪书。这些是您可以开箱即用的模板和模板集合的自封称谓。通常一个 cookbook 应该与一个任务相关，但是它可以根据所涉及的资源提供许多不同的服务器配置。由于它支持云供应 API，Chef 还可以很好地与其他 IaC 工具(包括 Terraform)以及其他多种云环境一起工作。

### **可回答的**

![](img/93fc8b698caa2314e0730d192ea28065.png)

[Ansible](https://www.edureka.co/blog/ansible-tutorial/) 是一个从一开始就以自动化的角度设计的工具。该工具专注于提供“极其简单”的配置语言，并且能够立即管理云实例，无需修改。它对于执行任意的 It 流程编排也很有用，例如零停机滚动更新、热修复等等，而不是特定于配置管理。您不需要将系统作为单独的单元来管理，您只需要描述组件和系统之间的交互方式，Ansible 会处理剩下的工作。

Ansible 也是目前市场上较为灵活的 IaC 工具之一。您不会受限于它提供的功能。相反，您可以开发自己的模块和例程来满足特定的需求。它甚至有一个吸引人的 GUI 用于设置和监控。

**木偶**

![Devops Blog - Puppet Logo - Edureka](img/5c9137fa6bbfd948c52fd39f8690b44e.png)

[Puppet](https://www.edureka.co/blog/puppet-tutorial/) 对 IaC 设置和自动化采取了更全面的方法。该工具运行 Reddit、Dell 和 Google 等几家大公司的数据中心，并运行在所有操作系统上。它还拥有这个列表中最先进的界面之一。这个工具使用基于 Ruby 的 DSL 作为主要语言来定义基础设施的最终状态。

然后，Puppet 将为您找出实现最终状态的最佳方式。它还监视基础设施是否有任何偏离定义的最终状态的变化。它会自动更正这些更改。这是一个专门为系统管理员开发的工具，并得到了企业和社区的大力支持。

所以现在我们已经结束了这篇关于基础设施作为代码的博客。我们已经介绍了关于这个主题的大部分基本知识。

*既然您已经将基础设施理解为代码，那么请查看 Edureka 提供的* *[DevOps 培训](https://www.edureka.co/devops-certification-training)，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka DevOps 认证培训课程帮助学员了解什么是 DevOps，并获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Nagios、Ansible、Chef、Saltstack 和 GIT，用于自动化 SDLC 中的多个步骤。*

*有问题吗？请在评论区提到它，我们会给你回复。*