# 初级 Java 教程

> 原文：<https://www.edureka.co/blog/basic-java-tutorial-getting-started/>

随着 Java 在我们日常生活中的普遍存在，它已经成为当今世界一种重要的编程语言。Sun Microsystems 于 1995 年发布了这种基于类的面向对象程序，由于其在编码方面的相似性，它经常与 C & C++之类的程序联系在一起。通常被称为“一次编写，随处运行”的编程语言，Java 应用程序被编译成字节码并在 Java 虚拟机(JVM)中运行。

任何程序员都会问的一个典型问题是如何开始？教程从下载，安装，设置环境，运行一个'**谜'** Java 应用，一步一步的给你讲解。

## **步骤 1:下载 Java**

Java 应用程序可以从链接 [下载](http://www.java.com/en/download/index.jsp) 下载，那里有当前版本(7.0 版)。您也可以点击此处的 [下载符合您操作系统的版本。](http://www.java.com/en/download/manual.jsp)

## **第二步:设置环境变量**

安装完成后，设置环境变量非常重要。它们是一组动态命名值，可以影响正在运行的进程在计算机上的行为方式。它们是运行进程的操作系统的一部分。

下载完 Java 文件后，我们必须运行。exe 文件在机器上安装 Java。如果您的操作系统是 Windows，则:

*   右键单击我的电脑，然后单击属性
*   点击高级选项卡下的环境变量
*   然后将 path 变量改为“C:windows system 32；程序文件 javajdkin

如果您的操作系统基于 Windows Vista/7，请右键单击“计算机”并选择“属性”选项。在属性窗口中选择“高级系统设置”，然后选择“高级”选项卡并单击“环境变量”。将出现一个窗口，您可以通过单击“新建”按钮在“用户/系统变量”下输入新的环境变量。

**class path**:class path 是设置环境变量的重要组成部分，它指向 JDK 主目录的位置。它还包含类加载器加载 jar 的文件夹的地址。

**Java_Home** :该环境变量将指向 Java 主目录的位置。

## **第三步:检查是否安装了 Java**

设置好环境后，我们可以进入命令提示符并键入以下命令来检查是否安装了 Java。

开始>运行>键入 Cmd

在命令提示符(黑色窗口)下，我们键入:

java 版本

如果安装正确，它将向您输出:

C:UsersJbt>java 版本

java version “1.6.0_25”Java(TM) SE Runtime Environment (build 1.6.0_25-b06)Java HotSpot(TM) Client VM (build 20.0-b11, mixed mode, sharing

*根据下载的版本

或者，如果没有安装，它将显示:

“java”不被识别为内部或外部命令，

operable program or batch file.

## **第四步:选择 Java 编辑器**

要开始编写和编译程序，选择 Java 编辑器(IDE)是很重要的，它是一个集成开发环境(IDEa 软件应用程序，为计算机程序员提供软件开发的综合设施。IDE 通常由源代码编辑器、构建自动化工具和调试器组成。

*   首先，您可以使用系统中预装的记事本或文本板。
*   **记事本:**在 Windows 机器上你可以使用任何简单的文本编辑器，比如记事本(本教程推荐)、TextPad。
*   **Netbeans:** 一款流行的开源 IDE，可以免费下载 [这里](http://www.netbeans.org/index.html) 。
*   **Eclipse:** 也是 Eclipse 开源社区开发的 Java IDE，可以从 [这里](http://www.eclipse.org/) 下载。

恭喜你。您已经准备好使用 Java 了。

## **神秘程序:猜输出？**

这里有一个程序，我们想与您分享一个特定的输出。基于程序的逻辑，填空编译知道输出！

提示:讲的是一个意大利人！

```
class ___________
{
public static void main(String args[])
{		
int prev, next, sum, n;
prev=next=1
for(n=1;n<=10;n++)
{
System.out.println(prev);
sum=prev+next;
prev=next;
next=sum;
}
}
}
```

有问题要问我们吗？在评论区提到它们，我们会给你回复。