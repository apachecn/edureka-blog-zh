# Java EnumSet:如何在 Java 中使用 EnumSet？

> 原文：<https://www.edureka.co/blog/java-enumset/>

Java 是最流行的编程语言之一，用于构建各种各样的应用程序。在构建应用程序时，我们经常使用枚举来服务一组命名的常量。但是，如果你想用枚举类型实现一个 Set 接口，那么你必须使用 [Java](https://www.edureka.co/java-j2ee-training-course) 中的 EnumSet。在这篇关于 Java EnumSet 的文章中，我将涉及以下主题:

![Java Logo - Java EnumSet - Edureka](img/4367041ac8dab1ef981e1e7b0148d5f6.png)

*   [什么是 EnumSet？](#enumset)
    *   [申报](#declaration)
*   [枚举设置的方法](#methodsofenumset)
*   [枚举设置的操作](#operationsofenumset)

## **什么是 Java EnumSet？**

EnumSet 是[集合](https://www.edureka.co/blog/sets-in-java/)的实现，与[枚举类型](https://www.edureka.co/blog/enumeration-in-java/)一起工作。EnumSet 从[抽象集](https://www.edureka.co/blog/abstract-classes-in-java/)扩展而来，实现了 Set 接口。以下是您需要了解的关于 Java 中 EnumSet 的几个要点:

*   仅包含属于同一枚举类型的枚举值
*   它是 [Java 集合框架](https://www.edureka.co/blog/java-collections/)的成员
*   提供高性能集实现，并且不同步
*   它不允许用户添加空值，并引发 NullPointerException
*   元素按照保存的顺序存储
*   使用防故障迭代，该迭代可用于确保引发 ConcurrentModificationException

您可以通过以下方式声明 Java enum set:

### **申报**

```
public abstract class EnumSet<E extends Enum<E>> 

```

接下来，在这篇关于 Java EnumSet 的文章中，让我们了解这个类提供的不同方法。

## **枚举设置的方法**

Java EnumSet 提供的各种方法如下:

| **方法** | **修改器和类型** | **描述** |
| 之**(E1)之** | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个最初包含上述元素的枚举集，即 e1。 |
| 的**(E E1，E e2)** | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个最初包含上述元素的枚举集。这里，是 e1，e2。 |
| **范围** (E 从，E 到) | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个枚举集，最初包含由两个提及的端点定义的范围内的所有元素。 |
| **allOf** ( 类 < E >元素类型) | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个包含 menioned 元素类型中所有元素的枚举集。 |
| **文案** ( 收藏 < E > c) | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个从上述集合初始化的枚举集。 |
| **copy of**(enum setE>s) | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个枚举集，该枚举集具有与上述枚举集相同的元素类型，最初包含相同的元素(如果有)。 |
| **的补充** ( 枚举E>s) | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建一个枚举集，该枚举集具有与上述枚举集相同的元素类型，最初包含指定集合中包含的 *而非* 的该类型的所有元素。 |
| **无** ( 类 < E >元素类型) | 静态< E 扩展枚举 < E > > 枚举设置 < E > | 用于创建具有指定元素类型的空枚举集。 |
| **克隆**() | 枚举设置<E> | 用于返回本套的副本。 |

**注意:**可以使用()方法的**最多 5 个参数。因此，您可以创建一个最初包含指定元素的枚举集，如下所示:**

*   的**(E E1，E e2，E e3)**
*   的**(E E1，E e2，E e3，E e4)**
*   的**(E E1，E e2，E e3，E e4，E e5)**

既然，我已经讨论了与 EnumSet 一起使用的方法，接下来在 Java EnumSet 教程中，让我们看看这些方法的实际操作。

## **Java 枚举集的操作**

为了向您解释 EnumSet 的操作，我将考虑下面的代码片段。这个代码片段包含一组枚举值[DevOps、大数据、Python、数据科学、RPA]。在代码的后面部分，我将向您展示如何按以下顺序使用不同的方法:

*   之**(E1)之**
*   的**(E E1，E e2)**
*   的**(E E1，E e2，E e3)**
*   的**(E E1，E e2，E e3，E e4)**
*   的**(E E1，E e2，E e3，E e4，E e5)**
*   **范围** (E 从，E 到)
*   **allOf** ( 类 < E >元素类型)
*   **文案** ( 收藏 < E > c)
*   **copy of**(enum setE>s)
*   **的补充** ( 枚举E>s)
*   **无**(类< E >元素类型)
*   **克隆**()

### **代码片段:**

```
package edureka;
import java.util.ArrayList;
import java.util.Collection;
import java.util.EnumSet; 
enum Courses 
{ 
	DevOps, BigData, Python, DataScience, RPA
}; 
public class Example {
	    public static void main(String[] args)  
	    { 
	    	// Create an EnumSet 
	        EnumSet<Courses> sample_set;  

	        //of method
	        // Add single element
	        sample_set = EnumSet.of(Courses.DevOps); 
	        // Display the set 
	        System.out.println("The EnumSet after adding a single element is: " + sample_set); 

	        // Add two elements
	        sample_set = EnumSet.of(Courses.DevOps, Courses.BigData); 
	        // Display the set 
	        System.out.println("The EnumSet after adding two elements is: " + sample_set); 

	        // Add three elements
	         sample_set = EnumSet.of(Courses.DevOps, Courses.BigData, Courses.Python); 
	        // Display the set 
	        System.out.println("The EnumSet after adding three elements is: " + sample_set); 

	        // Add four elements
	         sample_set = EnumSet.of(Courses.DevOps, Courses.BigData, Courses.Python, Courses.DataScience); 
	        // Display the set 
	        System.out.println("The EnumSet after adding four elements is: " + sample_set); 

	        // Add five elements
	         sample_set = EnumSet.of(Courses.DevOps, Courses.BigData, Courses.Python, Courses.DataScience,Courses.RPA); 
	        // Display the set 
	        System.out.println("The EnumSet after adding five elements is: " + sample_set); 

	        //Range method
	        sample_set = EnumSet.range(Courses.BigData, Courses.DataScience); 
	        // Display the set 
	        System.out.println("The range of the EnumSet is: " + sample_set); 

	        //allOf method
	        sample_set = EnumSet.allOf(Courses.class); 
	        // Display the set 
	        System.out.println("All the elements in the EnumSet are: " + sample_set); 

	        //copyOf(Collection) method

	        // Create an empty collection 
	        Collection<Courses> samplecollection = new ArrayList<Courses>();	        
	        // Add elements to the samplecollection 
	        samplecollection.add(Courses.DevOps); 
	        samplecollection.add(Courses.BigData); 
	        samplecollection.add(Courses.Python); 	        
	        // Display the sample collection set 
	        System.out.println("Elements in the sample collection set are: " + samplecollection); 	        
	        //Create a new EnumSet to store the collection items
	        EnumSet<Courses> final_enumset = EnumSet.copyOf(samplecollection);
	        // Display the EnumSet 
	        System.out.println("Elements in the EnumSet are: " + final_enumset); 

	        //copyOf(EnumSet) method

	        // Get all the elements from Courses  
	        EnumSet<Courses> example_set = EnumSet.allOf(Courses.class);
	        // Display the initial EnumSet(sample_set) 
	        System.out.println("The elements in the initial EnumSet are: " + example_set); 
	        // Copy the elements from the above set
	        EnumSet<Courses> final_set = EnumSet.copyOf(example_set);
	        // Display the elements in the copied EnumSet 
	        System.out.println("The elements in the copied EnumSet are: " + final_set); 

	        //complementOf method
	        //Sample Set
	        sample_set = EnumSet.of(Courses.DevOps, Courses.BigData, Courses.Python);
	        //Create an EnumSet
	        EnumSet<Courses> complement_set;
	        //Complement the above set
	        complement_set = EnumSet.complementOf(sample_set);
	        // Display the elements in the complement EnumSet 
	        System.out.println("The elements in the complement EnumSet are: " + complement_set); 

	        //noneOf method
	        // Create empty set 
	        EnumSet<Courses> none_example_set = EnumSet.noneOf(Courses.class); 
	        // Display the elements in the set 
	        System.out.println("EnumSet consists of the elements: " + none_example_set); 

	        //clone method
	        EnumSet<Courses> final_clone_set = sample_set.clone(); 
	        //Display the EnumSet
	        System.out.println("The clone set consists of the elements:" + final_clone_set);	    

	    } 
}

```

### **输出:**

```
The EnumSet after adding a single element is: [DevOps]
The EnumSet after adding two elements is: [DevOps, BigData]
The EnumSet after adding three elements is: [DevOps, BigData, Python]
The EnumSet after adding four elements is: [DevOps, BigData, Python, DataScience]
The EnumSet after adding five elements is: [DevOps, BigData, Python, DataScience, RPA]
The range of the EnumSet is: [BigData, Python, DataScience]
All the elements in the EnumSet are: [DevOps, BigData, Python, DataScience, RPA]
Elements in the sample collection set are: [DevOps, BigData, Python]
Elements in the EnumSet are: [DevOps, BigData, Python]
The elements in the initial EnumSet are: [DevOps, BigData, Python, DataScience, RPA]
The elements in the copied EnumSet are: [DevOps, BigData, Python, DataScience, RPA]
The elements in the complement EnumSet are: [DataScience, RPA]
EnumSet consists of the elements: []
The clone set consists of the elements:[DevOps, BigData, Python]

```

关于 Java EnumSet 的这篇文章到此结束。如果你想了解更多关于 Java 的知识，你可以参考我们的 [其他 Java 博客](https://www.edureka.co/blog/what-is-java/) 。

*如果您发现这篇文章与“Java EnumSet”相关，请查看[edu reka Java Certification Training，](https://www.edureka.co/java-j2ee-training-course)一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想成为  [Java 开发人员](https://www.edureka.co/blog/java-developer-skills)的学生和专业人士设计课程。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如[Hibernate](https://www.edureka.co/blog/what-is-hibernate-in-java/)&[Spring](https://www.edureka.co/blog/spring-tutorial/)。*

如果您遇到任何问题，请在“Java EnumSet”的评论区自由提问，我们的团队将很乐意回答。