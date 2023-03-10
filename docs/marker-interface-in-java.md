# 如何用 Java 实现 Marker 接口？

> 原文：<https://www.edureka.co/blog/marker-interface-in-java/>

本文将向您简要介绍接口的一个有趣的方面，在 [Java](https://www.edureka.co/blog/java-tutorial/) 中称为标记接口，并继续介绍它的实现。本文将涉及以下几点:

*   [可串行化接口](#SerializableInterface)
*   [可克隆界面](#CloneableInterface)
*   [远程接口](#RemoteInterface)
*   [实现远程接口的步骤](#StepstoimplementRemoteInterface)
*   [定义一个远程接口](#DefineaRemoteInterface)
*   [实现远程接口](#ImplementtheRemoteInterface)
*   [创建并启动远程应用](#CreateandstarttheRemoteapplication)
*   [创建并启动客户端应用](#Createandstarttheclientapplication)

那么让我们开始吧，

标记接口是空的接口，即它不包含任何方法或字段。它也被称为标记接口，用于指示或通知 JVM 实现该接口的类将具有一些特殊的行为。使用标记接口可以实现对代码进行分类的有效方式。这种接口的例子有:可串行化的、可克隆的和远程接口。

本文介绍了 Java 中的标记接口

## **可串行化接口**

java 中的序列化可以定义为将对象的状态转换为字节流的过程。这可以通过使用 java.io.package 中的 serializable 接口来实现。

**举例:**

```
import java.io.*;
class Main implements Serializable
{
int j;
String s;
// A class constructor
public Main(int j,String s)
{
this.j = j;
this.s = s;
}
}
public class Test
{
public static void main(String[] args)
throws IOException, ClassNotFoundException
{
Main obj = new Main(25,"HelloWorld");
// Serializing 'obj'
FileOutputStream fos = new FileOutputStream("pqr.txt");
ObjectOutputStream oos = new ObjectOutputStream(fos);
oos.writeObject(obj);
// De-serializing 'obj'
FileInputStream fis = new FileInputStream("pqr.txt");
ObjectInputStream ois = new ObjectInputStream(fis);
Main b = (Main)ois.readObject(); //down-casting object
System.out.println(b.j+" "+b.s);
// closing streams
oos.close();
ois.close();
}
}

```

**输出:** 25 HelloWorld

本文介绍了 Java 中的标记接口

## **可克隆界面:**

这个接口可以在 java.lang 包中找到。克隆是生成具有不同名称的对象的副本或精确拷贝的机制。Cloneable 接口由一个类实现，以向 object.clone()方法指示该方法对该类的实例进行逐字段复制是合法的。调用克隆方法但未实现可克隆接口的类会引发 CloneNotSupportedException。

**举例:**

```
import java.lang.Cloneable;
class javaClone implements Cloneable
{
int j;
String s;
// Defining a class constructor
public javaClone(int j,String s)
{
this.j = j;
this.s = s;
}
// Overriding clone() method
@Override
protected Object clone()
throws CloneNotSupportedException
{
return super.clone();
}
}
public class Main
{
public static void main(String[] args)
throws CloneNotSupportedException
{
javaClone c = new javaClone(18, "HelloWorld");
// cloning 'c' and holding
// new cloned object reference in b
// down-casting
javaClone b = (javaClone)c.clone();
System.out.println(b.j);
System.out.println(b.s);
}
}

```

**输出:** 18 HelloWorld

本文介绍了 Java 中的标记接口

## **远程接口:**

远程对象可以定义为一个对象，它的方法可以从不同的 JVM(可能在另一个主机上)调用。这个接口可以在 java.rmi 包中找到。远程对象必须直接或间接实现此方法。

**RMI:**

远程方法调用是一个 API，它使一个对象能够调用在不同 JVM 中运行的对象上的方法。它使用以下对象在两个应用程序之间提供远程通信:存根和框架。

**存根:**

存根可以定义为出现在客户端的对象，代表远程对象。它创建一个信息块，包括: α远程对象的标识符 α要调用的方法的名称 α远程 JVM 的参数

**骨架:**

骨架对象的主要工作是将请求从存根传递到远程对象。此外，它还执行下面给出的任务: α它调用原始远程对象上所需的方法 α读取为远程对象指定的参数

本文介绍了 Java 中的标记接口

## **实现远程接口的步骤:**

## **定义一个远程接口:**

```
import java.rmi.*;
public interface AddAll extends Remote{
public int add(int r,int s)throws RemoteException;
}

```

这里，远程接口被扩展，RemoteException 用远程接口的所有方法声明。

本文介绍了 Java 中的标记接口

## **实现远程接口:**

有两种方法为远程接口提供实现: α扩展 UnicastRemoteObject 类 α使用 UnicastRemoteObject 类的 exportObject()方法

```
import java.rmi.*;
import java.rmi.server.*;
public class AddAllRemote extends UnicastRemoteObject implements Adder{
AddAllRemote()throws RemoteException{
super();
}
public int add(int r,int s){return r+s;}
}

```

使用 rmic (rmi 编译器)，创建存根和框架对象。

存根和框架对象可以通过使用 rmi 编译器来创建。rmi 工具调用 RMI 编译器来创建对象。rmic AddAllRemote

使用 rmiregistry 工具，启动注册表服务。

可以使用 rmregistry 工具启动注册表服务。如果用户没有指定，则使用默认端口号。rmiregistry 5000

本文介绍了 Java 中的标记接口

## **创建并启动远程应用。**

```
import java.rmi.*;
import java.rmi.registry.*;
public class Server{
public static void main(String args[]){
try{
AddAll stub=new AddAllRemote();
Naming.rebind("rmi://localhost:5000/sak",stub);
}catch(Exception e){System.out.println(e);}
}
}

```

在上面的例子中，远程对象被名称 sak 绑定。

本文介绍了 Java 中的标记接口

## **创建并启动客户端应用程序。**

在给出的例子中，服务器和客户机应用程序运行在同一台机器上。因此，正在使用本地主机。

```
import java.rmi.*;
public class Client{
public static void main(String args[]){
try{
AddAll stub=(AddAll)Naming.lookup("rmi://localhost:5000/sak");
System.out.println(stub.add(29,18));
}catch(Exception e){}
}
}

```

要从不同的机器访问远程对象，必须将本地主机名更改为远程对象所在的 IP 地址或主机名。

使用标记接口可以实现对代码进行分类的有效方式。

这样我们就结束了这篇文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的  [Java 在线培训](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。