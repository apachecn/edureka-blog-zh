# Java 中抽象方法有什么用？

> 原文：<https://www.edureka.co/blog/abstract-method-in-java/>

在任何编程语言中， [抽象](https://www.edureka.co/blog/java-abstraction/) 意味着向用户隐藏不相关的细节，只关注必要的细节，以提高效率，从而降低复杂性。在 Java 中，抽象是使用抽象类和方法实现的。下面我们来详细了解一下 [Java](https://www.edureka.co/blog/java-tutorial/) 中的抽象方法。

本文讨论的主题如下:

*   什么是抽象类？
*   [什么是 Java 中的抽象方法？](#abstract-method)
*   [Ket 抽象方法的特点](#features)
*   [示例程序:Java 中的抽象方法](#example)
*   Java 中的[接口](#interface)

## 什么是抽象类？

在任何一种[编程语言](https://www.edureka.co/blog/top-10-programming-languages/)中，用关键字 *abstract* 声明的类被称为抽象类。一个[抽象类](https://www.edureka.co/blog/difference-between-abstract-class-and-interface#abstract-class)捕捉子类的共同特征，可能包含也可能不包含任何*抽象方法*。它不能被实例化，但只能被它的子类用作超类。

下面列出了一些关于抽象类的要点:

*   抽象类可以有[构造函数](https://www.edureka.co/blog/constructor-in-java/)和静态方法
*   它可以有[最终方法](https://www.edureka.co/blog/final-finally-and-finalize-in-java/#finalmethod)，它们强制子类不要改变方法的主体
*   你可以通过从另一个类继承来使用一个抽象类，然后为其中的抽象方法提供实现
*   如果抽象类没有任何方法实现，使用[接口](https://www.edureka.co/blog/java-interface/)总是更好

声明为抽象的类可能包含也可能不包含抽象方法。但是，抽象方法到底是什么？

## **什么是抽象方法？**

在抽象类中声明的没有主体(没有实现) 的方法是一个 **抽象方法。**换句话说，如果你希望一个[类](https://www.edureka.co/blog/java-objects-and-classes/#javaclass)包含一个特定的方法，但是你希望该方法的实际实现由子类决定，那么你可以在父类中将该方法声明为一个抽象。

Java 中的抽象方法是这样的:

```
abstract public void habitat(); 
```

## **抽象方法的主要特征**

下面列出了抽象方法的主要特征:

*   抽象方法没有实现(主体)，它们只有方法签名，如上面的例子所示
*   如果一个类有一个抽象方法，它应该被声明为抽象的，反之亦然
*   一个抽象方法将会有一个分号(；)在最后
*   如果一个[常规类](https://www.edureka.co/blog/java-objects-and-classes/#classtypes)扩展了一个抽象类，那么这个类必须实现这个类的所有抽象方法，否则它也必须被声明为抽象类

## **示例程序:Java 中的抽象方法**

查看示例程序，了解如何使用抽象类和抽象方法实现抽象。一定要看一看。

```
package MyPackage;
//abstract class
abstract class Animal{
	 String AnimalName = " "; 

	    Animal(String name) 
	    { 
	        this.AnimalName = name; 
	    } 

	    // declare non-abstract methods 
	    // it has default implementation 
	    public void BasicInfo(String details) 
	    { 
	        System.out.println(this.AnimalName + " " + details); 
	    } 

	    // abstract methods which will be 
	    // implemented by its subclass(es) 
	    abstract public void habitat(); 
	    abstract public void respiration(); 
	} 
class Terrestrial extends Animal 
{ 

    // constructor 
    Terrestrial(String name) 
    { 
        super(name);
    } 

    @Override
    public void habitat()  
    { 
        System.out.println("leave on land and");  
    } 

    @Override
    public void respiration()  
    { 
    	System.out.println("respire through lungs or trachea. ");  
    }
}
class Aquatic extends Animal 
{ 

    // constructor 
    Aquatic(String name) 
    { 
        super(name);
    } 

    @Override
    public void habitat()  
    { 
        System.out.println("It leaves in water and");  
    } 

    @Override
    public void respiration()  
    { 
    	System.out.println("respire through gills or their skin. ");  
    }
}

class AbstractClassDemo
{ 
    public static void main (String[] args)  
    { 

        // creating the Object of Terrestrial class 
        // and using Animal class reference. 
        Animal object1 = new Terrestrial("Humans"); 
        object1.BasicInfo("are terrestrial beings, they "); 
        object1.habitat(); 
        object1.respiration(); 

        System.out.println(" "); 

        // creating the Objects of circle class 
        Animal object2 = new Aquatic("Fishes"); 
        object2.BasicInfo("are aqautic beings, they "); 
        object2.habitat(); 
        object2.respiration(); 

    } 
} 

```

**输出:**

方法 *BasicInfo()* 是一个[的具体方法](https://www.edureka.co/blog/java-methods/#Different_types_of_methods_in_Java)，它被*陆地*和*水上*类使用。方法*栖息地()*和*呼吸()*是抽象方法，它们没有任何实现，只有签名。 *陆地*和*水上*类必须为这两种方法提供自己的实现。另外，注意这两种方法都是以关键字 ***抽象*** 开头的。此时，您可能想知道*抽象类*与*接口*有何不同。

Java 中的**接口**

在 Java 中实现  [抽象](https://www.edureka.co/blog/java-abstraction/#What-is-Java-Abstraction) 的另一种方式是通过使用  [接口](https://www.edureka.co/blog/java-abstraction/#Interface)。  接口是抽象方法的集合，它没有任何具体的[方法](https://www.edureka.co/blog/java-methods/)，不像抽象类。但与抽象类不同，接口在 Java 中提供了完全的抽象。它可以像类一样既有方法又有变量。但是，默认情况下，接口中声明的方法是抽象的。

抽象类和接口是 [Java 编程语言](https://www.edureka.co/blog/java-tutorial/)的两个主要构建块 。尽管两者都主要用于抽象，但它们彼此之间有很大的不同，不能互换使用。

“Java 中的抽象方法”这篇文章到此结束。我已经介绍过一个最常被问到的 [Java 面试问题](https://www.edureka.co/blog/interview-questions/java-interview-questions/)，它是 Java 中的一个抽象类。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 提供的 [**Java 课程**](https://www.edureka.co/java-j2ee-training-course) 培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。* *有问题吗？请在这篇 Java 中的抽象方法’**文章的评论部分提到它，我们会尽快回复您。*