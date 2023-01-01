# Chef 教程–将基础设施转化为代码

> 原文：<https://www.edureka.co/blog/chef-tutorial/>

## **厨师教程**

厨师教程是厨师博客系列的第二篇博客。在我之前的 [***博客***](https://www.edureka.co/blog/what-is-chef/) 中，我已经借助 Gannett 的一个用例解释了什么是 Chef、配置管理以及 Chef 如何实现配置管理。

本厨师教程将涵盖以下主题:

*   [厨师架构](#chef_architecture)
*   [动手](#hands_on)演示

我相信看了我的 [***之前的博客***](https://www.edureka.co/blog/what-is-chef/) 你一定很好奇厨师到底是怎么工作的。本主厨教程博客第一节将为您详细讲解主厨架构，为您扫清所有疑惑。

## **厨师教程——厨师建筑**

如下图所示，Chef 有三大组件:

*   工作站
*   服务器
*   节点

![ Chef Architecture - Chef Tutorial - Edureka](img/e3e17dd39338b44305005c520f5e50d8.png)

**厨师教程——工作站**

工作站是管理所有厨师配置的位置。这台机器保存所有的配置数据，这些数据可以在以后推送到中央 Chef 服务器。在将这些配置推送到 Chef 服务器之前，会在工作站中对其进行测试。工作站由一个名为**刀、**的命令行工具组成，用于与 Chef 服务器进行交互。可以有多个工作站一起管理中央 Chef 服务器。

![Multiple Workstations - Chef Tutorial - Edureka](img/70f451fcc67a26afa1c31e6908b6ff9d.png)

工作站负责执行以下功能:

*   **编写菜谱和食谱，稍后将推送到中央厨师服务器**
*   **管理中心厨师服务器上的节点**

现在，让我们一个一个地了解上面提到的要点。

**编写菜谱和食谱，稍后将推送到中央厨师服务器**

**配方:** 配方是描述特定配置或策略的资源集合。它描述了配置部分系统所需的一切。用户编写食谱，描述 Chef 如何管理应用程序和实用程序(如 Apache HTTP Server、MySQL 或 Hadoop)以及如何配置它们。

这些配方描述了一系列应该处于特定状态的资源，即应该安装的包、应该运行的服务或应该写入的文件。

*稍后在博客*中，我会通过在 Chef Workstation 中编写一段 ruby 代码，向大家展示如何编写在 Chef 节点上安装 Apache2 包的菜谱。

**菜谱:** 多个菜谱可以组合在一起形成一个菜谱。一本食谱定义了一个场景，包含了支持这个场景所需要的一切:

*   配方，指定要使用的资源及其应用顺序
*   属性值
*   文件分发
*   模板
*   Chef 的扩展，如库、定义和自定义资源

**管理中心厨师服务器上的节点**

工作站系统将具有所需的命令行实用程序，以控制和管理中央 Chef 服务器的各个方面。向中央 Chef 服务器添加新节点、从中央 Chef 服务器删除节点、修改节点配置等都可以从工作站本身进行管理。

现在让我们看看，执行上述功能需要工作站的哪些组件。

**工作站有两大组成:**

**刀实用:** 该命令行工具可用于从工作站与中央厨师服务器通信。添加、删除、更改中央 Chef 服务器中的节点配置将通过使用此刀工具来执行。使用 Knife 工具，可以将食谱上传到中央 Chef 服务器，还可以管理角色和环境。基本上，中央厨师服务器的每一个方面都可以从工作站使用小刀工具进行控制。

**一个本地 Chef 库:** 这是存储中央 Chef 服务器的每一个配置组件的地方。这个 Chef 存储库可以与中央 Chef 服务器同步(再次使用小刀工具本身)。

**厨师教程——厨师服务器**

Chef 服务器充当配置数据的中心。Chef 服务器存储 Cookbooks、应用于节点的策略以及描述由 Chef-Client 管理的每个注册节点的元数据。

节点使用 Chef-Client 向 Chef 服务器请求配置细节，例如食谱、模板和文件分发。然后，Chef-Client 在节点本身(而不是在 Chef 服务器上)完成尽可能多的配置工作。每个节点都安装了一个 Chef 客户端软件，该软件将从中央 Chef 服务器下载适用于该节点的配置。这种可扩展的方法将配置工作分布在整个组织中。

**厨师教程——厨师节点**

节点可以是基于云的虚拟服务器，也可以是您自己的数据中心中的物理服务器，使用 central Chef Server 进行管理。需要出现在节点上的主要组件是一个代理，它将与中央 Chef 服务器建立通信。这叫厨师客户端。

Chef 客户端执行以下功能:

*   负责与中央 Chef 服务器交互。
*   它管理节点到中央 Chef 服务器的初始注册。
*   它将 Cookbooks 下载下来，并将其应用到节点上，以对其进行配置。
*   定期轮询中央 Chef 服务器，以获取新的配置项目(如果有)。

***[点击此处了解如何安装 Chef 服务器、工作站和节点](https://www.edureka.co/blog/install-chef/)***

**厨师教程——厨师的优势:**

如果我不包括厨师的主要好处，这个厨师教程将是不完整的:

*   使用 Chef，您可以自动化整个基础设施。所有手动完成的任务现在都可以通过 Chef 工具完成。
*   使用 Chef，您可以在几分钟内配置数千个节点。
*   Chef automation 适用于大多数公共云产品，如[***AWS***](https://www.edureka.co/blog/amazon-aws-tutorial/)。
*   Chef 不仅会自动完成工作，还会对系统进行一致的检查，并确认系统确实按照要求的方式进行了配置(Chef 代理/客户完成这项工作)。如果有人在修改文件时犯了错误，Chef 会更正它。
*   整个基础设施可以以 Chef 存储库的形式记录下来，该存储库可以用作从零开始重建基础设施的蓝图。

我希望你喜欢这个厨师教程，不要再谈理论了！让我们享受动手的乐趣。

**厨师教程|厨师入门|爱德华卡**

[//www.youtube.com/embed/LTIjUJEehDA?rel=0&showinfo=0](//www.youtube.com/embed/LTIjUJEehDA?rel=0&showinfo=0)

## **厨师教程——动手**

在这里，我将向您介绍如何在 Chef Workstation 中创建食谱、食谱和模板。我还将向您解释如何将 Cookbook 从工作站部署到 Chef-Client (Chef 节点)。

我使用了两个虚拟映像，一个用于 Chef 工作站，另一个用于 Chef 节点。对于 Chef 服务器，我将使用托管版本的 Chef(在云上)。您也可以使用物理机作为 Chef 服务器。

**第一步:** 在你的 Chef 工作站安装 Chef DK(开发套件)。

Chef DK 是一个包，包含了你在编写 Chef 时需要的所有开发工具。下面是下载 ***[厨师 DK](https://downloads.chef.io/chef-dk/)*** 的链接。

![chef-dk-chef-tutorial-edureka](img/0dd424b5d2c367077f6553578ec98840.png)

在这里，选择你正在使用的操作系统。我用的是 CentOS 6.8。所以，我会点击 **红帽企业版 Linux** 。

![ CentOS Chef DK - Chef Tutorial - Edureka](img/cf20e8c4a4d5145267273caca3699552.png)

根据您使用的 CentOS 版本复制链接。我用的是 CentOS 6，你可以看到我在上面的截图中高亮显示了。

进入您的工作站终端，使用 wget 命令下载 Chef DK 并粘贴链接。

**执行此:**

```
wget https://packages.chef.io/stable/el/6/chefdk-1.0.3-1.el6.x86_64.rpm

```

![Download Chef DK - Chef Tutorial - Edureka](img/047b18d5d5c80c12f85b55033344a046.png)

软件包现已下载完毕。是时候使用 rpm 安装这个包了。

**执行此:**

```
rpm -ivh chefdk-1.0.3-1.el6.x86_64.rpm

```

![Install Chef DK - Chef Tutorial - Edureka](img/d4d7aa0c8e00687da26646da741df0a6.png)

Chef DK 现已安装在我的工作站上。

**第二步:** 在工作站 创建配方

让我们从在工作站中创建一个配方开始，并在本地测试它以确保它能正常工作。创建一个名为 chef-repo 的文件夹。我们可以在这个文件夹中创建我们的食谱。

**执行此:**

```
mkdir chef-repo
cd chef-repo

```

![chef-repo - Chef Tutorial - Edureka](img/2112c6a8e2536b34697f0c34fcf9107d.png)

在这个 chef-repo 目录中，我将创建一个名为 edureka.rb 的菜谱。rb 是 ruby 使用的扩展。我将使用 vim 编辑器，你可以使用任何其他编辑器，如 gedit，emac，vi 等。

**执行此:**

```
vim edureka.rb

```

在此添加以下内容:

```
file '/etc/motd' 
content 'Welcome to Chef'
end

```

![Recipe Content - Chef Tutorial - Edureka ](img/053a6cb2eea960dac7722ab3af64ce54.png)

本 r【ecpe】 【【【 rb 创建了一个名为/etc/motd 的文件，内容为“欢迎厨师”。

现在我要用这个食谱来检查它是否有效。

**执行** **本:**

```
chef-apply edureka.rb

```

![ Apply Motd Recipe - Chef Tutorial - Edureka](img/95609b9b11455f85ed807438d4cef9bf.png)

因此在 chef-repo 中创建了一个文件，其内容为 **欢迎来到 chef。**

**第三步:** M 修改配方文件安装 httpd 包

我将修改配方，在我的工作站上安装 httpd 包，并将一个 index.html 文件复制到默认的文档根目录，以确认安装。包资源的默认动作是安装，因此我不需要单独指定那个动作。

**执行** **本:**

```
vim edureka.rb

```

在这里添加以下内容:

```
package 'httpd'
service 'httpd' do
action [:enable, :start]
end
file '/var/www/html/index.html' do
content 'Welcome to Apache in Chef'
end

```

![HTTPD Package Recipe - Chef Tutorial - Edureka](img/a2e0ac2ecab3b62c873273465e5226b6.png)

现在，我将通过执行以下命令来应用这些配置:

**执行** **本:**

```
chef-apply edureka.rb

```

![Apply httpd Recipe - Chef Tutorial - Edureka](img/d34f2b81610f415f91d45442aacf26a6.png)

命令执行清楚地描述了配方中的每个实例。它安装 Apache 包，在工作站上启用并启动 httpd 服务。它在默认文档根目录下创建一个 index.html 文件，内容为“欢迎使用 Chef 中的 Apache”。

现在，打开您的网络浏览器，确认 Apache2 的安装。键入您的公共 IP 地址或主机名称。在我的例子中，它是 localhost。

![Confirm Installation - Chef Tutorial - Edureka](img/50c7b3ea21db2c6d8e1672e62bf6ef3c.png)

**第四步:** 现在我们将创建我们的第一本食谱。

创建一个名为 cookbooks 的目录，并执行下面的命令来生成 Cookbook。

**执行** **本:**

```
mkdir cookbooks
cd cookbooks
chef generate cookbook httpd_deploy

```

httpd_deploy 是 Cookbook 的一个名字。你可以给任何你想要的名字。

![Creating Chef Cookbooks - Chef Tutorial - Edureka](img/21ecbf62e4d53c2b2edcad3202870a62.png)

让我们转移到这个新目录 httpd_deploy。

**执行** **本:**

```
cd httpd_deploy

```

现在让我们看看创建的 Cookbook 的文件结构。

**执行** **本:**

```
tree

```

![Chef Cookbook Structure - Chef Tutorial - Edureka](img/23fbba3cd52de24d2562624ab9802994.png)

**第五步:** C 创建一个模板文件。

早些时候，我创建了一个包含一些内容的文件，但这不符合我的食谱和烹饪书的结构。因此，让我们看看如何才能创建一个 index.html 网页模板。

**执行** **本:**

```
chef generate template httpd_deploy index.html

```

![Create Chef Template - Chef Tutorial - Edureka](img/b5e482f80fcb137e43a786888a4dc658.png)

![ Cookbook Structure - Chef Tutorial - Edureka](img/6a3c8d954f68119ffd66a690d6499532.png)

现在，如果你看到我的 Cookbook 文件结构，有一个名为 templates with index . html . erb file 的文件夹。我将编辑这个 index.html.erb 模板文件，并将我的食谱添加到其中。参考下面的例子:

转到默认目录

**执行** **本:**

```
cd /root/chef-repo/cookbook/httpd_deploy/templates/default

```

在这里，使用您熟悉的任何编辑器编辑 index.html.erb 模板。我将使用 vim 编辑器。

**执行** **本:**

```
vim index.html.erb

```

现在添加以下内容:

```
Welcome to Chef Apache Deployment

```

**第六步:** C 用这个模板创建一个食谱。

转到菜谱目录。

**执行 t** **手下:**

```
cd /root/chef-repo/cookbooks/httpd_deploy/recipes

```

现在使用你想要的任何编辑器编辑 default.rb 文件。我将使用 vim 编辑器。

**执行** **本:**

```
vim default.rb

```

在这里添加以下内容:

```
package 'httpd'
service 'httpd' do
action [:enable, :start]
end
template '/var/www/html/index.html' do
source 'index.html.erb'
end

```

![Recipe - Chef Tutorial - Edureka](img/e5c2afe8090f212972ea63d24ef127a4.png)

现在，我将返回到我的 chef-repo 文件夹，在我的工作站上运行/测试我的食谱。

**执行** **本:**

```
cd /root/chef-repo
chef-client --local-mode --runlist 'recipe[httpd_deploy]'

```

![Apply Chef Recipe - Chef Tutorial - Edureka](img/cfbaecd2472506faf5877a4fd4df66df.png)

根据我的配方，Apache 安装在我的工作站上，服务在启动时启动。此外，在我的默认文档根目录下创建了一个模板文件。

现在我已经测试了我的工作站。是时候设置 Chef 服务器了。

**第七步:**设置厨师服务器

我将在云上使用主厨服务器的托管版本，但你也可以使用物理机。 本主厨-服务员现于*[**manage . Chef . io**](http://manage.chef.io)*

![ Chef Cloud Server - Chef Tutorial - Edureka.](img/06d8348a48d9bb41b30356f0bdeaaa7a.png)

如果您还没有帐户，请在这里创建一个。创建帐户后，使用您的登录凭据登录。

![Chef Server - Chef Tutorial - Edureka](img/a8c22a54e5017901b577ec1d78a510cf.png)

这是 Chef 服务器的样子。

如果你是第一次登录，你要做的第一件事就是创建一个组织。组织基本上是您将使用 Chef 服务器管理的一组机器。

首先，我将转到“管理”选项卡。在那里，我已经创建了一个名为 edu 的组织。所以我需要在我的工作站上下载初学者工具包。该初学者工具包将帮助您将文件从工作站推送到 Chef 服务器。单击右侧的设置图标，然后单击初学者工具包。

![Chef Starter Kit - Chef Tutorial - Edureka](img/93f5f5b3216c248883146542d73d2237.png)

当你点击那里时，你会看到一个下载初学者工具包的选项。只需单击它即可下载初学者工具包 zip 文件。

![ Starter Kit Download - Chef Tutorial - Edureka](img/6d307d86b089dc86e1728d15d970303a.png)

将此文件移动到您的根目录。 现在在你的终端中使用 unzip 命令解压这个 zip 文件。您会注意到它包括一个名为 chef-repo 的目录。

**执行** **本:**

```
unzip chef-starter.zip

```

![Unzip Chef Starter kit - Chef Tutorial - Edureka](img/9b2cb3ec9461d2ec7076f839ef5c925e.png)

现在，将这个初学者工具包移动到 chef-repo 目录中的 cookbook 目录。

**执行** **本:**

```
mv starter /root/chef-repo/cookbook

```

厨师烹饪书可以在烹饪书超市买到，我们可以去厨师超市。从 *[**超市. chef.io**](http://supermarket.chef.io)* 下载需要的食谱。我正在下载一本安装 Apache 的食谱。

**Execut****e t****h****是:**

```
cd chef-repo
knife cookbook site download learn_chef_httpd

```

有一本为阿帕奇食谱下载的焦油球。现在，我们需要从这个下载的 Tar 文件中提取内容。为此，我将使用 tar 命令。

```
tar -xvf learn_chef_httpd-0.2.0.tar.gz

```

![ Untar Apache Package - Chef Tutorial - Edureka](img/ff4e30c555dc36197ddf029a18ffbabc.png)

所有需要的文件都是在这个食谱下自动创建的。没有必要做任何修改。让我们检查一下我的食谱文件夹里的食谱描述。

**执行 t****h****是** **:**

```
cd /root/chef-repo/learn_chef_httpd/recipes
cat default.rb

```

![Cookbook Contents - Chef Tutorial - Edureka](img/4589b770d315fa5fc526b9fe669a55c1.png)

现在，我会把这本食谱上传到我的厨师服务器上，因为它看起来很完美。

**第八步:** 上传菜谱到厨师服务器。

为了上传我下载的 Apache Cookbook，首先将这个 learn_chef_httpd 文件移动到 chef-repo 中的 Cookbooks 文件夹。然后将您的目录更改为 cookbooks。

**执行 t** **h** **是** **:**

```
mv /root/chef-repo/learn_chef_httpd /root/chef-repo/cookbooks

```

现在转到这个食谱目录。

**执行此:**

```
cd cookbooks

```

现在在这个目录中，执行下面的命令来上传 Apache CookbooT2 k:

**Exec****ute t****h****是:**

```
knife cookbook upload learn_chef_httpd

```

![Upload Apache Cookbook - Chef Tutorial - Edureka](img/26785aef4e21bcee9159028352d0843b.png)

从 Chef 服务器管理控制台验证食谱。在策略部分，您将找到您已经上传的食谱。参考下面截图:

![Chef Server Policy Tab - Chef Tutorial - Edureka](img/365c6166b6455024ea05b6447dead5ef.png)

现在我们的最后一步是添加厨师节点。我已经设置了一个工作站和一个 Chef 服务器，现在我需要将我的客户端添加到 Chef 服务器以实现自动化。

**第九步:** 向 Chef 服务器添加 Chef 节点。

出于演示目的，我将使用一台 CentOS 机器作为 Chef 节点。一台 Chef 服务器上可能会连接数百个节点。我的节点机器的终端颜色与工作站不同，这样您就能够区分两者。

我只需要我的节点的 IP 地址，因为我将在我的节点机器 e. 中执行下面的命令

**Exec****u****t****e**

```
ifconfig

```

![Chef Node IP address - Chef Tutorial - Edureka](img/c205b98ec4bc79ec07e11ab74bd2e8b2.png)

我将通过执行 Knife Bootstrap 命令将我的 Chef 节点添加到服务器，在该命令中，我将指定 Chef 节点的 IP 地址及其名称。执行下图所示的命令T2 w:

**Exec****ute t****h****是:**

```
knife bootstrap 192.168.56.102 --ssh-user root --ssh-password edureka --node-name chefNode

```

![chef-node-bootstrap-1-chef-tutorial-edureka](img/83ed658af0c495775de45de55c380b0c.png)

![chef-node-bootstrap-2-chef-tutorial-edureka](img/37f065bf986caf1553337f53cb3d6eb3.png)

该命令还将初始化 Chef 节点中 Chef-Client 的安装。您可以在工作站的 CLI 中使用 knife 命令进行验证，如下图 w:

**Exec****ute t****h****是:**

```
Knife node list

```

![Chef Node List - Chef Tutorial - Edureka](img/0cd332cbc08622a2b1f28cc7bfc58a36.png)

也可以从 Chef 服务器验证。转到服务器管理控制台中的 nodes 选项卡，在这里您会注意到您添加的节点已经存在。参考下面的截图。

![Confirm Chef Node Addition - Chef Tutorial - Edureka](img/badf2886b439c00a7c8460fa9e036b87.png)

**第十步:** 管理节点运行列表

让我们看看如何向节点添加一个 Cookbook，并从 Chef 服务器管理它的运行列表。正如您在下面的屏幕截图中看到的，单击 Actions 选项卡并选择 Edit Run list 选项来管理运行列表。

![Edit Run List - Chef Tutorial - Edureka](img/695c15cf250fbb7cfa37d10d7aa24965.png)

在可用菜谱中，您可以看到我们的 learn_chef_httpd 菜谱，您可以将它从可用套餐中拖到当前运行列表中并保存运行列表。

![Run List - Chef Tutorial - Edureka](img/ff93170eda7ba8c62600090b58b1291c.png)

![Current Run List - Chef Tutorial - Edureka](img/035633fbc1ad84267d5df82a1f60a868.png)

现在登录到您的节点，运行 chef-client 来执行运行 Lis t.

**Exec****ute t****h****是:**

```
chef-client

```

![Execute Chef-Client - Chef Tutorial - Edureka](img/1c3fbd0ef24dac6b58f3cecac51f31c7.png)

我希望您喜欢这篇 Chef 教程，并了解了如何使用 Chef 来配置数百个节点。厨师在许多组织中发挥着至关重要的作用，以实现发展目标。随着厨师组织发布应用程序越来越频繁，relia b ly。

*如果你在“**厨师教程**”上找到这篇相关的博客，* *请查看 Edureka 的* *[**DevOps 培训**](https://www.edureka.co/devops/) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka DevOps 认证培训课程可帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Chef、Jenkins、Nagios 和 GIT，用于自动化 SDLC 中的多个步骤。*