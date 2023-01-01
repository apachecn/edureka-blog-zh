# 创建 Dapps 的最佳以太坊开发工具

> 原文：<https://www.edureka.co/blog/ethereum-development-tools/>

以太坊通过在其系统上实现智能合约支持，为区块链开启了无数可能性。这反过来又、向绝大多数开发者开放了以太坊，让他们通过用以太坊特有的语言开发智能合约，如 **Solidity** 、 **Serpent** 和 **LLL** ，来创建任何一种可以在区块链上运行的应用。抛开语言不谈，几个*以太坊开发工具*已经被开发了很多年，让我们作为开发者的生活变得不那么繁琐。

可以找到各种各样的文章，关于[以太坊](https://www.edureka.co/blog/what-is-ethereum/)和[智能合约](https://www.edureka.co/blog/smart-contracts/)的发展，但是很少有文章讨论让这些变得如此无缝的工具。因此，我决定写一篇文章，深入探讨各种以太坊开发工具。

## **以太坊开发工具**

为了方便起见，我将工具分为四大类，即:

1.  [集成开发环境](#ide)[1.1 Remix](#remix)[1.2 EthFiddle](#eth)
2.  [带有 RPC 接口的本地测试节点](#node)[2.1 Ganache/Test RPC](#ganache)[2.2 Pythereum](#pyeth)
3.  [命令行基础开发工具](#cli) [3.1 松露](#truffle)[3.2 Embark](#embark)[3.3 Dapp/Dapple](#dapp)
4.  [代码分析器](#code)[4.1 Solium](#solium)[4.2 Open-Zeppelin](#zeppelin)
5.  [浏览器](#browser) [5.1 薄雾](#mist) [5.2 元蒙版](#mask)

因此，让我们从以太坊开发工具列表开始，讨论 ide。

## **集成开发环境**

开发人员构建应用程序的第一项任务是编写核心逻辑，这通常是在集成开发环境中输入的。IDE 的总体目标和主要好处是 提高开发人员的生产力。ide 通过减少设置时间、提高开发任务的速度、让开发人员了解最新情况以及标准化开发过程来提高生产率。说到扎实，第一个想到的 IDE 就是 Remix。

### **混音**

Remix 以前被称为 Browser-Solidity，是一个基于 web 的 IDE，专门针对 Solidity 和以太坊开发环境。

![Remix IDE - Ethereum Development Tools - Edureka](img/48f8c9c58dd71d42d40d14ee921ee38f.png)

优点:

*   用最新的编译器版本编译代码
*   在定制环境中部署和运行智能合约，如 JavaScript 虚拟机或注入的 Web3.js 提供程序。
*   允许你从 GitHub 和 Swarm 导入代码

缺点:

*   初学者很难理解

除了 Remix，还有另一个基于浏览器的 IDE很棒，但有其他用途。这个叫做 Ethfiddle，非常适合用来展示代码。虽然 remix 提供了在不同网络和环境下测试代码的灵活性，但由于其简单的嵌入特性，ethfiddle 完全是为了在演示文稿上共享您的代码。

优点:

*   轻松嵌入和共享功能

缺点:

*   速度慢，功能不如混音丰富

为了在本地编译你的 solidity 代码，可以使用节点包管理器轻松安装 SOLC 编译器。除此之外，像 ***崇高文本*** 和 ***原子*** 这样的开源文本编辑器对可靠性语法高亮显示有很好的包支持。

## **以太坊开发工具|以太坊开发者课程| edu reka**

[//www.youtube.com/embed/Ysgv2wTSCd0?rel=0&showinfo=0](//www.youtube.com/embed/Ysgv2wTSCd0?rel=0&showinfo=0)

## **测试节点与 RPC 接口**

众所周知，区块链上的一切都是不可改变的。即使对智能合约的更新也不能注册到相同的地址，而必须作为新实例部署到新地址。这也意味着智能合同不能在主区块链网络上测试，因为一旦部署到主网络上，任何更改都是不可能的。因此，测试网络/节点构成了以太坊开发工具不可或缺的一部分，因为以太坊开发人员使用本地测试节点来测试契约的交互。

我们来讨论一下最受欢迎的本地测试网络

首先是 Ganache-cli，它是以太坊开发者使用最广泛的本地测试节点。Ganache 是一个用于以太坊开发的个人区块链，可以用来部署契约、开发应用程序和运行测试。它既可以作为桌面应用程序使用，也可以作为命令行工具使用(以前称为 TestRPC)。Ganache 可用于 Windows、Mac 和 Linux。

![Ganache - Ethereum Development Tools - Edureka](img/ead37b671b764666d5898384021a8ee6.png)

使用 ganache，您可以—

*   快速查看所有账户的状态，包括其地址、私钥、交易和余额。
*   查看 Ganache 内部区块链的日志输出，包括响应和其他重要的调试信息。
*   只需一次点击即可配置高级挖掘，设置最适合您的开发需求的阻塞时间。
*   检查所有的块和交易，以深入了解幕后发生了什么。

### 腐霉

接下来，在列表上，我们有**python ereum**，这是一个用 python 编写的本地测试节点工具。它比 ganache 轻量级得多，但功能不够丰富。

![Pythereum - Ethereum Development Tools - Edureka](img/7f1eadb1e0e4880fe4a7850e3582ce5f.png)

使用 pythereum，您可以

*   用创世模块创建一个新的测试区块链
*   用传入的起源状态创建新的测试状态。
*   使用给定的私钥向给定的地址发送带有给定值和数据的交易。

## **基于 CLI 的开发管理工具**

基于以太坊开发工具的命令行主要有三种，即

1.  松露
2.  上船
3.  斑纹

让我们一个接一个地简单了解一下。

### **松露**

所以我们的清单上的第一个是**松露**，它也恰好是列出的三种工具中最受欢迎的一种。Truffle 是以太坊的开发环境、测试框架和资产管道，旨在让以太坊开发者的生活更轻松。“ConsenSYS”公司负责块菌的开发和维护。

用松露，你得到:![TruffleSuit - Ethereum Development Tools - Edureka](img/6d1aba715b59e4da1c09eedddbc44b34.png)

*   内置智能合约编制、链接、部署和二进制管理。
*   使用 Mocha 和 Chai 进行自动化合同测试。
*   支持定制构建流程的可配置构建管道。
*   可脚本化的部署&迁移框架。
*   部署到许多公共&专用网络的网络管理。
*   用于直接合同沟通的交互式控制台。
*   在开发过程中即时重建资产。
*   在 Truffle 环境中执行脚本的外部脚本运行程序。

### **登上**

下一个以太坊开发工具是 **Embark** 。Embark 是一个框架，允许你使用无服务器的 html5 应用程序轻松开发和部署分散式应用程序(DApps)。Embark 目前集成了 EVM 区块链(以太坊)、分散存储(IPFS)和分散通信平台(耳语和轨道)。支持 Swarm 进行部署。

使用 Embark 您可以:![Embark - Ethereum Development Tools - Edureka](img/2e13826189a96f01e0703c78f75816b0.png)

*   自动部署契约，并使它们在您的 JS 代码中可用。Embark 观察变化，如果你更新合同，Embark 将自动重新部署合同(如果需要)和 dapp
*   使用 javascript 执行测试驱动的合同开发
*   跟踪已部署的合同；仅在真正需要时部署
*   通过登船 JS 在 DApp 上轻松存储&检索数据。包括上传和检索文件。
*   将整个应用程序部署到 IPFS 或 Swarm。
*   轻松管理相互依赖的合同的复杂系统。

### **Dapp**

最后一个基于命令行的以太坊开发工具是 **Dapple** 。目前，Dapple 已经被弃用，取而代之的是由同一组开发人员开发的名为 **Dapp** 的新工具。Dapp 是一个用于智能合约开发的简单命令行工具。它支持这些常见的用例:

*   套餐管理![Dapple - Ethereum Development Tools - Edureka](img/4de915e31f74ea642686fbea3771f095.png)
*   源代码构建
*   单元测试
*   简单合同部署

## **代码分析工具**

为分散式网络编写干净安全的代码绝非易事。从存储和安全的角度来看，有很多东西需要担心，尤其是当你的大部分代码都在处理别人的钱的时候。该州任何错误的回滚都可能导致重大损失。为了避免这种情况，开发了特殊的代码分析器来帮助开发人员编写干净安全的代码。

Solium 和 Open-Zeppelin 就是两个这样的工具，当谈到以太坊开发工具时，我会想到它们

Solium 是一个 solidity code linter，它允许你编写健壮而时髦的智能合同。Solium 的工作方式就像一个解释器，它不断检查你的代码的风格和安全问题

![Solium - Ethereum Development Tools - Edureka](img/63649f6fcd4cd96d9cffc879aed8ec01.png)

使用 Solium，您可以:

*   分析你的 Solidity 代码的安全问题并修复它们。
*   在您的整个组织中标准化智能合约实践，与您的构建系统集成并放心部署

### **开着飞艇**

![Open Zeppelin - Ethereum Development Tools - Edureka](img/8fd107b4e8f49f3e7d19e5669638849f.png)

Open-Zeppelin ，是一个用于编写安全智能合同的可靠框架。在开发者中使用 open-zeppel 可以使用通用的契约安全模式，用 solidity 语言构建分布式应用、协议和组织。open zeppelin 的伟大之处在于它与 Truffle 无缝集成，让您的生活稍微轻松一些。

## **浏览器**

区块链以太坊需要一个专门满足其需求的浏览器，以便查看有关状态、收据和交易的信息。让我们讨论一下开发人员用来分析他们在区块链上的应用交互的最流行的浏览器

### **薄雾**

Mist Browser(以前的以太坊 Dapp 浏览器)是以太坊的最终用户界面。它是浏览和使用 Dapps 的首选工具，是专门为非技术用户设计的。

![Mist - Ethereum Development Tools - Edureka](img/e62009daa894dd6adc6d757d2b7141fa.png)

使用 mist 您可以:

*   查看区块链状态

### **MetaMask**

![Metamask - Ethereum Development Tools - Edureka](img/5e371afad5debb0aec02c977578f35dc.png)

虽然 metamask 并不是真正的“浏览器”，但它将谷歌 Chrome 变成了一个以太坊浏览器，允许它从区块链获取数据，并允许用户安全地发送或接收签名交易。该扩展将以太坊 web3 API 注入到每个网站的 javascript 上下文中，因此 dapps 可以直接从区块链中读取。Metamask 可以作为浏览器扩展轻松安装在 *chrome* 、 *opera* 和 *firefox* 上。

虽然有很多工具可以帮助你在以太坊上进行分散化的应用开发，但这些工具对我帮助最大。尽管如此，我还是强烈建议大家去看看其他可用的以太坊开发工具，它们对我们的开发者生活有所帮助。

*如果您希望了解更多关于以太坊区块链的知识，并在区块链技术领域建立职业生涯，那么请查看我们的 [**区块链课程**](https://www.edureka.co/blockchain-training) ，该课程提供讲师指导的现场培训和真实项目体验。该培训将帮助您深入了解区块链，并帮助您掌握该主题。*

<article class="maincontentblog">*Got a question for us? Please mention it in the comments section **and we will get back to you as soon as possible.*</article>