# Java 中什么是向上造型和向下造型？

> 原文：<https://www.edureka.co/blog/upcasting-and-downcasting-in-java/>

将一个对象从一种类型转换成另一种类型是 Java 的一个非常重要的方面，也就是众所周知的类型转换。让我们以下面的方式来理解 Java 中向上转换和向下转换的概念:

*   [Java 中的向上造型和向下造型是什么？](#what)
*   [层级示例](#hierarchy)
*   [需要上抛](#need-upscaling)
*   [需要向下抛掷](#need-downscaling)

## **Java 中的向上造型和向下造型是什么？**

向上转换(泛化或扩大)就是转换为父类型。简单地说，将单个类型转换为一个公共类型称为向上转换，而向下转换(专门化或收缩)就是转换为子类型或将公共类型转换为单个类型。

![Upcasting and Downcasting in Java](img/2ca1e3fd18dcf1bb451b6486bd6112c7.png)

可以进行向上转换，但是对于向下转换，我们需要检查类型，否则我们可能会得到

`ClassCastException`

## **层级示例**

让我们举这个例子。

**食物- >水果- >苹果、橘子**

食物是最高层的界面

```
public interface Food { 
   public float getTotalCalories();
   public String getOrigin();
}
```

水果是抽象类

```
public abstract class Fruit implements Food {
public float getTotalCalories(){
      return 0.50f;
}
   public String getOrigin();
}
```

苹果和橘子是两个具体的子类

```
public class Apple extends Fruit {
public float getTotalCalories() {
    return 0.40f
}
public String getOrigin() {
    return "someCity";
  }
}
public class Orange extends Fruit {
public float getTotalCalories() {
    return 0.30f
}
public String getOrigin() {
    return "someOtherCity";
}
}
```

在你的例子中，从苹果到水果的转换是向上转换，因为苹果是水果。只要有继承，也就是两个类之间有关系，我们就可以向上转换。

例如，如果我们将苹果转换为水果，这是向上转换，因为苹果是水果类型，这里我们从子类型推广到父类型。因此，如果两个类之间存在 is-a 关系(继承),我们可以向上转换。

让我们看一个向下转换的例子:

这里我们缩小了对象的类型，也就是说，我们将普通类型转换为独立类型。

```
Fruit fruit = new Apple();
Apple castedApple = (Apple) fruit;
```

在这里，我们将公共类型转换为独立类型，即超类转换为子类，这在 Java 中是不可能的，所以我们显式地进行转换，并告诉编译器对象的运行时类型。在这种情况下是可能的，因为 水果 是 苹果 即使引用类型是水果。

现在，假设你这样做:

```
Fruit fruit = new Fruit();
Apple notApple = (Apple) Fruit;
```

上面的代码将抛出一个异常，因为 fruit 的运行时对象是 Fruit 而不是 Apple，不可能将超类转换为子类，所以这将以`ClassCastException`结束。

如果我们想要调用超类的方法，我们可以简单地使用 super 关键字作为super . method name()或者我们可以向上转换对象。

如果我们想要调用子类的方法，那么我们将需要向下转换对象，但是我们可能会遇到ClassCastException所以，如果你想要避免这个异常，你可以使用关键字 instanceof ，它将在我们转换对象之前检查对象的运行时类型，如下面的代码所示。

```
Fruit fruit = getSomeFruit(); #we dont really know what getSomeFruit is returning so we can check the type of fruit using instanceof
if (fruit instanceof Apple) {
    // the object can be casted and the code won't fail
    Apple castedApple = (Apple) fruit;
}
```

作为一名 Java 开发人员，你通常会遇到这种情况，你可能需要根据需求对对象进行造型，现在你知道如何进行造型了。这其实并不难做到。

## **为什么我们在 Java 中需要向上转换？**

通常，向上转换是不必要的。当我们想写只处理父类的代码时，我们需要向上转换。考虑下面的类

```
public class CalorieMeter{
     public void readCalorie(Fruit fruit){
          print("Calorie:" + fruit.getTotalCalories());
     }
}
```

在这里，我们可以将水果的任何子类型传递给 readCalorie()方法，因此它接受 Apple 和 Orange 类的对象，因为它们是水果类的子类型。

```
Apple apple = new Apple();
Orange orange = new Orange();
Caloriemeter caloriemeter = new CalorieMeter();
caloriemeter.readCalorie(apple);
caloriemeter.readCalorie(orange);
```

## 为什么我们在 Java 中需要向下转换？

每当我们想要访问子类型的行为时，我们就使用向下转换。这比向上抛掷更常用。考虑下面的例子:

```
public class CalorieMeter{
     public void readCalorie(Fruit fruit){
          print("Calorie:" + fruit.getTotalCalories());
          //if the fruit is orange the object should print city
          if(fruit instanceof Orange){
             Orange orange = (Orange) fruit;
             System.out.println("City:"+fruit.getOrigin());
          }
     }
}
```

在 readCalorie()方法中，我们已经检查了传递的对象，如果该对象是 Orange 类型，我们必须向下转换它并调用 getOrigin()方法，该方法将给出水果的来源。

## **重要话题**

*   当我们转换对象时，只改变对象的引用类型，而不是实际的对象类型。

*   向上抛掷是安全的，不会失败。

*   当我们使用 instance of 操作符向下转换对象时，我们需要检查对象的实例，否则我们可能会得到 ClassCastException。

在本文中，我们讨论了 Java 中的向上转换和向下转换。什么是需要的层次结构，以便对象可以向上转换和向下转换，以及如何使用 instanceof 操作符，以便在向下转换时检查对象的类型，这样我们就可以避免出现 ClassCastException。一些导入点，比如在强制转换时，只改变对象的引用，在向下转换时，我们应该检查对象的类型，向上转换是安全的。如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*查看 Edureka 提供的  [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 教程”博客的评论部分提到它，我们会尽快回复您，或者您也可以参加我们在沙迦举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-sharjah)