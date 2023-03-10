# Java 中的比较器接口是什么？

> 原文：<https://www.edureka.co/blog/comparator-interface-java/>

比较器是 Java 中最有用也是最令人困惑的话题之一。有用是因为它为[集合](https://www.edureka.co/blog/java-collections/)对象提供了排序方法，令人困惑是因为它听起来类似于 Java 中的[可比接口](https://www.edureka.co/blog/comparable-in-java/)。因此，我带来了这篇文章，在这篇文章中，我将消除围绕 Java 中的 Comparator 的所有疑问。

*   [Java 中的比较器是什么？](#whatiscomparator)
*   [Java 比较器接口的方法](#methodsofjavacomparator)
*   [演示:Java 比较器示例](#demo)
*   [比较国 vs 可比国](#comparatorvscomparable)

让我们开始吧。

## **Java 中的比较器是什么？**

Java Comparator 接口用于对自定义[类](https://www.edureka.co/blog/java-objects-and-classes/)中的[对象](https://www.edureka.co/blog/java-object/)进行排序。这个接口在 **java** 中都有。 **util 包**包括两个重要的方法 compare(Object obj1，Object obj2)和 equals(Object element)。

现在，让我们来了解一下 Java 比较器的各种方法:

## **Java 比较器接口的方法**

Java 中有两种比较器的方法，即:

| 方法 | 描述 |
| 比较(对象 obj1，对象 obj 2) | 将第一个对象与另一个对象进行比较 |
| 等于(对象对象) | 将当前对象与指定对象进行比较 |

下面的代码描述了 Java Comparator 对这两种方法的使用。

## **Java 比较器示例**

//员工数据

```
package JavaComparator;

import java.util.*;
import java.lang.*;
import java.io.*;

class Employee {
        int EmpID;
        String name, address;
        public Employee(int EmpID, String name, String address) {
                this.EmpID = EmpID;
                this.name = name;
                this.address = address;
        }
        public String toString() {
               return this.EmpID + " " + this.name + " " + this.address;
              }
        }
        class Sortbyroll implements Comparator<Employee> {
             public int compare(Employee a, Employee b){
                  return a.EmpID - b.EmpID;
             }
       }
       class Sortbyname implements Comparator<Employee> {
              public int compare(Employee a, Employee b) {
             return a.name.compareTo(b.name);
      }
}
class Main {
       public static void main (String[] args){
              ArrayList<Employee> Arr = new ArrayList<Employee>();
              Arr.add(new Employee(1011, "Rajesh", "Bangalore"));
              Arr.add(new Employee(1031, "Ralph", "Hyderabad"));
              Arr.add(new Employee(1201, "Karan", "Haryana"));
              System.out.println("Unsorted Data");
              for (int i=0; i<Arr.size(); i++)
                    System.out.println(Arr.get(i));
                    Collections.sort(Arr, new Sortbyroll());
                    System.out.println("nSorted data according to Employee IDs");
                    for (int i=0; i<Arr.size(); i++)
                          System.out.println(Arr.get(i));
                          Collections.sort(Arr, new Sortbyname());
                          System.out.println("nSorted data according to Employee name");
                          for (int i=0; i<Arr.size(); i++)
                                  System.out.println(Arr.get(i));
        }
}

```

**输出:**

未分类数据 1011 拉杰什班加罗尔 1031 拉尔夫海得拉巴 1201 卡兰哈里亚纳邦

根据员工 id 排序的数据 1011 Rajesh Bangalore1031 Ralph Hyderabad1201 Karan Haryana

根据员工姓名排序的数据 1201 Karan Haryana1011 Rajesh Bangalore1031 Ralph Hyderabad

让我们来理解一下 [Java](https://docs.oracle.com/javase/tutorial/) Comparable 的第二种方法，即 equals 方法。

**Java equals()示例:**

```
package Equals;

public class EqualsExample {
             public static void main(String equals) {
             System.out.println(new Eqls("Harsha", 35, 12000).equals(new Eqls("Hari",25,12000)));
             System.out.println(new Eqls("Karan", 44, 45000).equals(new Eqls("Karan", 44, 45000)));
             System.out.println(new Eqls("latha", 54, 60000).equals(new Object()));
      }
      static class Eqls{
             private String name;
             private int age;
             private int Salary;
             public Eqls(String name, int age, int Salary) {
                     this.name = name;
                     this.age = age;
                     this.Salary = Salary;
             }
  @Override
      public boolean equals(Object o) {
      if (this == o) {
              return true;
      }
      if (o == null || getClass() != o.getClass()) {
              return false;
      }
      Eqls eqls= (Eqls) o;
      return age == eqls.age &&
      Salary == eqls.Salary &&
      name.equals(eqls.name);
      }
   }
}

```

**输出:**

假真假

在了解了 Java Comparator 接口之后，让我们进入下一个话题，即 Comparable vs Comparable。

## **比较器与可比器**

| 比较仪 | 可比较的 |
| 比较器用于对不同对象的属性进行排序。 | 可比较接口用于以自然顺序对对象进行排序。 |
| 比较器接口比较提供的两个不同的类对象。 | Comparable 接口将“this”引用与指定的对象进行比较。 |
| java.util 包中有一个比较器。 | java.lang 包中有 Comparable。 |
| 比较器不影响原始类 | Comparable 影响原始类，即实际类被修改。 |
| 比较器提供 compare()方法，equals()方法对元素进行排序。 | Comparable 提供 compareTo()方法对元素进行排序。 |

这就把我们带到了这篇关于 Java comparator 的文章的结尾。如果你想了解更多关于 Java 的知识，你可以参考我们的 [其他 Java 博客](https://www.edureka.co/blog/what-is-java/) 。

**如果您找到了这篇关于“Java 中的比较器* *”的相关文章，*请查看 Edureka 提供的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，这是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate Spring。*

有问题要问我们吗？请在这篇“Java 中的比较器”文章*的评论部分提到它，我们会尽快回复您。*