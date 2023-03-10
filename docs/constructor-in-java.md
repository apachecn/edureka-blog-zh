# Java 中的构造函数是什么？

> 原文：<https://www.edureka.co/blog/constructor-in-java/>

就编程而言，Java 是一种多功能语言。尽管这很容易学，但必须首先掌握基本概念。一个这样的概念是 [Java](https://www.edureka.co/java-j2ee-soa-training) 中的构造器，这是一个非常重要的概念，因为它涉及到[类和对象](https://www.edureka.co/blog/java-tutorial/#obj)。构造函数是一种特殊的方法，用来给对象赋值。在本文中，我们将详细了解以下主题:

*   [什么是 Java 中的构造函数？](#whatisaconstructor)
*   [Java 中构造函数的规则](#rules)
*   [构造器的类型](#typesofconstructor)
    *   [默认构造函数](#defaultconstructor)
    *   [参数化构造器](#parametrizedconstructor)
*   [构造函数重载](#constructoroverloading)
*   [Java 中方法和构造函数的区别](#methodvsconstructor)

## **Java 中什么是构造函数？**

我们创建一个构造函数来初始化一个对象。它们与类同名，但是没有显式的返回类型。它可用于设置对象属性的初始值。它类似于 Java 方法

在调用构造函数时，内存是为对象分配的。Java 中的每个类都有一个构造函数。即使没有创建，Java 也会隐式调用一个所有数据成员值都设置为零的构造函数。

```

class Edureka
{
//constructor
new Edureka( )
}
//object is made and constructor is called.
Edureka ob1 = new Edureka( )

```

**构造函数什么时候被调用？**

创建对象或实例时会调用构造函数。它用于为同一类的数据成员赋值。

## **Java 中构造函数的规则**

1.  构造函数的名称应该与类名相同。
2.  构造函数不能声明为 [final](https://www.edureka.co/blog/final-finally-and-finalize-in-java/) ，static，synchronized 或 abstract。
3.  它不能有显式返回类型。
4.  构造函数可以有一个访问修饰符来控制访问。

创建构造函数时，您应该遵循这些规则。

## **Java 中构造函数的类型**

有两种类型的构造函数

1.  默认构造函数
2.  参数化构造函数

### **默认构造函数**

没有参数的构造函数称为 ***默认构造函数。*** 如果我们不创建一个类的构造函数， [Java](https://www.edureka.co/blog/what-is-java/) 会创建一个默认的构造函数，它的数据成员有零、空等值。

但是，如果我们指定一个不带参数的构造函数，它将是一个 ***默认构造函数*** 或一个 ***不带参数构造函数*** ，这是默认构造函数的另一个名称。下面的示例展示了如何在 Java 中使用默认构造函数:

```

class Edureka {
//creating the constructor
Edureka( )
{
System.out.println( 'hello learner') }

public static void main(String args[])
{
Edureka ob1 = new Edureka( )
}
}
output : hello learner

```

### **参数化构造器**

有参数的构造函数称为 ***参数化构造函数。*** 用来给不同的对象赋值。下面的例子展示了我们如何在 java 中声明一个参数化的构造函数:

```
class Edureka {
string name, course;
//creating a parametrized constructor
Edureka(string s , string n )
{
  name = s ;
  course = n;
}
void show( )
{ System.out.println( name+ " " + course); }

public static void main(String args[])
{
 Edureka ob1 = new Edureka("Java" , "J2EE");
 Edureka ob2 = new Edureka('Java" , "Advance Java");
 ob1.show( );
 ob1.show( );
     }
}
output: Java J2EE
        Java Advance Java

```

## **构造函数重载**

就像方法重载一样，构造函数可以被重载，以不同的方式创建[对象](https://www.edureka.co/blog/object-oriented-programming/)。编译器根据构造函数中有多少个参数和其他参数(如参数传递的顺序)来区分构造函数。

下面是构造函数重载的一个示例:

```
class Edureka 
{
 string name, course, technology;
 Edureka(string s , string n)
{
name = s ;
course = n ;
}
Edureka(string s , string n , string c)
{
name = s;
course = n;
technology = c;
}
void show( ) 
{ System.out.println(name +""+course+""+technology); }

public static void main(String args[ ])
{
 Edureka ob1 = new Edureka("edureka" , "Java") ;
 Edureka ob2 = new Edureka("edureka" , "J2EE" , "Java");
 ob1.show( );
 ob2.show( );
    }
}
output: edureka Java
        edureka J2EE Java

```

## **方法和构造函数的区别**

| 方法 | 构造器 |
| 

*   Method name does not have to be the same as class name.

相同 | 

*   Constructor name must be the same as class name

相同 |
| 

*   Method has a return type.

 | 

*   The constructor has no return type.

 |
| 

*   You can call a method any number of times.

 | 

*   Invoke the constructor when creating an object.

 |

在这篇博客中，我们讨论了 java 中的构造函数，我们如何使用它们以及不同类型的构造函数。Java 是一种有趣的语言，但是如果基础不清楚，它就会变得很棘手。要启动您的学习并掌握与 java 技术相关的所有技能，请注册参加 [java 认证计划](https://www.edureka.co/java-j2ee-soa-training)，释放您的 java 开发者潜能。

有问题要问我们吗？请在“什么是 Java 构造函数？”的评论部分提到这一点文章，我们会尽快回复您。