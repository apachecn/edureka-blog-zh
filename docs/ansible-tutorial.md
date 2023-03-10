# Ansible 教程-学习编写 Ansible 剧本

> 原文：<https://www.edureka.co/blog/ansible-tutorial/>

## **Ansible 教程**

我希望你浏览了我之前的博客，了解了 ***[什么是 Ansible](https://www.edureka.co/blog/what-is-ansible/)*** 以及 Ansible 最常用的术语。如果你还没有，请检查一下，这样你就可以更好地理解这个可翻译的教程。你也应该知道 Ansible 作为配置管理、部署和编排的工具，构成了 ***[DevOps 认证](https://www.edureka.co/devops)*** 的关键部分。

让我给你一个这个“可回答的教程”的概述:

*   你将学会[写剧本](#ansible_playbook)
*   你将在 Ansible 中了解不同的[模块](#ansible_modules)
*   你将学习编写[临时命令](#adhoc_commands)
*   [用手握住](#hands_on)

## **Ansible Playbook 教程| DevOps 培训| edu reka**

[//www.youtube.com/embed/dCQpaTTTv98?rel=0&showinfo=0](//www.youtube.com/embed/dCQpaTTTv98?rel=0&showinfo=0)

## **Ansible 教程——编写 Ansible 剧本**

Ansible 中的剧本是以 YAML 格式编写的。它是一种人类可读的数据序列化语言。它通常用于配置文件。它还可以用于存储数据的许多应用中。

对于 Ansible 来说，几乎每个 YAML 文件都是以列表开始的。列表中的每一项都是一个键/值对列表，通常称为“哈希”或“字典”。所以，我们需要知道如何在 YAML 写列表和字典。

列表的所有成员都是以“-”(破折号和空格)开始的相同缩进级别的行。更复杂的数据结构是可能的，例如字典列表或混合字典，其值是列表或两者的混合。

例如，edureka 的部门列表:

```
departments:
- marketing
- sales
- solutions
- content writing
- support
- product
```

现在让我给你举一个字典的例子:

```
-USA
-continent: North America
-capital: Washington DC
-population: 319 million
```

## **主机和用户:**

对于行动手册中的每个行动，您可以选择将基础架构中的哪些机器作为目标，以及由哪个远程用户来完成任务。为了将主机包括在可分析的清单中，我们将使用主机的 IP 地址。

一般来说，主机是由冒号分隔的一个或多个组或主机模式的列表。远程用户只是用户帐户的名称。

## **变量:**

Ansible 使用之前定义的变量，以便在剧本和角色中实现更大的灵活性。它们可用于遍历一组给定值，访问各种信息，如系统的主机名，以及用特定值替换模板中的某些字符串。

Ansible 已经为每个系统定义了丰富的变量。每当 Ansible 在一个系统上运行时，所有关于该系统的事实和信息都会被收集起来并设置为变量。

但是命名变量有一个*规则*。变量名应该是字母、数字和下划线。变量应该总是以字母开头。例如 wamp_21，port5 是有效的变量名，而 01_port，_server 是无效的。

## **任务:**

任务允许您将配置策略分解成更小的文件。任务包括从其他文件中提取。Ansible 中的任务和它的英文意思差不多。

例如:安装<包名>，更新<软件名>等。

## **经手人:**

处理程序就像一个可翻译剧本中的常规任务，但是只有当任务包含一个通知指令并表明它改变了某些东西时才运行。例如，如果配置文件被改变，那么引用该配置文件的任务可以通知服务重启处理程序。

让我给你一个剧本的例子，它将启动 Apache httpd 服务器程序:

```
--- - hosts: webservers
  vars:
    http_port: 80
    max_clients: 200
  remote_user: root
  tasks:
  - name: ensure apache is at the latest version
    yum: name=httpd state=latest
  - name: write the apache config file
    template: src=/srv/httpd.j2 dest=/etc/httpd.conf
    notify:
    - restart apache
  - name: ensure apache is running (and enable it at boot)
    service: name=httpd state=started enabled=yes
  handlers:
    - name: restart apache
      service: name=httpd state=restarted 
```

我希望这个例子能让你了解我上面提到的行动手册组件的所有描述。如果你仍然不清楚，不要担心，你所有的疑问都会在本博客的后面部分得到解答。

这都是关于行动手册的。你将要写的剧本。但是 Ansible 也为您提供了大量的模块，您可以使用这些模块。

## **Ansible 教程——模块**

Ansible 中的模是幂等的。从 RESTful 服务的角度来看，要使一个操作(或服务调用)是幂等的，客户机可以重复进行相同的调用，同时产生相同的结果。换句话说，发出多个相同的请求与发出一个请求具有相同的效果。

ansi ble 中有不同类型的模块

*   核心模块
*   临时演员模块

## **核心模块**

这些是 Ansible 核心团队维护的模块，并且将会一直与 Ansible 一起发布。与“额外”回购中的请求相比，它们在所有请求中也会获得稍高的优先级。

这些模块的源代码由 Ansible 托管在 Ansible-modules-core 中的 GitHub 上。

## **群众演员模块**

这些模块目前随 Ansible 一起发货，但将来可能会单独发货。它们也主要由 Ansible 社区维护。非核心模块仍然完全可用，但对问题和拉请求的响应率可能会稍低。

随着时间的推移，受欢迎的“额外”模块可能会提升为核心模块。

这些模块的源代码由 Ansible 托管在 GitHub 的 Ansible-modules-extras 中。

远程管理模块中的一个额外模块是 ipmi_power 模块，它是远程机器的电源管理器。它需要 python 2.6 或更高版本和 pyghmi 才能运行。

你可以通过写一个类似我下面写的命令来使用这个模块:

```
ipmi_power : name ="test.domain.com" user="localhost" password="xyz" state="on"
```

## **Ansible 教程——返回值**

Ansible 模块通常会返回一个数据结构，该数据结构可以注册到变量中，或者在 Ansible 程序输出时可以直接看到。每个模块可以有选择地记录自己唯一的返回值。

返回值的一些例子有:

*   changed:每当任务发生变化时，返回一个布尔值。
*   失败:如果任务失败，返回一个布尔值
*   msg:它返回一个字符串，其中包含一条转发给用户的通用消息。

## **Ansible 教程——即席命令**

临时命令是简单的一行命令，用来执行一些动作。使用 Ansible 命令运行模块是临时命令。

例如:

```
ansible host -m netscaler -a "nsc_host=nsc.example.com user=apiuser password=apipass"

```

上面的即席命令使用 netscaler 模块禁用服务器。Ansible 提供了数百个模块，您可以从中引用和编写即席命令。【T2

好了，理论上的解释已经说得够多了，让我用实际行动来解释给你听。

## **Ansible 教程——动手**

我将编写一个剧本，在我的节点/主机上安装 Nginx。

我们开始吧:)

**第一步:**使用 SSH 连接到您的主机。为此，您需要生成一个公共 SSH 密钥。

使用下面的命令:

**ssh-keygen**

![Generate Ssh Key - Ansible Tutorial - Edureka](img/85a15e68120896f5aa71ba7240acd29c.png)

从上面的快照中可以看到，命令 **ssh-keygen** 生成了一个公共 ssh 密钥。

**步骤 2:** 您的下一个任务是在您的主机上复制公共 SSH 密钥。为此，使用下面的命令:

**ssh-copy-id -i root@ <你的主机 IP 地址>**

![Copy Ssh Key - Ansible Tutorial - Edureka](img/0cb551b3f1999e53a03c37922f013a0c.png)

上面的快照显示了 SSH 密钥被复制到主机。

**步骤 3:** 在清单中列出主机/节点的 IP 地址。

使用以下命令:

**VI/etc/ansi ble/hosts**

![Test Server - Ansible Tutorial - Edureka](img/76cd35ce2bde660a7eb48aefd75d49aa.png)

这将打开一个 vi 编辑器，您可以在其中列出主机的 IP 地址。这是现在你的库存。

**第四步:**让我们 ping 一下，确保连接已经建立。

![Ping Hosts - Ansible Tutorial - Edureka](img/3ab9ba738d48b3dcf8437ee4eff45ef6.png)

上面的快照确认您的控制机器和主机之间已经建立连接。

**步骤 5:** 现在让我们写一个剧本，在主机上安装 Nginx。您可以在 vi 编辑器中编写您的剧本。为此，只需使用命令:创建您的剧本

**vi <你的文件名>。yml**

下面的快照展示了我用 YAML 格式写的安装 Nginx 的剧本。

![Yaml Nginx - Ansible Tutorial - Edureka](img/c8898ea84535a3f35d05872eac568f64.png)

在 YAML，剧本的任务被定义为一个字典列表，从上到下执行。如果我们有几台主机，那么在转移到下一台主机之前，每个任务都要在每台主机上尝试。每个任务都被定义为一个字典，可以有几个键，比如“name”或“sudo ”,它们表示任务的名称以及它是否需要 sudo 特权。

设置了一个变量 *server_port* ，它在 TCP 端口 **8080** 上监听传入的请求。

这里，第一个任务是获得安装 Nginx 所必需的包，然后安装它。 在内部，Ansible 会检查目录是否存在，如果不存在就创建它，否则什么也不做。

下一个任务是配置 Nginx。 在 Nginx 中，上下文包含配置细节。

这里，模板是一个可以在主机上部署的文件。然而，模板文件也包括一些参考变量，这些变量是从定义为可翻译剧本的一部分的变量或从主机收集的事实中提取的。包含配置细节的事实被从源目录中取出，并被复制到目标目录中。

这里的处理程序定义了只有在任务或状态改变的通知下才执行的动作。在本行动手册中，我们定义了 notify: restart Nginx 处理程序，它将在文件和模板复制到主机后重启 Nginx。

现在，保存文件并退出。

**步骤 6:** 现在让我们使用下面的命令运行这个剧本:

**ansible-playbook <你的文件名>。yml**

![Run Playbook - Ansible Tutorial - Edureka](img/57e4a91410fb213ceaaa9c85475738cc.png)

从上面的截图中我们可以看到，我们的任务正在执行；正在安装 Nginx。

**第七步:**让我们检查一下我的主机上是否安装了 Nginx。使用下面的命令:

**【PS wax | grep engine**

![Run Nginx - Ansible Tutorial - Edureka](img/1793e2d40903fccd2531bb9d67b43929.png)

你可以在上面的截图中看到，不同的进程 ids 3555 和 103316 正在运行，这确保了 Nginx 在你的主机上运行。

**恭喜恭喜！**您已经使用 Ansible 行动手册在您的主机上成功部署了 Nginx。我希望你喜欢阅读这个 Ansible 教程博客。如果你有任何疑问，请在下面的评论区告诉我。

*如果你发现了这篇《 **Ansible 教程*** *】相关，* *请查看 Edureka 的* [***DevOps 培训***](https://www.edureka.co/devops/) *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka DevOps 认证培训课程帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Ansible、Nagios 和 Git，用于自动化 SDLC 中的多个步骤。*