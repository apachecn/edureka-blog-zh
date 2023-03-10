# 设置智能合同开发环境

> 原文：<https://www.edureka.co/blog/building-smart-contract-development-environment/>

在任何区块链讨论中最常听到的术语是“智能合同”，这被称为区块链最引人注目的功能。智能合约是任何以太坊应用的支柱。而设置智能合约开发环境，对于一个区块链开发者来说，是一件非常重要的事情。

在这篇**设置智能合同开发环境**的博客中，我将涉及以下主题:

*   什么是智能合同？
*   [如何开始设置智能合约开发环境？](#Howtostartthedevelopmentofsmartcontracts)
*   [智能合同语言](#SmartContractLanguage)
*   [设置开发环境](#SettinguptheDevelopmentEnvironment)

## 什么是智能合同？

嗯，做一个简单的谷歌搜索最终会有多个链接。

维基百科 定义“智能合同是一种计算机协议，旨在以数字方式促进、验证或执行合同的协商或履行。”

尼克·萨博 将智能合约定义为发生在区块链或分布式账本上的通用计算。

一个[智能契约](https://www.edureka.co/blog/smart-contracts/)，本质上是一个内置于代码中的契约。例如，采购订单是存在于买方和卖方之间的合同，以最简单的形式保存。要成功执行采购订单，必须满足某些条件。几个条件

1.  买方成功支付货款。
2.  供应商以合适的条件向买方提供的货物。
3.  在购买时约定的到期日之前交付的货物。
4.  采购订单中约定的退货条件。

![Purchase order- What are smart contracts - edureka](img/b8a53b8e2be3f5fae2cb4001dae85e70.png)

这些是最简单的采购订单中的一些简单条件。

1.  这些条件可以转换成数字格式，即数字化处理。
2.  像创建采购订单、履行订单这样的操作在程序中被公开为一个功能，这些操作被称为事务。
3.  交易只能由指定的参与者(买方、卖方)执行，因此需要验证。例如，买方可以下订单，供应商可以履行订单。
4.  所有的交易都需要计算，即它们必须由处理器来执行。在区块链网络的情况下，它是分布式计算网络或通用计算。
5.  由于这些交易是由网络验证和执行的，一旦确认，交易就不能恢复。

智能合约可以概括为

1.  以程序形式建立的商业合同
2.  驻留在区块链网络上，网络提供执行程序所需的计算。
3.  为了执行程序的功能，权限被提供给指定的参与者。

[本博客](https://www.edureka.co/blog/smart-contracts/) 在 Edureka 上，提供了关于智能合约的深入信息。

我想到的下一个大问题是如何开始，构建智能合同需要什么。那么让我们来看看如何开始。

## **如何开始设置智能合同开发环境？**

在上一节中，我们讨论了什么是智能合同，在这一节中，我们将探讨以下主题:

1.  建立智能合同需要什么？
2.  有哪些不同的语言可用于构建智能合同？

语言的选择，建立智能合约依赖于区块链平台。 对于这个博客系列，区块链选择的平台是以太坊。[以太坊](https://www.edureka.co/blog/what-is-ethereum/)是区块链平台，被戏称为“行星级计算机或世界计算机”——一个由许多私人计算机组成的巨大公共网络，促进互联网应用(DApp——分布式应用)的运行，无需任何第三方。

## **智能合同语言**

智能合同语言(SCL)是一种编程语言，可以用来直接编写智能合同，也可以编译成智能合同。以太坊的智能合约语言有:

1.  坚固度
2.  电子邮件
3.  关闭
4.  以太坊字节码

![Smart contract languages - What are smart contracts - edureka](img/4e5a72bc3846312ea64a3d02e1390275.png)

在这个博客系列中，我们将关注作为智能合同开发语言的可靠性。 Solidity 是以太坊最流行的智能合约语言。现在，我们已经选择了智能合约开发的语言，让我们看看需要什么来开始。

## 设置开发环境

在物理学中，我们经常听到静摩擦力大于动摩擦力。开始使用智能合约需要设置开发环境，这是先决条件。在这篇博客中，我们将看看设置开发环境所需的步骤，以及有哪些可用的选项。 同样，了解智能合约开发的开发环境是比实际开发更大的障碍。有太多的选择，这让任何一个刚接触智能合同的人不知所措。简化环境设置是深入区块链世界的第一步。为了建立开发智能合同的环境，有两种选择。

1.  [Remix Online IDE](#RemixOnlineIDE)
2.  [本地设置](#LocalSetUp)

## **混音 IDE**

首选是使用在线 remix IDE(集成开发环境)来构建和测试智能合约。这是一个快速，简单，推荐初学者使用的方法。

优点

*   无需安装，完全在线
*   毫无挑战地开始，快速原型化和验证智能合同
*   提供本地以太坊虚拟网络

缺点

*   随着从构建智能合约到在 DApp(分布式应用程序)中使用智能合约的进展，Remix IDE 具有严重的局限性。

## **本地设置**

使用 Remix IDE 的另一种方法是建立一台本地机器来开发智能合约。

![Local set up - What are smart contracts - edureka](img/17502c16357f6f15c8098bd2f47524ec.png)

智能合同开发所需的工具集如下:

### 节点

最新版本的节点可以在这里下载 [。](https://nodejs.org/en/download/)

#### *【使用 NVM(节点版本管理器)*

##### **Windows 安装**

*   下载并运行安装程序，这将安装 nvm
*   打开 windows 终端并运行“nvm 版本”

`nvm --version`

*   这将返回 nvm 上的当前版本。

##### **Mac 安装**

*   运行下面的脚本，这会自动在机器上安装 nvm。

`curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash`

*   为了验证安装，运行以下命令“`nvm --version`”

##### **安装后**

*   安装 nvm 后，运行以下命令。
*   运行以下命令“nvm 列表”。这将列出本地安装的节点版本

`nvm list`

*   要列出可供下载的节点版本，请运行以下命令

`nvm ls-remote`

*   为了安装特定版本的节点，运行以下命令“nvm install<【node-version】例如“nvm install 10.15.0”这将安装节点版本 10.15.0。

`nvm install 10.15.0`

*   通过以下命令检查正在使用的节点的当前版本

`node --version`

*   关于 nvm 或 node 的更多详情，请在这里 看详情 [。](https://nodesource.com/blog/installing-node-js-tutorial-using-nvm-on-mac-os-x-and-ubuntu/)

### **Visual Studio 代码**

Visual Studio Code 是微软为 solidity smart contract 开发提供的最佳 IDE 之一。Visual Studio 代码可以从 [这里下载。](https://code.visualstudio.com/)

### **松露组曲**

Truffle suite 为智能合约提供了一个出色的框架。 松露的安装是通过 npm(节点包管理器)完成的，它是和 node 一起安装的。 为了安装松露，打开终端窗口或命令提示符窗口。 在终端窗口运行以下命令，

`npm install -g truffle`

(命令中的 g 标志代表全局)

truffle 安装完成后，运行以下命令验证安装的版本

`truffle --version`

### **Ganache(单节点本地以太网)**

1.  【ganache 的设置文件可以在 [这里](https://github.com/trufflesuite/ganache/releases) 下载
2.  根据操作系统选择安装包。
3.  运行安装程序，一旦安装完成，应出现以下屏幕

![Ganache sreen - What are smart contracts - edureka](img/ec8fbc451327f0a38e9e697fc6964550.png)

为了自定义 ganache 测试以太坊节点的运行，请点击 ganache 工具右上角的齿轮图标，应会看到以下屏幕。

![ganache test Ethereum node running - What are smart contracts - edureka](img/1e28efec98094ad9b945e8ccd51f15a1.png)

端口和网络 id 可以自定义，自定义后，请点击左上角的重启按钮。

这将重新初始化节点，RPC 位置将为。如果设置如上图所示，RPC 端点将是[http://127 . 0 . 0 . 1:7000](http://127.0.0.1:7000)

Ganache 安装正在运行，可以使用上述 RPC 端点进行交互。

优点

*   构建企业级应用的灵活性。
*   构建分布式应用程序的工具选择简易性(DApp)

缺点

*   环境设置既繁琐又耗时。

任何旅程的第一步都是了解该走哪条路，有哪些工具集可用。现在，我们知道了什么是智能合约，以及构建智能合约需要什么。构建它们可用语言和工具集的选择。这是一系列博客中的第一篇，将关注可靠性和智能合同开发。在下一篇博客中，我们将建立我们的第一个智能合同，并开始研究可靠性的基础。

*有问题吗？请将它发布在 [Edureka 社区](https://edureka.co/community)上，我们将会回复您。*

如果您希望学习区块链并在区块链技术方面建立职业生涯，那么请查看我们的 *[**区块链** **认证培训**](https://www.edureka.co/blockchain-training)* ，它带有讲师指导的现场培训和真实项目经验。本培训将帮助您全面了解什么是区块链，并帮助您掌握该主题。