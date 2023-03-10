# 如何在 Java 中实现生成器设计模式

> 原文：<https://www.edureka.co/blog/builder-design-pattern/>

在 Java 中创建复杂对象是 [Java](https://www.edureka.co/blog/java-tutorial/) 非常重要的一个方面。在本文中，我们将按照以下顺序理解 Java 中的构建器设计模式:

*   [Java 中的生成器设计模式是什么？](#what)
*   构建器设计模式在哪里使用？
*   [Builder 模式的优缺点](#adv)

## **Java 中的构建器模式是什么？**

Java 中的 *Builder 模式*是构造复杂对象的另一种方式。它用于构造复杂的对象。物体的构造是一步一步进行的，并且物体是在最后一步构造的。

![Builder Design Patterns](img/9c69846a3a07374d5185cd69ee2ce666.png)

构建器设计模式类似于工厂设计模式。唯一的区别是，与工厂方法相比，builder 模式为您提供了对对象创建的更多控制。

## 构建器设计模式在哪里使用？

假设你在做馅饼。有不同类型的馅饼，每一种都有不同的配料。但是有些成分可能是相似的。要为此编写代码，我们需要许多构造函数。这可能会导致问题。有两个主要问题。

1.  要处理的构造函数太多。

2.  因为可能有相似的参数，所以可能有错误。

这个问题可以通过使用构建器模式来解决。

**考虑代码:**

```
class Pie {
    private final double sugar;
    private final double butter;
    private final int eggs;
    private final int vanilla;
    private final double flour;
    private final double bakingpowder;
    private final double milk;
    private final int cherry;
    public static class Builder {
        private double sugar;
        private double butter;
        private int eggs;
        private int vanilla;
        private double flour;
        private double bakingpowder;
        private double milk;
        private int cherry;
        public Builder sugar(double cup){this.sugar = cup; return this; }
        public Builder butter(double cup){this.butter = cup; return this; }
        public Builder eggs(int number){this.eggs = number; return this; }
        public Builder vanila(int spoon){this.vanilla = spoon; return this; }
        public Builder flour(double cup){this.flour = cup; return this; }
        public Builder bakingpowder(double spoon){this.sugar = spoon; return this; }
        public Builder milk(double cup){this.milk = cup; return this; }
        public Builder cherry(int number){this.cherry = number; return this; }
        public Pie build() {
            return new Pie(this);
        }
    }
    private Pie(Builder builder) {
        this.sugar = builder.sugar;
        this.butter = builder.butter;
        this.eggs = builder.eggs;
        this.vanila = builder.vanila;
        this.flour = builder.flour;
        this.bakingpowder = builder.bakingpowder;
        this.milk = builder.milk;
        this.cherry = builder.cherry;
    }
    @Override
    public String toString() {
        return "pie{" + "sugar=" + sugar + ", butter=" + butter + ", eggs=" + eggs + ", vanila=" + vanila + ", flour=" + flour + ", bakingpowder=" + bakingpowder + ", milk=" + milk + ", cherry=" + cherry + '}';
    }

}
public class BuilderPatternInterface{
    public static void main(String args[]) {
        pie whitePie = new pie.Builder().sugar(1).butter(0.5).  eggs(2).vanila(2).flour(1.5). bakingpowder(0.75).milk(0.5).build();
        System.out.println(whitePie);
    }
}
```

**输出:**

## **![Builder Design Pattern in Java](img/52ae66f287bbf095b6b9c5c1d7193836.png)**

**代码说明:**

在上面的代码中，展示了构建器模式的演示。我们有班级馅饼。在这个类中，我们有一个 builder 类，它有用于设置属性的 builder 方法。在下一部分中，有一个构建代码的构造器。

这减少了对构造函数的需求。唯一的缺点是代码行数增加了。

## **Builder 设计模式的优势**

*   通过减少构造函数的参数，可以进行可读的方法调用。

*   它减少了构造函数中的参数数量。我们也不需要将 null 作为参数传递。

*   创建的对象总是在完整状态下实例化。

*   不可变对象的构建不需要复杂的逻辑。

**生成器设计模式的缺点**

*   代码的行数增加了

*   需要创建一个单独的生成器类。

至此，我们结束了这篇 Java 文章中的构建器设计模式。我希望您对什么是设计模式以及它们是如何工作的有所了解。

*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在“Java 中的构建器设计模式”博客的评论部分提到它，我们会尽快回复您。