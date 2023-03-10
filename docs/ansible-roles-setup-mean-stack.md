# 可变角色——解开剧本的终极方法

> 原文：<https://www.edureka.co/blog/ansible-roles-setup-mean-stack>

Ansible 允许我们自动进行系统的配置管理，并根据需要添加任意数量的客户端。你想过这会变得多复杂吗？你有没有想过剧本会有多长，会有多混乱？Ansible 是如何让它看起来轻而易举的？它使用了可变角色的概念，这也是我们将在这篇博客中讨论的内容。

涵盖的主题:

*   [岗位职责介绍](#Introduction-To-Ansible-Roles)
*   [可重用角色](#Reusability-Of-Ansible-Roles)
*   [角色目录结构](#Roles-Directory-Structure)
*   [演示:使用可变角色](#Demo) 安装平均堆栈

*如果你想掌握 DevOps，[这门](https://www.edureka.co/devops?qId=15528fae0b7b58fb1a3c599f1cbe9c02&index_name=prod_search_results_courses&objId=776&objPos=1)课程将是你的首选。*

## **岗位职责介绍**

职责是一个处理想法而不是事件的概念。它基本上是用于组织剧本的另一个抽象层次。它们为变量、任务、模板、文件和模块的独立和可重用集合提供了一个框架，这些集合可以自动加载到剧本中。剧本是角色的集合。每个角色都有特定的功能。

让我用一个例子来解释一下。假设您希望您的行动手册在 5 个不同的系统上执行 10 个不同的任务，您会使用一个行动手册吗？不，使用单一的剧本会使它变得混乱和容易出错。相反，您可以创建 10 个不同的角色，每个角色将执行一项任务。然后，你需要做的就是，在剧本中提到角色的名字来称呼他们。在这篇博客中，你将进一步了解如何使用角色。

## **可重用角色**

可互换的角色是相互独立的。一个角色的执行不依赖于其他角色，因此它们可以被重用。您甚至可以根据自己的需求修改和个性化这些角色。这减少了我们每次需要时重写整个代码段的任务，从而简化了我们的工作。

让我们回到上一个例子。您已经编写了 10 个角色，现在您需要将其中的 5 个用于另一组配置。你会把整个剧本重新写一遍吗？不，你只是在新剧本中重复使用这 5 个角色。如果需要的话，你也可以做一些修改，但最终还是会节省你很多时间。

假设你需要写一个剧本来设置灯组。您必须创建 4 个角色，分别用于创建 Linux、Apache、MongoDB 和 PHP。将来，如果你想要另外一个剧本来设置 LAMP stack 和 WordPress，你会再次为 LAMP stack 和 WordPress 创建新的角色吗？不要！你可以简单地重用旧的角色(用于 LAMP stack ),另外为 WordPress 创建一个新的角色。

## **角色目录结构**

使用可转换的角色，期望文件处于特定的文件结构中。使用角色最令人困惑的部分是理解文件层次结构。Ansible 提供了一个名为 Ansible Galaxy 的功能，可以帮助你玩角色。我们已经知道我们的 Ansible 在 Ubuntu 上的位置(/etc/ansible)。有没有见过/etc/ansible 下有一个叫 roles 的目录？该目录的存在正是出于这个原因。您可以在这个目录中创建不同的角色。

该目录将如下所示:

![Tree - Ansible Roles - Edureka](img/ee118b1dc0384024ffdc50eb650451ff.png)

你可以在/etc/ansible/roles 中使用 **ansible-galaxy** init 命令创建一个角色。

`$ sudo ansible-galaxy init <role-name>`

![Ansible Galaxy init - Ansible Roles - Edureka](img/70e8a6cd5b56c28cd0093600b875e5fa.png)

你会看到其他的角色目录也已经被创建了。

![Inside Roles - Ansible Roles - Edureka](img/605080839982ef27bfaaf6186055ec83.png)

这些目录是任务、处理程序、默认值、变量、文件、模板、元数据和自述文件。 md 文件。

**任务**–包含角色要执行的任务的主要列表。它包含特定角色的 main.yml 文件。

**处理程序**–包含该角色甚至该角色之外的任何地方可能使用的处理程序。

**默认值**–包含该角色将要使用的默认变量。

**变量**–该目录包含角色将要使用的其他变量。这些变量可以在您的剧本中定义，但是在本节中定义它们是一个好习惯。

**文件**–包含该角色可以部署的文件。它包含在配置角色时需要发送到主机的文件。

**元**–定义该角色的元数据。基本上，它包含建立角色依赖关系的文件。

每个**任务**目录必须由一个 **main.yml** 文件组成，该文件中写有特定角色的实际代码。

![Inside Tasks - Ansible Roles - Edureka](img/9c52b8cf84b689f1df9160e8cf8b7643.png)

现在让我们通过安装 MEAN Stack 的演示来了解工作或角色。

## **演示:使用可变角色** 安装平均堆栈

我将通过执行一个剧本来演示如何使用可转换的角色来安装 MEAN Stack。我们将有三个角色:1)安装先决条件，2)安装 MongoDB，3)安装 NodeJS。我假设你已经[安装了 Ansible 并在 Ubuntu](https://www.edureka.co/blog/ansible-provisioning-setting-up-lamp-stack) 上建立了服务器-客户端连接。让我们开始扮演可互换的角色。

**第 1 步**–导航到/etc/ansible/roles 目录，为先决条件、MongoDB 和 NodeJS 创建角色。

```

$ cd /etc/ansible/roles
$ sudo ansible-galaxy init prerequisites
$ sudo ansible-galaxy init mongodb
$ sudo ansible-galaxy init nodejs

```

您现在应该会在“角色”目录中看到三个角色。

![All Roles - Ansible Roles - Edureka](img/5c92de00f93f8ec336d4e0bd5d7b9e7f.png)

**第二步**–为安装 Git 的先决条件编写 main.yml。

```

$ cd prerequisites/tasks/main.yml

---
- name: Install git
  apt:
     name: git
     state: present
     update_cache: yes

```

**第三步**——为 MongoDB 角色编写 main . yml

```

$ cd /mongodb/tasks/main.yml
---
- name: MongoDB - Import public key
  apt_key:
    keyserver: hkp://keyserver.ubuntu.com:80
    id: EA312927

- name: MongoDB - Add repository
  apt_repository:
    filename: '/etc/apt/sources.list.d/mongodb-org-3.2.list'
    repo: 'deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse'
  state: present
  update_cache: yes

- name: MongoDB - Install MongoDB
  apt:
    name: mongodb-org
    state: present
    update_cache: yes

- name: Start mongod
  shell: "mongod &"

```

**第四步**——为 nodejs 角色写 main.yml

```

$ cd nodejs/tasks/main.yml

---
- name: Node.js - Get script
  get_url:
    url: "http://deb.nodesource.com/setup_6.x"
    dest: "{{ var_node }}/nodejs.sh"

- name: Node.js - Set execution permission to script
  file:
    path: "{{ var_node }}/nodejs.sh"
    mode: "u+x"

- name: Node.js - Execute installation script
  shell: "{{ var_node }}/nodejs.sh"

- name: Node.js - Remove installation script
  file:
    path: "{{ var_node}}/nodejs.sh"
    state: absent

- name: Node.js - Install Node.js
  apt: name={{ item }} state=present update_cache=yes
  with_items:
    - build-essential
    - nodejs

- name: Node.js - Install bower and gulp globally
  npm: name={{ item }} state=present global=yes
  with_items:
    - bower
    - gulp

```

**第五步**——写下你的主要剧本

```

$ cd /etc/ansible/mean.yml

---

- hosts: nodes
  remote_user: ansible
  become: yes
  become_method: sudo
  vars:
    #variable needed during node installation
    var_node: /tmp
  roles:
      - prerequisites
      - mongodb
      - nodejs

```

现在我们已经定义了安装必备组件的角色，M ongoDB 和 NodeJs ，让我们来部署它们。使用以下命令执行行动手册。

`$ sudo ansible-playbook /etc/ansible/mean.yml -K`

![Playbook Execution - Ansible Roles - Edureka](img/0225c9a21707bae69cca9d052ee7e199.png)

如您所见，所有的任务都已经执行，并且它们的状态已经改变。这意味着行动手册的更改已经应用到您的服务器和主机。设置均值堆栈只是一个例子。您可以使用 Ansible 角色设置任何事情。

这就把我们带到了 Ansible Roles 博客的结尾。如果你觉得这篇文章有帮助，去看看由 Edureka 提供的 [DevOps 课程](https://www.edureka.co/devops?qId=15528fae0b7b58fb1a3c599f1cbe9c02&index_name=prod_search_results_courses&objId=776&objPos=1)。它涵盖了让 It 行业变得更好的所有工具。

*有问题吗？请将它发布在 [Edureka 社区](https://edureka.co/community)上，我们将会回复您。*