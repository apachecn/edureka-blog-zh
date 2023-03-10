# 2023 年你需要知道的顶级 Java 项目

> 原文：<https://www.edureka.co/blog/java-projects>

对 [**Java**](https://www.edureka.co/java-j2ee-training-course) 的需求永无止境，许多顶级**跨国公司**都在寻找 **[Java 开发人员](https://www.edureka.co/blog/java-developer-skills)。如今，拥有 java 实践经验和尝试 java 项目将会为你的简历增加砝码。在本文中，我们将尝试 2021 年你需要知道的前 5 个项目。**

*   [在线考试](#on)
*   [群组对话](#gc)
*   [图书馆管理系统](https://www.edureka.co/blog/library-management-system-project-in-java)
*   [OTP 发生器](#otp)
*   [密码生成器](#pass)

## **在线考试**

这个特定的项目旨在提供一个用户界面，该界面询问**多项选择**问题，并将用户的输入作为答案，然后，最终评估所有问题，并将输出作为个人**结果返回。**

```
package Edureka;

import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

class OnlineTest extends JFrame implements ActionListener {
       JLabel l;
       JRadioButton jb[] = new JRadioButton[5];
       JButton b1, b2;
       ButtonGroup bg;
       int count = 0, current = 0, x = 1, y = 1, now = 0;
       int m[] = new int[10];

       OnlineTest(String s) {
              super(s);
              l = new JLabel();
              add(l);
              bg = new ButtonGroup();
              for (int i = 0; i < 5; i++) {
              jb[i] = new JRadioButton();
              add(jb[i]);
              bg.add(jb[i]);
        }
        b1 = new JButton("Next");
        b2 = new JButton("Bookmark");
        b1.addActionListener(this);
        b2.addActionListener(this);
        add(b1);
        add(b2);
        set();
        l.setBounds(30, 40, 450, 20);
        jb[0].setBounds(50, 80, 100, 20);
        jb[1].setBounds(50, 110, 100, 20);
        jb[2].setBounds(50, 140, 100, 20);
        jb[3].setBounds(50, 170, 100, 20);
        b1.setBounds(100, 240, 100, 30);
        b2.setBounds(270, 240, 100, 30);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(null);
        setLocation(250, 100);
        setVisible(true);
        setSize(600, 350);
}

public void actionPerformed(ActionEvent e) {
        if (e.getSource() == b1) {
              if (check())
                    count = count + 1;
                    current++;
                    set();
              if (current == 9) {
                    b1.setEnabled(false);
                    b2.setText("Result");
              }
        }
        if (e.getActionCommand().equals("Bookmark")) {
              JButton bk = new JButton("Bookmark" + x);
              bk.setBounds(480, 20 + 30 * x, 100, 30);
              add(bk);
              bk.addActionListener(this);
              m[x] = current;
              x++;
              current++;
              set();
              if (current == 9)
                    b2.setText("Result");
                    setVisible(false);
                    setVisible(true);
              }
              for (int i = 0, y = 1; i < x; i++, y++) {
                    if (e.getActionCommand().equals("Bookmark" + y)) {
                          if (check())
                          count = count + 1;
                          now = current;
                          current = m[y];
                          set();
                          ((JButton) e.getSource()).setEnabled(false);
                          current = now;
                    }
              }

              if (e.getActionCommand().equals("Result")) {
                     if (check())
                     count = count + 1;
                     current++;
                     JOptionPane.showMessageDialog(this, "correct ans=" + count);
                     System.exit(0);
              }
        }
        void set() {
                 jb[4].setSelected(true);
                 if (current == 0) {
                     l.setText("Que1: Which one among these is not a primitive datatype?");
                     jb[0].setText("int");
                     jb[1].setText("Float");
                     jb[2].setText("boolean");
                     jb[3].setText("char");
                 }
                 if (current == 1) {
                     l.setText("Que2: Which class is available to all the class automatically?");
                     jb[0].setText("Swing");
                     jb[1].setText("Applet");
                     jb[2].setText("Object");
                     jb[3].setText("ActionEvent");
                 }
                 if (current == 2) {
                     l.setText("Que3: Which package is directly available to our class without importing it?");
                     jb[0].setText("swing");
                     jb[1].setText("applet");
                     jb[2].setText("net");
                     jb[3].setText("lang");
                 }
                 if (current == 3) {
                     l.setText("Que4: String class is defined in which package?");
                     jb[0].setText("lang");
                     jb[1].setText("Swing");
                     jb[2].setText("Applet");
                     jb[3].setText("awt");
                 }
                 if (current == 4) {
                     l.setText("Que5: Which institute is best for java coaching?");
                     jb[0].setText("Utek");
                     jb[1].setText("Aptech");
                     jb[2].setText("SSS IT");
                     jb[3].setText("jtek");
                 }
                 if (current == 5) {
                     l.setText("Que6: Which one among these is not a keyword?");
                     jb[0].setText("class");
                     jb[1].setText("int");
                     jb[2].setText("get");
                     jb[3].setText("if");
                 }
                 if (current == 6) {
                     l.setText("Que7: Which one among these is not a class? ");
                     jb[0].setText("Swing");
                     jb[1].setText("Actionperformed");
                     jb[2].setText("ActionEvent");
                     jb[3].setText("Button");
                 }
                 if (current == 7) {
                     l.setText("Que8: which one among these is not a function of Object class?");
                     jb[0].setText("toString");
                     jb[1].setText("finalize");
                     jb[2].setText("equals");
                     jb[3].setText("getDocumentBase");
                 }
                 if (current == 8) {
                     l.setText("Que9: which function is not present in Applet class?");
                     jb[0].setText("init");
                     jb[1].setText("main");
                     jb[2].setText("start");
                     jb[3].setText("destroy");
                 }
                 if (current == 9) {
                     l.setText("Que10: Which one among these is not a valid component?");
                     jb[0].setText("JButton");
                     jb[1].setText("JList");
                     jb[2].setText("JButtonGroup");
                     jb[3].setText("JTextArea");
                 }
                 l.setBounds(30, 40, 450, 20);
                 for (int i = 0, j = 0; i <= 90; i += 30, j++)
                 jb[j].setBounds(50, 80 + i, 200, 20);
         }

        boolean check() {
              if (current == 0)
                      return (jb[1].isSelected());
              if (current == 1)
                      return (jb[2].isSelected());
              if (current == 2)
                      return (jb[3].isSelected());
              if (current == 3)
                      return (jb[0].isSelected());
              if (current == 4)
                      return (jb[2].isSelected());
              if (current == 5)
                      return (jb[2].isSelected());
              if (current == 6)
                      return (jb[1].isSelected());
              if (current == 7)
                      return (jb[3].isSelected());
              if (current == 8)
                      return (jb[1].isSelected());
              if (current == 9)
                      return (jb[2].isSelected());
              return false;
         }

         public static void main(String s[]) {
                new OnlineTest("Online Test Of Java");
       }
}

```

**//输出**

![online-test-Java-Projects-Edureka](img/156a4da95b5f185e56e96dc488bd211b.png)

**//回答完所有问题后的最终输出**

![online-test-Java-Projects-Edureka](img/ba9b1df727bf69f9b9d87a314338cd3f.png)

下一个项目是小组对话。

## **群组对话**

该项目旨在提供多个终端之间的**群组对话**。相同的代码如下。用户必须注意**端口号**和 **IP 地址。**相同的代码如下。

```
package groupchat;

import java.net.*;
import java.io.*;
import java.util.*;

public class GroupConversation {
        private static final String TERMINATE = "Exit";
        static String name;
        static volatile boolean finished = false;
        public static void main(String[] args) {
               if (args.length != 2)
                       System.out.println("Two arguments required: <multicast-host> <port-number>");
               else {
                       try {
                             InetAddress group = InetAddress.getByName(args[0]);
                             int port = Integer.parseInt(args[1]);
                             Scanner sc = new Scanner(System.in);
                             System.out.print("Enter your name: ");
                             name = sc.nextLine();
                             MulticastSocket socket = new MulticastSocket(port);
                             socket.setTimeToLive(0);
                             socket.joinGroup(group);
                             Thread t = new Thread(new ReadThread(socket, group, port));
                             t.start();
                             System.out.println("Start typing messages...n");
                             while (true) {
                                    String message;
                                    message = sc.nextLine();
                                    if (message.equalsIgnoreCase(GroupConversation.TERMINATE)) {
                                          finished = true;
                                          socket.leaveGroup(group);
                                          socket.close();
                                          break;
                                    }
                                    message = name + ": " + message;
                                    byte[] buffer = message.getBytes();
                                    DatagramPacket datagram = new DatagramPacket(buffer, buffer.length, group, port);
                                    socket.send(datagram);
                             }
                       } 
                       catch (SocketException se) {
                             System.out.println("Error creating socket");
                             se.printStackTrace();
                       } 
                       catch (IOException ie) {
                             System.out.println("Error reading/writing from/to socket");
                             ie.printStackTrace();
                       }
               }
        }
}

class ReadThread implements Runnable {
         private MulticastSocket socket;
         private InetAddress group;
         private int port;
         private static final int MAX_LEN = 1000;
         ReadThread(MulticastSocket socket, InetAddress group, int port) {
                this.socket = socket;
                this.group = group;
                this.port = port;
         }
         @Override
          public void run() {
                while (!GroupConversation.finished) {
                        byte[] buffer = new byte[ReadThread.MAX_LEN]; 
                        DatagramPacket datagram = new DatagramPacket(buffer, buffer.length, group, port);
                        String message;
                try {
                        socket.receive(datagram);
                        message = new String(buffer, 0, datagram.getLength(), "UTF-8");
                        if (!message.startsWith(GroupConversation.name))
                                System.out.println(message);
                        } 
                        catch (IOException e) {
                                System.out.println("Socket closed!");
                        }
                 }
          }
}

```

**//输出**

![group-conversation-Java-Projects-edureka](img/a393a505ec789279384ba9937bcf2538.png)

下一个项目是 OTP 生成器

## **OTP 发生器**

这个项目被设计成使用**随机函数实时生成 **OTP** 。**相同的代码如下。

```
package otp;
import java.util.*;

public class Edureka {
       static char[] OTP(int len) {
             System.out.println("Generating OTP using random() : ");
             System.out.print("You OTP is : ");
             String numbers = "0123456789";
             Random rndm_method = new Random();
             char[] otp = new char[len];
             for (int i = 0; i < len; i++) {
                    otp[i] = numbers.charAt(rndm_method.nextInt(numbers.length()));
             }
             return otp;
       }
       public static void main(String[] args) {
             int length = 4;
             System.out.println(OTP(length));
       }
}

```

**//输出**

`Generating OTP using random() :` 

下一个项目是密码生成器

**密码生成器**

这个项目被设计成使用**随机函数实时生成**密码**。**相同的代码如下。

```
package OTP_Generator;

import java.util.*;
public class Edureka {
     public static void main(String[] args) {
          int length = 10;
          System.out.println(geek_Password(length));
     }
     static char[] geek_Password(int len) {
          System.out.println("Generating password using random() : ");
          System.out.print("Your new password is : ");
          String Capital_chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
          String Small_chars = "abcdefghijklmnopqrstuvwxyz";
          String numbers = "0123456789";
          String symbols = "!@#$%^&*_=+-/.?<>)";
          String values = Capital_chars + Small_chars + numbers + symbols;
          Random rndm_method = new Random();
          char[] password = new char[len];
          for (int i = 0; i < len; i++) {
                password[i] = values.charAt(rndm_method.nextInt(values.length()));
          }
          return password;
     }
}

```

**//输出**

`Generating password using random() :` 

至此，本 Java 项目教程到此结束。我希望您已经理解了这些 Java 项目及其实现。

通过本“Java 项目”教程，您已经了解了和的基础知识，请查看 Edureka 提供的  **[Java 课程](https://www.edureka.co/java-j2ee-training-course)** 培训 *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这个“Java 项目”博客的评论部分提到它，我们会尽快回复您。