# 可翻译的备忘单——devo PS 快速入门指南

> 原文：<https://www.edureka.co/blog/cheatsheets/ansible-cheat-sheet-guide/>

你是一名有抱负的 DevOps 工程师，期待学习所有的 DevOps 工具吗？嗯，如果你是，那么你应该考虑通过学习所有的顶级工具来掌握 DevOps 。你的清单上必须有一个这样的工具是 Ansible。 Ansible 是一款*开源 IT* *配置管理*，*部署* & *编排*工具，旨在为各种自动化挑战提供巨大的生产力增益。Ansible 备忘单旨在让你开始使用 ansi ble，并让你理解它的所有基本概念。

## 可翻译的备忘单

**[Ansible](https://www.edureka.co/blog/what-is-ansible/)** 开源[持续部署](https://www.edureka.co/blog/continuous-deployment/)，配置管理，&编排。该工具旨在为各种各样的自动化挑战提供巨大的生产力增益，并且功能强大到足以自动化复杂的多层 IT 应用程序环境。

![Ansible Logo - Ansible Cheat Sheet - Edureka](img/be4f63682751b00d6a034b675fb72e79.png)

[![Ansible Cheat Sheet - Ansible Cheat Sheet - Edureka](img/6f813b62dd285b49467e28baa28e290d.png)](https://bit.ly/2qDmieD)

## SSH 密钥生成

Ansible 使用 SSH 在节点之间进行通信。

要建立 SSH 连接，请遵循下面提到的步骤:

*   设置 SSH 命令
*   生成 SSH 密钥
*   在主机上复制 SSH 密钥
*   检查 SSH 连接

```
#Setting Up SSH Command
$ sudo apt-get install openssh-server

#Generating SSH Key 
$ ssh-keygen

#Copy the SSH Key on the Hosts
$ ssh-copy-id hostname

#Check the SSH Connection 
$ ssh <nodeName>
```

## 安装 Ansible

要在基于 Debian 的 Linux 上安装 Ansible ，可以按照以下步骤进行:

*   在安装 Ansible 之前，将 Ansible 存储库添加到您的系统中
*   然后在安装前运行更新命令，更新现有的软件包
*   之后，安装易安装的软件包

```
#Add Ansible repository 
$ sudo apt-add-repository ppa:ansible/ansible
 #Run the update command
$ sudo apt-get update
 #Install Ansible package
$ sudo apt-get install ansible

#Check Ansible Version
$ ansible –version
```

## 清单文件和主机模式

Ansible 的清单文件列出了您想要跨平台自动化的所有平台。单个实例上的 Ansible 可以在基础结构中的多个主机上工作。也可以同时拥有多个库存文件。

*   主机清单文件可以包含单独或成组的主机名
*   可以通过在方括号中给出组名来创建主机组
*   群组成员可以列在下面，直到出现换行

## 设置并检查主机连接

按照以下步骤设置主机，然后检查它们的连接。

```
#Set up hosts by editing the hosts' file in the Ansible directory
$ sudo nano /etc/ansible/hosts

#To check the connection to hosts
#Change your directory to /etc/Ansible 
$ cd /etc/ansible

#Ansible’s ping module allows you to check whether Ansible is connecting to hosts 
$  ansible –m ping <hosts>

#To check on servers individually  
$ ansible -m ping server name

#To check a particular server group 
$ ansible -m ping servergroupname
```

## 易变宿主模式

参考下表了解可行的主机模式，如行动手册中所述。

|  |
| 全部 | 清单中的所有主机 |
| * | 清单中的所有主机 |
| 未分组 | 清单中未出现在组中的所有主机 |
| 10.0.0。* | IP 从 10.0.0 开始的所有主机。* |
| 网络服务器 | 群组网络服务器 |
| web 服务器:！莫斯科 | 仅网络服务器中的主机，不包括莫斯科组中的主机 |
| 网络服务器:&莫斯科 | 仅集团网络服务器和莫斯科的主机 |

## 库存文件示例

下面是一个库存文件的例子，你可以参考了解其中的各种参数。

```
#Default location for host file
$ /etc/ansible/hosts

#To define location for inventory, in CLI
-i<path>

#example host file 
ungrouped.example.com                                     #An ungrouped host

[webservers]                                              #a group called webservers
beta.example.com ansible_host = 10.0.0.5                  #ssh to 10.0.0.5
github.example.com ansible_ssh_user = abc                 #ssh as user abc

[clouds]
cloud.example.com fileuser = alice                        #fileuser is a host variable

[moscow]
beta.example.com                                          #host (DNS will resolve)
telecom.example.com                                       #host(DNS will resolve)

[dev1:children]                                           #dev1 is a group containing
webservers                                                #all hosts in group webservers
clouds                                                    #all hosts in group clouds
```

## 临时命令

临时命令是用于执行动作的快速命令，不会保存下来供以后使用。

您可以使用临时命令执行的一些任务如下:

*   并行和外壳命令
*   文件传输
*   管理软件包
*   从源代码管理部署
*   管理服务

我将用一个基本的例子来解释所有这些任务。

**基本例子:**重新启动欧洲所有的网络服务器，一次 20 台。

## 并行性和 Shell 命令

在这一部分，我将告诉你并行和 shell 的命令。

```
#To set up SSH agent
$ ssh-agent bash
$ ssh-add ~/.ssh/id_rsa

#To use SSH with a password instead of keys, you can use --ask-pass (-K)
$ ansible europe -a "/sbin/reboot" -f 20

#To run /usr/bin/ansible from a user account, not the root
$ ansible europe -a "/usr/bin/foo" -u username

#To run commands through privilege escalation and not through user account
$ ansible europe -a "/usr/bin/foo" -u username --become [--ask-become-pass]

#If you are using password less method then use  --ask-become-pass (-K)
#to interactively get the  password to be  used 
#You can become a user, other than root by using --become-user
$ ansible europe -a "/usr/bin/foo" -u username --become --become-user otheruser [--ask-become-pass]

```

## 管理包

本节包含管理软件包的命令。

```
#To ensure that a package is installed, but doesn’t get updated
$ ansible webservers -m apt -a "name=acme state=present"

#To ensure that a package is installed to a specific version
$ ansible webservers -m apt -a "name=acme-1.5 state=present"

#To ensure that a package at the latest version
$ ansible webservers -m apt -a "name=acme state=latest"

#To ensure that a package is not installed
$ ansible webservers -m apt -a "name=acme state=absent"
```

## 文件传输

Ansible 可以将文件安全地并行传输到多台机器上。

```
#Transfer a file directly to many servers
$ ansible europe -m copy -a "src=/etc/hosts dest=/tmp/hosts" 
#To change the ownership and permissions on files 
$ ansible webservers -m file -a "dest=/srv/foo/a.txt mode=600"
$ ansible webservers -m file -a "dest=/srv/foo/b.txt mode=600 owner=example group=example"
 #To create directories 
$ ansible webservers -m file -a "dest=/path/to/c mode=755 owner=example group=example state=directory"
 #To delete directories (recursively) and delete files
$ ansible webservers -m file -a "dest=/path/to/c state=absent"
```

## 从源代码管理部署

本节包含告诉您如何直接从 git 部署 web 应用程序的命令。

```
#GitRep:https://foo.example.org/repo.git
#Destination:/src/myapp
$ ansible webservers -m git -a "repo=https://foo.example.org/repo.git dest=/src/myapp version=HEAD"
```

## 管理服务

本节包含管理服务的命令。

```
#To ensure a service is started on all web servers
$ ansible webservers -m service -a "name=httpd state=started"

#To restart a service on all web servers
$ ansible webservers -m service -a "name=httpd state=restarted"

#To ensure a service is stopped
$ ansible webservers -m service -a "name=httpd state=stopped
```

## 剧本

Ansible 中的剧本是以 YAML 格式编写的。它是一种人类可读的数据序列化语言，通常用于配置文件。它还可以用于存储数据的许多应用中。

一个剧本有你需要提到的各种参数，像主机&用户、变量、任务、处理程序、模块和返回值。

## 剧本样本

这是启动 Apache httpd 服务器程序的示例手册。

```
#Every YAML file starts with ---
--- - hosts: webservers
  vars:
    http_port: 80
    max_clients: 200
  remote_user: root 
  tasks:
  - name: ensure apache is at the latest version
    apt: name=httpd state=latest
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

## 写剧本

按照以下步骤写一份行动手册。为了便于理解，命令采用通用格式。

```
#SSH Key Generation
$ ssh key-gen 
#Copy the  generated public SSH key on your hosts
**$ **ssh-copy-id -i root@<IP address of your host> 
# List the IP addresses of your hosts/nodes in your inventory 
$ vi /etc/ansible/hosts

#Ping to ensure a connection has been established
$ ansible -m ping <Name of the Host>

#You do not have to follow the above steps, if you already have host connected to the control machine.

#Create a Playbook
$ vi <name of your file>.yml

#To write the playbook refer to the snapshot [here.](https://www.edureka.co/blog/ansible-tutorial/#hands_on)

#Run the playbook
$ ansible-playbook <name of your file>.yml 
```

## [**下载 Ansible 小抄 Edureka**](https://bit.ly/2qDmieD)

至此，我们结束了**Ansible**Cheat Sheet。查看由 **Edureka** 提供的 DevOps 认证培训，Edureka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 [***DevOps 认证培训***](https://www.edureka.co/devops) 旨在为您提供成为一名成功的 DevOps 工程师所需的知识和技能。