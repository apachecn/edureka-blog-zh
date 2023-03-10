# Java 注释的完整介绍

> 原文：<https://www.edureka.co/blog/annotations-in-java/>

[Java](https://www.edureka.co/java-j2ee-training-course) 中的**注释是一种特殊的 Java 构造，用作源代码中使用的类元素的*装饰性语法元数据*，以提供特殊信息来指导 Java 解释器进行代码翻译。在本文中，我们将讨论以下概念。**

*   [Java 中的注释是什么？](#an)
*   我们为什么需要注释？
*   [注释类型](#type)
*   [Java 内置注释](#built)
*   [用 Java 自定义注释](#custom)

## **Java 中的注释是什么？**

注释用于表示与源代码中使用的 *类、接口、方法或字段*相关的语法元数据，以及 java 解释器和 JVM 使用的的一些附加信息。在这篇文章中，我们将讨论以下概念。

## 我们为什么需要注释？

**编译器指令**

内置注释如 **@Override、@Deprecated、**和 **@SuppressWarnings** 为解释器提供了与代码执行相关的信息。例如， *@Override* 用于指示解释器注释的方法正在被覆盖。

**![Compiler instructions](img/50282bde8384c5241d6e19fc6df1377f.png)构建时指令**

注释向解释器提供*构建时/编译时*指令，这些指令被软件构建工具用来生成代码， *Pom。XML* 文件等。

**![](img/b99e9887fbbc0fc73b7b79f9a4057a9d.png)运行时指令**

注释可以在*运行时*定义，这样它们就可以在运行时访问并向程序提供指令。

## **![](img/15d967a50991db738f1731c66261b8c5.png)**

现在，让我们来讨论它们的类型。

## **注释类型**

注释通常分为三种类型，如下所述:

**![Annotations-in-Java-Edureka-Types-of-Annotations](img/9da59487e1d4ccd2a7d6a2057289cbd7.png)**

**标记注释**

标记注释是为了描述其存在的标记而声明的。它们不包含任何成员，这使它们保持为空。 *@Override 是标记注释*的一个例子。

```
package Types;
@interface MarkerTypeAnnotation{}

```

**单个注释**

名称本身表明单个注释被设计成在其中包含一个*单个成员*。简写方法用于将值指定给在单个注释中声明的成员。

```
package Types;
@interface SingleTypeAnnotation{
int member() default 0;
}

```

**完整注释**

完整或多个注释类似于单个注释，但它们可以包括*多个*成员/名称、值、对。

```
package Types;
@interface FullAnnotationType{  
     int member1() default 1;  
     String member2() default "";  
     String member3() default "abc";  
}

```

Java 也提供了一些内置的注释。

## **Java 内置注释**

**![Annotations-in-Java-Edureka-Types-of-built-in-Annotations](img/fa8cd17a02cd2aad72fe1923230e9f68.png)**

**保留注释**

保留注释被设计为向*指示带有注释类型的特定注释将被保留多长时间*。以下是保留注释的示例

```
package Retention;

import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;

@Retention(RetentionPolicy.RUNTIME)
public @interface EdurekaAnnotation {
     String MethodName();
     String Description();
}

class RetentnionTest{
      @EdurekaAnnotation(MethodName = "Retention Annotation test", Description = "testing annotations")
       public void TestMethod(){
       }
}

```

**弃用的注释**

弃用的注释用于通知编译器，特定的方法、类或字段*不重要*，它表明一个声明已经过时。

```
package Deprecated;

public class Deprecated {
     @Deprecated
      public void Display() {
            System.out.println("Deprecated Annotation test Method()");
      }

      public static void main(String args[]) {
            Deprecated Dep = new Deprecated();
            Dep.Display();
      }
}

```

**覆盖注释**

它是一种标记类型的注释。Override 注释被设计为确保超类方法被覆盖，而不是重载。用@Override 注释的方法应该重写超类中的方法，否则将引发编译时错误。

```
package Override;

class Parent {
      public void Display() {
             System.out.println("Parent Class Method exrecuting()");
      }
      public static void main(String args[]) {
      Parent P1 = new Child();
      P1.Display();
      }
}
class Child extends Parent {
     @Override
      public void Display() {
            System.out.println("Child Class Method exrecuting()");
      }
}

```

**抑制警告注释**

抑制警告注释用于在程序执行期间*消除/抑制*解释器警告。抑制警告注释可以应用于任何类型的声明。下面是这种注释的一个例子。

```
package SuppressWarning;

class DeprecatedTest {
    @Deprecated
     public void Display() {
          System.out.println("Deprecated test display()");
     }
}

public class SuppressWarning{
     @SuppressWarnings({"checked", "deprecation"})
       public static void main(String args[]) {
       DeprecatedTest d1 = new DeprecatedTest();
       d1.Display();
       }
}

```

**继承注释**

默认情况下，Java 中的注释不会被子类继承。因此，继承的注释标记了将被继承给子类的注释。下面是一个继承注释的例子

```
package Inherited;
       public @interface MyAnnotation {
}

```

```
package Inherited;
       public @interface MyInheritedAnnotation {
}

```

```
package Inherited;
@MyAnnotation
@MyInheritedAnnotation
public class BaseClass {
}

```

```
package Inherited;
public class SubClass extends BaseClass {
}

```

```
package Inherited;
public class ExampleMain {
      public static void main(String[] args) {
            MyAnnotation myannotation = SubClass.class.getAnnotation(MyAnnotation.class);
            System.out.println(myannotation);
            MyInheritedAnnotation myannotation2 = SubClass.class.getAnnotation(MyInheritedAnnotation.class);
            System.out.println(myannotation2);
     }
}

```

**目标注释**

目标标签用于指定所用注释的类型。注释库声明了许多常量来指定需要应用注释的元素的类型，如*类型、方法、字段*等。我们可以从**Java . lang . annotation .****element type**中访问目标标签

| **元素类型** | **要应用的注释的位置** |
| **类型** | 类、接口或枚举 |
| **字段** | 菲尔茨 |
| **方法** | 方法 |
| **构造器** | 构造器 |
| **局部变量** | 局部变量 |
| **注释 _ 类型** | 注释类型 |
| **参数** | 参数 |

```
package Target;
public @interface CustomAnnotation {
}
import java.lang.annotation.ElementType;
import java.lang.annotation.Target;
@Target({ElementType.METHOD})
public @interface MyCustomAnnotation {
}
public class target {
      @CustomAnnotation
       public void myMethod(){
             System.out.println("Hello World");
       }
}

```

**已记录的注释**

这是一种标记类型的注释，用于与记录注释的工具进行通信。默认情况下，注释不包含在 Javadoc 注释中。在代码中使用文档化的注释使 Javadoc 能够在结果文档中处理和包含注释类型的信息。

```
package Documented;
import java.lang.annotation.Documented;
@Documented
public @interface DocumentAnnotation {
      class AddNumbers{
             public static void main(String args[]){
                   int x=10,y=20,z;
                   z = x + y;
                  System.out.println("Sum of the integers = " + z);
             }
       }
}

```

## **Java 中的自定义注释**

Java 自定义注释是用户自定义的注释，易于创建和使用。@Interface 元素用于声明一个注释。自定义注释的示例如下。

```
package Custom;

import java.lang.annotation.Documented;
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;

@Documented
@Retention(RetentionPolicy.RUNTIME)
@ interface TestAnnotation {
       String Developer() default "Edureka";
       String Expirydate();
}

public class Custom {
        @TestAnnotation(Developer="Rajesh", Expirydate="01-Aug-2026")
         void function1() {
                 System.out.println("Testing Annotation method 1");
          }

         @TestAnnotation(Developer="Anil", Expirydate="01-Oct-2025")
          void function2() {
                System.out.println("Test Annotation method 2");
          }
          public static void main(String args[]) {
                  System.out.println("Customized Annotations Example");
          }
}

```

就这样，我们来到了这篇文章的结尾。我希望您已经理解了 Java 中注释的基础知识，它的类型以及 Java 中可用的内置注释。

*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这篇“Java 注释”文章的评论部分提到它，我们会尽快回复您。