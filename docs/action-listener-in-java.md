# 如何用 Java 实现动作监听器

> 原文：<https://www.edureka.co/blog/action-listener-in-java/>

当用户执行某个动作[时，Java](https://www.edureka.co/blog/java-tutorial/) 必须能够有效地处理它。在这种情况下，Java 中的动作监听器非常有用。在本文中，我们将讨论以下几点:

*   [动作监听器简介](#intro)
*   [动作事件类](#action-event)
*   [用 Java 实现动作监听器](#code)

## **动作监听器简介**

作为程序员，你有责任定义一个动作监听器能为用户的操作做什么。例如，让我们考虑一个简单的场景，其中用户从菜单栏中选择某个项目，或者在文本字段中按 enter 键以转到新的一行。一旦这样的用户功能完成，一个“action performed”消息被发送到在相关组件中定义的所有相应的动作监听器。

下面生动地描述了如何编写一个动作监听器:

![Action-Listener-List](img/0b4bdfbe0cf784735530c24cf5feec41.png)

这里，至关重要且不可或缺的部分是可以实现动作监听器接口的对象。这个对象必须被程序识别为按钮上的一个动作监听器，它只是事件源。

因此，利用 addActionListener 方法，当用户单击按钮时，它会触发一个动作事件。这将调用操作侦听器的 actionPerformed 方法。请注意，它是 ActionListener 接口中唯一的方法。该方法的单个参数是一个 ActionEvent 对象，它提供关于事件及其来源的信息

## **动作事件类**

| **方法** | **描述** |
| **字符串 getActionCommand()** | 返回与此操作关联的字符串。大多数可以触发动作事件的对象都支持名为 setActionCommand 的方法，该方法允许您设置此字符串。 |
| **int get coders()** | 它返回一个整数，用户在操作期间事件发生时按下了该整数。一些 ActionEvent 定义的常量，如 SHIFT_MASK、CTRL_MASK、META_MASK 和 ALT_MASK，用于确定按下的键。例如，如果用户选择一个菜单项，那么表达式是非零的 |
| **Object getSource()****(在 java.util.EventObject 中)** | 返回触发事件的对象。 |

## **用 Java 实现动作监听器**

```
package com.javapointers.javase;

import java.awt.BorderLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JTextArea;

public class ActionListenerTest implements ActionListener {

    JButton button;
    JFrame frame;
    JTextArea textArea;

    public ActionListenerTest() {
        button = new JButton("Click Me");
        frame = new JFrame("ActionListener Test");
        textArea = new JTextArea(5, 40);

        button.addActionListener(this);
        textArea.setLineWrap(true);
        frame.setLayout(new BorderLayout());
        frame.add(textArea, BorderLayout.NORTH);
        frame.add(button, BorderLayout.SOUTH);
        frame.pack();

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        textArea.setText(textArea.getText().concat("You have clicked
        the buttonn"));
    }

    public static void main(String args[]) {
        ActionListenerTest test = new ActionListenerTest();
    }
}
```

![Action-Listener-in-Java](img/961c2cc2d6bd50ccc2186256517fe676.png)

在上面的代码中，需要在类中实现一个动作侦听器，然后才能访问它。因此，请确保添加 implements 关键字和侦听器。

**button.addActionListener(本)**

表示组件按钮将包含在动作事件被跟踪的组件中。必须将组件添加到操作侦听器中，以便在用户单击特定组件时添加代码。未添加操作监听器的组件将无法被监控。

现在让我们看另一个简单的 Java 动作监听器的例子以及它是如何工作的。

**例 2:**

这里有 3 个简单的 Java 按钮对象，它们被命名为红色、绿色和蓝色。根据点击的按钮，背景屏幕颜色会发生变化。

下图描述了本文件末尾代码的相应输出。只显示了一个屏幕变蓝的例子。通过实现这段代码可以看到其他颜色，如红色和绿色。

按钮对象“rb”与 ActionListener 链接。“this”参数表示 ActionListener。如果链接没有完成，程序将显示 3 个按钮，但没有事件处理。

ActionEvent 类的 getActionCommand()方法将用户点击的对应按钮的标签以字符串的形式返回。海峡。

```
import java.awt.*;
import java.awt.event.*;

public class ButtonDemo extends Frame implements ActionListener
{
Button rb, gb, bb;		            // the three Button reference variables
public ButtonDemo()	                    // constructor to define the properties to a button
{
FlowLayout fl = new FlowLayout();	    // set layout to frame
setLayout(fl);

rb = new Button("Red");		    // convert variables into objects
gb = new Button("Green");
bb = new Button("Blue");

rb.addActionListener(this);		    // link Java buttons with ActionListener
gb.addActionListener(this);
bb.addActionListener(this);

add(rb);			            // add each Java button to the frame
add(gb);
add(bb);

setTitle("Button in Action");
setSize(300, 350);                      // frame dimensions, (width x height)
setVisible(true);			    // defining frame visible on monitor, default is setVisible(false)
}
// override only abstract method of ActionListener interface
public void actionPerformed(ActionEvent e)
{
String str = e.getActionCommand();	    // to identify the button clicked
System.out.println("You clicked " + str + " button");  //

if(str.equals("Red"))
{
setBackground(Color.red);
}
else if(str.equals("Green"))
{
setBackground(Color.green);
}
else if(str.equals("Blue"))
{
setBackground(Color.blue);
}
}
public static void main(String args[])
{
new ButtonDemo();                       // anonymous object of ButtonDemo to call the constructor
}
}

```

![Action-Button](img/60cd2af9d3f7c89eaed8051ac1a46452.png)

至此，我们结束了 Java 文章中的这个动作监听器。我希望你对 Java 中的动作监听器有所了解。

*查看 Edureka 提供的  [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 中的动作监听器”博客的评论部分提到它，我们会尽快回复您。