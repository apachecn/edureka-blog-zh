# 如何在 Windows 上安装 Eclipse IDE 的分步指南？

> 原文：<https://www.edureka.co/blog/setup-eclipse-ide/>

当今世界， [Java](https://www.edureka.co/blog/what-is-java/) 是最流行的编程语言之一，被[最熟练的专业人士](https://www.edureka.co/java-j2ee-training-course)所使用。然而，在命令行上使用它有时并不可行。因此，要克服这一点，可以在 Eclipse IDE 上使用它。因此，在这篇关于“如何在 Windows 上设置 Eclipse IDE？”，我要讨论以下:

## **安装 Java**

按照以下步骤完成您的 [Java](https://www.edureka.co/blog/java-tutorial/) 安装。

**第一步:**进入 [Java 下载页面](http://www.oracle.com/technetwork/java/javase/downloads/index.html)，点击**下载选项。**

**![Download Java - How To Setup Eclipse IDE On Windows - Edureka](img/f98eb07ea846979870cebb2c82cd6847.png)**

**第二步:**一旦你点击**下载**，你将被重定向到一个页面，在那里你必须选择**接受许可协议**单选按钮。之后你要根据你匹配的系统配置选择下载链接如下。

在这里，我选择了 jdk-8u211-windows-x64.exe

**第三步:**现在，一旦文件下载完毕，运行安装程序并持续点击**下一步**，直到你最终得到一个对话框，上面写着，你已经完成下载。

第四步: O 安装完成后，按照下面的说明设置文件的路径。

**步骤 4.1:** 进入开始，搜索“**系统**”。然后，c 点击**系统**，进入**高级系统设置**。参考下文。

**![](img/3ed3d4cb40c531631571c9f785e57be9.png)**

**步骤 4.2:** 现在，c 点击'**高级**标签下的'**环境变量**，如下图:

**![Environment Variables - How To Setup Eclipse IDE On Windows - Edureka](img/f2247aacbd2ec6dcc42db7e35417f747.png)**

**步骤 4.3:** 接下来，在**系统变量**下选择**新建。**

**步骤 4.4:** 输入变量名为' **JAVA_HOME** ，并根据您的系统输入 JAVA 安装目录的完整路径，如下图:

**![Java Home - How To Setup Eclipse IDE On Windows - Edureka](img/89c3efeb63c2aa68b7ecb99d537ced59.png)**

第 4.5 步: 接下来你要做的就是配置你的环境变量。让我们看看如何做到这一点。 在这里，你要编辑系统变量的路径如下所示。

**![Set Path To Java - How To Setup Eclipse IDE On Windows - Edureka](img/37fa5fd8cc22a47e653eccb9b7cfca08.png)**

**第 4.6 步:**下的**变量值**，在最后一行，输入文件夹的路径。现在，你可以点击 **OK** 就大功告成了。

现在要交叉检查安装，只需在 cmd 中运行下面的命令—***Java-version***。它应该显示您系统中已安装的 Java 版本。

## **![Java Version - How To Setup Eclipse IDE On Windows - Edureka](img/bab54464620ab6d61c879bf490aea3f4.png)**

## **安装 Eclipse**

按照下面的步骤在您的系统上配置 Eclipse:

**第一步:** 导航至以下网址——[https://www.eclipse.org/downloads/packages/](https://www.eclipse.org/downloads/packages/)和 s 根据您的系统架构选择下载链接——(Windows、Mac OS 或 Linux)并下载。

**第二步:** 下载结束后，右击文件夹提取压缩文件，选择**提取全部**。参考下文。

**![Extract Eclipse - How To Setup Eclipse IDE On Windows - Edureka](img/b0cc081207e483b09ec53088d0fea686.png)**

第三步:你将被重定向到一个对话框，在这里你必须选择你想要解压文件的目录。然后点击**提取**。参考下文。

**![Extract Eclipse Folder - How To Setup Eclipse IDE On Windows - Edureka](img/f83d4369da4dfa9ee7091776cd0b927a.png)**

**第四步:**解压文件后，o 打开文件夹，启动**eclipse.exe。**

## **![Run Eclipse - How To Setup Eclipse IDE On Windows - Edureka](img/04c09d20961b1d7da297a1b2b198d52c.png)**

然后，您必须选择 Eclipse 的启动目录，然后点击 Launch。参考下文。

## **![Set Path For Eclipse - How To Setup Eclipse IDE On Windows - Edureka](img/dc94ce10d3fc177d0bda9c78e27510b9.png)**

一旦 Eclipse 启动，您将看到下面的窗口:

## **![Eclipse Open Window - How To Setup Eclipse IDE On Windows - Edureka](img/380c175f7e210250afc7d8dc8e19d601.png)**

## **Hello World 节目**

**步骤 1:** 启动 **Eclipse IDE** ，进入**文件- >新建- > Java 项目**

**第二步:**提及**项目名称**，点击**完成。**

**![Create Project - How To Setup Eclipse IDE On Windows - Edureka](img/43fef4b05438c9c146af016b09e1aec8.png)**

**第三步:**现在，转到**项目**，右键点击该项目，选择**包**。在打开的对话框中，如下所示提及**包名**，并点击**完成。**

![Package Name - How To Setup Eclipse IDE On Windows - Edureka](img/5e9247fd24f3dc62633ea492233fbbf4.png)

**第四步:**现在右击**包**，前往**新建**，选择**类**。提及**类名**并点击**完成**。参考下文。

![Java Class - How To Setup Eclipse IDE On Windows - Edureka](img/3e98e1d601d1958974691d0e94446497.png)

**第五步:**现在，在工作区中提及以下代码。

```

package Edureka;

public class helloworld {
public static void main(String args[]){
System.out.println("Hello World");
}
}

```

**第六步:**现在，通过右击【helloworld.java】文件的**并选择**运行方式- > Java 应用程序来执行您的文件。****

你会看到控制台上印着 Hello World。

这就把我们带到了这篇“如何在 Windows 上设置 Eclipse IDE”文章的结尾。我们已经学习了如何在 Windows 上设置 Java 和 Eclipse。

*查看 Edureka 提供的 [**Java 认证培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“如何在 Windows”*上设置 Eclipse IDE”的评论部分提及，我们会尽快回复您。*