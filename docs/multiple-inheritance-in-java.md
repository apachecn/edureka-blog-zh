# 如何在 Java 中实现多重继承？

> 原文：<https://www.edureka.co/blog/multiple-inheritance-in-java/>

本文将帮助您实现一个用 Java 无法实现的概念。我指的是 Java 中的多重[继承。本文将涉及以下几点:](https://www.edureka.co/blog/inheritance-in-java/)

*   [Java 中的多重继承](#MultipleInheritanceInJava)
*   [样本程序](#SampleProgram)
*   [多重继承无歧义](#MultipleInheritanceWithoutAmbiguity)

让我们从这篇 Java 多重继承的文章开始，

## **Java 中的多重继承**

面向对象编程为用户提供了多重继承的特性，其中一个类可以继承多个父类的属性。简单来说，多重继承意味着一个类扩展多个类。

java 编程语言不能直接利用这个特性。这可以通过使用接口间接实现。

继续这篇关于 Java 多重继承的文章，

## **样本程序**

在下面的例子中，我们有两个界面:摩托车和自行车。摩托车界面由速度属性组成。方法是 totalDistance()。循环接口由属性距离()和方法速度()组成。

这两个接口都由 TwoWheeler 类实现。

```
interface MotorBike
{
int speed=50;
public void totalDistance();
}
interface Cycle
{
int distance=150;
public void speed();
}
public class TwoWheeler implements MotorBike,Cycle
{
int totalDistance;
int avgSpeed;
public void totalDistance()
{
totalDistance=speed*distance;
System.out.println("Total Distance Travelled : "+totalDistance);
}
public void speed()
{
int avgSpeed=totalDistance/speed;
System.out.println("Average Speed maintained : "+avgSpeed);
}
public static void main(String args[])
{
TwoWheeler t1=new TwoWheeler();
t1.totalDistance();
t1.speed();
}
}

```

**输出**

总行程:7500

保持的平均速度:150

上面给出的程序避免了歧义，即使使用类而不是接口。但是，Java 不支持。当两个类中有相同的方法时，编译器无法决定调用哪个方法。使用接口避免了这种模糊性，因为默认情况下接口的方法是抽象的。

继续这篇关于 Java 多重继承的文章，

## **多重继承无歧义**

```
interface InterfaceOne
{
public void disp();
}
interface InterfaceTwo
{
public void disp();
}
public class Main implements InterfaceOne,InterfaceTwo
{
@Override
public void disp()
{
System.out.println("display() method implementation");
}
public static void main(String args[])
{
Main m = new Main();
m.disp();
}
}

```

**输出**

display()方法实现

Main 方法实现两个接口，即 InterfaceOne 和 InterfaceTwo。它执行起来没有任何歧义。

让我们看另一个例子来更好地理解多重继承:

界面信号

{

默认 void singRock(){

System.out.println("我在唱摇滚")；

}

}

界面舞蹈

{

默认 void danceSlow(){

System.out.println("我在慢舞！");

}

}

公共类人类工具唱歌，跳舞

{

公共静态 void main(String[] args)

{

人类 h =新人类()；

h . singrock()；

h . dances low()；

}

}

**输出**

我在唱摇滚

我跳得很慢！

***因此，多重继承可以通过本文讨论的方法实现。***

这样，我们就结束了这篇关于“Java 中的多重继承”的文章。如果您想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 在线课程](https://www.edureka.co/java-j2ee-training-course)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。