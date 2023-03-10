# Java AWT 教程——初学者的一站式解决方案

> 原文：<https://www.edureka.co/blog/java-awt-tutorial/>

Java 已经在业界存在了很长一段时间。它深深植根于编程世界的各个领域，无论是 web 应用程序、移动应用程序还是嵌入式系统。即使是谈论 GUI 编程， [**Java**](https://www.edureka.co/java-j2ee-training-course) 也为开发包装在 AWT API 内的高交互性 GUI 提供了一套丰富的库。在这篇 Java AWT 教程中，我将向您简要介绍它及其组件。

以下是本 Java AWT 教程涵盖的主题:

*   [什么是 Java AWT？](#javaawt)
*   [Java 中 AWT 的特性](#features)
*   [AWT UI 方面](#uiaspects)
*   [Java AWT 的层次](#hierarchy)
*   [AWT 组件](#components)
*   [用 Java AWT 开发计算器](#calculator)

让我们开始吧。

## **Java 中的 AWT 是什么？**

Abstract Window Toolkit 简称 AWT，是 Java 中[类](https://www.edureka.co/blog/java-objects-and-classes/)的 工具包，帮助程序员开发图形和图形用户界面组件。它是 Sun Microsystems 开发的 JFC (Java 基础类)的一部分。Java 中的 AWT API 主要由一组全面的类和方法组成，这些类和方法是以简化的方式创建和管理图形用户界面(GUI)所必需的。它是为设计跨平台 GUI 提供一套通用工具而开发的。AWT 的一个重要特性是它依赖于平台。这意味着 AWT 工具使用它们正在实现的平台的本地工具包。这种方法有助于 保留每个平台的外观和感觉。但是正如所说的一切都是有代价的，这种方法有一个主要的缺点。由于平台依赖性，当在各种平台上执行时，它在每个平台上看起来是不同的。这妨碍了应用程序的一致性和美观性。

除了与平台相关之外，AWT 类还有其他一些特性，我将在本 Java AWT 教程的下一节中讨论。

## **Java 中 AWT 的特性**

*   AWT 是一套原生用户[界面](https://www.edureka.co/blog/java-interface/)组件
*   它基于一个健壮的事件处理模型
*   它提供图形和图像工具，如形状、颜色和字体类
*   AWT 还利用了布局管理器，这有助于增加窗口布局的灵活性
*   数据传输类也是 AWT 的一部分，有助于通过本机平台剪贴板进行剪切和粘贴
*   支持为游戏产品、银行服务、教育目的等创建 图形所需的各种库。

既然您已经了解了 AWT 的各种特性，现在让我在 Java AWT 教程的下一部分介绍 GUI 的各个方面。

## **AWT UI 方面**

任何 UI 都将由三个实体组成:

*   **UI 元素** :这些是用户可见的核心视觉元素，用于与应用程序交互。Java 中的 AWT 提供了广泛使用的通用元素的完整列表。
*   布局 :这些定义了 UI 元素在屏幕上的组织方式，并为 GUI 提供了最终的外观。
*   **行为** :这些定义了当用户与 UI 元素交互时应该发生的事件。

我希望，到目前为止，您已经对 AWT 及其在任何应用程序中的作用有了简单的了解。在本 Java AWT 教程的下一节中，我将介绍完整的 AWT 层次结构。

**AWT 的层级**

![AWT Hierarchy - Java AWT Tutorial - Edureka](img/e76f2862a36e9b9932333f338d2600dc.png)在上图中可以看到，Component 是所有 GUI 控件的超类。它是一个抽象类， 封装了一个可视化组件的所有属性， 用图形化的方式表示一个对象。组件类实例基本上负责当前界面的外观。

下面我已经展示了Java . awt . component:的通用类描述

```
public abstract class Component
		extends Object
		implements ImageObserver, MenuContainer, Serializable{
  //class body
}
```

## **AWT 组件**

### **1。集装箱**

Java AWT 中的容器是一个组件，用于保存其他组件，如文本字段、按钮等。它是 java.awt.Component 的子类，负责跟踪添加的组件。Java 中 AWT 提供了四种类型的容器。

#### **容器类型**

1.  **Window** :它是 Window 类的一个实例，既没有边框也没有标题。它用于创建一个 顶层窗口。
2.  **Frame** : Frame 是 Window 的子类，包含标题、边框和菜单栏。它附带了一个可调整大小的画布，是开发 AWT 应用程序最广泛使用的容器。它能够容纳各种组件，如按钮、文本字段、滚动条等。 你可以通过两种方式创建 Java AWT 框架:
    1.  通过实例化框架类
    2.  通过扩展框架类
3.  **Dialog:** Dialog 类也是 Window 的子类，除了标题之外，还附带了边框。对话框类的实例总是需要关联的框架类实例才能存在。
4.  **Panel** : Panel 是容器的具体子类，不包含任何标题栏、菜单栏和边框。Panel 类是保存 GUI 组件的通用容器。为了添加组件，您需要 Panel 类的实例。

以上是关于容器及其类型的全部内容，现在让我们继续阅读这篇 Java AWT 教程文章，了解其余的组件。

### **2。按钮**

java.awt.Button 类用于创建带标签的按钮。点击时触发某个已编程的*动作*的 GUI 组件。按钮类有两个[构造函数](https://www.edureka.co/blog/parameterized-constructor-in-java/):

```
//Construct a Button with the given label
public Button(String btnLabel);

//Construct a Button with empty label
public Button();
```

下面列出了该类提供的一些方法:

```
//Get the label of this Button instance
public String getLabel();

//Set the label of this Button instance&nbsp;&nbsp;&nbsp;
public void setLabel(String btnLabel);

//Enable or disable this Button. Disabled Button cannot be clicked
public void setEnable(boolean enable);
```

### **3。文本字段**

一个Java . awt . textfield类创建一个单行文本框供用户输入文本。TextField 类有三个构造函数:

```
//Construct a TextField instance with the given initial text string with the number of columns.
public TextField(String initialText, int columns);

//Construct a TextField instance with the given initial text string.
public TextField(String initialText);

//Construct a TextField instance with the number of columns.
public TextField(int columns);
```

TextField 类提供的一些方法有:

```
// Get the current text on this TextField instance
public String getText();

// Set the display text on this TextField instance
public void setText(String strText);
//Set this TextField to editable (read/write) or non-editable (read-only)
public void setEditable(boolean editable);

```

### **4。标签**

java.awt.Label 类提供了一个在 GUI 上可见的描述性文本字符串。AWT 标签对象是用于将文本放置在容器中的组件。标签类有三个[构造函数](https://www.edureka.co/blog/constructor-in-java/)，分别是:

```
// Construct a Label with the given text String, of the text alignment
public Label(String strLabel, int alignment); 

//Construct a Label with the given text String
public Label(String strLabel);

//Construct an initially empty Label
public Label();
```

这个类还提供了 3 个常量，它们是:

```
public static final LEFT; // Label.LEFT

public static final RIGHT;  // Label.RIGHT

public static final CENTER; // Label.CENTER 
```

下面我列出了这个类提供的公共方法:

```
public String getText();

public void setText(String strLabel);

public int getAlignment();

//Label.LEFT, Label.RIGHT, Label.CENTER 
public void setAlignment(int alignment);
```

### **5。画布**

Canvas 类代表一个矩形区域，在这里你可以在应用程序中绘图或者接收用户创建的输入。

### **6。选择**

Choice 类用来表示一个弹出菜单的选项。选定的选项显示在给定菜单的顶部。

### **7。滚动条**

Scrollbar 类对象用于在 GUI 中添加水平和垂直滚动条。它使用户能够看到不可见的行数和列数。

### **8。列表**

List 类的对象表示文本项的列表。使用[列表](https://www.edureka.co/blog/linked-list-in-java/)a 级用户可以选择一个或多个项目。

### **9。复选框**

复选框是一个用于创建复选框的图形组件。它有两个状态选项；真真假假。在任何时间点，它可以拥有两者中的任何一个。

所以，这就是你需要知道的关于 AWT 组件的所有信息。现在，我希望您已经准备好使用 Java AWT 应用程序了。

在本 Java AWT 教程的下一节中，我将向您展示如何使用 AWT 组件构建一个计算器。

## **用 Java AWT 开发计算器**

在这里，我将向您展示如何使用 AWT 创建一个计算器，在这里您将能够执行基本的数学运算。下面是您的计算器的屏幕截图:

现在，为了构建它，您需要键入以下代码:

```
package edureka.awt;

import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

class Calculator extends Frame implements ActionListener

{
    Label lb1,lb2,lb3;

    TextField txt1,txt2,txt3;

    Button btn1,btn2,btn3,btn4,btn5,btn6,btn7;

    public Calculator()
    {
        lb1 = new Label("Var 1");
        lb2 = new Label("Var 2");
        lb3 = new Label("Result");

        txt1 = new TextField(10);
        txt2 = new TextField(10);
        txt3 = new TextField(10);

        btn1 = new Button("Add");
        btn2 = new Button("Sub");
        btn3 = new Button("Multi");
        btn4 = new Button("Div");
        btn5 = new Button("Mod");
        btn6 = new Button("Reset");
        btn7 = new Button("Close");

            add(lb1);
            add(txt1);
            add(lb2);
            add(txt2);
            add(lb3);
            add(txt3);
            add(btn1);
            add(btn2);
            add(btn3);
            add(btn4);
            add(btn5);
            add(btn6);
            add(btn7);

            setSize(200,200);
            setTitle("Calculator");
            setLayout(new FlowLayout());
            //setLayout(new FlowLayout(FlowLayout.RIGHT));
            //setLayout(new FlowLayout(FlowLayout.LEFT));
            btn1.addActionListener(this);
            btn2.addActionListener(this);
            btn3.addActionListener(this);
            btn4.addActionListener(this);
            btn5.addActionListener(this);
            btn6.addActionListener(this);
            btn7.addActionListener(this);

    }
    public void actionPerformed(ActionEvent ae) {
        double a=0,b=0,c=0;
        try
        {
            a = Double.parseDouble(txt1.getText());
        }
        catch (NumberFormatException e) {
            txt1.setText("Invalid input");
        }
        try
        {
            b = Double.parseDouble(txt2.getText());
        }
        catch (NumberFormatException e) {
            txt2.setText("Invalid input");
        }
        if(ae.getSource()==btn1)
        {
            c = a + b;
            txt3.setText(String.valueOf(c));
        }
        if(ae.getSource()==btn2)
        {
            c = a - b;
            txt3.setText(String.valueOf(c));
        }
        if(ae.getSource()==btn3)
        {
            c = a * b;
            txt3.setText(String.valueOf(c));
        }
        if(ae.getSource()==btn4)
        {
            c = a / b;
            txt3.setText(String.valueOf(c));
        }
        if(ae.getSource()==btn5)
        {
            c = a % b;
            txt3.setText(String.valueOf(c));
        }
        if(ae.getSource()==btn6)
        {
            txt1.setText("0");
            txt2.setText("0");
            txt3.setText("0");
        }
        if(ae.getSource()==btn7)
        {
            System.exit(0);           
        }     
    }
    public static void main(String[] args)
    {
        Calculator calC = new Calculator();
        calC.setVisible(true);
        calC.setLocation(300,300);
    }
}
```

您可能已经注意到，这里我们只使用了功能。您可以随时向您的应用程序添加更多的功能，并创建一个功能齐全的计算器。

至此，本 Java AWT 教程到此结束。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*现在您已经了解了什么是 Java AWT 教程，请查看 Edureka 的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-training-course)*，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java AWT 教程”文章的评论部分提到它，我们会尽快回复您。*