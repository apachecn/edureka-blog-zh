# 如何用 Java 实现 JFrame 类

> 原文：<https://www.edureka.co/blog/jframe-class-in-java/>

Java 中的 JFrame 类是图形用户界面的一个重要方面。本文将讨论以下几点。

*   [简介](#intro)
*   [在 Java 中创建 JFrame](#CreatingAJFrame)
*   [改变 JFrame 的窗口大小](#ChangewindowsizeofaJFrame)
*   [在 Java 中调整 JFrame 的大小](#ResizingaJFrame)
*   [改变屏幕上的位置](#Changingpositiononthescreen)
*   [关闭 Java 中的 JFrame](#ClosingaJFrame)
*   [代码说明](#Explanationofthecode)

## **简介**

JFrame 类基本上是 Java.awt.Frame 的扩展版本，或者我们也可以说 javax.swing.JFrame 类是一种继承 java.awt.Frame 类的容器类型。无论何时使用 Java Swing 功能创建图形用户界面(GUI ),都需要一个容器，在其中添加标签、按钮、文本字段等组件来创建图形用户界面(GUI ),这就是 JFrame。JFrame 有自己的方法和构造函数，就像一个类一样。方法是影响 JFrame 属性的函数，包括其大小或可见性，而构造函数在实例创建后运行。

**注意**:必须导入 Java Swing 接口才能使用这个类:-import javax . Swing . *；

## **在 Java 中创建 JFrame**

要创建 JFrame，我们必须创建 JFrame 类的实例。我们有许多构造函数来创建一个 JFrame。

*   JFrame() :创建一个框架，但不可见
*   **JFrame(graphics configuration GC)**:创建一个框架，该框架具有空白标题和设备屏幕的图形配置。
*   **JFrame(字符串标题)**:创建一个有标题的 JFrame。
*   **JFrame(String title，GraphicsConfiguration gc)** :创建一个具有特定图形配置和指定标题的 JFrame。

用 Java 创建 JFrame 的代码:

```

package ExampleNumber1;
import java.awt.GraphicsConfiguration;
import javax.swing.JFrame;
public class JFrameExample {

static GraphicsConfiguration gc;
public static void main(String[] args){
JFrame frame= new JFrame(gc);
frame.setVisible(true);
}
}

```

**输出:**

## **![Output- JFrame Class in Java - Edureka](img/192966ac7e42c9338df4af7605d3bda7.png)**

让我们了解一下 JFrame 的变化窗口大小！

## **改变 JFrame 的窗口大小**

要调整框架的大小，有一个方法 JFrame.setSize(int width，int height ),它采用两个参数 width 和 height。下面是更改 JFrame 窗口大小的代码。

```

package ExampleNumber2;
import java.awt.GraphicsConfiguration;
import javax.swing.JFrame;
public class JFrameExample {

static GraphicsConfiguration gc;
public static void main(String[] args){
JFrame frame= new JFrame(gc);
frame.setTitle("Hello, My name is Yashwinder");
frame.setSize(600, 400);
frame.setVisible(true);
}
}

```

让我们继续调整 JFrame 的大小。

## **在 Java 中调整 JFrame 的大小**

在设置了 JFrame 的某个大小后，可以看到我们仍然可以通过简单地将光标悬停在角上并根据大小要求拖动它来更改大小。如果按下右上角关闭旁边的调整大小选项，它将最大化到全屏大小。这通常是因为默认情况下 resize 设置为 true。您还可以将 false 设为 JFrame . setresizable(false)–它将根据您在代码中给出的尺寸显示，现在我们将无法通过图形用户界面(GUI)来调整 JFrame 的大小。

让我们理解改变屏幕上的位置。

## **改变屏幕上的位置**

为了改变 JFrame 在屏幕上的位置，JFrame 提供了一个名为 JFrame.setlocation(int a，int b)的方法，该方法采用两个参数，a 代表沿 x 轴的位置，b 代表沿 y 轴的位置。你屏幕的左上角是(0，0)。

让我们继续关闭 JFrame。

## **关闭 Java 中的 JFrame**

我们可以通过点击 JFrame 左上角的 X(叉)按钮轻松关闭您的 JFrame。但是 JFrame . setdefaultcloseoperation(int)是 JFrame 类提供的方法。您可以设置当用户点击十字时将发生的操作。如果在任何情况下“0”被作为参数传递，JFrame 将永远不会关闭，即使在点击十字之后。关闭 JFrame 的最佳方式是使用 JFrame。EXIT _ ON _ CLOSE–退出应用程序(JFrame)并释放已用内存。 JFrame。HIDE _ ON _ CLOSE–不关闭 JFrame。它只是把它藏了起来。 JFrame。DISPOSE_ON_CLOSE-关闭帧，但它会继续运行。还会消耗内存。 JFrame。DO_NOTHING_ON_CLOSE-当用户点击关闭时不做任何事情。

**示例:** 下面是两个简单的例子，用给定的维度、resize 和 no resize 属性创建 JFrame，并设置 JFrame 的标题等。

```
import java.awt.*;
import javax.swing.*;
public class JFrameExam implements Runn
{
public static void main(String[] args)
{
JFrameExample example = new JFrameExample();
// schedule this for the event dispatch thread (edt)
SwingUtilities.invokeLater(example);
}

public void run()
{
JFrame frame = new JFrame("My First JFrame ExampleNumber 3 ");
frame.setDefaultCloseOperation(WindowConstants.EXIT_ON_CLOSE);
frame.setPreferredSize(new Dimension(400, 200));
frame.pack();
frame.setVisible(true);
}
}

```

```
package ExampleNumber4;
import java.awt.GraphicsConfiguration;
import javax.swing.JFrame;
public class JFrameExample {

static GraphicsConfiguration gc;
public static void main(String[] args){
JFrame frame= new JFrame(gc);
frame.setTitle("Hello, my name is Yash");
frame.setSize(600, 400);
frame.setLocation(200, 200);
frame.setVisible(true);
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
frame.setResizable(false);
}

```

如何创建、居中和显示 JFrame

代码:

```

import java.awt.Dimension;
import javax.swing.JFrame;
import javax.swing.SwingUtilities;

// A sample class demonstrating to create and display a JFrame.

public class SimpleJFrame
{
public static void main(String[] args)
{
SwingUtilities.invokeLater(new Runnable()
{
public void run()
{
// creating a jframe, giving it an initial title
JFrame frame = new JFrame("First JFrame Demo Here");

// set the jframe size. in a more complicated application you will
// probably call frame.pack() before displaying it.
frame.setSize(new Dimension(300,200));

// center the frame
frame.setLocationRelativeTo(null);

// set this so the application can easily be stopped/Ended.
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

// displaying the frame
frame.setVisible(true);
}
});
}
}

```

继续解释代码。

## **代码说明:**

执行从 SimpleJFrame Java 类的 main 方法开始。

SwingUtilities invokeLater 方法被用作大多数代码的包装器。不幸的是，这是最复杂的一行代码，它排在第一位，但一般来说，这种技术用于确保它在事件调度线程(EDT)上执行类似这样的 Swing 代码。

frame . setlocationrelativeto(null)是一种稍微特殊的在屏幕上居中 JFrame 的方式。它实际上在 JFrame Javadoc 中讨论过，但是当你第一次使用 Swing 和 JFrame 时，这一点并不明显。frame . setdefaultcloseoperation(JFrame。EXIT_ON_CLOSE)方法设置应用程序，以便当用户按下他们在左上角看到的窗口上的关闭按钮时，整个应用程序将关闭。这种技术对于像这个例子这样的简单应用程序来说是很好的，但是对于更复杂的应用程序，您将希望更小心地控制关闭过程

**总结**

JFrame 是 Java 中的一个类，有自己的方法和构造函数。至此，我们结束了这篇 Java 文章中的 JFrame 类。*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。*

有问题要问我们吗？请在这个“Java 中的 JFrame 类”博客的评论部分提到它，我们会尽快回复您。