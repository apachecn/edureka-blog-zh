# Java 中的自动装箱和拆箱是什么？

> 原文：<https://www.edureka.co/blog/autoboxing-and-unboxing-java/>

在用任何语言编写程序时，大多数时候我们都使用原始数据类型。但是在面向对象编程的领域中，原始数据类型有所欠缺和 [**Java**](https://www.edureka.co/java-j2ee-soa-training?) 就是其中之一。为了克服原始数据类型的缺点，我们使用了[包装器](https://www.edureka.co/blog/wrapper-class-in-java/)。这个过程称为自动装箱。我们将通过下面的摘要详细讨论 Java 中的自动装箱:

*   [Java 中的装箱和自动装箱是什么？](#BoxingandAutoboxing)
*   [拆箱和自动拆箱](#UnboxingandAutounboxing)
*   [包装类](#WrapperClasses)

我们开始吧。

## **Java 中的装箱和自动装箱是什么？**

装箱和自动装箱经常被用来指代同一个概念。但实际上，它们并不完全相同。先说拳击的概念。什么是拳击？听起来像是我们把什么东西藏在盒子里，对吗？是的，当我们说我们正在装箱或包装一个原始数据类型时，这意味着我们正在包装它以形成一个对象。还在迷茫？我们举个例子。

```
int FirstNumber = 1;
```

变量‘first number’的类型为 int，这是一个[原始数据类型](https://www.edureka.co/blog/data-types-in-java/#PrimitiveDataTypes)。现在，如果我想把变量' FirstNumber '转换成一个对象呢？Java 提供了一种方法。

```
Integer SecondNumber = new Integer(2);
```

请注意，“SecondNumber”不是 int 类型，而是 Integer 类型的对象。将原始数据类型转换为对象的过程称为装箱。你可能会问这怎么可能？让我们想想完成这项任务最简单的方法是什么。我们可以创建一个包含单个 int 类型属性的[类](https://www.edureka.co/blog/java-objects-and-classes/)，一个接受 int 类型值并将其赋给我们的类属性的构造函数，以及一些操作这个 int 值的方法。要了解更多信息，请参考这份[文件](https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html)。

我们看到了如何将 int 类型转换成 Java。有没有办法把其他原始数据类型转换成对象？是的，Java 对于不同的原始数据类型有各自的[包装类](https://www.edureka.co/blog/wrapper-class-in-java/)。我们将在这篇文章的下一部分探讨这些问题。

### **自动装箱**

至此，我们知道了什么是拳击。现在让我们了解一下什么是自动装箱。当编译器在没有明确说明的情况下完成装箱过程时，称为自动装箱。

我们用一个例子来理解这个:

```
import java.util.ArrayList;
import java.util.List;class Box {
public static void main (String[] args)
{
List<Integer> Mylist = new ArrayList<Integer>();
for (int i = 0; i < 10; i++)
Mylist.add(i);
}
}
```

正如我们之前讨论的 [ArrayList](https://www.edureka.co/blog/java-arraylist/) 只接受对象，原始数据类型不起作用。在上面的程序中，我们没有将 In 类型转换为 Integer 类型的对象，但程序执行时没有任何错误。怎么会？这个问题的答案是，编译器在将值添加到“Mylist”之前自动执行装箱过程，因此命名为自动装箱。

```
Mylist.add(Integer.valueOf(i));
```

上面的代码行是由编译器添加到我们的程序中的。

**注意-** 上面一行代码中类名' Integer '是在 valueOf()方法之前提到的，因为 valueOf()是一个静态方法。更多示例请参考[文档](https://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)[。](https://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)

## **拆箱和自动拆箱**

我们看到了原始数据类型的[变量](https://www.edureka.co/blog/java-tutorial/#variables)是如何转换成对象的。但这只是故事的一半。故事的另一半是将类型包装类的对象转换为其原始数据类型，这被称为[拆箱](https://www.edureka.co/blog/wrapper-class-in-java/#unboxing)。

例如-

```
Integer FirstNumber = new Integer(1);
int SecondNumber = FirstNumber.intValue( );
System.out.println(SecondNumber);
```

输出- 1

自动拆箱当编译器在没有明确提及的情况下完成的拆箱过程称为自动拆箱。

例如-

```
Integer Number = new Integer(20);
int num = Number;
```

上面的代码就是一个自动拆箱的例子。在下一节中，我们将学习包装类。

## **包装类**

我们在类型变量中转换成 intl 整型对象。这个整数类是一个包装类。在 Java 中，每个原始数据类型都有一个包装类。这些包装类帮助我们将变量从原始类型转换成相应的包装类类型对象。包装类的方法在操作值时很有用。

下表告诉我们原始数据类型及其各自的包装类。

| **原始类型** | **包装类** |
| 布尔型 | 布尔型 |
| 再见 | 字节 |
| 字符 | 字符 |
| 浮动 | 浮动 |
| int | 整数 |
| 龙 | 龙 |
| 短 | 短 |
| double | Double |

注意包装类中的大写字母。

这样，我们就结束了这篇关于“Java 中的自动装箱”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客“Java 中的自动装箱”的评论部分提到它，我们会尽快回复你。