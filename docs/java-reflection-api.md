# Java 反射 API:您需要知道的一切

> 原文：<https://www.edureka.co/blog/java-reflection-api/>

**[Java](https://www.edureka.co/blog/java-tutorial/) 反射** 是一个 *在运行时检查或修改类的运行时行为的过程* **。** **Java 反射 API** 用于操纵类及其成员，包括字段、方法、构造函数等。在运行时。在本文中，我们将详细了解 Java 反射 API。

本文将关注以下几点:

*   【Java 反射 API 用在哪里？
*   java.lang.reflect 包中的[类](#Classinjava.lang.reflectPackage)
*   [Java . lang . class 中使用的方法](#Methodsusedinjava.lang.Class)
*   [如何获取 Class 类的对象？](#HowtogettheobjectofClassclass?)
*   [使用 Java 反射 API 的优缺点](#AdvantagesandDisadvantagesofUsingJavaReflectionAPI)

因此，让我们从这篇关于 Java 反射 API 的文章中的这些指针开始

## **Java 反射 API 用在哪里？**

反射 API 主要用于:

*   IDE(集成开发环境),如 Eclipse、MyEclipse、NetBeans 等。
*   调试器
*   测试工具等。

那么 Java lang 反射包中的类是什么呢？

## **Java . lang . reflect 包中的类？**

下面是 java.lang.package 中实现反射的各种 Java 类的列表-

*   **字段** :这个类用于收集声明性信息，比如数据类型、访问修饰符、变量名和值。
*   **方法** :该类用于收集声明性信息，如方法的访问修饰符、返回类型、名称、参数类型和异常类型。
*   **构造函数** :这个类用于收集声明性信息，比如构造函数的访问修饰符、名称和参数类型。
*   修饰符 :这个类用来收集特定访问修饰符的信息。

让我们来看看 Java 反射 API 方法，

## **Java . lang . class 中使用的方法**

| **方法** | **描述** |
| 公共字符串 getName() | 返回类名 |
| 公共静态类 forName(String className)抛出 ClassNotFoundException | 加载类，返回类 class 的引用。 |
| 公共对象 newInstance()抛出 InstantiationException，IllegalAccessException | 创建新实例。 |
| 公共布尔 isInterface() | 检查是否是接口。 |
| public boolean isArray() | 检查它是否是数组。 |
| public boolean is primitive() | 检查它是否是原始的。 |
| 公共类 getSuperclass() | 返回超类的类引用。 |
| 公共字段[] getDeclaredFields()抛出安全异常 | 返回该类的字段总数。 |
| 公共方法[] getDeclaredMethods()抛出安全异常 | 返回该类方法的总数。 |
| 公共构造函数[] getDeclaredConstructors()抛出安全异常 | 返回该类构造函数的总数。 |
| 公共方法 getDeclaredMethod(String name，Class[] parameterTypes)抛出 NoSuchMethodException，SecurityException | 返回方法类实例。 |

让我们带着文章前进，

## **如何获取 Class 类的对象？**

有 3 种方法可以获得类 Class 的实例。它们如下:

*   for Class 类的 Name()方法
*   对象类的 getClass()方法
*   the。类语法

### **for Class 类的 Name()方法**

*   用于动态加载类。
*   返回 Class 类的实例。
*   如果您知道类的完全限定名，应该使用它。这不能用于基元类型。

让我们来看看 forName()方法的简单例子。

```
class Simple{}
class Test{
public static void main(String args[]){
Class c=Class.forName("Simple");
System.out.println(c.getName());
}
}

```

**输出:**

简单

### **Java 反射:对象类的 API getClass()方法**

它返回 Class class 的实例。如果你知道类型，就应该使用它。此外，它可以与原语一起使用。

```
class Simple{}
class Test{
void printName(Object obj){
Class c=obj.getClass();
System.out.println(c.getName());
}
public static void main(String args[]){
Simple s=new Simple();
Test t=new Test();
t.printName(s);
}
}

```

**输出:**

简单

### **The。类语法**

如果一个类型是可用的，但是没有实例，那么可以通过添加。类”添加到该类型的名称。它也可以用于原始数据类型。

```
class Test{
public static void main(String args[]){
Class c = boolean.class;
System.out.println(c.getName());
Class c2 = Test.class;
System.out.println(c2.getName());
}
}

```

**输出:**

布尔型

测试

现在让我们继续这篇 Java 反射 API 文章

## **使用 Java 反射 API 的优缺点**

### **使用 Java 反射 API 的优势**

*   **可扩展性特性:** 应用程序可以通过使用完全限定名创建可扩展性对象的实例来利用外部的、用户定义的类。
*   **调试和测试工具** :调试器使用反射的属性来检查类中的私有成员。

### **使用 Java 反射 API 的缺点**

*   **性能开销:** 反射操作的性能比非反射操作慢，应该避免在对性能敏感的应用程序中频繁调用的代码段中使用。
*   内部暴露: 反射代码打破了抽象，因此可能会随着平台的升级而改变行为。

至此，我们已经结束了这篇关于“Java 反射 API”的文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。