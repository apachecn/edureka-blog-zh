# Java 中的访问修饰符:您需要知道的一切

> 原文：<https://www.edureka.co/blog/access-modifiers-in-java/>

Java 中的访问修饰符用于指定类、变量方法和构造函数的访问级别。它帮助更新一个 [*变量*](https://www.edureka.co/blog/java-tutorial/#variables) 的值。它们也被称为*可见性修改器。*通过这个博客的媒介，我将帮助你理解 [*Java*](https://www.edureka.co/blog/what-is-java/) 中访问修饰符的重要性。

我将按照以下顺序讲述这些主题:

*   什么是访问修饰符？
*   [访问修饰符的类型](#Types_of_Access_Modifier)
    *   [默认访问修饰符](#Default_Access_Modifier)
    *   [私人访问修饰符](#Private_Access_Modifier)
    *   [公共访问修饰符](#Public_Access_Modifier)
    *   [受保护的访问修饰符](#Protected_Access_Modifier)
*   [用方法覆盖访问修饰符](#Access_modifiers_with_method_overriding)
*   [访问控制和继承](#Access_Control_and_Inheritance)

让我们从第一个话题开始。

什么是访问修饰符？

你可能在练习任何一个[](https://www.edureka.co/blog/java-programs/)Java 程序的时候遇到过 *public* 、 *private* 和 *protected* 关键字，这些被称为访问修饰符。顾名思义，Java 中的访问修饰符有助于限制类、构造函数、变量、方法或数据成员的范围。

可以为类、构造函数、字段和方法分别指定访问修饰符。它们也被称为 *Java 访问说明符* ，但正确的名称是 **Java 访问修饰符**。

那么，让我们深入研究一下 Java 中不同类型的访问修饰符。

**访问修饰符的类型**

在 [*Java*](https://www.edureka.co/blog/java-tutorial/) 中有四个访问修饰符关键字，它们是:

*   默认访问修饰符
*   私有访问修饰符
*   公共访问修饰符
*   受保护的访问修饰符

让我们详细了解一下他们每一个人。

**默认访问修饰符**

当没有为一个特定的类、方法或数据成员指定访问修饰符时，我们称之为具有 *默认* 访问修饰符。

没有使用任何入口修饰符声明的日期成员、 [*类*](https://www.edureka.co/blog/java-tutorial/#obj) 或方法将具有默认修饰符，该修饰符只能在类似的包中访问。它意味着你没有为一个类、字段、方法等显式声明一个访问修饰符。

示例:

```

package p1;

//Class Course is having Default access modifier

class Course{

void display()

{
System.out.println("Hello World!");

}

}

```

接下来，让我们进入下一个类型，私有访问修饰符。

**私人访问修饰符**

*   声明为私有的方法或数据成员只能在声明它们的类中访问。
*   顶级类或接口不能被声明为私有，因为

*   如果一个类有一个私有构造函数  ，那么你就不能从这个类的外部创建这个类的对象。
*   不能用*私有访问修饰符*来标记类。
*   用 private 访问修饰符表示一个类意味着没有不同的类可以访问它。这通常意味着你不能通过任何想象来利用这个类。这样，私有访问修饰符就不会考虑类。

    ***注意*** :类或接口不能声明为私有。

    语法:

    ```
    public class Clock {
        private long time = 0;
    }

    ```

    看一个例子来清楚地了解这个私有访问修饰符。

    示例:

    ```
    package p;
    class A {
    private void display(){
    System.out.println("Edureka");
    }
    }
    class B {
    public static void main(String args[]){
    A obj = new A();
    //trying to access private method of another class
    obj.display();
    }
    }
    ```

    这个程序的输出是:

    `error: display() has private access in A`

    `obj.display();`

    希望你们清楚私有访问修饰符。接下来，让我们转到下一个类型，公共访问修饰符。

    **公共访问修饰符**

    *   使用关键字 ***public 指定公共访问修饰符。***
    *   在所有其他访问修饰符中，public 访问修饰符的范围很广。
    *   [*类*](https://www.edureka.co/blog/java-tutorial/#obj) ，被声明为*公共*的方法或数据成员在整个  程序中的任何地方都是  可访问的。对公共数据成员的范围没有限制。

    语法:

    ```
    package edureka.co;
    public class PublicClassDemo {
    // Here I didnt mention any modifier so it acts as a default modifier
    public int myMethod(int x){
    return x;
    }
    }
    ```

    现在，看一个例子来清楚地了解这个公共访问修饰符。

    示例:

    ```

    package p1;
    public class A
    {
    public void display()
    {
    System.out.println("edureka!");
    }
    }

    ```

    ```
    package p2;
    import p1.*;
    class B
    {
    public static void main(String args[])
    {
    A obj = new A;
    obj.display();
    }
    }

    ```

    输出:edureka！

    这就是 Java 中关于公共访问修饰符的一切。

    让我们前进到 Java 中的下一个访问修饰符，受保护的访问修饰符。

    **受保护的访问修饰符**

    *   使用关键字 **protected** 指定受保护的访问修饰符。
    *   声明为 protected 的方法或数据成员可以在同一个包或不同包的子类中访问。
    *   受保护成员只能在子类或派生类中访问。

    ***语法:***

    ```
    package packageFourProtected;
    public class ProtectedClassFour
    {
    protected int myMethod(int a){
    return a;
    }
    }
    ```

    让我们看一个例子。

    示例:

    ```
    spackage p1;
    //Class A
    public class A
    {
    protected void display()
    {
    System.out.println(" Java Certification Training");
    }
    }

    ```

    ```

    package p2;

    import p1.*; //importing all classes in package p1
    //Class B is subclass of A
    class B extends A |
    {
    public static void main(String args[])
    {
    B obj = new B();
    obj.display();
    }
    }

    ```

    ![Output - Access modifiers in Java - Edureka](img/c51f0af0b2ddeb727bc964e608e65ac5.png)

    这是你需要知道的关于 Java 中访问修饰符下不同方法的一切。让我们进入下一个话题。

    **用方法覆盖访问修饰符**

    如果您正在重写任何方法，那么在子类中声明的被重写的方法不能是限制性的。

    看看下面的例子。

    ```
    class A
    {
    protected void msg()
    {
    System.out.println("Hello java");
    }
    }
    public class Simple extends A { void msg()
    {
    System.out.println("Hello java");
    }
    //C.T.Error
    public static void main(String args[])
    {
    Simple obj=new Simple();
    obj.msg();
    }
    }
    ```

    默认修饰符比受保护修饰符更严格。这就是为什么会出现编译时错误。

    **访问控制和继承**

    *   如果你创建了某个类的一个子类，那么这个子类中的方法不能有比超类更难访问的访问修饰符。
    *   例如，如果超类中的一个方法是*公共的*，那么它在子类中也必须是公共的。如果超类中的一个方法是*保护的，*那么它在指定的子类中必须是保护的或公共的。
    *   声明为私有的方法根本不会被继承。

    这就把我们带到了本文的结尾，在这里我们学习了关于 Java 中访问修饰符的 *[常见问题](https://www.edureka.co/blog/interview-questions/java-interview-questions/)* 。希望你清楚本教程中与你分享的所有内容。

    ***确保你尽可能多的练习，恢复你的经验。***

    如果你觉得这篇文章与“Java 中的访问修饰语”相关，可以看看 *Edureka 的 [Java 课程](https://www.edureka.co/java-j2ee-training-course)* ，这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。 *我们在这里帮助你踏上成为 java 开发者的每一步。除了这些 Java 面试问题，我们还为想成为 Java 开发者的学生和专业人士设计了一套课程。该课程旨在为您提供 Java 编程的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

    如果您遇到任何问题，请在“Java 中的访问修饰符”的评论部分自由提问，我们的团队将很乐意回答。