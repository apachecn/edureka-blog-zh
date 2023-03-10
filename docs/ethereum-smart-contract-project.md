# 以太坊智能合约——如何执行智能合约？

> 原文：<https://www.edureka.co/blog/ethereum-smart-contract-project>

区块链技术在顶级技术中获得一席之地的主要原因是因为它的去中心化特性。虽然区块链的主要目的是在没有中央机构的情况下维护交易记录，但为了实现自动化，引入了[智能合同](https://www.edureka.co/blog/smart-contracts/#NickSzabo)。但是在[写了一份智能合同](https://www.edureka.co/blog/solidity-tutorial/)之后呢？在本以太坊智能合约教程中，我们将看到如何使用[松露以太坊](https://www.edureka.co/blog/developing-ethereum-dapps-with-truffle)和[以太坊私有网络](https://www.edureka.co/blog/ethereum-private-network-tutorial/)来执行一份智能合约。

*对以太坊开发感兴趣？看看这个现场[以太坊开发者培训](https://www.edureka.co/ethereum-developer-course)。*

本期以太坊智能合约教程我们会看以下几个话题:

1.  [用例:保险流程中的智能合约](#SmartContractUseCase)
2.  [智能合约的好处](#BenefitsOfSmartContract)
3.  [安装先决条件](#InstallingPrerequisites)
4.  [配置创世纪块](#ConfiguringGenesisBlock)
5.  [运行以太坊专用网络](#RunningEthereumPrivateNetwork)
6.  [创建以太坊账号](#CreatingEthereumAccount)
7.  [创建以太坊智能合约](#CreatingEthereumSmartContract)
8.  [执行以太坊智能合约](#ExecutingEthereumSmartContract)

## **用例:保险流程中的智能合约**

区块链遵循的是“无中央权威”，这也是引入智能合约的原因。但是，您有没有想过如何使用智能合约？好了，在以太坊智能合约这一节，我来解释一下智能合约在保险流程中的一个用例。

让我们考虑一个航班延误保险的例子。假设你想乘坐从 A 地到 C 地的航班，但是你没有直达航班。所以，你决定乘联运航班(通过 B)。现在，你的路线是从 A 到 B，然后从 B 到 C，B 是你要转机的机场。不幸的是，从 A 到 B 的航班和从 B 到 c 的航班之间没有太多的时间差。因此，如果从 A 到 B 的航班延误，那么你将错过从 B 到 c 的航班。你意识到这一点，为了避免重大损失，你购买了航班延误保险。

![Flight Delay Insurance - Edureka](img/fa56214388d83d620347dbf481a1963a.png)

现在，如果你从 A 到 B 的航班延误(这会让你错过 B 到 C 的航班)，你会得到保险金额的赔付。正常的工作方式是，如果你的航班延误，你要求保险。然后，有人会核实和批准保险，最后，你会得到你的保险金额。但这是一个相当漫长的过程。

### **您如何使用智能合同来改善保险流程？【T2**

在金融交易中，尤其是当你得到钱的时候，“越快越好”，不是吗？因此，让我们看看智能合同如何加快保险流程。智能合同是在满足特定条件时自动执行的数字合同。如果航班延误，可以写一份智能合同，向选择了航班延误保险的人支付保险金额。因此，当航班延误并且系统记录了这一延误，保险会立即赔付。

![](img/7615a1c0e259a69f8f50af12ff4dd17f.png)

你好！几秒钟内支付的保险金额。这就是简单快速的智能合同如何使流程发生的。

## **智能合约的好处**

在上面的例子中，您已经看到了智能合同如何加快财务流程。除了快速交易，智能合约还有更多好处。在这里，我列出了使用智能合同的其他一些好处:

*   **自动:**智能合约中的所有步骤都会自动发生
*   **没有中介:**当你使用智能合约时，你不需要一个中介来完成工作，因为所有事情都将由智能合约来处理
*   **成本效益:**使用智能合约将为您节省银行收取的交易费和中介服务费(如果有)

现在，我们知道了如何使用智能合约让世界变得更快，让我们开始这个以太坊智能合约教程的实践部分。

## **安装先决条件**

对于本以太坊智能合约教程，我们将需要 5 个重要应用:

*   节点 j
*   NPM
*   以太坊
*   松露
*   可靠性编译器

### **安装节点**

NodeJS 是一个 JavaScript 框架，用于构建服务器应用程序。由于我们使用的是私有网络，NodeJS 将使构建网络应用程序变得容易。

要安装 Nodejs，在您的终端中运行以下命令:

```
$ sudo apt-get install nodejs
```

### **安装 NPM**

NPM 代表节点包管理器，用于运行 Nodejs 应用程序。

要安装 NPM，在您的终端中运行以下命令:

```
$ sudo apt-get install npm
```

### **安装以太坊**

以太坊是一个基于开源&公共区块链的分布式计算平台，用于构建分散的应用程序。

要安装以太坊，在您的终端上运行以下命令:

```
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository -y ppa:ethereum/ethereum
$ sudo apt-get update
$ sudo apt-get install ethereum
```

### **安装松露**

Truffle 是以太坊区块链的开发环境、测试框架和资产管道。

要安装 Truffle，在您的终端中运行以下命令:

```
$ npm install -g truffle
```

### **安装 Solidity 编译器**

Solidity 是一种用于编写智能合同的编程语言。要在我们的系统上运行智能合同，我们必须安装 Solidity 编译器。

要安装 Solidity 编译器，在您的终端中运行以下命令:

```
$ sudo npm install -g solc 
```

## **配置创世纪块**

Genesis 区块是区块链的起点，我们需要一个 Genesis 文件来启动区块链。在以太坊智能合约的这一部分，我们将编写一个 Genesis 文件，并对其进行配置以允许我们运行智能合约。

让我们首先创建一个新目录，然后在这个目录中我们将创建**创世纪文件**

```
$ mkdir ethereum-network
$ cd ethereum-network
$ nano genesis.json
```

现在，在 **genesis.json** 文件中输入以下几行:

```
{
"config": {
"chainId": 2019,
"homesteadBlock": 0,
"eip155Block": 0,
"eip158Block": 0
},
"alloc": {},
"difficulty" : "200"
"gasLimit" : "99999999999999"
}
```

保存并退出。

## **运行以太坊专用网络**

在本以太坊智能合约教程中，我们将在私有网络上部署一个以太坊智能合约。因此，要启动这个网络，我们将使用以下命令:

```
$ geth --datadir ./dataDir init ./genesis.json
```

![Genesis block initialization - Ethereum Smart Contract - Edureka](img/8fc26a6813e6d28400630d29c025ef1d.png)

```
$ geth --port 4321 --networkid 1234 --datadir=./dataDir  --rpc --rpcport 8543 --rpcaddr 127.0.0.1  --rpcapi "eth,net,web3,personal,miner"
```

![Running Ethereum Private Blockchain - Ethereum Smart Contract - Edureka](img/657e124f34d97385704c395bd1cfcb3e.png)

在继续之前，让我解释一下上面命令中使用的一些重要标志:

**datadir:** 存储区块链相关数据的目录。

**rpc:** 启用 HTTP-RPC 服务器。

**rpcport** 和 **rpcaddr** 分别用于设置网络的端口和地址。

**rpcapi:** 允许我们使用不同的 api 与以太坊网络进行交互。

### **连接 Geth 到以太坊私有区块链**

Geth 控制台是我们可以与以太坊私有区块链进行交互的控制台。要连接 Geth 到以太坊私有区块链，打开一个新的终端，运行下面的命令:

```
$ geth attach http://127.0.0.1:8543
```

![Geth attach - Ethereum Smart Contract - Edureka](img/a271fc02c668cdaeb44039566ba342b3.png)

现在，我们在 Geth 控制台中，可以运行命令与区块链进行交互。

## **创建以太坊账号**

为了进行任何交易，我们需要一个账户。在以太坊智能合约教程的这一节，我们将看到如何从 Geth 控制台创建新的以太坊账户。

按照到目前为止的步骤，我们已经在 Geth 控制台中。要创建新帐户，请在 Geth 控制台中运行以下命令:

```
> personal.newAccount('seedphrase')
```

用您想要为此帐户设置的密码替换“种子短语”。

我们已经创建了一个新账户，但是这个账户没有乙醚 。我们需要 乙醚来进行任何交易，为了让乙醚 进入我们的账户，我们将开始开采乙醚。要开始挖掘，我们需要首先解锁帐户。让我们解锁帐户并开始挖掘。

```
> personal.unlockAccount(web3.eth.coinbase, "seedphrase")
> miner.start()
```

![Create geth account - Ethereum Smart Contract - Edureka](img/c6d4383a521e17b8c3ca3742771fb1d3.png)

随着采矿的继续进行，一些醚类会被存入这个账户。

**注**:这些醚是**虚醚**，没有现实价值。

为了检查账户中的余额醚类，我们将运行以下命令:

```
> web3.fromWei(eth.getBalance(eth.coinbase), "ether")
```

当你定期运行这个命令时，你会看到醚由于采矿而增加。

![Account balance - Ethereum Smart Contract - Edureka](img/c1e73ffc3f2451b004b8e725cbf7edf9.png)

要停止挖掘，运行以下命令:

```
> miner.stop()
```

## **创建以太坊智能合约**

### **创造松露项目**

现在我们已经准备好了我们的私有区块链，我们将看看如何使用 Truffle 创建一个以太坊智能合约。对于本教程，我们将创建一个简单的“Hello World”以太坊智能合约。

从这里开始，让我们首先创建一个新目录来存储 Truffle 项目。然后在这个目录中，我们将创建一个新的 Truffle 项目。打开一个新的终端，运行下面的命令:

```
$ mkdir truffle
$ cd truffle
$ truffle init
```

![Truffle init - Ethereum Smart Contract - Edureka](img/d5e6169d75f72f673d7c064a73826913.png)

块菌初始化命令将创建一个块菌项目所需的所有必要文件。

既然我们已经为部署以太坊智能合约做好了一切准备，让我们开始编写一个“Hello World”智能合约。

### **编写一份《Hello World》智能合约**

所有的合同都应写在“合同”目录中。我们将切换到这个目录，创建一个名为“HelloWorld.sol”的契约，并在这个文件中添加以下行:

```
pragma solidity ^0.4.15;
contract HelloWorld {
    string public message;
    function Hello() public{
    message = "Hello World!";
    }
}
```

就是它了！但是这个智能合同不能自己执行。我们将不得不对它进行一些配置。

### **配置松露迁移**

要迁移我们的智能合同，我们必须在**“迁移”**目录的**“松露”**目录中添加一个文件。在这个目录中，我们将添加一个名为 **"2_deploy_contracts.js"** 的文件，其中包含以下内容:

```
var HelloWorld = artifacts.require("./HelloWorld.sol");
module.exports = function(deployer) {
   deployer.deploy(HelloWorld);
};
```

保存并退出。

要在我们的网络上运行 truffle，我们需要编辑**“truffle”**目录**中的“ **truffle.js** ”文件。**打开该文件，输入以下内容:

```
module.exports = {
rpc: {
host:"localhost",
port:8543
},
networks: {
development: {
host: "localhost", 
port: 8543,
network_id: "*",
from: "0xfa2361236b5ac8079cb6cf250e5284922ed9ba9a",
gas: 20000000
}
}
};
```

**注:**用您在上一步中创建的帐户地址替换**【发件人】**地址。

## **执行以太坊智能合约**

在以太坊智能合约教程的最后一部分，我们将了解如何在以太坊专用网络上部署我们的“Hello World”智能合约。

### **编译部署智能合约**

在执行我们的智能合约之前，我们必须首先编译它并将其部署到我们的以太坊专用网络中。我们将使用以下命令来完成这个任务:

```
$ truffle compile
```

![Truffle Compile - Ethereum Smart Contract - Edureka](img/607f85cbe478c0c0ffe23b6e0ce13f38.png)

现在，我们必须解锁我们的帐户并开始采矿。使用 Geth 控制台返回终端并运行以下命令:

```
> personal.unlockAccount(web3.eth.coinbase)
> miner.start()
```

然后，回到当前工作目录为**【松露】**的终端，运行以下命令:

```
$ truffle migrate
```

等待部署完成。

![](img/58be45e25fc0aa2167738015111130a6.png)![Truffle Migrate 2 - Ethereum Smart Contract - Edureka](img/27bc94be54d1005ed2e4c399c9aca333.png)

### **在私有以太坊区块链上执行智能合约**

为了执行“Hello World”智能合约，我们必须进入松露控制台。为此，运行以下命令:

```
$ truffle console
```

你现在将进入松露控制台。要执行智能合约，请运行以下命令:

```
> var first_contract
> HelloWorld.deployed().then(function(instance) { first_contract = instance; })
> dApp.message.call()
```

![Smart Contract Output - Ethereum Smart Contract - Edureka](img/0371ae67d5c345401f3c951039d4c91a.png)

*恭喜恭喜！你已经创建了你的第一个以太坊智能合约并执行了它。我希望这篇以太坊智能合约教程能够提供信息，帮助你理解如何执行以太坊智能合约。现在，继续尝试编写其他智能合约并执行它。*

*有问题吗？请将它发布在 [Edureka 社区](https://edureka.co/community)上，我们将会回复您。*

如果你希望学习区块链，并在区块链技术方面建立职业生涯，那么请查看我们的 *[**区块链** **认证**](https://www.edureka.co/blockchain-training)* ，它带有讲师指导的现场培训和真实项目经验。该培训将帮助您全面了解什么是区块链，并帮助您掌握该主题。