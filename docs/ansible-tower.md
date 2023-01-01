# 探索可行的塔，亲自动手

> 原文：<https://www.edureka.co/blog/ansible-tower/>

当今的扩展行业旨在大幅提高生产率，但他们必须应对各种各样的自动化挑战，Ansible 等工具可以克服这些挑战。这篇关于 Ansible Tower 的博客将让你对以下内容有一个完整的了解:

*   [什么是 ansi ble——塔？](#What%20is%20Tower?)
*   [安装 ansi ble-Tower](#Prerequisites%20To%20Install%20Tower)T3 的先决条件
*   [ansi ble–塔架参数](#Ansible%20Tower%20Parameters)
*   [安装步骤](#Installation%20Steps)
*   [动手](#Hands-On)

好吧！！那么，让我们从什么是安塞布尔塔开始。

## **什么是 Ansible 塔？**

Ansible Tower 可以在更大的企业级别上使用。它是一个基于 web 的解决方案，通过非常简单的用户界面来管理您的组织，提供了一个包含所有主机的所有状态摘要的控制面板，允许快速部署，并监控所有配置。

该塔允许您共享 SSH 凭据而不暴露它们，记录所有作业，以图形方式管理库存，并与各种各样的云提供商同步。

## **安装天线塔的先决条件**

以下是安装塔的先决条件:

以下操作系统支持 ansi ble Tower:

*   红帽企业版 Linux 6 64 位
*   红帽企业版 Linux 7 64 位
*   CentOS 6 64 位
*   CentOS 7 64 位
*   Ubuntu 12.04 lt 64 位
*   Ubuntu 14.04 lt 64 位
*   Ubuntu 16.04 lt 64 位

您应该拥有 Ansible 的最新稳定版本。

需要 64 位支持(内核和运行时)和 20 GB 硬盘。

至少需要 2 GB 内存(建议 4gb 以上的内存)。

*   2 GB RAM(最低，建议用于流动试用安装
*   建议 4 GB 内存/100 个分叉

对于 Amazon EC2:少于 100 台主机需要 m3.medium 或更大的实例大小，如果您有超过 100 台主机，那么您需要 m3.xlarge 或更大的实例大小。

对于 HA MongoDB 设置，您可以使用下面的公式粗略估计所需的空间量。

(编号【主机】盘点】 * (编号 扫描 * (平均 模块 事实 大小) * (编号

#### 订阅我们的 youtube 频道获取新的更新..！