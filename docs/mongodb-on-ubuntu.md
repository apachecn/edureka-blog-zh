# 如何在 Ubuntu 操作系统上安装 MongoDB？

> 原文：<https://www.edureka.co/blog/mongodb-on-ubuntu/>

仅次于 windows 操作系统，Linux 是目前业界最流行的操作系统之一。但与标准版本的 Windows 和 Mac OS 不同，Linux 操作系统有各种不同的风格，用户可以根据自己的需要下载。其中一个 Linux 操作系统版本是 Ubuntu，它是目前最流行的 Linux 版本。如果你想在你的 Ubuntu 操作系统上使用 [MongoDB](https://www.edureka.co/blog/mongodb-the-database-for-big-data-processing/) ,首先要在你的 Ubuntu 操作系统上安装 MongoDB，在本文中我们将讨论这个问题。

本文将涉及以下几点:

*   [导入 MongoDB 包](#ImportMongoDBPackage)
*   [安装 MongoDB 包](#InstallMongoDBPackage)
*   [启动 MongoDB 平台](#LaunchMongoDBPlatform)
*   [配置并连接到 MongoDB 服务器](#ConfiguringandConnectingtotheMongoDBServer)

让我们开始吧！

**如何在 Ubuntu 上安装 MongoDB**

为了在 Ubuntu 操作系统上安装 MongoDB，请遵循以下步骤。

## **导入 MongoDB 包**

在这一步中，您需要首先导入 ubuntu 软件包管理系统使用的公钥。使用 Ubuntu 软件包管理系统的一个最大的好处是，它导入的所有密钥都是一致的和真实的，因为它验证所有的东西都是用 GPG 密钥签名的。

![Output - Install MongoDB On Ubuntu - Edureka](img/04c8e42a11dee4f865610b2bfefb5625.png)

为了导入 MongoDB 公钥，可以使用下面的命令。

> sudo apt-key adv–key server hkp://key server . Ubuntu . com:80–recv 7f 0 CEB 10

完成后，您需要为 MongoDB 创建一个源代码列表文件

您需要创建的列表是，/etc/apt/sources . list . d/MongoDB-org-3.4 . list，为了做到这一点，您可以使用以下命令。

> echo " deb http://repo.mongodb.org/apt/ubuntu xenial/MongoDB-org/3.4 多元宇宙" | sudo tee/etc/apt/sources . list . d/MongoDB-org-3.4 . list

完成后，您需要更新本地包存储库。为此，请使用以下命令。

```
> sudo apt-get update
```

现在让我们看看如何安装 MongoDB 包

## **安装 MongoDB 包**

既然您已经成功导入了 MongoDB 存储库，那么是时候安装 MongoDB 包了。

您需要安装 MongoDB for Ubuntu 的最新稳定版本，为了做到这一点，请使用以下命令。

```
> sudo apt-get install -y mongodb-org
```

如果在某种情况下，你需要为 Ubuntu 安装一个特定版本的 MongoDB，你可以利用下面的命令. sudo apt-get install-y MongoDB-org = 3.4 MongoDB-org-server = 3.4 MongoDB-org-shell = 3.4 MongoDB-org-mongos = 3.4 MongoDB-org-tools = 3.4

现在我们知道了如何在 Ubuntu 上安装 MongoDB，让我们看看如何启动它，

## **启动 MongoDB 平台**

既然 mongoDb 已经成功安装在您的 Ubuntu 系统上，现在是时候启动它了。为此，您可以使用下面的代码。

![Output - Install MongoDB On Ubuntu - Edureka](img/04c8e42a11dee4f865610b2bfefb5625.png)

```
> sudo vim /etc/systemd/system/mongodb.service
```

在上面的例子中，我们在/etc/systemd/system 中创建了一个名为 mongodb.service 的配置文件，并使用它来管理我们需要的所有 mongodb 服务。

成功创建文件后，打开该文件并将以下代码复制粘贴到其内容中。

#Unit 包含服务启动前需要满足的依赖关系。

```
[Unit]
Description=MongoDB Database
After=network.target
Documentation=https://docs.mongodb.org/manual
# Service tells systemd, how the service should be started.
# Key `User` specifies that the server will run under the mongodb user and
# `ExecStart` defines the startup command for MongoDB server.
[Service]
User=mongodb
Group=mongodb
ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf
# Install tells systemd when the service should be automatically started.
# `multi-user.target` means the server will be automatically started during boot.
[Install]
WantedBy=multi-user.target
```

完成后，使用下面的命令更新系统服务。

```
> systemctl daemon-reload
```

使用 systemcl 启动服务。

```
> sudo systemctl start mongodb
```

您需要确保 mongoDb 已经在端口 27017 上启动。为此，请使用下面的代码。

```
> netstat -plntu
```

之后，您需要检查服务是否已经正确启动。使用下面的代码做同样的事情，

```
> sudo systemctl status mongodb
```

如果系统按预期启动并运行，您的输出应该显示 active(正在运行),以及当前消耗的 PID 和内存/CPU。

如果在某种情况下，您需要启用 MongoDb 的自动启动，您需要使用以下命令。

```
> sudo systemctl enable mongodb
```

要停止 MongoDB，请使用以下命令。

```
> sudo systemctl stop mongodb
```

如果您需要重启 mongoDb，请使用这个命令。

```
> sudo systemctl restart mongodb
```

这就把我们带到了本文的最后一点，

## **配置并连接到 MongoDB 服务器**

首先打开 mongoDb 外壳。为了在您的服务器上做到这一点，请使用以下命令。

```
> mongo
```

打开后，使用下面的代码切换到管理数据库。

```
> use admin
```

现在使用这个命令创建 root 用户。

```
> db.createUser({user:"admin", pwd:&rdquo;password", roles:[{role:"root", db:"admin"}]})
```

现在，当所有这些都完成后，退出 MongoDb shell。

重新启动 mongoDb，并连接上一步中创建的用户。

```
> mongo -u admin -p admin123 --authenticationDatabase admin
```

如果您想查看正在连接的当前数据库，请使用以下命令。

```
Show dbs
```

这就把我们带到了本文的结尾。希望你已经学会了如何在 Ubuntu 操作系统上安装 MongoDB。

*现在您已经了解了什么是大数据，请查看 Edureka 提供的 [**大数据培训**](https://www.edureka.co/big-data-and-hadoop)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 大数据 Hadoop 认证培训课程使用零售、社交媒体、航空、旅游和金融领域的实时用例，帮助学员成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 领域的专家。*

有问题要问我们吗？在评论区提到它们，我们会给你回复。