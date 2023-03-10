# Java 中的 Swing:知道如何用例子创建 GUI

> 原文：<https://www.edureka.co/blog/java-swing/>

java 中的 Swing 是 Java 基础类的一部分，它是轻量级的和平台无关的。它用于创建基于窗口的应用程序。它包括按钮、滚动条、文本字段等组件。将所有这些组件放在一起就形成了一个图形用户界面。在本文中，我们将在 **[Java](https://www.edureka.co/java-j2ee-training-course)** 中介绍使用 swing 构建应用程序的过程中涉及的概念。以下是本文中讨论的概念:

*   [什么是 Java Swing？](#whatisswing)
*   [集装箱等级](#containerclass)
*   [AWT 和 Swing 之间的差异](#awtvsswing)
*   [Java Swing 类层次结构](#hierarchy)
*   [布局管理器](#layoutmanager)
*   [示例-聊天框](#example)

## **Java 中的 Swing 是什么？**

Swing in Java 是一个轻量级的 GUI 工具包，它有各种各样的小部件，用于构建优化的基于窗口的应用程序。它是 JFC( Java 基础类)的一部分。它构建在 AWT API 之上，完全用 java 编写。与 AWT 不同，它是独立于平台的，并且具有轻量级的组件。

构建应用程序变得更加容易，因为我们已经有了 GUI 组件，如按钮、复选框等。这很有帮助，因为我们不必从头开始。

## **集装箱类**

任何包含其他组件的类称为容器类。要构建 GUI 应用程序，至少需要一个容器类。

以下是三种类型的容器类:

1.  面板–它用于将组件组织到一个窗口上

2.  框架——带有图标和标题的全功能窗口

3.  对话框——它像一个弹出窗口，但不像框架那样功能齐全

## **AWT 和 Swing 的区别**

| **AWT** | **摇摆** |
| 

*   Platform dependence

 | 

*   Platform independence

 |
| 

*   Do not follow MVC

 | 

*   Follow MVC

 |
| 

*   Secondary component

 | 

*   More powerful components

 |
| 

*   Non-pluggable look and feel supported

 | 

*   Support pluggable look and feel

 |
| 

*   heavyweight

 | 

*   light and handy

 |

## **Java Swing 类层次结构**

## **![hierarchy-swing in java-edureka](img/dd7104c219bd33c36a7a713cb138ae03.png)**

**说明**:swing 中的所有组件，如 JButton、JComboBox、JList、JLabel，都是从 JComponent 类继承而来，可以添加到容器类中。容器是像框架和对话框一样的窗口。基本的 swing 组件是任何 gui 应用程序的构建块。像 setLayout 这样的方法会覆盖每个容器中的默认布局。像 JFrame 和 JDialog 这样的容器只能向自身添加一个组件。下面是几个组件，并举例说明如何使用它们。

### **JButton 类**

它用于创建带标签的按钮。使用 ActionListener，当按钮被按下时会产生一些动作。它继承了 AbstractButton 类，并且独立于平台。

**举例:**

```

import javax.swing.*;
public class example{
public static void main(String args[]) {
JFrame a = new JFrame("example");
JButton b = new JButton("click me");
b.setBounds(40,90,85,20);
a.add(b);
a.setSize(300,300);
a.setLayout(null);
a.setVisible(true);
}
}

```

**输出:**

### **JTextField 类**

它继承了 JTextComponent 类，用于编辑单行文本。

**举例:**

```
import javax.swing.*;
public class example{
public static void main(String args[]) {
JFrame a = new JFrame("example");
JTextField b = new JTextField("edureka");
b.setBounds(50,100,200,30);
a.add(b);
a.setSize(300,300);
a.setLayout(null);
a.setVisible(true);
}
}

```

**输出:**

### **JScrollBar 类**

它用于添加水平和垂直滚动条。

**举例:**

```
import javax.swing.*;
class example{
example(){
JFrame a = new JFrame("example");
JScrollBar b = new JScrollBar();
b.setBounds(90,90,40,90);
a.add(b);
a.setSize(300,300);
a.setLayout(null);
a.setVisible(true);
}
public static void main(String args[]){
new example();
}
}

```

**输出:T2**

### **JPanel 类**

它继承了 JComponent 类，并为可以附加任何其他组件的应用程序提供了空间。

```
import java.awt.*;
import javax.swing.*;
public class Example{
Example(){
JFrame a = new JFrame("example");
JPanel p = new JPanel();
p.setBounds(40,70,200,200);
JButton b = new JButton("click me");
b.setBounds(60,50,80,40);
p.add(b);
a.add(p);
a.setSize(400,400);
a.setLayout(null);
a.setVisible(true);
}
public static void main(String args[])
{
new Example();
}
}

```

**输出:**

**![](img/4cc105e28ee808667d13c1de350ebb51.png)**

### **命名为 clas****T3**

它继承了 JMenuItem 类，是从菜单栏显示的下拉菜单组件。

```
import javax.swing.*;
class Example{
JMenu menu;
JMenuItem a1,a2;
Example()
{
JFrame a = new JFrame("Example");
menu = new JMenu("options");
JMenuBar m1 = new JMenuBar();
a1 = new JMenuItem("example");
a2 = new JMenuItem("example1");
menu.add(a1);
menu.add(a2);
m1.add(menu);
a.setJMenuBar(m1);
a.setSize(400,400);
a.setLayout(null);
a.setVisible(true);
}
public static void main(String args[])
{
new Example();
}
}

```

**输出:**

### **![](img/ba01a3e0731f64b9bbc68097782d7bf3.png)**

### **JList 类**

它继承了 JComponent 类，JList 类的对象表示一个文本项列表。

```
import javax.swing.*;
public class Example
{
Example(){
JFrame a  = new JFrame("example");
DefaultListModel<String> l = new DefaultListModel< >();
l.addElement("first item");
l.addElement("second item");
JList<String> b = new JList< >(l);
b.setBounds(100,100,75,75);
a.add(b);
a.setSize(400,400);
a.setVisible(true);
a.setLayout(null);
}
public static void main(String args[])
{
new Example();
}
}

```

**输出:**

### **![](img/154c26d50428e2fb6ae85efa5e5ca430.png)**

### **JLabel 类**

它用于在容器中放置文本。它还继承了 JComponent 类。

```
import javax.swing.*;
public class Example{
public static void main(String args[])
{
JFrame a = new JFrame("example");
JLabel b1;
b1 = new JLabel("edureka");
b1.setBounds(40,40,90,20);
a.add(b1);
a.setSize(400,400);
a.setLayout(null);
a.setVisible(true);
}
}

```

**输出:**

### **![](img/578ed79d47cdd057abd409f97bb0f4d4.png)**

### **JComboBox 类**

它继承了 JComponent 类，用于显示选项的弹出菜单。

```
import javax.swing.*;
public class Example{
JFrame a;
Example(){
a = new JFrame("example");
string courses[] = { "core java","advance java", "java servlet"};
JComboBox c = new JComboBox(courses);
c.setBounds(40,40,90,20);
a.add(c);
a.setSize(400,400);
a.setLayout(null);
a.setVisible(true);
}
public static void main(String args[])
{
new Example();
}
}  

```

**输出:**

## **![](img/b03caebd50b9c8f25c95ae6d538c316b.png)**

## **布局管理器**

为了在容器中安排组件，我们使用布局管理器。以下是几个布局管理器:

1.  边框布局

2.  流程布局

3.  GridBag 布局

### **边框布局**

每个 JFrame 的默认布局管理器是 BorderLayout。它将组件放置在最多五个位置，即顶部、底部、左侧、右侧和中间。

### **![BorderLayout-Java Swing-Edureka](img/7822d1587ffdaad57e4fd61cdb026a6d.png)**

### **流程布局**

FlowLayout 只是将组件一个接一个地放在一行中，它是每个 JPanel 的默认布局管理器。

### **![Flowlayout-swing in java-edureka](img/0c98faa055725950b4ee376920aea908.png)**

### **GridBag 布局**

GridBagLayout 将组件放置在一个网格中，该网格允许组件跨越多个单元格。

## **![Gridlayout-Swing in Java- edureka](img/aa9f477c5f433afa62d52493c6129b48.png)**

## **举例:聊天框**

```
import javax.swing.*;
import java.awt.*;
class Example {
    public static void main(String args[]) {

        JFrame frame = new JFrame("Chat Frame");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(400, 400);

        JMenuBar ob = new JMenuBar();
        JMenu ob1 = new JMenu("FILE");
        JMenu ob2 = new JMenu("Help");
        ob.add(ob1);
        ob.add(ob2);
        JMenuItem m11 = new JMenuItem("Open");
        JMenuItem m22 = new JMenuItem("Save as");
        ob1.add(m11);
        ob1.add(m22);

        JPanel panel = new JPanel(); // the panel is not visible in output
        JLabel label = new JLabel("Enter Text");
        JTextField tf = new JTextField(10); // accepts upto 10 characters
        JButton send = new JButton("Send");
        JButton reset = new JButton("Reset");
        panel.add(label); // Components Added using Flow Layout
        panel.add(label); // Components Added using Flow Layout
        panel.add(tf);
        panel.add(send);
        panel.add(reset);
        JTextArea ta = new JTextArea();

        frame.getContentPane().add(BorderLayout.SOUTH, panel);
        frame.getContentPane().add(BorderLayout.NORTH, tf);
        frame.getContentPane().add(BorderLayout.CENTER, ta);
        frame.setVisible(true);
    }
}

```

![](img/f2bb1fd5b1fc0b6f90bc0ddc0fcb3a79.png)

这是一个在 Java 中使用 swing 创建 GUI 的简单例子。

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

在本文中，我们讨论了 Java 中的 swing 和 Java swing 类的层次结构。有了 swing 在 Java 中附带的所有组件，构建优化的 GUI 应用程序变得更加容易。Java 编程语言是一种结构化编程语言，随着需求的增长，掌握 [Java 编程](https://www.edureka.co/blog/java-tutorial/)中的所有概念变得极其重要。要开始学习并成为 java 编程专家，请注册 Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)项目。

有问题要问我们吗？请在这篇“Swing In Java”文章的评论部分提到这一点，我们会尽快回复您。