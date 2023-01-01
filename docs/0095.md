# 9 个简单步骤的 Informatica 安装

> 原文：<https://www.edureka.co/blog/informatica-installation/>

Informatica 提供市场领先的数据集成平台。经过近 500，000 种平台和应用程序组合的测试，数据集成平台可以与尽可能多的不同标准、系统和应用程序进行互操作。这种不偏不倚的普遍观点使 Informatica 成为当今市场上独一无二的数据集成平台领导者和 [***Informatica 认证***](https://www.edureka.co/informatica) 最引人入胜的技能之一。在这篇博客中，我将帮助您安装和配置 Informatica 的服务。

让我们从在您的系统上设置 Oracle 数据库作为我们的主数据库开始。如果您已经安装并配置了 Oracle 数据库和 SQL Developer，您可以直接进行 [Informatica 安装。](#info)

## **Oracle 数据库安装**

要开始安装 Oracle，首先从下面的链接下载安装 zip 文件。

**第一步** : 从下面的链接下载Oracle Database Express Edition(我是在 Windows 64 位操作系统上安装的，所以我选择了 windows x64):

*   [www . Oracle . com/tech network/database/database-technologies/express-edition/downloads/index . html](http://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/index.html)

**第二步** :文件下载完成后，解压文件:

![downloaded setup file-Informatica Installation](img/5b7fddb9732ad1a4685c2354b3aba468.png)

![extracting-the-file-Informatica Installation](img/7de6d55d344788f2dbc7aabfab4f31f9.png)

**第三步** :解压文件后你会得到 **DISK1** 文件夹，打开文件夹。

![folder-open-Informatica Installation](img/7c702ab14a9386ca225c5df213380a7f.png)

**第四步**:双击**设置**开始安装:

![launch-setup-Informatica Installation](img/5eba0fee7d322fd90e454114a2851a07.png)

点击 **下一个** 。

![oracle-setup-1- Informatica Installation](img/2bdebca518c02ac6c2787378f1229278.png)

**第五步**:接受条款，点击 **下一步** 。

![oracle-setup-2- Informatica Installation](img/76c38e53ef3f267d3fc0c76fc7a4a26c.png)

点击 **下一步。**

![oracle-setup-3- Informatica Installation](img/68dc7d7a4171770ffe44ee7632fee8a1.png)

**第六步**:指定数据库密码。

*   输入密码:**Oracle 123**

**注意:** 如果您正在选择自己的密码，请做好记录，我们将再次需要此密码。



![oracle-setup-4- Informatica Installation](img/119d89214c711888d48d9400941a967f.png)

**注意:**Oracle 监听的默认端口是 **1521。**

点击 **安装** 。

![oracle-setup-5- Informatica Installation](img/7ede0a22b4c8b367dd787529df95c223.png)

这可能需要一段时间。

![oracle-setup-6- Informatica Installation- Edureka](img/5bfb79c7ba2a64d7755b5bd324c40c37.png)

**第七步**:点击完成，完成安装。

![oracle-setup-6- Informatica Installation- Edureka](img/ed8148505d1c41598203e62e6f85a7ad.png)

## **Oracle SQL Developer 的配置**

在开始安装 SQL developer 之前，请确保您已经启动了数据库。如果数据库没有启动，SQL developer 和数据库之间的连接将会失败。

启动数据库:进入**开始**->-**Oracle Database 11g Express Edition**->点击**启动数据库。**

![Starting databasel- Informatica Installation- Edureka](img/8accce91b7c6a71f4ebcb8eabb889e3b.png)

现在我们可以开始配置 Oracle SQL Developer:

**第一步**:从下载 Oracle SQL Developer zip 文件开始。我建议您使用 SQL Developer 3.2.20，因为更高版本要求您安装 Java 1.8 并手动设置路径。您可以从下面的链接下载该文件:

*   [http://www . Oracle . com/tech network/developer-tools/SQL-developer/downloads/index . html](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html)

**第二步**:下载完成后，解压下载的文件。

![sql-developer-file- Informatica Installation- Edureka](img/30aebd0333877addc8afbf1574d48e7e.png)

![extract-sql-developersql- Informatica Installation- Edureka](img/e83e69c1fe6b2c526bb303bd98ff8e08.png)

**第三步**:提取完成后，会得到 SQL developer**–3 . 2 . 20 . 09 . 87**文件夹。进入 sqldeveloper**–3 . 2 . 20 . 09 . 87**文件夹，双击点击 SQL developer 开始配置。![sql-folderl- Informatica Installation- Edureka](img/a6682a8fdc397dc59f98f68e6afeff3d.png)

![sqldeveloper-launchingl- Informatica -Installation- Edureka](img/c871f2a739980fd4401ebf4d9402c4a6.png)

**注意:** 如果我们使用 SQL Developer 4.0 或更高版本，我们需要安装 JDK 1.8，并且我们必须手动配置完整路径，因此我们将建议使用 3.2 版本。

**第四步**:初始化完成后，你会进入下面的主屏幕。不要选择任何配置文件类型关联，直接单击取消。

![sql-developer-homepagel- Informatica Installation- Edureka](img/fc8ca859681d7291dda0e31d5eb82596.png)

**第五步**:要建立连接，首先右键点击连接，然后点击**新建连接**。

![new connection- Informatica Installation- Edureka](img/bb539a224f66259f716b0da4ce1f49f8.png)

**第六步**:我们现在将连接到 Oracle 数据库。输入如下详细信息:

*   连接名称: **ORACLEXE**
*   用户名:**sys**
*   密码: **oracle123** (这里我们要指定和数据库安装时设置的相同的密码)
*   角色: **SYSDBA**

点击 **保存**->--**测试**->--**连接**-

![new-connection- Informatica Installation- Edureka](img/7d73c7d8f5a776d8d6d89ee39d2ab559.png)

单击“连接”后，我们可以看到该连接已添加到列表中。

![oracle-connection-sucessful - Informatica Installation- Edureka](img/9392062ab0f84b144ad2b7547a882457.png)

**第 7 步**:现在点击 **ORACLEXE** 旁边的加号图标，得到下面的画面:

![ocraclexe- Informatica Installation- Edureka](img/93b8f659d49afc4262fef9337906f134.png)

**第八步**:现在我们要创建 2 个用户。

1.  INFA_DOM(为域名)
2.  INFA 代表(存储库)

右键单击其他用户创建用户。

![adding-user-1 - Informatica Installation- Edureka](img/e90227f5eba2b912e6749aed534dcd4d.png)

点击 **创建用户** 。

![creating-user - Informatica Installation- Edureka](img/a32e03dfdec621f222a8273a4f15e880.png)

**第 9 步**:我们现在将为域创建用户。输入以下用户详细信息:

*   用户名:**inb _ DOM**
*   密码: **INFA_DOM**
*   默认表空间: **用户**
*   临时表空间: **临时**

![dom-user-details- Informatica Installation- Edureka](img/335eaa9055dfdcd9153f3a9d4ac71c6b.png)

**注意**:指定所有细节后不要点击应用

**第十步:**点击角色选项卡，定义用户的角色。

![Roles - Informatica Installation- Edureka](img/1e479e460c1babf42a6426a3dfba2f1f.png)

**第十一步**:我们要为分配域用户完全权限

*   DBA
*   连接
*   资源

![DBA- Connect - Informatica Installation- Edureka](img/9d13530a40acbb26ed555d8c7249e4f4.png)

向下滚动以查找资源角色:

![Resources- Informatica Installation- Edureka](img/a8736a740ddee3e648e4fba34352b9a5.png)

**第 12 步**:现在点击 Quotas 选项卡分配表空间区域:

![Quotas - Informatica Installation- Edureka](img/aa233871b99b945c8b185436bd7e04f0.png)

**第十三步**:选择用户，分配无限选项。点击应用

![assigning-quotas](img/c268a9943b9f0c1dc30e60bb26d9ff0d.png)

点击 **关闭** 。

![user creation close- Informatica Installation- Edureka](img/a6af9074a88bad29da18f247f852666a.png)

用户 **INFA_DOM** 已成功创建。

**第 14 步**:现在我们将点击 Connection 和 New Connection 连接到域用户。

![dom-connection-1- Informatica Installation- Edureka](img/c039b8fa615a28c94e0137b2152471d0.png)

**第十五步**:输入以下用户详细信息:

*   连接名称: **INFA_DOM**
*   用户名:**INFA _ DOM**
*   密码: **INFA_DOM**
*   连接类型: **基本**
*   角色: **默认**

点击 **保存**->--**测试**->--**连接**-

![dom-user- Informatica Installation- Edureka](img/2f5fcaa80e5fbbaf9ee22b68803f626e.png)

单击“连接”后，我们可以看到用户已添加到列表中

![connection successful- Informatica Installation- Edureka](img/2552e12b261f784f56933aa6bccb2125.png)

**步骤 16** :我们现在将以类似的方式添加存储库用户。点击其他用户并在 **ORACLEXE 下添加用户。**

![adding-user-2r- Informatica Installation- Edureka](img/1acc57dcdc7ae71aec64ec3327eb3cc5.png)

**第 17 步**:输入仓库用户的以下详细信息:

用户名: **INFA 代表**

密码:**INFA _ 代表**

默认表空间:**用户**

临时表空间:**TEMP**

**![rep-user-details- Informatica Installation- Edureka](img/66bbc1793c8c8d749d0b679eceee31ce.png)**

**第 18 步**:作为域用户， 为存储库用户提供

*   DBA
*   连接
*   资源

![DBA- Connect - Informatica Installation- Edureka](img/9d13530a40acbb26ed555d8c7249e4f4.png)

**第 19 步**:点击配额选项卡，为用户选择无限制选项，如下图:

![finishing-rep-access](img/7bd7b8f4693348d77e1c2075ba937167.png)

点击 **关闭。**

![Finish- rep-Informatica Installation- Edureka](img/68cf7ae3977cea71880f7bf029ebc484.png)

用户**【INFA _ REO】**已成功创建。

**第 20 步**:现在我们将点击 Connection 和 New Connection 来连接到存储库用户。

![dom-connection-1- Informatica Installation- Edureka](img/c039b8fa615a28c94e0137b2152471d0.png)

**步骤 21** :输入以下用户详细信息:

*   连接名称:INFA 代表
*   用户名:INFA 代表
*   密码:INFA 代表
*   连接类型:基本角色:默认

点击 **保存**->--**测试**->--**连接**-

![rep-user- Informatica Installation- Edureka](img/c3e8703b27d6bcb7313137325b971772.png)

现在你可以看到新用户**INFA _ 代表** 已经创建并成功连接。

![SQl Final- Informatica Installation- Edureka](img/2df2658dd5fb727c7fe2735c306cf0ad.png)

现在我们已经完成了 Oracle 和 SQL 的安装，现在我们必须下载 Informatica 工具并安装它们。

## **信息化安装**

Informatica 安装将遵循以下步骤:

1.  [下载安装包。](#step1)
2.  [拆包安装。](#step2)
3.  [Informatica PowerCenter 安装前检查。](#step3)
4.  [安装 Informatica PowerCenter。](#step4)
5.  [域配置。](#step5)
6.  [配置存储库服务。](#step6)
7.  [配置集成服务。](#step7)
8.  [客户端安装。](#step8)
9.  [PowerCenter Designer 配置。](#step9)

现在开始安装过程:

## **步骤 1:下载安装包**

从 Informatica 安装开始，我们先下载 oracle 提供的 Informatica PoweCenter 的免费版本。

**步骤 1.1:** 使用下面的链接 下载 Informatica 9.6.1

*   [【https://edelivery.oracle.com/】](https://edelivery.oracle.com/)

**步骤 1.2:** 登录您的账户，如果您没有 Oracle 账户使用 **新用户** 选项创建账户。

![Oracle-home-page - Informatica installation - Edureka](img/928c62a543c0bd8963fac82ce047b64a.png)

**                                           Fig: Oracle Home page**



![Oracle-signin - Informatica installation - Edureka](img/ad1f1b1502601ecdd8534c4aabc88213.png)

**                                          Fig: Oracle Sign In page**



**步骤 1.3:在搜索框中输入****power center**。

**步骤 1.4:** 选择**Oracle Informatica power center 和 PowerConnect 适配器**。

**步骤 1.5:** 选择平台(我在一个 **Windows 64** 位 OS 上安装，所以我选择了 Windows 64)。

![Product-selection- Informatica installation - Edureka](img/1ae4ab85b87b86b34ed8a2cb1ae9ecde.png)

**                                 Fig: Product Selection in Oracle Cloud**



**步骤 1.6:** 点击**继续。**

![Download-queue- Informatica installation - Edureka](img/0fb297c214f113e0eca11fe91552e4ba.png)

**                                             Fig: Product Selection in Oracle Cloud**



**步骤 1.7:** 接受甲骨文许可。

![Oracle Licence- Informatica installation - Edureka](img/a83d5691b299e2d49febf6ede708dacf.png)

**                                  Fig: Product Selection in Oracle Cloud**



**步骤 1.8:** 现在如下图截图，你要从列表中选择最后四个文件。

**步骤 1.9:** 选择文件后点击 **下载**。

![package-list- Informatica installation - Edureka](img/ae9ef86582ca45878a490746ff189dfc.png)

**                                         Fig: Setting Download Queue**



**步骤 1.10:** 你会得到一个弹出窗口，要求你下载 **安装程序。**

![Informatica-installation-Installer-downloader](img/5ab251c456eadb649ef4d0a92a23ea83.png)

**                  Fig: Click on the Download manager to download the required files**



**步骤 1.11:** 下载安装程序并安装到您的系统中。一旦安装程序启动，它将自动下载指定目录中的所有四个文件。

由于现在已经下载了所需的文件，我们将通过解压下载的文件继续进行 Informatica 安装。

## **第二步:打开安装包**

**注意**:使用 WinRAR 提取文件，因为任何其他文件浏览器在提取**DAC _ win _ 11g _ infa _ win _ 64 bit _ 961**时可能会出错

**步骤 2.1:** 现在将四个文件全部逐一提取出来。

**步骤 2.2:** 使用下面截图中建议的选项将其提取到同一个目录中。

![unzip - 1- Informatica installation - Edureka](img/aafbd0d666ff7bab7c6bee3fa2671fa8.png)

![unzip - 2- Informatica installation - Edureka](img/ce3fc3591c848feb2efe6d31afcc0e61.png)

**        Fig: Extracting the downloaded files**



**步骤 2.3:** 提取后会得到四个文件:

*   V76290-01_1of4。

*   V76290-01_2of4。

*   V76290-01_3of4。

*   V76290-01_4of4。

![extracted-files- Informatica installation - Edureka](img/9289cd4f5e481bd90a29bfa5ff2ec473.png)

**                                                              Fig: Extracted files**



**步骤 2.4:** 现在进入第四个文件 **V76290-01_4of4** ，提取名为**DAC _ win _ 11g _ infa _ win _ 64 bit _ 961**的文件。

![file-extraction-1- Informatica installation - Edureka](img/d8bac6dc6859a9319a4116455fc4bc86.png)

**                                            Fig: File located in V76290-01_4of4**



**步骤 2.5:** 提取该文件时，需要按照下面截图的提示，逐一输入 4 个提取文件的路径:

![unzip-3 - Informatica installation - Edureka](img/e50d03262887353e1278169412ccd265.png)

**第 2.6 步:** 当出现上述窗口时，浏览到第一个解压文件的位置，点击确定，如下提示:

![file-extraction-3- Informatica installation - Edureka](img/c31ec2dc9e8fa86d2905bdeb0c7fab8d.png)

**                                       Fig: Specifying Extraction location**



**步骤 2.7:** 以同样的方式浏览并提取第二、第三和第四个文件。

![Informatica-installation-file-extraction-4 -Informatica installation - Edureka](img/c6178676e29361c82232210dbb6bbc66.png)

**   Fig: Selecting location to extract the remaining files**



**步骤 2.8:** 现在进入解压文件**DAC _ win _ 11g _ infa _ win _ 64 bit _ 961**并解压 **服务器** 和 **客户端** 安装程序，使用选项如下截图所示。

![Informatica-installation-client-extract](img/64ccc7089fada2097213c4d0934e6a78.png)

![Informatica-installation-server-extract](img/b969b7cc0e0c99d997add04d1d72bfe9.png)

**                           Fig: Extracting Server and client installer**



## **第三步:Informatica PowerCenter 安装前检查。**

从这一点开始，Informatica 安装过程开始，但是在我们开始实际过程之前，我们需要检查当前系统是否满足 Informatica 安装的最低要求。

**步骤 3.1:** 进入目录**961 _ Server _ Installer _ winem-64t**双击 **install.bat** 文件开始安装 **。**

![Informatica-installation-launch - Informatica installation - Edureka](img/55cc299c18dd64c2ac560a1eb4f23330.png)

**                                 Fig: Selecting Server Installation file**



**步骤 3.2:** 如下截图。

![Informatica-installation-pre-install-1 - Informatica installation - Edureka](img/bca84ce501cfa1a25b0163fd7c3a850b.png)

**                     Fig: Selecting to launch pre-installation system check tool**



![Informatica-installation-pre-install-2 - Informatica installation - Edureka](img/537112279b9726d3ce716bcdb7f9ab86.png)

点击**下一步。**

![Informatica-installation-pre-install-3 - Informatica installation - Edureka](img/0ec2ee555c7f0de20c422fc88fb32193.png)

**                                Fig: Selecting Installation Directory**



**步骤 3.3:** 进入**域配置**如下:

*   主机名:EDUREKA23(这是我的机器的主机名)
*   数据库密码:INFA_DOM
*   数据库用户 ID : INFA_DOM
*   数据库类型:Oracle

要连接到远程主机，你必须从 Informatica 购买许可证，每年花费几千美元，这取决于某些参数，如用户数量、操作系统、处理器数量等。

![Informatica-installation-pre-install-4 - Informatica installation - Edureka](img/308417f6d5e240e35ffd8cfcbbe74d3c.png)

**                                         Fig: Domain Configuration repository database information**



*   要找到您机器的主机名，请转到 oracle 安装目录并打开 **tnsname.ora** 文件，该文件位于**C:Oracle xepporacleproduct . 2.0 serveretworkadamin**path

![Informatica-installation-host-name - Informatica installation - Edureka](img/b90239b83e24580b787a6e23dac6f7a4.png)

**                                              Fig: Host name and Port number of current Host machine**



**步骤 3.4:** 点击 **测试连接** 和 **接下来。**

![Informatica-installation-pre-install-5 - Informatica installation - Edureka](img/5f91c7bb8e7dc2b333ba0eea1df0f701.png)

**                                                Fig: Domain Connection test**



**步骤 3.5:** 点击 **完成。**

![Informatica-installation-pre-install-6 - Informatica installation - Edureka](img/d48b90ff87fddf76dac8e055ad1ec028.png)

**                          Fig: Informatica Pre-Installation check results **



## **步骤 4:安装 Informatica PowerCenter**

现在我们已经验证了当前系统满足最低要求，我们将继续进行实际的 Informatica 安装。

**步骤 4.1:** 现在再次转到解压后的目录**961 _ Server _ Installer _ winem-64t**双击 **install.bat** 文件。

![Informatica-installation-installer-1 - Informatica installation - Edureka](img/5a8e0dc647d2f46ba5df391ae2770cb3.png)

**步骤 4.2:** 遵循以下步骤。

![Informatica-installation-installer-2 - Informatica installation - Edureka](img/a6468a928b48c6b79f22151c6b8e4d49.png)

**                                           Fig: Click on Install or upgrade Option**



点击**下一步。**

![Informatica-installation-installer-3 - Informatica installation - Edureka](img/434dd60a920d93d70171c64005cb2848.png)

**                                                 Fig: System Requirements**



**第 4.3 步:** 现在在下面的窗口中浏览 **下的产品密钥 v 76290-01 _ 4 of 4 DAC _ win _ 11g _ infa _ win _ 64 bit _ 961。**

![Informatica-installation-installer-4 - Informatica installation - Edureka](img/f20a1b2392ab18b54ba74a91a5b4f3ef.png)

![Informatica-installation-installer-5 - Informatica installation - Edureka](img/2cd881a1c9f530b6b41e8f156bd73e86.png)

**                                             Fig: Select Oracle_All_OS_Prod.key**



![Informatica-installation-installer-6 - Informatica installation - Edureka](img/0f4dd4277b4741051c2e6a5d3bce144c.png)

点击**下一步。**

![Informatica-installation-installer-7 - Informatica installation - Edureka](img/be883dbdb9f7a630093e29c35cfc738f.png)

点击**安装。**

*   安装这个软件需要一点时间。



## **第五步:域配置**

现在我们已经完成了 Informatica 的安装，我们开始配置过程。需要配置的第一个组件是操作域。

**步骤 5.1:** 取消勾选“为 Informatica 管理员启用 HTTPS”，点击下一步。

![Informatica-installation-domain-1 - Informatica installation - Edureka](img/86939fe6ac46ac4bc09fb023ed8fb980.png)

**                                              Fig: Select Create a domain option**



**步骤 5.2:** 进入域配置如下:

*   数据库类型:Oracle
*   数据库用户 ID : INFA_DOM
*   用户密码:INFA_DOM
*   其余参数都是默认的。

**步骤 5.3:** 点击 **测试连接** 点击 **下一步。**

![Informatica-installation-domain-2 - Informatica installation - Edureka](img/d570dc50f1ad4c7e284fdb9525d6da9d.png)

![Informatica-installation-domain-3 - Informatica installation - Edureka](img/27a3de2de15fc92cf748f673fbb0625c.png)

**                                                   Fig: Domain Connection test**



您已经成功测试了域连接。

**第 5.4 步:** 输入加密密钥信息(我是选 Edu@1122，可以选一样):

*   关键词:Edu@1122

点击 **下一步**和**确定。**

![Informatica-installation-domain-4 - Informatica installation - Edureka](img/0f71f868db6eb610217536545ad56be8.png)

![Informatica-installation-domain-5 - Informatica installation - Edureka](img/e36fd41f3d98debbddf644c0903b5278.png)

**                                           Fig: Specifying encryption key to be used **



**步骤 5.5:** 输入如下关于信息领域的详细信息:

*   域名用户名:管理员
*   域密码:管理员

在 **上勾选 标记，显示高级端口配置页面，在** 上点击 **下一步。**

![Informatica-installation-domain-6 - Informatica installation - Edureka](img/128ead60a9af0d5350fe7cb676d42d36.png)

**                                                                            Fig: Informatica Domain details **



点击 **下一步。**

![Informatica-installation-domain-ports - Informatica installation - Edureka](img/f9b22ddca11b7d2ab882e5bd9f7666be.png)

**                                                   Fig: Informatica port details **



*   配置设置需要时间。

![Informatica-installation-domain-7 - Informatica installation - Edureka](img/4fd7e53c13f119307b80f2482929b9a0.png)



**步骤 5.6:取消勾选** 在不同的用户账户下运行 Informatica，点击 **下一步。**

![Informatica-installation-domain-8 - Informatica installation - Edureka](img/1e827e62e503e42511f8c64a20ac55d5.png)

**步骤 5.7** :点击 **Informatica 管理员主页**链接。

![Informatica-installation-domain-9 - Informatica installation - Edureka](img/fdaedfdbb0a130e336e9a9fd12025596.png)

**                                     Fig: Launching Informatica Administrator home page **



## **第六步:配置存储库服务**

一旦配置了操作域，我们需要配置将从客户端应用程序连接到存储库的存储库服务。

**步骤 6.1:** 点击以上链接后，浏览器中会打开 **Informatica 管理员控制台** 。

*   用户名:管理员
*   密码:管理员

![Informatica-installation-admin-homepage - Informatica installation - Edureka](img/b64951cc423c0bd411aed1fec0a149d3.png)

**                                                                 Fig: Informatica Administrator login page**



![Informatica-installation-admin-consol - Informatica installation - Edureka](img/26a6a0545997147efae7f34222884fa5.png)

**                                                                      Fig :Informatica Administrator console **



**步骤 6.2:** 创建存储库服务:

*   **点击操作- >新建- > PowerCenter 存储库服务。**

![Informatica-installation-repository-2 - Informatica installation - Edureka](img/73c92cc2b7f7745e6386509e55eeba95.png)

![Informatica-installation-repository-3 - Informatica installation - Edureka](img/ad09f44c539f16766bbb69774ada1502.png)

**  Fig : Creating New Repository**



**步骤 6.3:** 输入以下仓库服务详情:

*   名称:Repsvc_Edureka
*   从 下拉列表中选择 **许可证** 和 **节点** ，点击 **下一步。**

![Informatica-installation-repository-4 - Informatica installation - Edureka](img/bceb46f3d49a1c8deb65c44a3a618001.png)

**                                                       Fig : Specifying repository details **



点击 **下一步。**

**步骤 6.4:** 为数据库属性输入如下详细信息:

*   数据库类型:Oracle
*   用户名:INFA 代表
*   密码:INFA 代表
*   连接字符串:XE

![Informatica-installation-repository-5 - Informatica installation - Edureka](img/1825a9d8b0841327ac02893c94e8c6ac.png)

**                                                     Fig : Database properties **



点击**完成。**

**步骤 6.5:** 现在将运行模式从独占改为 **正常。**

![Informatica-installation-repository-6 - Informatica installation - Edureka](img/f57a730e9f8a784d65ee8761daed6985.png)

![Informatica-installation-repository-7 - Informatica installation - Edureka](img/86296b9c00b291c96d178bf474b1353f.png)

![Informatica-installation-repository-8 - Informatica installation - Edureka](img/679d2ac131f5398d3d7037eed61a4a7e.png)

**                                            Fig : Changing Operating mode of Repository**



现在我们已经成功地使存储库可用于进一步的操作。

## **第七步:配置集成服务**

作为存储库服务配置的一部分，我们还需要配置集成服务，它将从存储库加载工作流，并帮助组合来自不同平台和源类型的数据。

**步骤 7.1:** 创建集成服务

*   **点击动作- >新增- > PowerCenter 集成服务**

![Informatica-installation-integration-1 - Informatica installation - Edureka](img/336859d5254f3fa6f7682c3104a3ca24.png)

**                                                                     Fig : Creating new integration service**



**步骤 7.2:** 输入以下集成服务详情

*   名称:Intsvc_Edureka
*   从 下拉列表中选择 **牌照** 和 **节点** ，点击 **下一个**

![Informatica-installation-integration-2 - Informatica installation - Edureka](img/9c7204c6c6359eb45c438fa6805af82b.png)

**                                    Fig : Specifying integration service properties**



点击 **下一个**

**步骤 7.3:** 输入以下存储库服务详细信息

*   PowerCenter 存储库服务:Repsvc_Edureka
*   用户名:管理员
*   密码:管理员

![Informatica-installation-integration-3 - Informatica installation - Edureka](img/021cbd732d02fee1947fb89aa72e6d01.png)

![Informatica-installation-integration-4 - Informatica installation - Edureka](img/7de3bbd93043f742f2429ffe5072054d.png)

**                                              Fig : Specifying repository properties**



*   现在，集成服务已创建，但已禁用，因此我们必须启用它。

**步骤 7.4:** 按照以下步骤启用集成服务

![Informatica-installation-integration-5 - Informatica installation - Edureka](img/05078111420b03defa7e6c772fa45ead.png)

![Informatica-installation-integration-6 - Informatica installation - Edureka](img/add0b52826a2f0d774a5c36238488d81.png)

![Informatica-installation-integration-7 - Informatica installation - Edureka](img/bcf45c290e458b6b6d4fa85d05deb273.png)

**                                                                   Fig : Enabling integration services**



我们现在已经成功地使集成服务可用于进一步的操作。

## **第八步:客户端安装**

为了继续进行 Informatica 安装，我们从客户端安装开始。

**步骤 8.1:** 现在安装 **PowerCenter 客户端**

*   进入目录**961 _ Client _ Installer _ win32-x86**，双击进入 **install.bat。**

![Informatica-installation-client-1 - Informatica installation - Edureka](img/fed0b9cac7fe8ac7abcf5a52185ee471.png)

**                                                 Fig :Launching client installer**





![Informatica-installation-client-2 - Informatica installation - Edureka](img/f4f20c85d1e2f445bce14ae0ff2ae5dd.png)

**                                                Fig : Enabling integration services**



点击**下一步。**

**步骤 8.2:** 标记 **勾选** **PowerCenter 客户端** 上的 ，点击 **下一步。**

![Informatica-installation-client-3 - Informatica installation - Edureka](img/8f7465207f8f64e3b898cb7420382b4f.png)

**                                             Fig : Select PowerCenter Client option**



**步骤 8.3:** 点击 **下一步**，指定安装目录。

![Informatica-installation-client-4 - Informatica installation - Edureka](img/77f7983f9007957ae6bee6b43d604783.png)

**                                           Fig : Specifying installation directory**



**步骤 8.4:** 点击 **安装。**

![Informatica-installation-client-4 - Informatica installation - Edureka](img/ddde1ec466d20e99522c273ffaa16623.png)

现在这一步需要一些时间来安装软件。

![Informatica-installation-client-6 - Informatica installation - Edureka](img/cd65de574028aa230ea05bc6eafed71b.png)

**步骤 8.5:** 点击 **搞定**

![Informatica-installation-client-6 - Informatica installation - Edureka](img/95b6030e17065715ae1fd8969161b5c5.png)

**                                              Fig : Completing client installation**



## **第九步:配置 PowerCenter Designer**

Informatica 安装的最后一步是配置 PowerCenter Designer，以连接到域和存储库来加载数据库

**步骤 9.1:** 现在点击 Windows 开始按钮启动 PowerCenter Designer。

![Informatica-installation-launching-designer - Informatica installation - Edureka](img/4ae792a616d80a723f174aac89730df1.png)

**                    Fig : Launching PowerCenter Designer**



![Informatica-installation-designer-1 - Informatica installation - Edureka](img/714044cc5862f5026687d520a5739ea8.png)

**                                               Fig : PowerCenter Designer Homepage**



**步骤 9.2:** 点击 **储存库- >配置域名。**

![Informatica-installation-designer-2 - Informatica installation - Edureka](img/e7f7f61aa6496ac6d3f7446de7ba86f2.png)

**                                                              Fig : Configuring Domain**



**步骤 9.3:** 点击 **添加域名。**

![Informatica-installation-designer-3 - Informatica installation - Edureka](img/9f7ee867222cba93359cb4376293cc4a.png)

**步骤 9.4:** 输入以下详细信息添加一个域:

*   域名:Domain_Edureka23(此处应输入您机器的 Domain _ Host Name)
*   网关主机:Edureka23(您机器的主机名)
*   网关端口:6005

![Informatica-installation-designer-4 - Informatica installation - Edureka](img/67c2f06d34b7eb22e6bfa27d1609bef9.png)

**                                                    Fig : Specifying Domain details**



点击 **确定。**

**第 9.5 步:** 选择 **Repsvc_Edureka** 点击 **确定。**

![Informatica-installation-designer-5 - Informatica installation - Edureka](img/5044a1eb4ad5a0052e91971cb4563597.png)

**                                                   Fig : Selecting repository**



**第 9.6 步:** 选择 **Repsvc_Edureka** 连接资源库 如下图。

![Informatica-installation-designer-6 - Informatica installation - Edureka](img/8d7c914f07b497fc5de1506875c5c7c7.png)

![Informatica-installation-designer-7 - Informatica installation - Edureka](img/259a52b4fe7d4154eb1d4ba3d76b3809.png)

**                                                  Fig : Connecting to repository**



*   在下面的截图中，你可以看到连接是成功的。

![Informatica-installation-designer-8 - Informatica installation - Edureka](img/44c74a1b8ed04c80c3f267970ca69490.png)

*   您可以在 Informatica 管理控制台的存储库服务中验证连接。
*   可以看到表中列出的 **域属性** 。

![Informatica-installation-designer-9 - Informatica installation - Edureka](img/b5572fe2f2700f06f6bf32604e121863.png)

**                                                                         Fig : Domain Properties**



这就完成了 Informatica 的安装，希望这篇博客对在你的系统中安装 Informatica PowerCenter 有用。

如果你觉得这个博客很有帮助，你也可以看看我们的 Informatica 教程博客系列[什么是 Informatica:Informatica power center 的初学者教程](https://www.edureka.co/blog/what-is-informatica/)和 [Informatica 教程:理解 Informatica‘Inside Out’](https://www.edureka.co/blog/informatica-tutorial)。如果你正在寻找 Informatica 认证的细节，你可以查看我们的博客 [Informatica 认证:所有需要知道的事情](https://www.edureka.co/blog/informatica-certification-all-there-is-to-know/)。

如果你已经决定以信息学为职业，我会推荐你为什么不看看我们的[信息学培训](https://www.edureka.co/informatica)课程页面。Edureka 的 Informatica 认证培训将通过现场讲师指导课程和使用真实案例的实践培训，使您成为 Informatica 专家。

*有问题吗？请在评论区提到它，我们会给你回复。*