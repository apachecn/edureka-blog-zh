# 什么是 Java 中的克隆及其类型？

> 原文：<https://www.edureka.co/blog/cloning-in-java/>

在编程时，我们经常会遇到需要重用一段完整代码的情况。重写代码使程序变得庞大，同时降低了程序的效率。这样，Java 为我们提供了一个优秀的特性，把我们从这个繁重的任务中解救出来。这就是 Java 中的克隆，通过这篇文章，我将让您对它有一个全面的了解。

以下是我将在本文中讨论的主题:

*   [克隆 Java 中的](#cloning)
*   [利用克隆的优势](#advantages)
*   [克隆类型](#types)
    *   [浅克隆](#shallow)
    *   [深度克隆](#deep)

## **在 Java 中克隆**

Java 中的对象克隆是创建原始对象的精确副本的过程。换句话说，它是一种通过复制原始对象的所有数据和属性来创建新对象的方法。这只能通过实现 **java.lang.Object** 类的 clone()方法来实现。克隆方法创建一个对象的精确副本，该对象已按逐个字段的赋值顺序被调用，并将返回新的对象引用 **。** 有一点你一定要记住，在 Java 中，实现 clone 接口的对象是允许使用 clone()的，clone 接口是一个标记接口。

现在你已经知道了什么是 Java 中的克隆，让我们来看看使用这个特性的各种优势。

## **Java 克隆的优势**

下面我列出了在 Java 中使用克隆的一些最有趣的特性。

*   有助于减少代码行数。
*   复制对象的最有效和高效的方式。
*   另外，clone()被认为是复制数组最快的方法。

注意:虽然使用克隆技术可能会导致一些设计问题，但是如果你以一种恰当的战略方式使用它，它会给你带来好处。

## **Java 中克隆的类型**

Java 中的克隆可以分为两类:

1.  浅层克隆
2.  深度克隆

让我们逐一了解一下。

### **浅层克隆**

在 Java 中，当克隆过程通过调用 clone()方法来完成时，这被称为浅层克隆。这是 Java 中默认的克隆过程，其中原始对象的浅层副本将使用精确字段创建。如果原始对象引用了其他一些对象作为字段，那么只会克隆该对象的引用，而不会创建新的对象。换句话说，如果您更改克隆对象的值，它也会反映在原始对象中。因此，浅层克隆依赖于原始对象。

![shallow copy - Cloning in Java - Edureka](img/46f57527cc458818764c76b6bcda9d85.png)下面我已经举了同样的例子:

```
package edureka;

class EduCourse
{
    String course1; 
    String course2;
    String course3;

    public EduCourse(String crs1, String crs2, String crs3)
    {
        this.course1 = crs1;

        this.course2 = crs2;

        this.course3 = crs3;
    }
}

class EduLearner implements Cloneable
{
    int eduId; 
    String learnerName; 
    EduCourse eduCourse;

    public EduLearner(int eduId, String learnerName, EduCourse eduCourse)
    {
        this.eduId = eduId; 
        this.learnerName = learnerName; 
        this.eduCourse = eduCourse;
    }

    //Default version of clone() method

    protected Object clone() throws CloneNotSupportedException
    {
        return super.clone();
    }
}

public class ShallowCloneSample
{
    public static void main(String[] args)
    {
        EduCourse j2ee = new EduCourse("Java", "Spring", "Microservices");

        EduLearner learner1 = new EduLearner(2811, "Max", j2ee);

        EduLearner learner2 = null;

        try
        {
            //Creating a clone of learner1 and assigning it to learner2

        	learner2 = (EduLearner) learner1.clone();
        }
        catch (CloneNotSupportedException e)
        {
            e.printStackTrace();
        }

        //Printing Details of Learner1
        System.out.println("Details of Learner 2: ");
        System.out.println("Id: "+learner1.eduId);
        System.out.println("Name: "+learner1.learnerName);
        System.out.println("Course Id: "+learner1.eduCourse);

        //Printing all the courses of 'learner1'
        System.out.println("Courses of Learner 1: ");
        System.out.println(learner1.eduCourse.course1);
        System.out.println(learner1.eduCourse.course2);
        System.out.println(learner1.eduCourse.course3);

      //Printing Details of Learner2
        System.out.println("Details of Learner 2: ");
        System.out.println("Id: "+learner2.eduId);
        System.out.println("Name: "+learner2.learnerName);
        System.out.println("Course Id: "+learner2.eduCourse);

      //Printing all the courses of 'learner2'
        System.out.println("Courses of Learner 2: ");
        System.out.println(learner2.eduCourse.course1);
        System.out.println(learner2.eduCourse.course2);
        System.out.println(learner2.eduCourse.course3);       

        //Changing the course3 of 'learner2' 
        learner2.eduCourse.course3 = "JSP";

        //This change will be reflected in original 'learner1' 
        System.out.println("Updated Courses of Learner 2:");
        System.out.println(learner1.eduCourse.course1);
        System.out.println(learner1.eduCourse.course2);
        System.out.println(learner1.eduCourse.course3);
    }
}
```

**输出:**

```
Details of Learner 2: 
Id: 2811
Name: Max
Course Id: EduCourse@15db9742
Courses of Learner 1: 
Java
Spring
Microservices
Details of Learner 2: 
Id: 2811
Name: Max
Course Id: EduCourse@15db9742
Courses of Learner 2: 
Java
Spring
Microservices
Updated Courses of Learner 2:
Java
Spring
JSP
```

### **Java 中的深度克隆**

在 Java 中，当克隆过程通过实现 Cloneable 接口来完成时，这被称为深度克隆。在这种类型的克隆中，将创建原始对象的所有字段的精确副本。但是如果原始对象引用其他对象作为字段，那么通过调用 clone()方法也将创建这些对象的副本。这使得克隆对象独立于原始对象，并且在任一对象中所做的任何更改都不会反映到另一个对象上。

![deep copy - Cloning in Java - Edureka](img/1532465f42555e2bd6d72b9526e3b567.png)

下面我已经举了同样的例子:

```
package edureka;
class EduCourse implements Cloneable
{
    String course1;
    String course2;
    String course3;

    public EduCourse(String crs1, String crs2, String crs3)
    {
        this.course1 = crs1; 
        this.course2 = crs2; 
        this.course3 = crs3;
    }

    protected Object clone() throws CloneNotSupportedException
    {
        return super.clone();
    }
}

class EduLearner implements Cloneable
{
	int eduId; 
    String learnerName; 
    EduCourse eduCourse;

    public EduLearner(int eduId, String learnerName, EduCourse eduCourse)
    {
    	this.eduId = eduId; 
        this.learnerName = learnerName; 
        this.eduCourse = eduCourse;
    }

    //Overriding clone() method for creating a deep copy of an object

    protected Object clone() throws CloneNotSupportedException
    {
        EduLearner learner = (EduLearner) super.clone();

        learner.eduCourse = (EduCourse) eduCourse.clone();

        return learner;
    }
}

public class DeepCloneSample
{
    public static void main(String[] args)
    {
        EduCourse j2ee = new EduCourse("Java", "Spring", "Microservices"); 
        EduLearner learner1 = new EduLearner(2811, "Max", j2ee); 
        EduLearner learner2 = null;

        try
        {
            //Creating a clone of learner1 and assigning it to learner2

            learner2 = (EduLearner) learner1.clone();
        }
        catch (CloneNotSupportedException e)
        {
            e.printStackTrace();
        }

      //Printing Details of Learner1
        System.out.println("Details of Learner 2: ");
        System.out.println("Id: "+learner1.eduId);
        System.out.println("Name: "+learner1.learnerName);
        System.out.println("Course Id: "+learner1.eduCourse);

        //Printing all the courses of 'learner1'
        System.out.println("Courses of Learner 1: ");
        System.out.println(learner1.eduCourse.course1);
        System.out.println(learner1.eduCourse.course2);
        System.out.println(learner1.eduCourse.course3);

      //Printing Details of Learner2
        System.out.println("Details of Learner 2: ");
        System.out.println("Id: "+learner2.eduId);
        System.out.println("Name: "+learner2.learnerName);
        System.out.println("Course Id: "+learner2.eduCourse);

      //Printing all the courses of 'learner2'
        System.out.println("Courses of Learner 2: ");
        System.out.println(learner2.eduCourse.course1);
        System.out.println(learner2.eduCourse.course2);
        System.out.println(learner2.eduCourse.course3);       

        //Changing the course3 of 'learner2' 
        learner2.eduCourse.course3 = "JSP";

        //This change won't be reflected in original 'learner1' 
        System.out.println("Courses of Learner 1:");
        System.out.println(learner1.eduCourse.course1);
        System.out.println(learner1.eduCourse.course2);
        System.out.println(learner1.eduCourse.course3);

        //Updated Courses of learner2
        System.out.println("Courses of Learner 2:");
        System.out.println(learner2.eduCourse.course1);
        System.out.println(learner2.eduCourse.course2);
        System.out.println(learner2.eduCourse.course3);
    }
}
```

**输出:**

```
Details of Learner 2: 
Id: 2811
Name: Max
Course Id: edureka.EduCourse@15db9742
Courses of Learner 1: 
Java
Spring
Microservices
Details of Learner 2: 
Id: 2811
Name: Max
Course Id: edureka.EduCourse@6d06d69c
Courses of Learner 2: 
Java
Spring
Microservices
Courses of Learner 1:
Java
Spring
Microservices
Courses of Learner 2:
Java
Spring
JSP
```

这就把我们带到了这篇关于 Java 克隆的文章的结尾。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*既然您已经理解了什么是 Java 中的克隆，那么就来看看 Edureka 的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-training-course)*吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“用 Java 克隆”文章的评论部分提到它，我们会尽快回复您。*