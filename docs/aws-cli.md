# 什么是 AWS CLI？了解它的应用和好处

> 原文：<https://www.edureka.co/blog/aws-cli/>

亚马逊网络服务(AWS)是云计算领域的市场领导者和顶级创新者。它帮助公司处理各种各样的工作负载，如游戏开发、数据处理、仓储、存档、开发等等。但是，AWS 不仅仅是引人注目的浏览器控制台。是时候看看亚马逊的命令行界面了——AWS CLI。你可以通过 [AWS 认证培训](https://www.edureka.co/aws-certification-training)了解更多关于亚马逊网络服务的信息。

在深入研究之前，让我们先来看看本文涉及的主题。

*   [什么是 AWS CLI？](#AWSCLI)
*   [AWS CLI 的用途](#BenifitsOfAWSCLI)
*   [安装 AWS CLI](#InsatllAWSCLI)
*   [如何使用 AWS CLI？](#AWSCLIUses)

你可以浏览 AWS CLI 视频讲座，我们的培训专家正在讨论每一个&技术的细节。

## **AWS 命令行界面介绍| AWS 培训| Edureka**



[//www.youtube.com/embed/sLtf7Sx8lsQ?rel=0&showinfo=0](//www.youtube.com/embed/sLtf7Sx8lsQ?rel=0&showinfo=0)

Edureka 制作的这段“AWS 命令行界面”视频将帮助您了解如何使用 AWS CLI 访问和管理 AWS 服务。

**什么是 AWS CLI？**

*AWS 命令行界面(AWS CLI)是一个统一的工具，使用它，您可以从客户端 上的终端会话管理和监控您的所有 AWS 服务。*

虽然大多数 AWS 服务都可以通过 AWS 管理控制台或 API 来管理，但还有第三种方式非常有用:命令行界面(AWS CLI)。AWS 使得 Linux、MacOS 和 Windows 用户可以从本地终端会话的命令行管理主要的 [AWS 服务](https://www.edureka.co/blog/amazon-aws-tutorial/) 。因此，只需一步安装和最少的配置，您就可以使用终端程序开始使用 [AWS 管理控制台](https://www.edureka.co/blog/aws-console/) 提供的所有功能。那就是:

*   **Linux shell:**可以使用 bash、tsch 和 zsh 等命令 shell 程序在 Linux、macOS 或 Unix 等操作系统中运行命令
*   **Windows 命令行:** 在 Windows 上，可以在 PowerShell 中运行命令，也可以在 Windows 命令提示符下运行
*   **远程:**您可以通过 PuTTY 或 SSH 之类的远程终端在 Amazon EC2 实例上运行命令。您甚至可以使用 AWS Systems Manager 在您的 AWS 资源中自动执行操作任务

除此之外，它还提供对 [AWS](https://www.edureka.co/blog/amazon-aws-tutorial/) 服务公共 API 的直接访问。除了低级 API 等效命令之外，AWS CLI 还提供了对多种服务的定制。

本文将告诉您开始使用 AWS 命令行界面以及在日常操作中熟练使用它所需要知道的一切。

## **AWS CLI 的用途**

下面列出了一些足以让您开始使用 AWS 命令行界面的理由。

**安装方便**

![Easy Install - AWS CLI - Edureka](img/d32d28a6ec2b28c49e285b88c42c8454.png)在 AWS CLI 推出之前，像老 AWS API 这样的工具包的安装涉及太多复杂的步骤。用户必须设置多个环境变量。但是 AWS 命令行界面的安装是快速、简单和标准化的。

**节省时间**

尽管 AWS 管理控制台用户界面友好，但有时也很麻烦。假设你试图找到一个大的![saves time - AWS CLI - Edureka](img/bae79a8727471a945d4428d7e52c8aac.png) [亚马逊 S3](https://www.edureka.co/blog/s3-aws-amazon-simple-storage-service/) 文件夹。你必须登录你的帐户，搜索正确的 S3 桶，找到正确的文件夹，寻找正确的文件。但是使用 AWS CLI，如果您知道正确的命令，整个任务只需几秒钟。

**自动化流程**

![automate process - AWS CLI - Edureka](img/e0ef175c9fe535880c0c098ad4040b4d.png) AWS CLI 使您能够通过脚本自动化控制和管理 AWS 服务的整个过程。这些脚本使用户可以轻松地完全自动化云基础架构。

**支持所有亚马逊网络服务**

![support - AWS CLI - Edureka](img/3f956ab85941250568c20871d1554fb9.png)在 AWS CLI 出现之前，用户需要一个专用于 EC2 服务的 CLI 工具。它工作正常，但它不允许用户控制其他亚马逊网络服务，例如 [AWS RDS](https://www.edureka.co/blog/rds-aws-tutorial/) (关系数据库服务)。但是，AWS CLI 让您可以从一个简单的工具控制 *所有*  服务。

现在我们已经了解了什么是 AWS CLI，让我们开始安装过程。

## **安装 AWS CLI**

AWS 命令行界面有三种安装方式:

*   使用画中画
*   使用虚拟环境
*   使用捆绑的安装程序

在本文中，我们将了解如何使用 pip 安装 AWS CLI。

**先决条件**

1.  Python 2 版本 2.6.5 以上或 [Python 3](https://www.youtube.com/watch?v=mOtBZidwre0&feature=youtu.be) 版本 3.3 以上
2.  Windows、Linux、macOS 或 Unix 操作系统

### **使用 pip 安装 AWS CLI**

安装 AWS CLI 的常用方法是使用 pip。 pip 是一个软件包管理系统，用于安装和管理用 [Python](https://www.edureka.co/blog/videos/python-tutorial/) 编写的软件包。

**第一步:**安装 pip(在 Ubuntu OS 上)

```
$ sudo apt install python3-pip
```

第二步:安装 CLI

```
$ pip install awscli --upgrade --user
```

**步骤 3:** 检查安装

```
$ aws --version 
```

一旦确定 AWS CLI 安装成功，您需要对其进行配置，以开始通过 AWS CLI 访问您的 AWS 服务。

### **配置 AWS CLI**

步骤 4:使用以下命令配置 AWS CLI

```
$ aws configure
AWS Access Key ID [None]: ***AKI***************
AWS Secret Access Key [None]: ***wJalr***********
Default region name [None]: ***us-west-2***
Default output format [None]: ***json***
```

作为上述命令*、*的结果，AWS CLI 将提示您输入四条信息。前两项是必需的。这些是您的 AWS 访问密钥 ID 和 AWS 秘密访问密钥，它们充当您的帐户凭证。您需要的其他信息是区域和输出 格式，您可以暂时保留为默认格式。

**注意:**如果您还没有新的凭证，您可以在 AWS 身份和访问管理(IAM)中生成它们。

一切就绪！您现在可以开始使用 AWS CLI 了。让我们借助几个基本示例来看看 AWS CLI 有多强大。

**查看我们在顶级城市的 AWS 认证培训**

| 印度 | 美国 | 其他国家 |
| [在海德拉巴的 AWS 培训](https://www.edureka.co/aws-certification-training-hyderabad) | [亚特兰大 AWS 培训](https://www.edureka.co/aws-certification-training-atlanta) | [AWS 伦敦培训](https://www.edureka.co/aws-certification-training-london) |
| [班加罗尔的 AWS 培训](https://www.edureka.co/aws-certification-training-bangalore) | [波士顿 AWS 培训](https://www.edureka.co/aws-certification-training-boston) | [阿德莱德的 AWS 培训](https://www.edureka.co/aws-certification-training-adelaide) |
| [钦奈的 AWS 培训](https://www.edureka.co/aws-certification-training-chennai) | [纽约市的 AWS 培训](https://www.edureka.co/aws-certification-training-new-york-city) | [新加坡 AWS 培训](https://www.edureka.co/aws-certification-training-singapore) |

## **如何使用 AWS** **CLI？**

假设您已经在 AWS 上运行了一些服务，并使用 AWS 管理控制台实现了这些服务。完全相同的工作可以完成，但是使用 Amazon 命令行界面要简单得多。

这是一个演示，

假设您想从 [EC2](https://www.edureka.co/blog/ec2-aws-tutorial-elastic-compute-cloud/) 启动一个 Amazon Linux 实例。

如果您希望使用 AWS 管理控制台来启动实例，您需要:

*   加载 EC2 仪表板
*   点击*启动实例*
*   选择 AMI 和实例类型
*   在“配置实例详细信息”页面上设置网络、生命周期行为、 [IAM](https://youtu.be/UqKWHZ36yEM) 和用户数据设置
*   在“添加存储”页面上选择存储卷
*   在“添加标签”页面上添加标签
*   在“配置安全组”页面上配置安全组
*   最后，检查并启动实例

另外，不要忘记弹出的，在这里您将确认您的密钥对，然后返回到 EC2 实例仪表板以获取您的实例数据。这听起来没那么糟糕，但是想象一下，当使用慢速互联网连接工作时，或者如果您必须多次启动不同变体的多个实例时，都要这样做。这要花很多时间和精力，不是吗？

详细的，你甚至可以通过 [AWS 云迁移培训](https://www.edureka.co/migrating-to-aws)了解迁移到 AWS 的细节。

现在，让我们看看如何使用 AWS CLI 完成相同的任务。

***步骤 1:使用 AWS CLI 创建新的 IAM 用户***

***让我们看看如何创建一个新的 IAM 组和一个新的 IAM 用户&然后使用 AWS 命令行界面*** 将用户添加到组中

*   首先，使用 *create-group* 创建一个新的 IAM 组

```
$ aws iam create-group --group-name *mygroup*
```

*   使用*创建用户*创建一个新用户

```
$ aws iam create-user --user-name *myuser*
```

*   然后使用*添加用户到组*命令将用户添加到组

```
$ aws iam add-user-to-group --user-name *myuser* --group-name *myiamgroup*
```

*   最后，使用命令*put-user-policy*将策略(保存在文件中)分配给用户

```
$ aws iam put-user-policy --user-name *myuser* --policy-name *mypoweruserole* --policy-document file://MyPolicyFile.jso
```

*   如果您想为 IAM 用户创建一组访问密钥，使用命令 *create-access-key*

```
$ aws iam create-access-key --user-name *myuser* 
```

*****步骤 2:使用 AWS CLI***** 启动 Amazon Linux 实例

***就像当您使用 AWS 管理控制台启动 EC2 实例时，您需要在启动实例之前创建一个密钥对和安全组***

*   使用 create-key-pair 命令创建一个密钥对&使用–query 选项将您的密钥直接传输到一个文件中

```
$ aws ec2 create-key-pair --key-name *mykeypair* --query 'KeyMaterial' --output text > mykeypair.pem
```

*   然后创建一个安全组，并向该安全组添加规则

```
$ aws ec2 create-security-group --group-name *mysecurityg* --description "My security group" 
```

```
$ aws ec2 authorize-security-group-ingress --group-id *sg-903004f8* --protocol tcp --port 3389 --cidr 203.0.113.0/24
```

*   最后，使用 run-instance 命令启动您选择的 EC2 实例

```
$ aws ec2 run-instances --image-id ami-09ae83da98a52eedf --count 1 --instance-type t2.micro --key-name *MyKeyPair* --security-group-ids sg-903004f8
```

看起来有很多命令，但是你可以通过将所有这些命令合并成一个，然后保存为一个脚本来达到相同的效果。这样您可以在任何需要的时候修改和运行代码，而不是像使用 AWS 管理控制台那样从第一步开始。这可以将五分钟的过程缩短到几秒钟。

***现在，您知道了如何使用 AWS CLI 创建 IAM 用户并启动您选择的 EC2 实例。但是 AWS CLI 可以做得更多。***

*如果这激发了您的兴趣，并且您想了解更多关于应用安全的信息，那么请参加我们在达拉斯举办的 [AWS 培训，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解网络安全，并帮助您掌握该主题。](https://www.edureka.co/aws-certification-training-dallas)*

有问题要问我们吗？请在“AWS CLI”的评论部分提到它，我们将回复您。