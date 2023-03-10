# 关于 Java 中的实现，你需要知道的是

> 原文：<https://www.edureka.co/blog/implements-in-java/>

接口是 [Java](https://www.edureka.co/blog/java-tutorial/) 中 [OOPs](https://www.edureka.co/blog/object-oriented-programming/) 的一个重要方面。在这篇文章中，我们将理解什么是用 Java 实现的，以及如何以下面的方式使用它:

*   [Java 中的实现有哪些？](#what)
*   [Java 中实现的例子](#code)
*   [机具和延伸之间的差异](#difference)

## **Java 中的实现有哪些？**

*“Implements”*是一个关键字，用于在 java 语言中实现一个接口。那么，Java 中的接口是什么呢？

接口就像只有静态常量和抽象方法的 Java 类。java 类可以通过使用关键字 implements 来实现这些接口。一次可以实现多个接口。所有方法都是抽象和公共的。

![Java Logo](img/ba2e139ba09d4bcd6574457af0fe6049.png)

关于接口，有两个主要规则

*   必须用抽象方法抽象。

*   该类可以实现任意数量的接口。

java 不支持多重继承，但这可以通过使用接口来实现。可以实现多个接口。

**语法:**

`class **classname** implements **interfacename**`

**举例:**

`class Dog implements Pet`

## **Java 中的实现示例**

```
interface Animal {
    public void eat();
    public void travel();
}
public class PetInt implements Animal {
            public void eat() {
                  System.out.println("Pet eats");
               }
               public void travel() {
                  System.out.println("Pet travels");
               }
               public int noOfLegs() {
                  return 0;
               }
               public static void main(String args[]) {
                  PetInt m = new PetInt();
                  m.eat();
                  m.travel();
               }
}
```

**输出:**

## **![Implements In Java](img/4dd81abd9a360c6a93de5c442294747b.png)**

## **上述代码的解释:**

在上面的代码中，使用 implements 关键字创建并实现了一个接口。

```
interface Animal {
   public void eat();
   public void travel();
}
```

创建接口时声明了两个方法。PetInt 类实现了这个接口。

```
public void eat() {
                  System.out.println("Pet eats");
               }
               public void travel() {
                  System.out.println("Pet travels");
               }
```

创建了两个方法，分别叫做 eat 和 travel。两种方法都有简单的打印语句。

在 main 函数中，我们创建了一个 pet 变量 m，并调用了它的两个方法。这就是接口的实现方式。

## **机具和延伸之间的差异**

1.  当我们想要继承一个接口时，使用 Implements 关键字，而 extends 关键字用于继承类。

2.  一次可以继承多个接口，而一次只能继承一个类。

3.  子类可以覆盖超类的一些方法，而所有方法都是由类从接口实现的。

更深入的区别，可以参考我们的另一个 **[博客](https://www.edureka.co/blog/extends-vs-implements/)** 。

至此，我们结束了这篇用 Java 实现的文章。我希望你了解工具到底是什么，以及它们是如何使用的。

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*