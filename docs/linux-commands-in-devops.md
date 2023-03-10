# DevOps 中的 Linux 命令:每个 DevOps 专业人员都必须知道

> 原文：<https://www.edureka.co/blog/linux-commands-in-devops/>

Linux 基础和脚本是 DevOps 专业人员最基本的技能之一。大多数公司的环境都在 Linux 上，许多配置管理工具，如 Puppet、Chef 和 Ansible 也在 Linux 上有它们的主节点。所以在这篇博客中，我将涵盖整个命令行部分，这是 DevOps 中[专业认证项目的重要组成部分。我们将在此讨论的主题如下](https://www.edureka.co/executive-programs/purdue-devops)

所以让我们开始吧，

## **什么是 Linux？**

Linux 是一个开源的、由社区开发的操作系统，适用于计算机、服务器、大型机、移动设备和嵌入式设备。它支持几乎每一个主要的计算机平台，包括 x86，ARM 等，使其成为最广泛支持的操作系统之一。![linux-linuxcommands in devops-Edureka](img/84e620be7e08e738b208ac29d6e439a1.png)

Linux 的设计类似于 UNIX，但它已经发展到可以在从电话到超级计算机的各种硬件上运行。每个基于 Linux 的操作系统都包含 Linux 内核——它管理硬件资源——和一组软件包，它们组成了操作系统的其余部分。

## 【Linux 为什么流行？

Linux 在许多重要方面都不同于其他操作系统。其中一些如下

1.**免费**–首先，或许也是最重要的，Linux 是免费的。不像 windows，你不必花任何钱去下载和使用它。

2.**开源**–Linux 是开源软件。用于创建 Linux 的代码是免费的，公众可以查看、编辑，并且——对于具有适当技能的用户来说——可以做出贡献。

3.**安全**–一旦在系统上安装了 Linux，就不需要使用杀毒软件了！Linux 是一个高度安全的系统。此外，全球发展界一直在寻找增强其安全性的方法。每一次升级都让操作系统变得更加安全和健壮。

4.**稳定性和性能**–Linux 提供了非常高的稳定性，即在短时间内不需要重启。你的 Linux 系统很少变慢或者死机。您可以在 Linux 系统上不受任何干扰地工作。Linux 在各种网络和工作站上提供了显著的高性能。

## **devo PS 中的 Linux 命令**

在这一节中，我们将看看在 DevOps 中工作时最常用的 [Linux 命令](https://www.edureka.co/blog/linux-tutorial/)。

**ls**

这个命令列出了当前工作目录中的所有内容。

***语法:***

`*$ ls <flag>*`

| 命令 | 描述 |
| ***ls <路径名>*** | 通过在 ls 后指定路径，将显示该路径中的内容 |
| ***ls–l*** | 使用“l”标志，列出所有内容及其所有者设置、权限和时间邮票(长格式) |
| ***ls–a*** | 使用“a”标志，列出指定目录中的所有隐藏内容 |

**![](img/8fd06a647779c06a600211fd3dd135bf.png)须藤**

该命令仅执行具有 root/超级用户权限的命令。

***语法:***

`*$ sudo <command>*`

| **命令** | **描述** |
| ***sudo user add<username>*** | 添加新用户 |
| ***须藤密码<用户名>*** | 为新用户设置密码 |
| ***【sudo user del】<【用户名】>*** | 删除用户 |
| ***须藤组添加<组名>*** | 添加新组 |
| ***须藤组德尔<组名>*** | 删除组 |
| ***sudo usermod -g <组名> <用户名>*** | 将用户添加到主要组 |

**![](img/4526253953f5a174e823ad514987286d.png)**

**猫**

该命令可以读取、修改或连接文本文件。它还显示文件内容。

**

***语法:***

`*$ cat <flag> {filename}*`

| 命令 | 描述 |
| ***cat -b*** | 这将向非空行添加行号 |
| ***猫-n*** | 这将向所有行添加行号 |
| ***cat -s*** | 这将空行压缩成一行 |
| ***cat–E*** | 这显示了行尾的$号 |

**![](img/fb284c0c977d08e54500427f21ec507b.png)抓到了**

该命令在文本文件中搜索特定的字符串/单词。这类似于“Ctrl+F ”,但通过 CLI 执行。

***语法:***

`*$ grep <flag or element_to_search> {filename}*`

| 命令 | 描述 |
| ***抓-和*** 抓 | 返回不区分大小写的字符串的结果 |
| ***grep -n*** | 返回匹配的字符串及其行号 |
| ***grep-v*T3** | 返回与搜索字符串不匹配的行的结果 |
|  | 返回结果与搜索字符串匹配的行数 |

**![](img/5add2ffa79fcacbb34ab54f87e948168.png)排序**

此命令按字母顺序或数字顺序对搜索结果进行排序。它还对文件、文件内容和目录进行排序。

***语法:***

`*$ sort <flag> {filename}*`

| 命令 | 描述 |
| ***排序-r*** | 该标志以相反的顺序返回结果； |
|  | 该标志进行不区分大小写的排序 |
| ***排序-n*** | 该标志按照数字顺序返回结果 |

**![](img/1935978d8cb9be35b60e032afce6bf92.png)**

**尾巴**

它是头部命令的补充。tail 命令，顾名思义，打印给定输入的最后 N 个数据。默认情况下，它打印指定文件的最后 10 行。如果您给出了多个文件名，那么每个文件中的数据都以其文件名开头。

***语法:***

`*tail [OPTION]... [FILE]...*`

**tail -n 3 state.txt 或 tail -3 state.txt = > -n 代表行数**

tail +25 state.txt

**-c num:** 打印指定文件的最后“num”字节。

**chown**

操作系统中的不同用户拥有所有权和权限来确保文件的安全，并限制谁可以修改文件的内容。在 Linux 中，有不同的用户使用该系统:

*   每个*用户*都有一些与之相关的属性，比如用户 ID 和主目录。我们可以将用户添加到一个组中，使管理用户的过程更加容易。
*   一个*组*可以有零个或多个用户。指定的用户与“默认组”相关联。它也可以是系统中其他组的成员。

**所有权和权限:**为了保护 Linux 中的文件和目录，我们使用权限来控制用户可以对文件或目录做什么。Linux 使用三种类型的权限:

*   **Read:** 该权限允许用户读取文件和目录，它允许用户读取存储在其中的目录和子目录。
*   **Write:** 该权限允许用户修改和删除文件。此外，它允许用户修改目录的内容(创建、删除和重命名其中的文件)。除非您授予目录的执行权限，否则更改不会影响它们。
*   **执行:**对文件的写权限执行文件。例如，如果我们有一个名为 *sh* 的文件，那么除非我们给它执行权限，否则它不会运行。

**文件权限类型:**

*   **用户:**这种类型的文件权限影响文件的所有者。
*   **组:**这种类型的文件权限影响拥有该文件的组。如果所有者用户在该组中，将应用用户权限，而不是组权限。
*   **其他:这种**类型的文件权限影响系统中的所有其他用户。

**注意:**要查看我们使用的权限:

`*ls -l*`

**chown** 命令用来改变文件的所有者或组。每当你想改变所有权，你可以使用 chown 命令。

**语法:**

`*chown [OPTION]… [OWNER][:[GROUP]] FILE…*`

`*chown [OPTION]… –reference=RFILE FILE…*`

**示例:**要更改文件的所有者:

`*chown owner_name file_name*`

`*chown master file1.txt*`

其中*主*是系统中的另一个用户。假设您是名为 user1 的用户，并且想要将所有权更改为 root(其中您的当前目录是 user1)。在语法前使用“sudo”。

`*sudo chown root file1.txt*`

**chmod**

此命令用于更改文件和目录的访问权限。

语法:

`*chmod <permissions of user,group,others> {filename}*`

4–读 权限

2–写 权限

1–执行 权限

0–没有 权限

**![](img/420aa2757d08a1c7532952bf74a63f15.png)**

**![](img/9523f2b0c4bde3c061b0a9be189653da.png)**

**lsof**

在 Linux/Unix 系统中工作时，可能有几个文件和文件夹正在被使用，其中一些是可见的，一些是不可见的。 **lsof** 命令代表**打开文件列表**。该命令提供了打开的文件列表。基本上，它给出了找出哪个进程打开了哪些文件的信息。它一口气列出了输出控制台中所有打开的文件。

**语法:**

`*$lsof [option][user name]*`

**带示例的选项:**

*   **列出所有打开的文件:**该命令列出系统中任何进程打开的所有文件。

`*~$ lsof*`

*   在这里，您可以看到已打开文件的详细信息。ProcessId、与进程相关联的用户、FD(文件描述符)、文件大小一起给出了关于由命令打开的文件的详细信息、进程 Id、用户、其大小等。

*   **FD** 表示为文件描述符。
*   **cwd** :当前工作目录。
*   **txt:** 文本文件。
*   **mem** :内存文件。
*   **mmap** :内存映射设备。

**列出一个用户打开的所有文件:**一个系统有多个用户，每个用户有不同的需求，因此他们使用文件和设备。要查找特定用户打开的文件列表，此命令非常有用。

*   **语法:**

*   `*lsof -u username*`

除此之外，我们还可以在这里看到文件的类型，它们是:

*   **目录:**目录
*   **REG:** 常规文件
*   **CHR:** 字符特殊文件

**![](img/bc585a59c1bcea26513ae556f628287b.png) ifconfig**

**ifconfig** (接口配置)命令用于配置驻留内核的网络接口。它在引导时用于根据需要设置接口。之后，通常在调试过程中需要的时候或者需要系统调优的时候使用。此外，此命令用于为接口分配 IP 地址和网络掩码，或者启用或禁用给定的接口。

**语法:**

`*ifconfig [...OPTIONS] [INTERFACE]*`

**选项:**

*   **-a :** 该选项用于显示所有可用的接口，即使它们已关闭。

**语法:**

`*ifconfig -a*`

**-s :** 显示简短列表，而不是详细信息。

**语法:**

`*ifconfig -s*`

**![](img/8dd2da61f5cf7787ec770bd74713aa2b.png) id**

Linux 中的 **id 命令**用于找出服务器中当前用户或任何其他用户的用户名和组名以及数字 id(UID 或组 ID)。该命令对于查找下列信息非常有用:

*   用户名和真实用户 id。
*   找出特定用户的 UID。
*   显示与用户关联的 UID 和所有组。
*   列出用户所属的所有组。
*   显示当前用户的安全上下文。

**语法:**

`*id [OPTION]… [USER]*`

**选项:**

*   ***-g*** :只打印有效的组 id。
*   ***-G*** :打印所有组 ID。
*   ***-n*** :打印名字而不是数字。
*   ***-r*** :打印真实的 ID 而不是数字。
*   ***-u*** :只打印有效的用户 ID。
*   ***–帮助*** :显示帮助信息并退出。
*   ***–版本*** :显示版本信息并退出。

**注意:**没有任何选项，它打印每组识别信息，即数字 id。

**例子:**

*   **打印自己的 id，没有任何选项:**

`*id*`

输出显示了当前用户 UID 和 GID 的 ID。

**![](img/466cc3759c080dbcf784e8029498845d.png)**

*   **查找特定用户 id:** 现在假设我们有一个名为 master 的用户，要查找他的 UID，我们将使用以下命令:

`*id -u master*`

**![](img/abadd66cd8754acb7f8313cb3babbe42.png)**

*   **获取特定用户的 GID:** 再次假设要找到 master 的 GID，我们将使用命令:

*T2`id -g master`*

**![](img/709020f618e0ed8c74336d427e9ec970.png)**

*   **知道与用户名关联的 UID 和所有组:**在这种情况下，我们将使用用户“master”来查找 UID 和与其关联的所有组，使用命令:

`*id master*`

**![](img/15c67bb06fd5f926866d3716947d91b2.png)**

*   **找出用户所属的所有组:**显示用户“master”所属的 UID 和所有组:

`*id -G master*`



**切**

剪切命令用于使用列和分隔符提取文件的一部分。如果您想要列出选定列中的所有内容，请在 cut 命令中使用“-c”标志。例如，让我们从 demo1.txt 文件中选择前两列。

`*cut -c1-2 demo1.txt*`

**![](img/4c459f55dc581b15f4df2e8cff499cf9.png)**

**sed**

Sed 是一个文本编辑器，可以以非交互方式执行编辑操作。sed 命令从标准输入或文件中获取输入，以对文件执行编辑操作。Sed 是一个非常强大的工具，您可以使用 sed 进行许多文件操作。我将解释您可能想要对文本文件执行的重要操作。

如果希望通过在文件中搜索来替换文件中的文本，可以使用带有替换“s”标志的 sed 命令来搜索特定的模式并对其进行更改。

例如，让我们将 test.txt 文件中的“mikesh”替换为“Mukesh”

`*sed 's/mikesh/mukesh/' test.txt*`

**![cat1-linux commands in devops-Edureka](img/6c97785647a6f122885545819241fda6.png)**

**差异**

diff 命令用于查找两个文件之间的差异。该命令分析文件并打印不相似的行。假设我们有两个文件 test 和 test1。您可以使用以下命令找到这两个文件之间的差异。

语法–

`*  diff test.txt test1.txt*`

**![cat-linux commands in devops-Edureka](img/47c68d7f1ce39e1db3507a5b611e2339.png)**

**历史**

历史命令用于查看以前执行的命令。这个特性在 Bourne shell 中是不可用的。Bash 和 Korn 支持这个特性，在这个特性中，执行的每个命令都被视为事件，并与一个事件号相关联，如果需要，可以使用这个事件号来调用和更改它们。这些命令保存在历史文件中。在 Bash shell 中**历史**命令显示了整个命令列表。

**语法:**

`*$ history*`

显示之前执行的有限数量的命令，如下所示:

`*$ history 10*`

**![history-linux commands in devops-Edureka](img/94cb0b7be8fb7a3f3da3478b9ac8e4f2.png)**

**dd**

dd 是 Unix 和类 Unix 操作系统的命令行工具，其主要目的是转换和复制文件。

*   在 Unix 上，硬件的设备驱动程序(如硬盘驱动器)和特殊设备文件(如/dev/zero 和/dev/random)就像普通文件一样出现在文件系统中。
*   dd 也可以从这些文件中读取和/或向这些文件中写入，前提是该功能在它们各自的驱动程序中实现
*   因此，dd 可用于备份硬盘引导扇区和获取固定数量的随机数据等任务。
*   dd 程序还可以在复制数据时对数据执行转换，包括字节顺序交换以及 ASCII 和 EBCDIC 文本编码之间的相互转换。

**用法:**DD 的命令行语法与许多其他 Unix 程序不同，它使用语法 *option=value* 作为其命令行选项，而不是更标准的 *-option value* 或*-option = value*格式。默认情况下，dd 从 stdin 读取数据并写入 stdout，但是可以使用 if(输入文件)和 of(输出文件)选项来更改这些数据。

**DD 命令的一些实际例子:**

1.  **备份整个硬盘:**要将一个硬盘的整个副本备份到连接到同一系统的另一个硬盘上，执行 dd 命令，如下所示。在这个 dd 命令示例中，源硬盘的 UNIX 设备名是/dev/hda，目标硬盘的设备名是/dev/hdb。

2.  **#** `*dd if = /dev/sda of = /dev/sdb*`

*   *“if”*表示输入文件，“的*表示输出文件。所以 */dev/sda* 的精确副本将会在 */dev/sdb* 中提供。*
*   如果有任何错误，上述命令将会失败。如果给定参数*“conv =无错误”*，那么如果有读取错误，它将继续复制。
*   输入文件和输出文件应该非常小心地提到。为了以防万一，您在目标中提到了源设备，反之亦然，您可能会丢失所有数据。

**找到**

UNIX 中的 **find** 命令是一个用于遍历文件层次结构的命令行实用程序。它可以用来查找文件和目录，并对它们执行后续操作。它支持按文件、文件夹、名称、创建日期、修改日期、所有者和权限进行搜索。通过使用'-exec '，可以对找到的文件或文件夹执行其他 UNIX 命令。

**语法:**

$ `*find [where to start searching from]*`

`*[expression determines what to find] [-options] [what to find]*`

**选项:**

*   **-exec CMD:** 符合上述条件的被搜索文件，如果命令执行成功，则返回 0 作为其退出状态。
*   **-ok CMD :** 除了首先提示用户之外，它的工作方式与-exec 相同。
*   **-inum N :** 搜索索引节点号为‘N’的文件。
*   **-链接 N :** 搜索具有“N”个链接的文件。

**免费**

在 LINUX 中，有一个命令行实用程序可以实现这一点，那就是 **free** 命令，它显示可用的空闲空间总量，以及系统中使用的内存和交换内存量，还有内核使用的缓冲区。

这就是 free command 为你做的。 **语法:**

`*$free [OPTION]*`

**选项:**是指兼容自由命令的选项。

因为 free 显示了与你的系统相关的内存的细节，所以它的语法不需要传递任何参数，只需要传递你可以根据自己的意愿使用的选项。

**使用自由命令**

您可以将 free 命令用作:`*$free*`

![free-linux commands in devops-Edureka](img/1cea60254971fff683d432180c1695fa.png)

/*免费命令，没有任何

选项显示使用的

和交换的自由空间

以及物理内存 **KB** */

当不使用选项时，free 命令产生如上所示的列输出，其中列:

1.  **total 显示**安装的总内存(MemTotal 和 SwapTotal *e* 存在/proc/meminfo 中)。
2.  **已用显示**已用内存。
3.  **空闲显示**未使用的内存。
4.  **共享显示**tmpfs 使用的内存(Shmen *e* 存在/proc/meminfo 中，不可用时显示 0)。
5.  **buffers 显示**内核缓冲区使用的内存。
6.  **cache 显示**页面缓存和 Slab 使用的内存(缓存和 Slab 在/proc/meminfo 中可用)。
7.  **缓冲区/缓存显示**缓冲区和缓存的总和。

**自由命令选项**

*   **-b，–-bytes:**以字节显示内存。
*   **-k，–-kilo:**以千字节为单位显示内存量(默认)。
*   **-m，–-mega:**以兆为单位显示内存量。
*   **-g，–-giga:**以千兆字节为单位显示内存量

**ssh-keygen**

使用 ssh-keygen 命令生成公钥/私钥对。身份验证密钥允许用户连接到远程系统，而无需提供密码。必须为每个用户单独生成密钥。如果您以 root 用户身份生成密钥对，则只有 root 用户可以使用这些密钥。

以下示例创建 RSA 密钥的公钥和私钥部分:

`*ssh-keygen -t rsa*`

![sshkeygen-linux commands in devops-Edureka](img/b1a53a7a0174245c1ba5db067d1addf2.png)

使用–t 选项指定要创建的密钥类型。对于协议版本 1，可能的值是“ **rsa1** ，对于协议版本 2，可能的值是“ **dsa** ”、“ **ecdsa** ”或“ **rsa** ”。

您可以选择指定一个密码来加密密钥的私有部分。如果您加密您的个人密钥，您必须在每次使用密钥时提供密码。这可以防止攻击者(他可以访问您的私钥，可以冒充您并访问您可以访问的所有计算机)能够这样做。攻击者仍然需要提供密码短语。

**ip**

Linux 中的 **ip** 命令出现在 net-tools 中，用于执行几个网络管理任务。此命令用于显示或操作路由、设备和隧道。此命令用于执行多项任务，如为网络接口分配地址或配置网络接口参数。它可以执行其他几项任务，如配置和修改默认和静态路由、建立 IP 隧道、列出 IP 地址和属性信息、修改接口状态、分配、删除和设置 IP 地址和路由。

**语法:**

`*ip [ OPTIONS ] OBJECT { COMMAND | help }*`

**选项:**

**-address:** 该选项用于显示所有网络设备关联的所有 IP 地址。

`*ip address*`

**![ip2-linux commands in devops-Edureka](img/d0f28c39eaa6fc0c8e17bd9efc093fdd.png)**

**-link:** 用于显示链路层信息，获取当前可用的链路层设备的特性。任何加载了驱动程序的网络设备都可以归类为可用设备。

`*ip link*`

**![ip-linux commands in devops-Edureka](img/9fdc4791d4d54b36d268bcc68f01afb1.png)**

**nslookup**

Nslookup (代表“名称服务器查找”)是一个从 DNS 服务器获取信息的有用命令。它是一个网络管理工具，用于查询域名系统(DNS)以获取域名或 IP 地址映射或任何其他特定的 DNS 记录。它还用于解决与 DNS 相关的问题。

**语法:**

`*nslookup [option]*`

的**选项**nslookup**命令:**

*   `*nslookup google.com:*`

    nslookup 后跟域名将显示该域的“A 记录”(IP 地址)。使用此命令查找域的地址记录。它查询域名服务器并获得详细信息。

**![nslookup-linux commands in devops-Edureka](img/59f1bb7732c2144ba21a70640e806cdb.png)**

**卷曲**

curl 是一个命令行工具，使用任何支持的协议(HTTP、FTP、IMAP、POP3、SCP、SFTP、SMTP、TFTP、TELNET、LDAP 或 FILE)向服务器传输数据或从服务器接收数据。这个命令是由 Libcurl 提供的。这个工具是自动化的首选，因为它被设计为无需用户交互即可工作。它可以一次传输多个文件。

**语法:**

`*curl [options] [URL...]*`

curl 最基本的用法是键入命令，后跟 url。

`*curl https://www.python.org*`

**-o :** 用参数中提供的名称将下载的文件保存在本地机器上。

**语法:**

`*curl -o [file_name] [URL...]*`

**举例:**

`*curl -o hello.zip ftp://speedtest.tele2.net/1MB.zip*`

**tr**

UNIX 中的 tr 命令是一个用于翻译或删除字符的命令行实用程序。它支持一系列转换，包括大写到小写，挤压重复字符，删除特定字符和基本的查找和替换。它可以与 UNIX 管道一起使用，以支持更复杂的翻译。tr 代表翻译。

**语法:**

`*$ tr [flag] SET1 [SET2]*`

**选项**

-c:补充字符串中的字符集，即操作适用于不在给定集合中的字符-d:从输出中删除第一个集合中的字符。 -s:用单次出现的替换集合 1 中列出的重复字符-t:截断集合 1

**样本命令**

1.  **如何将小写转换成大写** 要将小写转换成大写，可以使用 tr 中的预定义集合。

`*![cat-linux commands in devops-Edureka](img/9154b378c8d3b48cc5deca55490d7652.png)*`

**iptables**

**iptables**是一个命令行界面，用于为 Netfilter firewall for IPv4 设置和维护表格，包含在 Linux 内核中。防火墙将数据包与这些表中定义的规则进行匹配，然后对可能的匹配采取指定的操作。

*   *表是*一组链的名称。
*   *链是*规则的集合。
*   *规则*是用于匹配数据包的条件。
*   *目标*是当可能的规则匹配时采取的行动。目标的例子有接受、丢弃、排队。
*   *策略*是在与内置链不匹配的情况下采取的默认动作，可以接受或丢弃。

**语法:**

`*iptables --table TABLE -A/-C/-D... CHAIN rule --jump Target*`

**apt-get**

apt-get 是一个命令行工具，可以帮助处理 Linux 中的包。它的主要任务是从经过验证的源中检索信息和包，以便安装、升级和删除包及其依赖项。这里 APT 代表*高级封装工具*。

**语法:**

`*apt-get [options] command*`

**更新:**该命令用于再次从源文件同步包索引文件。您需要在升级之前执行更新。

`*apt-get update*`

**df，du**

df ( *disk free* )命令报告文件系统正在使用的可用磁盘空间量。du ( *disk usage* )命令报告目录树的大小，包括所有目录树的内容和单个文件的大小。

目的是确保你不会超过 80%的门槛。如果您超过了阈值，是时候进行扩展或清理混乱了，因为资源耗尽了，您的应用程序会出现一些变化无常的行为。

要以人类可读的格式检入:

`*$ sudo df -h*`

![df-linux commands in devops-Edureka](img/f738a2c9356ed7328b7afa75cf4df47a.png)

但是在大多数情况下，您希望检查系统的哪个部分消耗了大量磁盘空间。使用以下命令:

`*$ sudo du -h -d 1 /var/*`

**![du-linux commands in devops-Edureka](img/fdca55e3879737bd4e05cab6562b58af.png)**

**htop**

Linux 系统中的 htop 命令是一个命令行实用程序，允许用户实时交互地监控系统的重要资源或服务器进程。这个是一个比最高统帅部更新的程序，它提供了比最高统帅部更多的改进。它支持鼠标操作，在其输出中使用颜色，并给出关于处理器、内存和交换空间使用情况的可视指示。htop 还打印进程的完整命令行，并允许用户分别垂直和水平滚动进程和命令行。

**语法—**

`*htop <flag>*`

*   **-d–延迟:**用于显示更新之间的延迟，以十分之一秒为单位。
*   **-C–无色–无色**:以单色模式启动 htop。
*   **-h–帮助:**用于显示帮助信息并退出。
*   **-u–user = USERNAME:**用于仅显示给定用户的进程。

**ps**

Linux 中的每个进程都有一个惟一的 ID，可以使用命令 ps 来查看。

*   `*$ sudo ps aux*`
*   **a** =显示所有用户的流程
*   **u** =显示流程的用户/所有者
*   **x** =还显示未连接到终端的进程

**![ps-linux commands in devops-Edureka](img/5d0a24c50a0c0f21d70bce08a8538bda.png)**

**杀死**

*kill* 命令在 Linux 中(位于/bin/kill)，是一个内置命令，用来手动终止进程。该命令向一个进程发送一个信号，终止该进程。如果用户没有指定任何要与 kill 命令一起发送的信号，则默认的*术语*信号被发送，从而终止该过程。

`*kill -l*` **:** 要显示所有可用的信号你可以使用下面的命令选项:

**语法:** `*$kill -l*`

![kill-linux commands in devops-Edureka](img/822ac565c86f46d9fbe11ae3c7d8b7d7.png)

*   负 PID 值用于指示进程组 ID。如果您传递一个进程组 ID，那么该组中的所有进程都将收到该信号。
*   PID 非常特殊，因为它指示除 kill 和 init 之外的所有进程，而 kill 和 init 是系统中所有进程的父进程。
*   要显示正在运行的进程列表，使用命令 *ps* ，这将显示正在运行的进程及其 PID 号。为了指定哪个进程应该接收终止信号，我们需要提供 PID。

**语法:**

`*$ps*`

**kill pid:** 展示如何使用带有 *kill* 命令的 *PID* 。

**语法:**

`*$kill pid*`

**telnet**

Telnet 有助于-

*   连接到远程 Linux 计算机
*   远程运行程序并进行管理

句法

*   telnet 主机名= " "或= " "
*   示例:
*   `*telnet localhost*`

## **外壳脚本**

### **壳是什么？**

一个操作系统包含许多组件，但是它的两个主要组件是内核和外壳。

你可以把内核看作是计算机的核心。它使得硬件和软件之间的通信成为可能。内核是操作系统最里面的部分，而外壳是最外面的部分。

Linux 操作系统中的 shell 以命令的形式接受用户的输入，对其进行处理，然后给出输出。它作为一个界面，用户通过它来处理程序、命令和脚本。终端访问 shell 并运行命令。

当终端运行时，Shell 会发出一个命令提示符(通常是$)，在这里可以键入您的输入，之后，当您按下 Enter 键时，终端会执行该命令。然后，终端会显示命令的输出。

外壳包裹着操作系统脆弱的内部，保护它免受意外损坏。因此名字叫壳牌。

Linux 中有两个主要的 shells:

1.  **Bourne Shell**:这个 Shell 的提示是$及其派生如下:

*   POSIX shell 也称为 sh
*   光辉国际也被称为上海
*   Bourne Again SHell 也被称为 bash(最流行的)

2.**C shell:**%

*   C shell 也称为 csh
*   托普斯-C 壳牌公司也被称为 tcsh

### **什么是 Shell 脚本？**

外壳脚本是为外壳编写一系列可以执行的命令。它可以将冗长和重复的命令序列合并成一个简单的脚本。您可以存储这个脚本，并随时执行它。这大大减少了最终用户所需的工作量。

**以下是创建 Shell 脚本的步骤—**

*   使用文本编辑器(如 vi 或任何其他编辑器)创建文件。用扩展名命名脚本文件。嘘
*   以#开始脚本！/bin/sh
*   写点代码。
*   将脚本文件另存为 filename.sh
*   用于执行脚本类型 bash filename.sh

"#!"是一个名为 shebang 的操作符，它将脚本指向解释器的位置。所以，如果我们用“#！/bin/sh "脚本指向 bourne-shell。

我们现在将使用像 vi 这样的编辑器创建一个文件，并用。sh 扩展。复制下面的程序，该程序将用户输入的数字相加并打印出来。然后使用 bash filename.sh 命令运行这个程序。

`#!/bin/sh`

`echo "Enter a number"``read Num`

`# store the sum of``# digits`

`# use while loop to``# caclulate the sum``# of all digits``while [ $Num -gt 0 ]``do``k=$(( $Num % 10 ))`

`# get next digit`

`# calculate sum of``# digit``s=$(( $s + $k ))`

`done`

## **Git 命令**

### **Git 是什么？**

![Git architecture-Linux Commands in DevOps-Edureka](img/1d093ef8cd8a51394620c237e4c1f657.png)

Git 是一个免费的开源分布式版本控制系统。这个工具可以快速有效地处理从小到大的项目。Linus Torvalds 在 2005 年创建了它来开发 Linux 内核。Git 拥有大多数团队和个人开发人员需要的功能、性能、安全性和灵活性。

![Git And Git Work Flows -Linux Commands in DevOps - Edureka](img/c21fcc5c6f2b7992259afade8ad52fd2.png)

像 Git 这样的工具支持开发和操作团队之间的交流。当您开发一个有大量协作者的大型项目时，在项目中进行更改时，协作者之间的交流非常重要。Git 中的 Commit 消息在团队交流中起着非常重要的作用。我们都部署在版本控制系统中，如 Git。为了在 DevOps 中取得成功，您需要在版本控制中拥有所有的通信。因此，Git 在 DevOps 的成功中起着至关重要的作用。

### **Git 命令**

**去启动**

**用法**:git init[存储库名称]

该命令创建一个新的存储库。

**![init-linux commands in devops-Edureka](img/e0778b2499a2541f8cbca5f06a816cf7.png) git 配置**

**用法** : `*git config --global user.name “[name]”*`

**用法** : `*git config --global user.email “[email address]”*`

该命令分别设置作者姓名和电子邮件地址。这是关于提交的有用信息。

**![config-linux commands in devops-Edureka](img/15f176417fd39c484e641d09a7215cc3.png)**

**git 克隆**

**用法** : `* git clone [url]*`

此命令允许您从现有 URL 获取存储库的副本。

**![clone-linux commands in devops-Edureka](img/93e60af066c5015eb0090d7eb153733b.png)**

**去添加**

**用法:** `*git add [file]*`

此命令将文件添加到临时区域。

**![add1-linux commands in devops-Edureka](img/f3b7f20bb2a940e9ed623e00cf82a41e.png)用法:** `*git add **`

此命令将一个或多个添加到临时区域。

**![add2-linux commands in devops-Edureka](img/b51383ab6a874b6644ddffd894678180.png)**

**去委员会**

**用法:** `*git commit -m “[ Type in the commit message]”*`

该命令在版本历史记录中永久记录或快照文件。

**![commit-linuxcommandsindevops-Edureka](img/e9f98dd398f7566f1d38c70b784d8b77.png)用法:** `*git commit -a*`

该命令提交您使用 git add 命令添加的任何文件，并且还提交您从那时起更改的任何文件。

**![commit-linuxcommandsindevops-Edureka](img/caa11995df1a1d4a70adabbea7712e3b.png)**

**git status**

**用法:** `*git status*`

git status命令显示工作目录和暂存区的状态。这个命令可以让您看到暂存中的变更，那些没有被暂存和没有被 Git 跟踪的变更。

**![status-linuxcommandsindevops-Edureka](img/aff1e04b0848c02ea27781d6c02aa70c.png)**

**去表演**

**用法:** `*git show [commit]*`

此命令显示指定提交的元数据和内容更改。

**![show-linuxcommandsindevops-Edureka](img/f284913bfd12ada59d98398bc44929df.png)**

**![show2-linuxcommandsindevops-Edureka](img/d619c9b838a67e708c273cc2cd11aa08.png)**

**git rm**

**用法:** `*git rm [file]*`

此命令从您的工作目录中删除文件，并分阶段删除。

**![rm-linuxcommandsindevops-Edureka](img/a9d2244fa596a6be400951ee8627d863.png)**

**git remote**

**用法:** `*git remote add [variable name] [Remote Server Link]*`

该命令将您的本地存储库连接到远程服务器。

**![remote-linuxcommandsindevops-Edureka](img/1cc03ba12a209aab47fd9ffad77c2173.png)**

**去推**

**用法:** `*git push [variable name] master*`

该命令将主分支提交的更改发送到您的远程存储库。

**![push-linuxcommandsindevops-Edureka](img/fa8ec076cb2f5ef1e01ad2f682a8a236.png)**

**用法:** `*git push [variable name] [branch]*`

这个命令将分支提交发送到您的远程存储库。

**用法:** `*git push –all [variable name]*`

该命令将所有分支推送到您的远程存储库。

**用法:** `*git push [variable name] :[branch name]*`

此命令删除远程存储库上的分支。

**git pull**

**用法:** `*git pull [Repository Link]*`

该命令获取远程服务器上的更改并将其合并到您的工作目录中。

**![pull-linuxcommandsindevops-Edureka](img/da41abb6d75b790c7644deea01cc1cd5.png)**

**去分支**

**用法:** `* git branch*`

该命令列出了当前存储库中的所有本地分支。

**![branch2-linux commands in devops-Edureka](img/536b7e964bb6297b098b5c3b0be6eb2c.png)用法:** `*git branch [branch name]*`

该命令创建一个新分支。

**![branch1-linux commands in devops-Edureka](img/52136b28903c55563f3b00670f33a5e5.png)用法:** `*git branch -d [branch name]*`

该命令删除特征分支。

**![checkout3-linux commands in devops-Edureka](img/83e0d9ff4310bf0339c805220d702a01.png) git checkout**

**用法:** `*git checkout [branch name]*`

该命令允许您从一个分支切换到另一个分支。

**![checkout2-linux commands in devops-Edureka](img/dd895d424fe7e05565f56752c38d6607.png)用法:** `* git checkout -b [branch name]*`

该命令创建一个新分支，并切换到该分支。

**![checkout-linux commands in devops-Edureka](img/9d6b1582d832684635a0f4e963e58bb0.png)去髓**

**用法:** `*git merge [branch name]*`

该命令将指定分支的历史记录合并到当前分支中。

**![merge-linux commands in devops-Edureka](img/1ca39974179ca42da7efc0f9ed7accdf.png) git rebase**

**用法:** `*git rebase [branch name]*`

git rebase master–这个命令将把我们所有的工作从当前分支转移到主节点。

至此，我们结束了关于 DevOps 中 Linux 命令的博客。我试图在这里涵盖尽可能多的命令。这个博客一定会帮助你开始你的 DevOps 之旅。

现在您已经了解了 DevOps 中的 Linux 命令，请查看 Edureka 提供的 [DevOps 培训课程](https://www.edureka.co/devops-certification-training)，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka [DevOps 工程师认证](https://www.edureka.co/masters-program/devops-engineer-training)培训课程帮助学习者了解什么是 DevOps，并获得各种 DevOps 流程和工具的专业知识，例如 Puppet、Jenkins、Nagios、Ansible、Chef、Saltstack 和 GIT，用于自动化 SDLC 中的多个步骤。

有问题要问我们吗？请在评论区提及，我们会尽快回复您