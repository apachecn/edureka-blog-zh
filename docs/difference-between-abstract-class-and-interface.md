# Java 中抽象类和接口的区别？

> 原文：<https://www.edureka.co/blog/difference-between-abstract-class-and-interface>

抽象类和接口是 [Java 编程语言](https://www.edureka.co/blog/java-tutorial/)的两个主要构建块 。尽管两者都主要用于抽象，但它们彼此之间有很大的不同，不能互换使用。在本文中，让我们弄清楚 Java 中抽象类和接口的区别。

本文讨论的主题如下:

*   [什么是 Java 中的抽象类？](#abstract-class)
*   Java 中的[接口](#interface)
*   [抽象类 vs 接口](#abstractclassVSinterface)
*   [什么时候使用抽象类&什么时候使用接口？](#choice)

要理解 [Java](https://www.edureka.co/blog/what-is-java/) 中抽象类和接口的区别，你需要知道什么是抽象类，什么是接口。那么，让我们从讨论这些是什么开始。

## **什么是 Java 中的抽象类？**

在任何编程语言中，[抽象](https://www.edureka.co/blog/java-abstraction/)意味着向用户隐藏不相关的细节，只关注必要的细节，以提高效率，从而降低复杂性。在 Java 中，抽象是通过使用[抽象类](https://www.edureka.co/blog/java-abstraction/#AbstractClass)实现的。抽象类捕捉子类的共同特征，可能包含也可能不包含任何抽象方法。它不能被实例化，但只能被它的子类用作超类。下面是一个演示抽象类的示例程序:

***注:**一个**抽象方法**，是一个实现不到位，给[类](https://www.edureka.co/blog/java-objects-and-classes/)增加不完整性的方法。*

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

**输出**

```
Humans are terrestrial beings, they 
leave on land and
respire through lungs or trachea. 

Fishes are aqautic beings, they 
It leaves in water and
respire through gills or their skin. 

```

*basic info()*是由*陆地*和*水上*类共享的方法。由于*动物类*不能被初始化，我们正在创建*陆地类*和*水生类*的对象用于编程目的。接下来，我们有界面。

## Java 中的**接口**

在 Java 中实现[抽象](https://www.edureka.co/blog/java-abstraction/#What-is-Java-Abstraction)的另一种方式是使用[接口](https://www.edureka.co/blog/java-abstraction/#Interface)。接口是抽象方法的集合，它没有任何具体的[方法](https://www.edureka.co/blog/java-methods/)，不像抽象类。但与抽象类不同，接口在 Java 中提供了完全的抽象。它可以像类一样既有方法又有变量。但是，默认情况下，接口中声明的方法是抽象的。 这里有一个[示例程序](https://www.edureka.co/blog/java-programs/)演示抽象类:

```
package MyPackage;

interface Animals{

	    // abstract methods 
	    void habitat(); 
	    void respiration(); 
	} 
class TerrestrialA implements Animals
{ 
	String AnimalName = " "; 
	// constructor   
	TerrestrialA(String name) 
    { 
        this.AnimalName = name; 
    } 

  @Override
  public void habitat()  
  { 
      System.out.println(this.AnimalName + " leave on land and");  
  } 

  @Override
  public void respiration()  
  { 
  	System.out.println("respire through lungs or trachea. ");  
  }
}
class AquaticA implements Animals
{ 
	String AnimalName = " "; 
	// constructor   
	AquaticA(String name) 
    { 
        this.AnimalName = name; 
    } 
  @Override
  public void habitat()  
  { 
      System.out.println(this.AnimalName + " leave in water and");  
  } 

  @Override
  public void respiration()  
  { 
  	System.out.println("respire through gills or their skin. ");  
  }
}

class JavaInterfaceDemo
{ 
  public static void main (String[] args)  
  { 

      // creating the Object of Terrestrial class 
      // and using Animal class reference. 
      Animals object1 = new TerrestrialA("Humans"); 
      object1.habitat(); 
      object1.respiration(); 

      System.out.println(" "); 

      // creating the Objects of circle class 
      Animals object2 = new AquaticA("Fishes");  
      object2.habitat(); 
      object2.respiration(); 

  } 
} 

```

**输出**

```
Humans leave on land and
respire through lungs or trachea. 

Fishes leave in water and
respire through gills or their skin.  
```

如果你的[类](https://www.edureka.co/blog/java-objects-and-classes/)之间没有任何公共代码，那么你可以使用接口。接口更像是一个类的蓝图，因为它没有任何非抽象方法。

从上面的内容中，你可能已经注意到了 [Java](https://www.edureka.co/blog/java-tutorial/) 中抽象类和接口的关键区别。与抽象类不同，接口在 Java 中提供了完整的[抽象](https://www.edureka.co/blog/java-abstraction/)。现在让我们继续列出其他不同之处。

## **抽象类 vs 接口**

下表列出了抽象类和接口之间的主要区别。

| **参数** | **抽象类** | **界面** |
| **默认方法实现** | 它可以有默认的方法实现 | 接口提供纯抽象&根本不能有实现 |
| **变量** | 它可能包含非最终变量。 | 默认情况下，在接口中声明的变量是最终变量 |
| **使用的关键字** | 可以使用关键字“扩展”来扩展抽象类 | 该接口应该使用关键字“实现”来实现 |
| **访问修饰符** | 可以有公共的、受保护的、私有的和默认的修饰符 | 默认情况下，接口方法是公共的。不能使用任何其他访问修饰符 |
| **执行速度** | 它比接口更快 | 接口有点慢&需要额外的间接寻址 |
| **普通班** | 它只能扩展一个抽象类 | 可以实现多个接口 |
| **构造函数** | 抽象类可以有构造函数 | 一个接口不能有构造函数 |
| **多重继承** | 一个抽象类可以扩展另一个类，并且可以实现多个 Java 接口 | 该接口只能扩展另一个 Java 接口 |

好了，现在你知道 Java 中抽象类和接口的主要区别了。但是，如何决定何时使用这两者中的哪一个呢？

## **什么时候使用抽象类&什么时候使用接口？**

考虑在下列情况下使用抽象类:

*   如果你有一些相关的类需要共享*行相同的代码*
*   当你想定义*非静态或非最终字段*
*   当有个方法或字段 或需要[个访问修饰符](https://www.edureka.co/blog/access-modifiers-in-java/) *而不是公共*(比如受保护的和私有的)

考虑在下列情况下使用接口:

*   当你想达到*纯抽象*
*   如果你想使用*多个[继承](https://www.edureka.co/blog/inheritance-in-java/)，即实现多个接口*
*   当您想要指定特定数据类型的行为，但不关心谁实现它的行为时。

这就把我们带到了本文的结尾。我曾经报道过一个在面试中最常被问到的 Java 问题，就是 Java 中抽象类和接口的区别。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“Java Map interface”**文章的评论部分提到它，我们会尽快回复您。*