# Java 中的 Maven 是什么，怎么用？

> 原文：<https://www.edureka.co/blog/maven-in-java/>

Maven 是一个强大的 Java 项目构建工具。这是一个管理和自动化工具。它基本上是用 [Java 语言](https://www.edureka.co/blog/java-tutorial/)编写的，用于构建和管理用 C#、 [Ruby](https://www.edureka.co/blog/ruby-on-rails-tutorial/) 、Scala 和其他语言编写的项目。在我深入 Java 的 Maven 世界之前，让我向您解释一下本文的议程。

我将讨论以下提到的主题:

*   [Java 中的 Maven 是什么？](#WhatisMaveninJava)
*   [如何安装 Maven？](#HowtoinstallMaven)
*   [Maven pom.xml 文件](#Mavenpom.xmlfile)
*   [Maven 知识库](#MavenRepository)
*   [Maven 的优缺点](#AdvantagesanddisadvantagesofMaven)

既然你已经清楚了我们讨论的主题，让我们从理解 Java 中的 Maven 到底是什么开始。

## **![Maven logo](img/8eefc950ca1c1e7f1e36dfd3c1cc8cef.png)Java 中的 Maven 是什么？**

Maven 是一个非常强大的项目管理工具，用于构建和管理任何与 Java 相关的项目。Maven 有助于减轻 Java 开发人员的工作。它能够处理项目的构建、报告和文档。

在理解了 Java 中 Maven 的含义之后，让我借助一个图表向您展示它的工作原理。

这里有一些对你来说可能是新的术语。我将逐一阐述它们。

**POM 文件:**首先，为了配置 Maven，您需要使用[项目对象模型](https://www.edureka.co/blog/page-object-model-in-selenium/) (POM)，它存储在一个 pom.xml 文件中。POM 包括与 Maven 相关的配置设置。它也有目标和插件。在执行过程中，Maven 读取目标，在目录中搜索 POM 并获得所需的信息。

构建生命周期、阶段和目标:构建生命周期是一个定义良好的阶段序列。它定义了目标执行的顺序。每个构建阶段由一系列目标组成。如果执行一个生命周期，则执行该生命周期中的所有构建阶段。如果一个构建阶段被执行，那么在预定义的构建阶段序列中在它之前的所有构建阶段都被执行。

构建插件: [Maven](https://www.edureka.co/blog/maven-tutorial/) 基本上是一个插件执行框架，每个任务都通过插件来完成。如果需要为您的项目执行一组标准 Maven 构建阶段和目标没有涵盖的特定操作，您可以向 POM 文件添加一个插件。Maven 有一些可以在 java 项目中使用的标准插件。一个插件实际上给出了一组目标。pom.xml 中使用插件元素提到了插件。

**构建概要文件:**如果您需要以多种方式构建您的项目，可以使用构建概要文件。您还可以为多个环境定制构建，例如生产 v/s 开发环境。有三种类型的构建概要文件:每个概要文件、每个用户、全局。

存储库:存储库就是你机器上的一个目录。项目 jar、插件或任何其他与项目相关的材料都存储在这里。有三种不同类型的存储库:本地、中央和远程。

鉴于您对上述术语非常熟悉，让我们继续了解安装过程。

## **如何安装 Maven？**

你需要遵循这些简单的步骤: 1。你的系统应该已经安装了 Java。 2。设置 Java 环境变量(点击此处)3。下载 Maven(从此处) 4。现在，您必须在您想要的位置打开 Maven 的 zip 文件。 5。将您创建的目录的 bin 目录，即 apache-maven-3.5.3(无论您安装了什么版本)添加到 PATH 环境变量和系统变量中。 6。现在打开 cmd，运行 mvn -v 命令 7。如果您的屏幕显示如下所示的屏幕截图，则安装过程完成。

```
Apache Maven 3.5.3 (3383c37e1f9e9b3bc3df5050c29c8aff9f295297; 2018-02-25T01:19:05+05:30)
Maven home: C:apache-maven-3.5.3bin..
Java version: 1.8.0_151, vendor: Oracle Corporation
Java home: C:Program FilesJavajdk1.8.0_151jre
Default locale: en_US, platform encoding: Cp1252
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"

```

现在，在您的系统中安装了 Maven 之后，让我们继续理解 Maven pom.xml 文件

## **Maven pom.xml 文件**:

POM 代表项目对象模型。pom.xml 文件包含有关项目的信息和构建项目的配置信息。它包含依赖项、构建目录、源目录、测试源目录、插件等。Maven 浏览 pom.xml 文件，然后执行目标。为了创建一个简单的 pom.xml 文件，您必须需要以下元素:

**项目:**POM . XML 文件的根元素。

**groupId:** 项目的子元素。它描述了项目的 Id。

**modelVersion:** 项目的子元素。它告诉你模型版本。

**artifactId:** 项目的子元素。它指定项目的 id。一个工件要么是由一个项目产生的，要么是由一个项目使用的。工件的例子:jar、源代码和二进制发行版以及 war。

**版本:**项目的子元素。它告诉您给定组下工件的版本。

pom.xml 文件的示例如下所示:

```
<project  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"&gt;
<modelVersion>4.0.0</modelVersion>
<groupId>com.edureka.application1</groupId>
<artifactId>my-app</artifactId>
<version>1</version>
</project>

```

pom.xml 文件中还有一些附加元素: **打包:**定义了打包类型，如 war、jar 等。

**范围:**定义 maven 项目的范围。

**Url:** 指定项目的 Url。

**Name:** 定义 maven 项目的名称。

**依赖关系**:定义一个依赖关系。它在依赖关系中使用。

pom.xml 文件的示例代码显示了附加元素:

```
<project  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"&gt;  
<modelVersion>4.0.0</modelVersion>
<groupId>com.edureka.application1</groupId>
<artifactId>my-application1</artifactId>
<version>1.0</version>
<packaging>jar</packaging>
<name>Maven Quick Start Archetype</name>
<ur>http://maven.apache.org</url>
<dependencies>
<dependency> 
<groupId>junit</groupId>
<artifactId>junit</artifactId>
<version>4.8.2</version>
<scope>test</scope>
</dependency>  
</dependencies>
</project>

```

现在我们已经非常清楚 pom.xml 文件的概念，是时候详细讨论 Maven repository 了。

## **Maven 知识库:**

存储库只是您机器上的一个目录。项目 jar、插件或任何其他与项目相关的材料都存储在这里。让我详细说明不同类型的存储库。 1。本地知识库 2。中央储存库 3。远程存储库

每当需要搜索任何依赖项时，都会在存储库中进行。Maven 从本地存储库初始化它的搜索，然后是中央存储库，最后是远程存储库。

**本地存储库:**

Maven 的本地存储库是您机器上的一个文件夹位置，其中存储了所有与项目相关的元素。一旦执行了 Maven 构建，Maven 就会自动将所有依赖关系 jar 下载到本地存储库中。默认情况下，maven 本地存储库是 user_home/m2 目录。

**中央储存库:**

如果在本地存储库中没有找到任何依赖项，那么 Maven 将遍历中央存储库。然后 Maven 将这些依赖项下载到您的本地存储库中。

**远程存储库:**

当 Maven 想要下载依赖项时，它会转到远程存储库。远程存储库是 web 服务器上的存储库，广泛用于托管组织的内部项目。

掌握了存储库的概念后，让我们继续下一个主题，讲述 Maven 的优点和缺点:

## **Maven 的优缺点:**

从优点入手: 1。Maven 让项目在不同的环境中轻松起步。 2。您可以使用 Maven 轻松地将项目构建到 jar 中，并根据您需求进行 war。 3。通过在 pom 文件中编写依赖关系代码，可以很容易地添加新的依赖关系。现在，劣势: 1 .如果现有依赖项的 maven 代码不可用，那么就不能添加该依赖项。 2。Maven 安装和插件是必须的。

我的文章到此结束。我希望以上解释的内容能对你有所帮助。我们将继续探索 Java 世界。敬请期待！

*查看 Edureka 提供的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-soa-training)*，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“Java 中的 Maven”博客的评论部分提到它，我们会尽快回复您。