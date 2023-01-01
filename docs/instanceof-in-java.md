# 如何用 JAVA 实现 InstanceOf？

> 原文：<https://www.edureka.co/blog/instanceof-in-java/>

[Java](https://www.edureka.co/blog/java-tutorial/) 中的 InstanceOf 是一个运算符，用来检查对象的类型。换句话说，它测试对象是特定类的实例还是接口。这种运算的输出或者是 ***真*** 或者是 ***假***

本文将涉及以下几点:

*   [的实例](#instanceOf)
*   [使用空值变量](#UsingaVariablewithNullValue)
*   [父对象不是子对象](#AParentobjectisnotaninstanceofchild)的实例
*   [向下投射](#Downcasting)
*   [了解](#UnderstandinginstanceOf)的实例

继续这篇关于 Java 实例的文章。

该操作符也称为类型*比较操作符*，因为实例与类型进行比较。

**语法:**

```
(object) instanceof (type)
```

下面是 instanceOf 运算符的一个示例:

```
public class Main 
{  
public static void main(String[] args) 
{  
Main s = new Main();  
System.out.println(s instanceof Main); 
}  
}

```

**输出**

真实的

在这个例子中，返回给用户的输出是 *true* ，即 **s** 是类 Main 的一个实例。

**例子**

子类类型的对象也是父类的类型。

在下面的例子中，摇滚扩展了音乐。摇滚的对象既可以指摇滚，也可以指音乐。

```
class Music{}
class Rock extends Music
{
//Rock inherits Music
public static void main(String args[])
{
Rock r=new Rock();
System.out.println(r instanceof Rock);
}
}

```

**输出**

真实的

继续这篇关于 Java 实例的文章。

## **使用空值变量**

```
class Music
{
public static void main(String args[])
{
Music m=null;
System.out.println(m instanceof Music);//false
}
}

```

在上面给出的例子中，定义的变量有一个空值。

因此，返回的输出为假。

**输出**

错误的

使用 instanceOf 运算符时，必须注意以下几点:

继续这篇关于 Java 实例的文章。

## **父对象不是子对象**的实例

```
class Parent {  } 
class Child extends Parent { } 
class Main
{ 
public static void main(String[] args) 
{ 
Parent p = new Parent(); 
if(p instanceof Child) 
System.out.println("p is an instance of Child"); 
else
System.out.println("p is not an instance of Child"); 
} 
}

```

**输出**

p 不是 Child 的实例

继续这篇关于 Java 实例的文章。

## **下**上**下**

当父类的对象被子类引用时，这种方法称为向下转换。

在直接执行向下转换时，编译器会返回一个编译错误。

```
Rock r=new Music();//compilation error
```

在使用类型转换时，会在运行时引发 ClassCastException。

```
Rock r=(Rock)new Music();//compilation successful but ClassCastException thrown
```

向下转换的唯一方法是使用 instanceof 运算符。

```
class Music { }
class Rock extends Music {
static void method(Music m) {
if(m instanceof Rock){
Rock r=(Rock)m; //downcasting
System.out.println("Downcasting Successful");
}
}
public static void main (String [] args) {
Music m=new Rock();
Rock.method(m);
}
} 

```

**输出**

向下转换成功

继续这篇关于 Java 实例的文章。

## **了解实例 Of:**

通过下面给出的示例，可以更清楚地理解 instanceOf 方法:

此示例使用了一个接口:

```
interface Instance{}
class S implements Instance
{
public void s()
{
System.out.println("First method");
}
}
class T implements Instance
{
public void t()
{
System.out.println("Second method");
}
}
class Invoke
{
void invoke(Instance i)
{ //upcasting
if(i instanceof S)
{
S s=(S)i; //Downcasting 
s.s();
}
if(i instanceof T)
{
T t=(T)i; //Downcasting 
t.t();
}
}
} 
class Main
{
public static void main(String args[])
{
Instance i=new T();
Invoke v=new Invoke();
v.invoke(i);
}
}

```

示例的输出如下:第二种方法

这个例子以精确的方式演示了这个概念。这里，父类是乐器，两个子类是吉他和钢琴:

```
class Instrument{}
class Guitar extends Instrument{}
class Piano extends Instrument{}
class Main
{
public static void main(String[] args)
{
Instrument i =new Instrument();
Guitar g = new Guitar();
Piano p = new Piano();
System.out.println(g  instanceof Instrument);		
System.out.println(p  instanceof Instrument);		
System.out.println(i instanceof Guitar);		
System.out.println(i  instanceof Piano);		
i = g;
System.out.println(i instanceof Guitar);		
System.out.println(i instanceof Piano);		
i = p;
System.out.println(i instanceof Guitar);		
System.out.println(i instanceof Piano);		
}
} 

```

输出如下所示:

真实的

真实的

错误的

错误的

真实的

错误的

错误的

真实的

***这就是高效找到对象类型的方法。如果方法执行得当，instanceOf 操作符被证明是非常有用的。***

关于“Java 中的实例”的这篇文章到此结束。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。 [Edureka 的 Java J2EE 和 SOA 培训和认证课程](https://www.edureka.co/java-j2ee-soa-training/)旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。