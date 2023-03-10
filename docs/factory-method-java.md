# Java 中的工厂方法是什么，如何使用？

> 原文：<https://www.edureka.co/blog/factory-method-java/>

简单地说，一个 *[Java](https://www.edureka.co/blog/java-tutorial/)* 工厂模式有助于为你的类创建实例。顾名思义，工厂是一个生产不同产品的地方，这些产品有相似的特征，但又有不同的类别。所以，让我们深入挖掘，详细理解 Java 中工厂方法的概念。

以下是本教程将涉及的主题:

*   [什么是 Java 工厂模式？](#WhatisJavafactorypattern?)
*   [工厂模式的优势](#Advantagesoffactorypattern)
*   [工厂模式实现](#Factorypatternimplementation)

我们开始吧！

从 Java 工厂模式的定义开始。

## **什么是 Java 工厂模式？**

一个小问题。如何在 Java 中创建一个 *[类的实例？主要是通过使用“*新的*关键字。嗯，这里有一个更好的方法，这就是 Java 工厂模式的全部内容。](https://www.edureka.co/blog/java-objects-and-classes/)*

工厂模式用于创建类的实例。对象的创建不向客户端公开，并且客户端使用相同的公共接口来创建新类型的对象。 *[静态](https://www.edureka.co/blog/java-static-method/)* 工厂方法背后的核心思想是创建并返回实例，其中类模块的细节对用户是隐藏的。

简而言之，一个超类将指定所有的标准和通用行为，然后将创建细节委托给客户端提供的子类。

在理解了 Java 中工厂方法模式的实际含义之后，让我们来理解它所提供的优势。

## **Java 工厂方法的优势**

我列举了 Java 工厂方法提供的一些优点:

1.  您创建的[对象](https://www.edureka.co/blog/java-object/)可以在没有重复代码的情况下使用。
2.  如果使用工厂方法而不是构造函数，工厂方法也可以有不同的、更具描述性的名称。
3.  此外，它还从客户端代码中删除了实现类的实例化。
4.  这种方法使得代码更加健壮，耦合性更低，易于扩展。
5.  工厂模式通过[继承](https://www.edureka.co/blog/inheritance-in-java/)在实现和客户端类之间提供[抽象](https://www.edureka.co/blog/java-abstraction/)。

了解了优势之后，让我们进入本文的下一部分。

## **工厂模式实现**

现在，对您来说，实现过程可能看起来有点复杂。按照我的指示一步一步地理解程序。

首先，我将创建一个 shape 接口，以及实现 shape 接口的各个具体类。之后，定义一个工厂类。

首先，创建一个接口:

```
 public interface Shape 
{ 
void draw(); 
} 
```

然后，创建具体的类来以这种方式实现接口:

```
 public class Rectangle implements Shape 
{ 
@Override public void draw() 
{ 
System.out.println("Rectangle::draw() method."); 
} 
} 
public class Square implements Shape 
{ 
@Override public void draw() 
{ 
System.out.println("Square::draw() method."); 
} 
}
public class Circle implements Shape 
{ 
@Override public void draw() 
{
System.out.println("Circle::draw() method."); 
} 
} 
```

在创建具体的类之后，创建一个工厂来生成对象。

```
 public class ShapeFactory 
{ 
//use getShape method to get object of type shape 
public Shape getShape(String shapeType)
{ 
if(shapeType == null)
{ 
return null; 
} 
if(shapeType.equalsIgnoreCase("CIRCLE"))
{ 
return new Circle(); 
} 
else if(shapeType.equalsIgnoreCase("RECTANGLE"))
{ 
return new Rectangle(); 
} 
else if(shapeType.equalsIgnoreCase("SQUARE"))
{ 
return new Square(); 
} 
return null; 
} 
} 
```

现在，工厂被创建来使用具体类的对象来传递所需的信息:

```
 public class FactoryPatternDemo
{ 
public static void main(String[] args) 
{ 
ShapeFactory shapeFactory = new ShapeFactory();
//get an object of Circle and call its draw method. 
Shape shape1 = shapeFactory.getShape("CIRCLE"); 
//call draw method of Circle shape1.draw();
//get an object of Rectangle and call its draw method. 
Shape shape2 = shapeFactory.getShape("RECTANGLE"); 
//call draw method of Rectangle 
shape2.draw(); 
//get an object of Square and call its draw method.
Shape shape3 = shapeFactory.getShape("SQUARE"); 
//call draw method of square 
shape3.draw(); 
} 
}
```

**输出:**

Circle::draw()方法。 Rectangle::draw()方法。 Square::draw()方法。

这就是通过 Java 代码实现工厂模式方法的方式。

我希望上述内容证明对增强你的 *[Java](https://www.edureka.co/blog/what-is-java/)* 知识有所帮助。继续阅读，继续探索！

*还可以查看由 Edureka 提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate Spring。*

*有问题吗？请在“Java 工厂方法”博客的评论部分提到它们，我们会尽快回复您。*

[">]("><span data-mce-type=)

[chrome-extension://kdfieneakcjfaiglcfcgkidlkmlijjnh/content/popups/definitionPopup/index.html?title=What&description=what%20thing](chrome-extension://kdfieneakcjfaiglcfcgkidlkmlijjnh/content/popups/definitionPopup/index.html?title=What&description=what%20thing)