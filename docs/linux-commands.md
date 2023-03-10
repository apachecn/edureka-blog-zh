# 你在生活中会用到的 20 个 Linux 命令

> 原文：<https://www.edureka.co/blog/linux-commands/>

Linux 用户和管理员不能仅仅依靠 GUI 生活。通过学习如何使用您的工具，您可以充分利用 Linux。因此，我们将一系列有用的 ***Linux 命令*** 汇集到这个方便的指南中，无论你选择学习哪个 ***Linux 课程*** ，它都会有所帮助。

因此，我将这些命令分为以下几个部分:

*   [**Linux 基本命令**](#basiccommands)
*   [**处理文件的命令**](#workingwithfiles)
*   [**使用目录的命令**](#workingwithdirectories)
*   [**具有用户权限的命令**](#workingwithuserpermissions)
*   [**处理压缩文件的命令**](#workingwithzippedfiles)
*   [**使用安全外壳进行远程机器访问**](#ssh)

## **Linux 命令:基本命令**

Linux 提供了一个 **CLI** (命令行界面)来与操作系统通信。以下是最基本的 Linux 命令。

### **1。pwd**

该命令显示终端的当前工作目录。

***语法:***

*T2`$ pwd`*

### **![pwd - linux commands - edureka](img/e5fe6461b8b12540df253d4329566d88.png) 2。呼应**

该命令将其参数写入标准输出。

***语法:***

*T2`$ echo "<text>"`*

### **![echo - linux commands - edureka](img/c7cd1dba1dbfc6bf076c1a99df36439d.png) 3。苏**

该命令用于切换到 root 用户，以便使用超级用户权限来执行命令。

***语法:***

`*$ su*`

### **![su - linux commands - edureka](img/e4f90a8d94d7b7afff7209a32151a94c.png) 4。苏<用户名>**

该命令用于切换到一个不同的用户，该用户的名字作为参数传递。

***语法:***

`*$ su <username>*`

### **![su user - linux commands - edureka](img/824a054e97dbca1714ef49eec4740317.png) 5。须藤**

该命令仅执行具有根/超级用户权限的命令。

***语法:***

*T2`$ sudo <command>`*

| **命令** | **解说** |
| ***【sudo user add】<【username】>*** | 添加新用户 |
| ***须藤密码<用户名>*** | 为新用户设置密码 |
| ***【sudo user del】<【username】>*** | 删除用户 |
| ***须藤组添加<组名>*** | 添加新组 |
| ***须藤组<组名>*** | 删除群组 |
| ***须藤 usermod -g <组名> <用户名>*** | 将用户添加到主要组 |

### **6。清除**

该命令用于清除终端屏幕。在这种情况下，内容实际上不会被删除，只是向下滚动。也可以通过按键盘上的 ***Ctrl+L*** 来清空屏幕。

***语法:***

`*$ clear*`

## **Linux 命令:使用文件**

### **7。CP**

这个命令复制文件和目录。复制的文件/目录的副本仍保留在工作目录中。

***语法:***

`*$ cp <flag> {filename} /pathname/*`

![cp - linux commands - edureka](img/1c6c5047a66aaef442b7f5cc4dc43369.png)

| **命令** | **解说** |
| ***CP-I*** | 进入交互模式；CLI 在覆盖文件前询问 |
| ***CP-n*** | 不覆盖文件 |
| ***CP-u*** | 仅当源文件不同于目标文件时更新目标文件 |
| ***cp -R*** | 递归复制，用于复制目录；甚至复制隐藏文件 |
| ***CP-v*** | 啰嗦；打印信息消息 |

### **8。mv**

这个命令将文件和目录从一个目录移动到另一个目录。文件/目录一旦移动，就会从工作目录中删除。

***语法:***

`*$ mv <flag> {filename} /pathname/*`

![mv - linux commands - edureka](img/dc89fadf9616cfa6ee97865afcd19fc8.png)

| **命令** | **解说** |
| ***mv-I*** | 进入交互模式；CLI 在覆盖文件前询问 |
| ***mv-u*** | 仅当源文件不同于目标文件时更新目标文件 |
| ***mv-v*** | 啰嗦；打印源文件和目标文件 |

### **9。RM**

这个命令从一个目录中删除文件。默认情况下，rm 命令不会删除目录。一旦删除，文件的内容就无法恢复。

***语法:***

`*$ rm <flag> {filename} *`

![rm - linux commands - edureka](img/f13f8da345737f4e7d5350f3a0ef549e.png)

| **命令** | **解说** |
| ***RM–r*** | 删除非空目录。 |
| ***RM–RP*** | 删除非空目录，包括父目录和子目录。 |

### 10 .抓稳了

该命令用于在文本文件中搜索特定的字符串/单词。这类似于“Ctrl+F ”,但通过 CLI 执行。

***语法:***

`*$ grep <flag or element_to_search> {filename}*`

![grep - linux commands - edureka](img/6fb82426eef28e17ca5a25f599a79d5c.png)

| **命令** | **解说** |
| *抓到了-* | 返回不区分大小写字符串的结果 |
|  | 返回匹配的字符串及其行号 |
|  | 返回与搜索字符串不匹配的行的结果 |
|  | 返回结果与搜索字符串匹配的行数 |

## **Linux 命令| edu reka**



[//www.youtube.com/embed/G23ef2D-qrY?rel=0&showinfo=0](//www.youtube.com/embed/G23ef2D-qrY?rel=0&showinfo=0)

*这个 Edureka 实时会议为您提供了关于基本 Linux 命令的详细解释，以便您可以开始使用 Linux CLI。*

### **11。猫**

该命令可以读取、修改或连接文本文件。它还显示文件内容。

***语法:***

`*$ cat <flag> {filename}*`

![cat - linux commands - edureka](img/90c0cf0190664f8b50f50e79087683b1.png)

| **命令** | **解说** |
| ***cat-b*** | 用于给非空行添加行号 |
| ***猫-n*** | 用于给所有行添加行号 |
|  | 用于将空行压缩成一行 |
| ***cat–E*** | 在行尾显示$号 |

## **Linux 命令:使用目录**

### **12。lsT3**

该命令列出了当前工作目录中的所有内容。

***语法:***

*T2`$ ls <flag> ![ls - linux commands - edureka](img/90c61a811929742fda9b7ae62aeccc18.png)`*

| **命令** | **解说** |
| ***ls <路径名>*** | 通过在 ls 后指定路径，将显示该路径中的内容 |
| ***ls–l*** | 使用‘l’标志，列出所有内容及其所有者设置，权限&时间戳(长格式) |
| ***ls–a*** | 使用‘a’标志，列出指定目录下的所有隐藏内容 |
| ***ls——作者*** | 使用'–author '标志，列出指定目录中的内容及其所有者 |
| ***ls–S*** | 使用“a”标志，按大小排序并列出指定目录中的所有内容 |
| ***ls *。html*** | 使用' * '标志，仅列出目录中特定格式的内容 |
| ***lS–lS>file . txt*** | 使用“>标志，将 ls 命令的结果复制到文本文件 |

### **13。CD**

该命令用于改变用户的当前工作目录。

***语法:***

*T2`$ cd /pathname/`*

![cd - linux commands - edureka](img/ad936c7e433aa37c49fbae73649b3f89.png)

| **命令** | **解说** |
| ***CD ~*** | 该命令也将目录更改为主目录 |
| ***CD/*** | 将目录更改为根目录 |
| ***光盘..*** | 将目录更改为其父目录 |
| ***CD‘xx YY’*** | 我们用引号指定文件夹名，因为文件夹名中有一个空格 |

### **14。排序**

该命令将搜索结果按字母或数字排序。使用此命令可以对文件、文件内容和目录进行排序。

***语法:***

`*$ sort <flag> {filename}*`

![sort - linux commands - edureka](img/db9cc6be04e3d2d143f53e14e4d95cfe.png)

| **命令** | **解说** |
| ***排序-r*** | 标志以逆序返回结果； |
|  | 该标志不区分大小写排序 |
| ***排序-n*** | 标志按照数字顺序返回结果 |

### **15。mkdir**

该命令用于创建一个新目录。

***语法:***

`*$ mkdir <flag> {directoryname} /pathname/*`

![mkdir - linux commands - edureka](img/623b617c6ee4d91cf7817d222410bfaf.png)

| **命令** | **解说** |
| ***mkdir-p*** | 创建新的父目录和子目录 |
| ***mkdir–p<filename 1>/{ f1，f2，F3 }*** | 用于在新的父目录下创建多个子目录 |

### **16、人民币T3**

该命令用于删除指定的目录。虽然默认情况下，它只能删除空目录，但也可以部署一些标志来删除非空目录。

***语法:***

`*$ rmdir <flag> {directoryname} *`

![rmdir - linux commands - edureka](img/5d677342233e562e09f199ebce9ebb01.png)

| **命令** | **解说** |
| ***rmdir–p*** | 删除父目录和子目录 |
| *是指-PV* | 删除所有父目录和子目录以及详细目录。 |

## **Linux 命令:使用用户权限**

### **17。chmod**

该命令用于改变文件和目录的访问权限。考虑下面的例子。

![chmod script - linux commands - edureka](img/f1e513f6a20a9e2852be794c31234ee1.png)

在尝试运行新创建的名为 ***chmodtest.sh*** 的文件时，出现错误。在使用上述 Linux 命令修改了文件的权限之后，它变成了可执行文件。

***语法:***

`*$ chmod <permissions of user,group,others> {filename}*`

![chmod - linux commands - edureka](img/befa51f035575a03e729c43e3f8d9390.png)与每个数字相关的权限如下。

| **数量** | **读作** | **写** | **执行** |
| **0** | – | – | – |
| **1** | – | – | 是 |
| **2** | – | 是 | – |
| **3** | – | 是 | 是 |
| **4** | 是 | – | – |
| **5** | 是 | – | 是 |
| **6** | 是 | 是 | – |
| **7** | 是 | 是 | 是 |

## **Linux 命令:安装包**

大多数软件的稳定版本已经可以在 Linux 仓库中获得。下面是安装它们的 Linux 命令。

### **18。安装包**

对于 RHEL 系统；

***语法:***

*T2`$ sudo yum install package-name`*

对于基于 Debian 的系统；

***语法:***

*T2`$ sudo apt-get install package-name`*

对于基于 Fedora 的系统；

***语法:***

*T2`$ sudo dnf install package-name`*

## **Linux 命令:处理压缩文件**

当你从网上下载软件包时，下载的文件是以压缩形式出现的。这里有几个在 Linux 中解压和压缩文件的命令。

### **19。焦油**

以下命令用于压缩 ***的文件。tar*** 格式。

***语法:***

*T2`$ tar –cvf tar-filename source-folder-name`*

以下命令用于解压 ***的文件。tar*** 格式。

***语法:***

*T2`$ tar –xvf tar-file-name`*

## **Linux 命令:使用安全外壳** **进行远程机器访问**

### **20。宋承宪**

此命令指的是一种加密网络协议，用于在不安全的网络上安全地运行网络服务。典型的用例包括远程命令行执行，但是任何网络服务都可以用 SSH 来保护。

在从节点上运行的以下命令将对主节点进行远程访问。

***语法:***

*T2`$ ssh <master's ip>`*

在主节点上运行的以下命令将远程访问从节点。

***语法:***

*T2`$ ssh <slave's ip>`*

好了，你知道了。您在日常 IT 生活中肯定会用到的所有 Linux 命令。

*想了解更多 Linux 中的命令？* *Edureka 的 [Linux 课程](https://www.edureka.co/linux-admin)旨在塑造您的 Linux 职业生涯&帮助您运行应用程序，在您的系统和网络上执行所需的功能，创建网络配置，以及维护安全管理。*