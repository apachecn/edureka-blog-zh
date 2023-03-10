# 如何在 Ubuntu 18.04 上安装 Java/JDK

> 原文：<https://www.edureka.co/blog/how-to-install-java-on-ubuntu/>

***Oracle Java JDK(Java Development Kit)***是基于 ***Java*** 开发应用和工具的开发环境。这是一个多用途的工具包，可用于使用 Java 编程语言测试应用程序和程序开发。这将是初学者如何在 ***Ubuntu 18.04*** 上下载和安装 java 的简要指南。这对于任何在 [***Linux 管理***](https://www.edureka.co/linux-admin) 寻找机会的专业人士来说都是必不可少的。

你也可以使用 ***apt-get 命令*** 非常容易地安装 ***开放 Java JDK / JRE*** (一个开源的替代方案)。有大量的教程可以向您展示如何通过第三方 PPA 工具安装 Java。然而，本文主要关注两种简单的方法，即从原始存储库下载 Java，而不是通过第三方下载开源版本的 Java。

所以，如果你遵循这几个简单的步骤，你应该能够下载和安装 JDK 在你的操作系统上，完全没有麻烦。

*   [**甲骨文网站**](#oraclewebsite)
*   [**方法一:下载&使用 tarball**T3 在 Ubuntu 上安装 Java/JDK](#downloadjdkusingtarfile)
*   [**方法二:下载&使用 deb 包**T3 在 Ubuntu 上安装 Java/JDK](#downloadjdkusingdebfile)
*   [**在系统上配置 Java**](#configurejava)
*   [**创建 Java 环境变量**](#javaenvironmentvariables)

## **甲骨文网站**

*   要在 Ubuntu 上安装 JDK，首先要登录甲骨文官网。

*   前往屏幕左上角的 ***菜单*** 按钮(看起来像 3 条短线条堆叠在一起)并进入 ***产品> > Java > >为开发者下载 Java(JDK)***。![oracle website - how to intall jdk on ubuntu - edureka](img/6c33de3cb5d3603e0ad1377071ddf9db.png)

### **第一步:访问甲骨文网站**

*   你也可以直接从登录甲骨文官方网站的 [***下载页面***](https://www.oracle.com/technetwork/java/javase/downloads/index.html) 开始。

*   单击上面有 Java 徽标的下载按钮。![Java website - how to intall jdk on ubuntu - edureka](img/65fed7f22d6ed89ffcb3086406b1b9e2.png)

### **第二步:Java SE 开发套件**

*   向下滚动，你可能会看到一个类似下图的方框。你会看到一堆不同的选项来为 Linux、MacOS 和 Windows 下载 JDK。

    ![JDK options - how to intall jdk on ubuntu - edureka](img/6724fc773eab5a897328ac8ecffe0f75.png)

*   在盒子的顶部，您会看到一个名为 ***接受许可协议*** 的选项。选择它旁边的复选框。

## **下载&使用 tarball 在 Ubuntu 上安装 Java(方法 1)**

### **第一步:下载目标文件**

*   在甲骨文网站的下载页面，选择 **Linux x64** 的 **.tar.gz 包**进行下载。![JDK tarball file - how to intall jdk on ubuntu - edureka](img/9ec3183782a5263bb18e5c1c54a4564d.png)

*   下载后，你可以去解压下载的软件包，在 Ubuntu 上安装 JDK。

### **第二步:提取文件**

*   既然您已经为您的系统下载了正确的存档包，运行下面的命令来提取它。

`*tar -zxvf ~/Downloads/jdk-12.0.1_linux-x64_bin.tar.gz*`

*   接下来，创建一个目录来存储 Java 编译器包。您可以随意命名，但最好以您正在安装的 Java 版本命名。

`*sudo mkdir -p /usr/lib/jvm/jdk-12.0.1/*`

*   接下来，运行下面的命令，将提取的 Java 内容复制到新创建的目录中。

`*sudo mv jdk-12.0.1_linux-x64 /usr/lib/jvm/jdk12.0.1/*`

## **下载&使用 deb 包在 Ubuntu** **上安装 Java(方法二)**

**第一步:下载 deb 包**

*   你也可以在官方网站上选择另一个选项。确保您正在下载的版本号。如果有比我提到的版本号更新的版本号，请选择它。![JDK deb file - how to intall jdk on ubuntu - edureka](img/ab89e7bf5ad684e430403f57862aafb4.png)

*   你也可以通过运行下面的命令来轻松安装 DEB 包。

`*cd /tmp*`

*T2`wget --no-cookies --no-check-certificate --header "Cookie: oraclelicense=accept-securebackup-cookie" https://download.oracle.com/otn-pub/java/jdk/12.0.1+33/312335d836a34c7c8bba9d963e26dc23/jdk-12.0.1_linux-x64_bin.deb`*

**第二步:安装 Oracle Java**

*   现在你已经为你的系统下载了正确的存档包，运行下面的命令在 Ubuntu 上安装 JDK。

`*sudo dpkg -i jdk-12.0.1_linux-x64_bin.deb*`

## **步骤 3:在您的系统上配置 Java**

*   之后，运行下面的命令将 Java 12.0.1 配置为 Ubuntu 的默认版本。下面的命令配置 Ubuntu 使用 Java 替代品。

`*sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-12.0.1/bin/java 2*`

`*sudo update-alternatives --config java*`

假设您安装了其他版本的 Java，并且运行了上面的命令，那么您应该会看到一个提示，要求您选择想要作为默认版本的 Java 版本。如果您没有安装其他版本的 Java，那么这些命令将不会返回任何内容。

*   接下来，运行以下命令，使最新版本的 Java 成为 Ubuntu 桌面的默认 Java 编译器。

`*sudo update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk-12.0.1/bin/jar 2*`

`*sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-12.0.1/bin/javac 2*`

`*sudo update-alternatives --set jar /usr/lib/jvm/jdk-12.0.1/bin/jar*`

`*sudo update-alternatives --set javac /usr/lib/jvm/jdk-12.0.1/bin/javac*`

这应该可以安装和配置 Java。

*   运行下面的命令，看看 Ubuntu 是否能识别 Java。

*java 版本*

您应该会看到下面的输出:

`*java 12.0.1 2019-04-16*``*Java(TM) SE Runtime Environment (build 12.0.1+12)*`

## **步骤 4:创建 Java 环境变量**

*   要设置 JAVA 环境变量，请在/etc/profile.d 目录中为 JDK 创建一个新文件。

`*sudo nano /etc/profile.d/jdk12.0.1.sh*`

*   然后将这些行复制并粘贴到文件的末尾并保存。

`*export J2SDKDIR=/usr/lib/jvm/java-12.0.1*`

`*export J2REDIR=/usr/lib/jvm/java-12.0.1*`

`*export PATH=$PATH:/usr/lib/jvm/java-12.0.1/bin:/usr/lib/jvm/java-12.0.1/db/bin*`

`*export JAVA_HOME=/usr/lib/jvm/java-12.0.1*`

`*export DERBY_HOME=/usr/lib/jvm/java-12.0.1/db*`

*   接下来，运行下面的命令

`*source /etc/profile.d/jdk12.0.1.sh*`

*   上面的命令应该可以配置 Java 来和 Ubuntu 一起工作。要测试 JDK 是否正确安装在 Ubuntu 上，运行下面的命令。您应该看到 Java 已经安装好了。

**T2`*java -version*`**

`*java 12.0.1 2019-04-16 Java(TM) SE Runtime Environment (build 12.0.1+12) Java HotSpot(TM) 64-Bit Server VM (build 12.0.1+12, mixed mode, sharing)*`

恭喜你！你刚刚在 Ubuntu 18.04 上成功安装了 ***Java/JDK 12.0.1。***

*想了解更多 Ubuntu？你可以登录 www.edureka.co/linux-admin 的。* *Edureka 的 Linux 管理认证培训旨在塑造您作为 Linux 专业人员的职业生涯&帮助您运行应用程序，在您的系统和网络上执行所需的功能，创建网络配置，以及维护安全管理。*