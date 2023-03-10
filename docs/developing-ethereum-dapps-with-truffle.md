# 块菌以太坊教程-用块菌开发以太坊 DApps

> 原文：<https://www.edureka.co/blog/developing-ethereum-dapps-with-truffle>

从之前的[以太坊博客](https://www.edureka.co/blog/what-is-ethereum/)中，我们了解到 [**智能合约**](https://www.edureka.co/blog/smart-contracts/) 包含了一套管理**区块链**的规则。为了简化以太坊智能合约的工作，构建了一个名为 **Truffle Suite** 的开发环境。 在这个松露以太坊教程中，我们会看以下几个话题:

1.  [什么是松露套件？](#WhatIsTruffleSuite)
2.  [松露以太坊的特点](#TruffleFeatures)
3.  [什么是元掩码？](#WhatIsMetamask)
4.  [在 Ubuntu](#InstallingTruffle) 上安装松露并创建松露项目
5.  [在谷歌 Chrome 上安装元蒙版](#InstallingMetamask)
6.  [在 Ubuntu 上安装 test RPC](#InstallingTestrpc)
7.  [演示:用松露和 MetaMask 开发一个简单的 DApp 并进行交易](#DemoEthereumDappTruffleMetamask)

*如果你有兴趣成为一名以太坊开发者，你可能想看看这个[区块链课程](https://www.edureka.co/blockchain-training)。*

**了解我们在顶级城市/国家的区块链培训**

| **印度** | **其他城市/国家** |
| [班加罗尔](https://www.edureka.co/blockchain-training-bangalore) | [纽约](https://www.edureka.co/blockchain-training-new-york-city) |
| [海德拉巴](https://www.edureka.co/blockchain-training-hyderabad) | [英国](https://www.edureka.co/blockchain-training-uk) |
| 喀拉拉邦 | [美国](https://www.edureka.co/blockchain-training-usa) |
| [钦奈](https://www.edureka.co/blockchain-training-chennai) | [加拿大](https://www.edureka.co/blockchain-training-canada) |
| [孟买](https://www.edureka.co/blockchain-training-mumbai) | [澳大利亚](https://www.edureka.co/blockchain-training-australia) |
| [浦那](https://www.edureka.co/blockchain-training-pune) | [新加坡](https://www.edureka.co/blockchain-training-singapore) |

## **什么是松露套件？**

Truffle Suite 是一个基于以太坊区块链的开发环境，用于开发 DApps(分布式应用)。Truffle 是构建 dapp 的一站式解决方案:编译合同、部署合同、将其注入 web 应用程序、为 dapp 创建前端和测试。

![Truffle Suite - Truffle Ethereum tutorial - Edureka](img/877e86999fb7bd75bf24defb5fdca86b.png)

松露套装–松露以太坊教程

松露套件有三个组件:

1.  ***松露***:是以太坊区块链的开发环境、测试框架和资产管道
2.  ***Ganache***:Ganache 是一个个人以太坊区块链，用于测试智能合约，您可以在其中部署合约、开发应用程序、运行测试和执行其他任务，而无需任何成本
3.  ***毛毛雨***:毛毛雨是一个库的集合，用于为以太坊 DApps 创建更容易和更好的前端

## **松露** **以太坊**

这里列出了一些特性，这些特性使得 Truffle 成为一个强大的工具来构建基于[以太坊](https://www.edureka.co/blog/what-is-ethereum/)的 DApps:

*   内置支持编译、部署和链接智能合同
*   自动化合同测试
*   支持控制台应用和网络应用
*   网络管理和包管理
*   Truffle 控制台直接与智能合约通信
*   支持紧密集成

## **什么是元掩码？**

MetaMask 是一个易于使用的浏览器插件(适用于 Google-Chrome、Firefox 和 Brave 浏览器)，它提供了一个图形用户界面来进行以太坊交易。它允许您在浏览器上运行以太坊 DApps，而无需在系统上运行完整的以太坊节点。基本上，MetaMask 是以太坊区块链和浏览器之间的桥梁。MetaMask 是开源的，提供了以下令人兴奋的特性:

*   您可以更改元掩码的代码，使其成为您想要的样子
*   提供内置硬币购买
*   本地密钥存储

![MetaMask - Truffle Ethereum tutorial - Edureka](img/901d5a50256ebfb2b8290aa760912109.png)

松露元面具–松露以太坊教程

现在，我们已经知道了松露和 MetaMask，让我们开始实际操作部分，看看如何将它们用于 DApps。

## **在 Ubuntu** 上安装松露并创建松露项目

在这一节松露以太坊教程中，我们将看到如何安装松露以及如何创建松露项目。

要安装 Truffle，您必须运行如下简单命令:

```
$ npm install -g truffle
```

现在，让我们开始在 Truffle 中创建一个项目。首先，让我们创建一个新目录，并使用下面的命令进入该目录:

```
$ mkdir truffle-pro
$ cd truffle-pro
```

要创建一个项目，执行以下命令:

```
$ truffle unbox metacoin
```

成功执行该命令后，您将看到该目录中的项目结构，其中包含项目所需的最少文件。

![Create truffle project - Truffle Ethereum tutorial - Edureka](img/74f2ae2fdc46d44ed6ee0fdce4217f57.png)

就是这样！您已经创建了一个简单的松露以太坊项目。

## **在谷歌 Chrome 上安装元蒙版**

在这一节松露以太坊教程中，我们将看看如何为 Google-Chrome 浏览器安装 MetaMask 插件。

下面是安装元蒙版浏览器插件的步骤:

1.  先去以下链接:[https://metamask.io/](https://metamask.io/)
2.  点击**获取 CHROME 扩展**按钮。这将打开一个新的标签![MetaMask Installation - Truffle Ethereum tutorial - Edureka](img/82ad90309d6ae9b51dcf2f85fc0479f6.png)
3.  点击“**添加到 Chrome** ”按钮，然后“**添加扩展**”。
4.  现在，在浏览器的右上角，你可以看到元蒙版图标。![MetaMask Plugin - Truffle Ethereum tutorial - Edureka](img/c11278a0afb6a0c3d09375c176411f98.png)
5.  接受条款和条件。

然后嘭！元掩码已安装。

现在我们已经在系统中安装了 Truffle Ethereum 和 MetaMask，让我们看看如何使用 Truffle Ethereum 开发一个 DApp，并使用 MetaMask 进行交易。

## **在 Ubuntu 上安装 TestRPC**

对于这个松露以太坊教程，我们将使用“TestRPC”，这是一个区块链仿真器，来开发我们的 DApp。TestRPC 允许您运行网络进行测试。它允许您在不运行实际以太坊节点的情况下调用区块链。

要安装 TestRPC，运行以下命令:

```
$ npm install -g ethereumjs-testrpc
```

## **演示:用松露和 MetaMask 开发一个简单的 DApp 并进行交易**

打开一个新的终端，用下面的命令运行 TestRPC。这将在您的系统上启动一个测试网络。

```
$ testrpc
```

您将看到一个可用帐户列表、这些帐户的私钥、助记短语以及 TestRPC 正在监听的端口。

![TestRPC - Truffle Ethereum tutorial - Edureka](img/8c3aa7863397be97e1f1112f8a81f342.png)

**注意:**不要在主以太网上使用助记短语。仅在专用网络上使用它。

现在，让我们设置松露。

打开一个新的终端，进入创建项目的目录。

为了在我们的网络上运行 truffle，我们需要编辑“ **truffle.js** ”文件。打开该文件并输入以下内容:

```
module.exports = {
      networks: {
            development: {
                  host: 'localhost',
                  port: 8545,
                  network_id: '*' //* will match to any network id
                  }
         }
};
```

![truffle.js - Truffle Ethereum tutorial - Edureka](img/02a9f22d210a2b3376d08a136f1f74fa.png)

保存文件并退出。

现在，我们必须编译合同并将其迁移到网络上。执行此操作的命令如下:

```
$ truffle compile
$ truffle migrate 
```

您可以看到代码已经成功迁移并部署到网络上。

![truffle compile - Truffle Ethereum tutorial - Edureka](img/6065cf89f5cac1ca0657dd2fdc837257.png)

![truffle migrate - Truffle Ethereum tutorial - Edureka](img/2bc5b6b23f0a4b9e324bc565be86e4f4.png)

现在，打开 Chrome 浏览器，点击 MetaMask 图标。点击**导入已有的窝点**。输入执行“ **testrpc** 命令时显示的助记短语，输入密码，点击“ **Ok** ”。

![MetaMask import - Truffle Ethereum tutorial - Edureka](img/4533a21634859df2633528efad91f9f2.png)

![MetaMask login - Truffle Ethereum tutorial - Edureka](img/f3927f667b18f6f3bc989b24de680c42.png)

默认情况下，MetaMask 运行在主网络上。我们不想仅仅为了一个演示而花钱，对吗？因此，我们必须将网络改为私有网络。在我们的例子中，这个网络是**本地主机 8545** 。

![MetaMask network - Truffle Ethereum tutorial - Edureka](img/3bb13ba77fba1f39ce5bc28911a8ddf2.png)

![MetaMask account1 - Truffle Ethereum tutorial - Edureka](img/97f2eb10d6977c791c7a6989dc9fe1c6.png)

我们现在可以看到一个包含 99+个醚的帐户。“哇！自由醚！”让你失望的是，这些不是真正的醚。这些是测试醚，仅用于测试目的，没有实际价值。

我们需要两个账户来进行交易:发送者和接收者。那么，让我们创建一个新帐户。为此，在 MetaMask 插件中，点击“**切换账户**，然后点击“**创建账户**”。您的新帐户已创建。

![MetaMask account2 - Truffle Ethereum tutorial - Edureka](img/14f5cb414cc2aeb1ce76b8acef0a6c6c.png)

![MetaMask create account - Truffle Ethereum tutorial - Edureka](img/06c55adacb5ad602d5a88b41f2b78806.png)

现在，要向这个帐户发送乙醚，我们需要复制这个帐户的地址。

![MetaMask copy - Truffle Ethereum tutorial - Edureka](img/82176161dfeac6f7f243c2b2bdb5d6ce.png)

在这个松露以太坊教程中，我们将从账户 1 向账户 2 发送以太。因此，让我们将帐户切换回帐户 1。在这里，点击**发送**，输入你要发送账户的地址(我复制的账户 2 的地址)和要发送的醚数，点击**下一步**。

![MetaMask send - Truffle Ethereum tutorial - Edureka](img/5cf2a1d27ab9f53808d75e75afc956be.png)

它将向您显示交易摘要并要求确认。点击**提交**，交易完成。

![MetaMask transaction - Truffle Ethereum tutorial - Edureka](img/cb4cd67047fd76ad79bf13975b38408b.png)

我们现在可以看到，帐户 1 中少了 50 个醚。

![MetaMask account1 balance - Truffle Ethereum tutorial - Edureka](img/f620910e093b564a8dbe32d20ac92598.png)

要验证交易，请切换到账户 2。这里，还有 50 多个醚。这表明 50 个醚从账户 1 转移到账户 2。

![MetaMask account2 balance - Truffle Ethereum tutorial - Edureka](img/9609ea35132ec9da0cde9e020fa7c8b3.png)

*恭喜恭喜！您已经创建了您的第一个松露以太坊 DApp，并完成了一笔交易。我希望这个块菌以太坊教程博客能提供信息，帮助你了解块菌。现在，继续尝试构建新的 DApps。*

*有问题吗？请将它发布在 [Edureka 社区](https://edureka.co/community)上，我们将会回复您。*

如果您希望学习区块链并在区块链技术方面建立职业生涯，那么请查看我们在班加罗尔的[***区块链培训***](http://www.edureka.co/blockchain-training-bangalore) ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您全面了解什么是区块链，并帮助您掌握该主题。