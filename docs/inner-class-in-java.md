# 如何在 Java 中实现内部类？

> 原文：<https://www.edureka.co/blog/inner-class-in-java/>

java 中的内部类意味着一个类是另一个类的成员。在 [Java](https://www.edureka.co/blog/java-tutorial/) 中，有各种类型的内部类。这篇文章将帮助你解开所有这些类。将详细讨论以下指针，

*   [嵌套内部类](#NestedInnerclass)
*   [方法局部内部类](#MethodLocalinnerclasses)
*   [匿名内部类](#Anonymousinnerclasses)
*   [静态嵌套类](#Staticnestedclasses)

让我们从 Java 文章中的这个内部类开始，

## **Java 中的内部类**

**嵌套内部类**

这个类可以访问外部类的任何私有实例值。Java 也允许在另一个类中编写一个类。内部编写的类称为嵌套类，包含内部类的类称为外部类。

**语法**

```
class outerplace
{
class innerplace
{
}
}

```

**例子**

在下面给出的例子中，我们将内部类设为私有，并在方法的帮助下访问该类。

```
class Outer_place
{
int num;
private class Inner_place
{
public void print()
{
System.out.println("It is an inner class");
}
}
void display_Inner()
{
Inner_place inner = new Inner_place();
inner.print();
}
}
public class My_class
{
public static void main(String args[])
{
Outer_place outer = new Outer_place();
outer.display_Inner();
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/4d20b920ab3a6745cfdbac2fb54729b0.png)

在这里，外部地方是外部类，内部地方被称为内部类。

继续这篇 Java 文章中的内部类，

## **访问私有成员**

内部类也用于访问类的私有成员。假设有一个类拥有私有成员来访问它们。现在，在类中编写一个内部类，并从内部类的方法中访问私有成员。

这是一个例子，

```
class Outer_place
{
private int num = 162;
class Inner_place
{
public int getNum()
{
System.out.println("It is a getnum method of inner class:");
return num;
}
}
}
public class My_class
{
public static void main(String args[])
{
Outer_place outer = new Outer_place();
Outer_place.Inner_place inner = outer.new Inner_place();
System.out.println(inner.getNum());
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/110cfbc5dac9c745b0394c9af22831b2.png)

继续前进，

**局部内部类的方法**

在 Java 中，你可以在方法中写一个类，这就是所谓的局部类型。像所有的局部变量一样，内部类的范围被限制在一个方法中。

**例子**

下面的例子将展示一个方法局部内部类是如何实现的。

```
public class Outerplace
{
void my_Method()
{
int num = 45;
class MethodInner_place
{
public void print()
{
System.out.println ("method for inner classes "+num);
}
}
MethodInner_place inner = new MethodInner_place();
inner.print();
}
public static void main(String args[])
{
Outerplace outer = new Outerplace();
outer.my_Method();
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/bd19a52aaa8eadcbee88443a40ba38ec.png)

继续这篇 Java 文章中的内部类，

**匿名内部类**

任何不带类名声明的内部类都称为匿名内部类。在匿名内部类的情况下，我们同时实例化和声明它。

每当我们想要覆盖类或接口的方法时，我们就使用这个类。

**语法**

```
AnonymousInner obj1 = new AnonymousInner()
{
public void method()
{
}
};

```

**例子**

```
abstract class AnonymousInner
{
public abstract void mymethod();
}
public class Outer_class
{
public static void main(String args[])
{
AnonymousInner inner = new AnonymousInner()
{
public void mymethod()
{
System.out.println(" example of anonymous inner class");
}
};
inner.mymethod();
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/71e114c68dda4f46d5e91f6027d48377.png)

继续这篇 Java 文章中的内部类，

**作为匿名内部类**的参数

在这种情况下，如果一个方法接受接口、抽象类或具体类的对象，那么我们就能够实现接口，将对象传递给方法并扩展抽象类。

**语法**

```
obj. method
(
new class()
{
public void do
{
}
} );

```

**例子**

```
// interface
interface Message
{
String greet();
}
public class My_class {
//object of interface message is accepted by this method
public void displayMessage(Message m)
{
System.out.println(m.greet() +
", example of anonymous inner class as argument");
}
public static void main(String args[])
{
//Instantiating of class
My_class obj = new My_class();
//Passing the anonymous inner class as argument
obj.displayMessage(new Message()
{
public String greet()
{
return "Hey";
}
});
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/907a48532c1fa72e784738982505b3a5.png)

继续这篇 Java 文章中的内部类，

#### **指定子类的匿名内部类**

**源代码**

```
class Demo
{
void show()
{
System.out.println("i was in show method of class");
}
}
class Flavor1Demo
{
static Demo d = new Demo()
{
void show()
{
super.show();
System.out.println("i was present in Flavor1Demo class");
}
};
public static void main(String[] args)
{
d.show();
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/b9571dd80e9fb0b71b64719ae1d22fad.png)

继续这篇 Java 文章中的内部类，

**匿名内部类作为指定** **接口**的实现者

**源代码**

```
class Flavor2Demo
{
//class which implements Hello interface
static Hello h = new Hello()
{
public void show()
{
System.out.println("i was present in anonymous class");
}
};
public static void main(String[] args)
{
h.show();
}
}
interface Hello
{
void show();
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/52dc7242586e2ae21a3e6d2f11b8ec84.png)

继续这篇 Java 文章中的内部类，

**静态嵌套类**

这些类在技术上不被称为内部类。这些类类似于外部类的静态成员。静态嵌套类不能访问外部类的变量和方法。我们不需要实例化外部类，可以使用静态成员直接访问它。

**语法**

```
Class outer
{
Static class nested_example{
}
}

```

**例子**

```
public class Outer
{
static class Nested_Example
{
public void my_method()
{
System.out.println("It is the nested class");
}
}
public static void main(String args[])
{
Outer.Nested_Example nested = new Outer.Nested_Example();
nested.my_method();
}
}

```

**输出**

![Output - Inner Class In Java - Edureka](img/24a4c86ebc481923d1710d3b673e1d56.png)

我们就此结束了这篇文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。