# 关于 Java 中的 Final、Finally 和 Finalize，你需要知道的就是

> 原文：<https://www.edureka.co/blog/final-finally-and-finalize-in-java/>

如果你以前有过 **[Java 面试](https://www.edureka.co/blog/interview-questions/java-interview-questions/)** 的经验，那么你可能会注意到面试官往往会问一些通常从基本概念中挑选出来的刁钻问题。最常被问到的一个问题是如何区分 Java[中的 final、finally 和 finalize。通过这篇文章，我将在 Java 中的 final、finally 和 finalize 之间划出一条清晰的界限，这将帮助你获得更好的见解。](https://www.edureka.co/blog/java-tutorial/)

在这篇文章中，我将涉及以下主题:

*   [最终关键字](#final)
*   [终于挡住](#finally)
*   [敲定方法](#finalize)
*   [对照表 Java 中的 Final、Final 和 Finalize](#comparison)

那么，让我们从 Java 中 final、finally 和 finalize 的第一个关键字开始。

## **最终关键字**

在 Java 中，final 是一个关键字，也可以用作访问修饰符。换句话说，final 关键字用于限制用户的访问。它可用于各种环境，如:

1.  [最终变量](#finalvariable)
2.  [最终方法](#finalmethod)
3.  [期末班](#finalclass)

对于其中的每一个，final 关键字都有不同的效果。现在让我们来看看它是如何逐一影响它们的。

### **1。最终变量**

每当 [Java](https://www.edureka.co/blog/what-is-java/) 中的 final 关键字与变量、字段或参数一起使用时，这意味着一旦引用被传递或实例化完成，其值就不能在整个程序执行过程中改变。如果一个没有任何值的[变量](https://www.edureka.co/blog/java-tutorial/#variables)被声明为 final，那么它被称为空白/未初始化的 final 变量，只能通过构造函数初始化。

现在让我们看一个例子。

```
public class A {
int var1 = 123;
//declaring final variables
final int var2 = 345;
final int var3;

//Trying to initialize a blank final variable
var = 555; //Error

A (){
var1 = 111; //No Error
var2 = 333; //Compilation Error

//Initializing a blank final variable
var3 = 444; //No Error
}

//passing final parameters
void avg(int param1, final int param2){
param1 = 2345; //No Error
param2 = 1223; //Compilation Error
}

//declaring final fields
void show(){
final int fieldVal = 300000;
fieldVal = 400000; //Error
}

}
```

所以，这就是 final 关键字如何影响变量的全部内容，现在让我们看看它是如何影响一个方法的。

### **2。最终方法**

在 Java 中，每当一个方法被声明为 final 时，在整个程序执行过程中，它不能被任何子类覆盖。

让我们看一个例子。

```

//FINAL METHOD
class A {
final void method_abc(){
System.out.println("This is a Final method and cannot be overridden");
}

void method_xyz(){
System.out.println("This is a normal method and can be overridden");
}
}

class B extends A {
void method_abc{
//Compile Time Error
}

void method_xyz(){
System.out.println("This is an overridden method in class B");
}

}

```

到目前为止，你已经看到了将一个变量和一个方法声明为 final 的结果，现在让我们进一步看看当一个类在 Java 中被声明为 final 时会发生什么。

### **3。最后一堂课**

在 Java 中，每当一个类被声明为 final，它就不能被任何子类继承。这是因为，一旦一个类被声明为 final，该类中包含的所有数据成员和方法都将被隐式声明为 final。同样，一旦一个类被声明为 final，它就不能再被声明为 abstract。换句话说，一个类可以是两者之一，final 或 abstract。

让我们看一个例子。

```

//FINAL CLASS
final class A {
//class body
}

class B extends A{ //Compilation Error
//class body
}

```

我希望到现在为止，你已经清楚地了解了 final 关键字的工作原理。所以，现在让我们继续这篇关于 Java 中的 final、finally 和 finalize 的文章，找出 finally 关键字的作用。

## **最终阻塞**

在 Java 中，finally 是一个可选块，用于[异常处理](https://www.edureka.co/blog/java-exception-handling)。它前面通常有一个 try-catch 块。最后，块用于执行重要的代码，如资源清理或释放内存使用等。无论异常是否被处理，finally 块都将被执行。因此，将清理代码包装在 finally 块中被认为是一种好的做法。您还可以将它与 try 块一起使用，而不需要任何 catch 块。

现在让我们来看一个同样的例子。

```
class A {
public static void main(String args[]) {
try {
System.out.println("Try Block");
throw new Exception();
} catch (Exception e) {
System.out.println("Catch Block");
} finally {
System.out.println("Finally Block");
}
}
}

```

到现在为止，我已经讨论了 Java 中的 final 和 final 关键字。现在让我们来看看三个关键字中的最后一个，也就是 Java 中的 finalize 关键字。

## **完成方法**

Finalize 是一个在 Object 类中定义的受保护的非静态方法，因此可用于 Java 中的任何和所有对象。这个方法是在对象被完全销毁之前由垃圾收集器调用的。有时，一个[对象](https://www.edureka.co/blog/java-tutorial/#obj)可能必须在被破坏之前完成一些重要的任务，比如关闭一个打开的连接，释放一个资源等等。如果这些任务没有完成，可能会降低程序的效率。因此，垃圾收集器为那些不再被引用并被标记为垃圾收集的对象调用它。

这个方法被声明为 protected，以限制它在类外的使用。但是您可以在垃圾回收时从类内部重写它以定义它的属性。

让我们看一个同样的例子。

```

public class A {
public void finalize() throws Throwable{
System.out.println("Object is destroyed by the Garbage Collector");
}
public static void main(String[] args) {

Edureka test = new Edureka();
test = null;
System.gc();
}
}

```

就这样，我们结束了这篇关于 final 的文章，最后用 Java 和 finalize。最后，我添加了所有三个关键字之间的比较，这将有助于您一目了然地获取主要差异。

## **对照表–Java 中的 Final vs Finally vs Finalize 关键字**

| **因子** | **决赛** | **最后** | **最终确定** |
| ***定义*** | Final 是一个关键字，在 Java 中用作访问修饰符 | 最后是 Java 中用于异常处理的块 | Finalize 是 Java 中用于垃圾收集的方法 |
| ***应用*** | Java 中的 Final 与变量、方法和类一起使用来设置访问权限 | Finally 块与 try 和 catch 块一起使用 | Java 中的 Finalize 方法用于不再使用的对象 |
| ***功能*** | Final variable in Java is a constant whose value can’t be changed once assigned.Java 中的 Final 方法不能被它的子类覆盖。Java 中的 Final 类不能被任何子类继承。 | Java 中的 Finally 块有助于清理 try 块中已经使用的资源 | Finalize 方法有助于在对象被垃圾收集器销毁之前清理对象的活动 |
| ***执行*** | 被编译器调用时执行 | 在 try-catch 块执行后立即执行 | 它在对象被销毁之前执行 |

我希望通过这次 Java 的 Final，Finally 和 Finalize，我能够理清这些概念，并帮助你增加知识的价值。

*If you found this article on “Final, Finally and Finalize in Java**” relevant, **check out the [**Java Certification Training**](https://www.edureka.co/java-j2ee-training-course)**by Edureka, a trusted online learning company with a network of more than 250,000 satisfied learners spread across the globe. **Got a question for us? Please mention it in the comments section of this *Final, Finally and Finalize in Java* and we will get back to you.*