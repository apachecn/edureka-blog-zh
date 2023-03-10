# 什么是 Java 中的动态绑定，如何使用？

> 原文：<https://www.edureka.co/blog/dynamic-binding-in-java/>

Java 中的动态绑定是每个程序员都必须熟悉的基本概念，因为它解决了各种实时问题。本文将涉及以下几点:

*   [静态绑定](#StaticBinding)
*   [动态绑定](#DynamicBinding)
*   [静态和动态绑定的区别](#DifferencebetweenStaticandDynamicBinding)

java 中的动态绑定是每个程序员都必须熟悉的基本概念。为了理解动态绑定的工作原理，我们必须了解另一种类型的绑定，即静态绑定。

继续这篇关于 Java 动态绑定的文章

**静态绑定**

也称为早期绑定，它是由编译器在编译时解析的绑定。

必须注意，私有、最终和静态方法的绑定是在编译时完成的。这是因为静态绑定提供了更好的性能。编译器知道这些方法不能被重写，并且总是由局部类的对象访问。因此，编译器很容易确定类(局部类)的对象。

**举例:**

```
public class Main
{
public static class superclass
{
static void print()
{
System.out.println("This is the superclass");
}
}
public static class subclass extends superclass
{
static void print()
{
System.out.println("This is the subclass");
}
}
public static void main(String[] args)
{
superclass sup = new superclass();
superclass sub = new subclass();
sup.print();
sub.print();
}
}

```

在上面给出的例子中，超类的 print 方法是静态的，编译器知道它不能在子类中被覆盖。因此，代码的输出如下:

**输出:** 这是超类这是超类

继续这篇关于 Java 动态绑定的文章

**Java 中的动态绑定**

在这种类型的绑定中，要调用的方法不是由编译器决定的。动态绑定的一个合适的例子是重写。这里，父类和子类有相同的方法。

**举例:**

```
public class Main
{
public static class superclass
{
void print()
{
System.out.println("This is superclass");
}
}
public static class subclass extends superclass
{
@Override
void print()
{
System.out.println("This is subclass");
}
}
public static void main(String[] args)
{
superclass sup = new superclass();
superclass sub = new subclass();
sup.print();
sub.print();
}
}

```

**输出:**

在上面给出的例子中，编译器不知道要调用的打印。编译器通过引用变量而不是对象的类型来工作。因此，绑定被推迟到运行时。这是超类，这是子类

继续这篇关于 Java 动态绑定的文章

**静态和动态绑定的区别**

静态绑定由私有、静态和最终成员使用。对于 Java 中的虚方法，绑定是在运行时根据运行时对象完成的。静态绑定使用类型信息，而动态绑定使用对象进行绑定。 α静态支持重载，动态绑定支持重写。

这样，我们就结束了这篇关于“Java 中的动态绑定”的文章。如果你想了解更多，可以去看看 Edureka 值得信赖的在线学习公司提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。