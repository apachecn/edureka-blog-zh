# Java 中有哪些不同类型的类？

> 原文：<https://www.edureka.co/blog/types-of-classes-in-java/>

一个类对于用 Java 编码来说，就像我们为了生存而呼吸一样重要。你可能正在使用 Java 中的一个基本 *[类，或者你可能是一个初学者，不要担心，我已经为你准备好了一切。这篇关于“Java 中类的类型”的文章将帮助你深入了解在](https://www.edureka.co/blog/java-objects-and-classes/)*[Java 编程中使用的各种类型的类。](https://www.edureka.co/blog/cheatsheets/java-cheat-sheet/)**

我将讨论以下主题:

*   [Java 中有哪些类？](#whatareclasses)
*   [Java 中的类类型](#types)
    *   [POJO 类](#pojo)
    *   [静态类](#static)
    *   [混凝土类](#concrete)
    *   [抽象类](#abstract)
    *   [期末班](#final)
    *   [内部类](#inner)
        *   [嵌套内部类](#nestedinner)
        *   [方法局部内部类](#method)
        *   [匿名内部阶层](#anonymous)
        *   [静态嵌套类](#staticnested)

在讨论类的类型之前，让我们先了解一下*Java*中的类是什么？

## **Java 中有哪些类？**

Java 中的 *[类](https://www.edureka.co/blog/java-objects-and-classes/)* 是用于创建和定义[对象](https://www.edureka.co/blog/java-object/)、对象数据类型和[方法](https://www.edureka.co/blog/java-methods/)的模板。类作为一个整体是类别，而对象是每个类别中的项目。类声明由以下部分组成:

**JAVA 中的类类型**

现在让我们了解 Java 中不同类型的类。

### **POJO 类**

POJO 代表“[普通旧 Java 对象](https://www.edureka.co/blog/pojo-in-java/)”。只包含私有变量以及使用这些变量的 setter 和 getter 方法的类称为 POJO 类。它是一个纯数据结构，有字段，可以覆盖 Object(如 equals)或 serializable 等其他接口的一些方法，但没有自己的行为。

**POJO 类的属性—**

*   编写 POJO 类时，公共 setter 和 getter 方法是必须的。
*   所有实例变量都应该是私有的。
*   它不应该扩展预先指定的类。
*   它不应该实现预先指定的接口。
*   不应包含预先指定的批注。
*   它可能没有无参数构造函数。

**例子**

```
class POJO {
  private int value=365;
  public int getValue() {
      return value;
   }
   public void setValue(int value) {
      this.value = value;
   }
}
public class Test {
   public static void main(String args[]){
      POJO p = new POJO();
      System.out.println(p.getValue());
   }
}

```

**输出** 365

### **静态类**

在 *[Java](https://www.edureka.co/blog/what-is-java/)* 中，静态是用来描述对象在内存中如何被管理的关键字。静态对象专门属于该类，而不是该类的实例。该类的唯一目的是提供其继承类的蓝图。静态类只能包含静态成员。不能为静态类创建对象。

**例子**

```
 public class Bank
{
private static String note = "Bank";
public static class SBISavings
{
public void displayOutput()
{
System.out.println(" SBISaving is: " + note);
}
}
}
public static void main(String[] args)
{
//creating instance of static class Bank.
SBISavings bs = new Bank.SBISavings();
//calling the method
bs.displayOutput();
} 
```

**输出**

SBISavings 为:银行

**示例:使用静态类将两个数相加。**

```
 import java.util.Scanner;
class staticclasses
{
static int s;
// static variable
static void met(int a, int b)
{
// static method
System.out.println("static method to calculate sum");
s = x + y;
System.out.println(x + "+" + y);
// print two numbers
}
static class MyNestedClass
{
// static class 
static
{
// static block
System.out.println("static block inside a static class");
}
public void disp()
{
int x1, y1;
Scanner sc = new Scanner(System.in);
System.out.println("Enter two numbers");
x1 = sc.nextInt();
y1 = sc.nextInt();
met(x1, y1);
// calling static method
System.out.println("Sum of the two numbers-" + s);
// print the result in static variable
}
}
}
public class Test
{
public static void main(String args[])
{
staticclasses.MyNestedClass mnc = new staticclasses.MyNestedClass();
// object for static class
mnc.disp();
// accessing methods inside a static class
} 
```

**输出** 静态块内部一个静态类输入两个数字 11 13 静态方法计算总和 11+13T7 两个数字的总和-24

### **混凝土类**

任何没有任何抽象方法的普通类，或者所有方法都有实现的类，基本上都是一个*具体类*。它们不能有任何未实现的方法。一个具体的类可以扩展它的父类、抽象类或者实现一个接口，如果它实现了它们所有的方法 。 是一个完整的可以实例化的类。

**例子**

```
public class Concrete { // Concrete Class
   static int sum(int x, int y) {
      return a + b;
   }
   public static void main(String args[]) {
      int p = sum(6, 8);
      System.out.println("Sum: " + p);
   }
}

```

**输出**

总和:14

### **抽象类**

抽象类是用抽象关键字声明的，并且有零个或多个抽象方法。这些类是不完整的类，因此，要使用抽象类，我们必须将抽象类扩展为具体类。它也可以有构造函数和静态方法。它可以有 final 方法，强制子类保持方法体不挂起。

上图有三种形状，矩形和圆形。形状是抽象的，而矩形和圆形是继承 shape 类的具体类。这是因为矩形和圆形实现了 area()方法。

**展示具体类如何扩展抽象类的示例代码**

```
 // Java program to illustrate concrete class
//This is an interface
interface X
{
int product(int x, int y);
}
// This is an abstract class
abstract class Product implements X
{
// this method calculates
// product of two numbers
public int product(int x, int y)
{
return x * y;
}
}
// This is a concrete class that implements
class Main extends Product
{
// main method
public static void main(String args[])
{
Main ob = new Main();
int p = ob.product(20, 10);
// print product
System.out.println("Product: " + p);
}
} 
```

**输出**

产品:200

### **期末班**

一旦一个变量、方法或类被声明为 final，它的值始终保持不变。方法声明中的 *[final](https://www.edureka.co/blog/final-finally-and-finalize-in-java/#final)* 关键字表示该方法不能被任何子类覆盖，即已声明为 final 的类不能被子类化。这在创建像 String 类这样的不可变类时很有帮助。一个类不能在不使一个类成为最终类的情况下使它成为不可变的。

**例子**

```
final class BaseClass {
   void Display() {
    System.out.print("This is the Display() method of BaseClass.");
   }
}
class DerivedClass extends BaseClass { //Compile-time error - can't inherit final class
   void Display() {
      System.out.print("This is Display() method of DerivedClass.");
   }
}
public class FinalClassDemo {
   public static void main(String[] arg) {
      DerivedClass d = new DerivedClass();
      d.Display();
   }
}

```

**输出**

不能从最终基类 继承

编译时错误——无法继承最终类

### **内部类**

内部类是指作为另一个类的成员的类。java 中有四种类型的[内部类](https://www.edureka.co/blog/inner-class-in-java/)。 1)嵌套内部类 2)方法局部内部类 3)匿名内部类 4)静态嵌套类

#### **嵌套内部类**

它可以访问外部类的任何私有实例变量。像任何其他实例变量一样，我们可以拥有 *[访问修饰符](https://www.edureka.co/blog/access-modifiers-in-java/)* 私有、受保护、公共和默认修饰符。

**一个展示演示内部类的例子:**

```
class Outer { 
   // Simple nested inner class 
   class Inner { 
      public void show() { 
           System.out.println("This is inside a nested class method "); 
      } 
   } 
} 
class Main { 
   public static void main(String[] args) { 
       Outer.Inner in = new Outer().new Inner(); 
       in.show(); 
   } 
} 

```

**输出**

这是在嵌套类方法中

#### **方法局部内部类**

内部类可以在外部类的方法中声明。

**例子**

```
class Outer { 
    void outerMethod() { 
        System.out.println("This is outerMethod"); 
        // Inner class is local to outerMethod() 
        class Inner { 
            void innerMethod() { 
                System.out.println("This is innerMethod"); 
            } 
        } 
        Inner y = new Inner(); 
        y.innerMethod(); 
    } 
} 
class MethodDemo { 
    public static void main(String[] args) { 
        Outer x = new Outer(); 
        x.outerMethod(); 
    } 
} 

```

**输出**

这是外部方法 这是内部方法

#### **匿名内部阶层**

匿名内部类是在没有任何名字的情况下声明的。它们可以通过两种方式创建。

**示例:作为指定类型的子类**

```
class Demo { 
   void show() { 
      System.out.println("This is show method of super class"); 
   } 
} 
class FlagDemo { 

   //  An anonymous class with Demo as base class 
   static Demo d = new Demo() { 
       void show() { 
           super.show(); 
           System.out.println("This is Flag1Demo class"); 
   } 
   }; 
   public static void main(String[] args){ 
       d.show(); 
   }
)

```

**输出**

这是一个超类的显示方法

这是 Flag1Demo 类

在上面的代码中，有两个类 Demo 和 FlagDemo。这里，demo 充当超类，匿名类充当子类，两个类都有一个方法 show()。在匿名类 show()中，方法被重写。

**举例:作为指定接口**的实现者

```
class Flag2Demo { 

    // An anonymous class that implements Hello interface 
    static Hello h = new Hello() { 
        public void show() { 
            System.out.println("This is an anonymous class"); 
        } 
    }; 

    public static void main(String[] args) { 
        h.show(); 
    } 
} 

interface Hello { 
    void show(); 
}

```

**输出**

这是一个匿名类

#### **静态嵌套类**

静态嵌套类就像外部类的静态成员。

```
class Outer { 
   private static void outerMethod() { 
     System.out.println("inside outerMethod"); 
   } 

   // A static inner class 
   static class Inner { 
     public static void main(String[] args) { 
        System.out.println("inside inner class Method"); 
        outerMethod(); 
     } 
   } 

}

```

**输出**

内类方法 内类方法外类方法

这就把我们带到了这篇文章的结尾。您已经了解了 Java 中存在的不同类型的类以及一些例子。

如果您觉得这篇“Java 中的类的类型”相关，请查看 Edureka 的 [Java 认证培训](https://www.edureka.co/java-j2ee-training-course)，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念，以及各种 [Java 框架](https://www.edureka.co/blog/java-frameworks/)，如 Hibernate & Spring。

有问题要问我们吗？请在“Java 类的类型”博客的评论部分提到它，我们会尽快回复您。