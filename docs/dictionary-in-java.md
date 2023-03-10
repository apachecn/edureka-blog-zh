# Java 中的字典是什么，如何创建？

> 原文：<https://www.edureka.co/blog/dictionary-in-java/>

Java 中的 Dictionary 是一个抽象类，它是任何使用键值对关系的类的父类。在这篇博客中，我们将学习更多关于 Java 中的 Dictionary 类，并熟悉不同的方法。以下是本博客的主题-

*   [Java 中的字典是什么？](#what)
*   [利用的方法。字典类](#methods)

*   [用 Java 实现字典](#implement)

## **Java 中的字典是什么？**

Dictionary 是一个[抽象类](https://www.edureka.co/blog/abstract-classes-in-java/)，表示一个键/值存储库，其操作类似于[映射](https://www.edureka.co/blog/java-map-interface)。您可以将值存储在 Dictionary 对象中，一旦存储，就可以使用它的键来检索它。

### **声明:**

公共抽象类字典扩展对象

### **建造师:**

Dictionary()构造函数

## **利用的方法。字典类**

让我们来看看字典类的几种不同的方法。

### **检查字典的大小**

size():返回字典中键值对的数量

**语法:** 公共抽象 int size()

### **在字典中添加/放置值**

put(K key，V value):Java . util . dictionary . put(K key，V value)将键值对添加到字典中

**语法:** 公共抽象 V 放(K 键，V 值)

### **返回字典中存在的值**

elements():Java . util . dictionary . elements()返回字典中的值表示

**语法:** 公共抽象枚举元素()

### **Get 方法获取用键**映射的值

get(对象键):java.util.Dictionary.get(对象键)返回用字典中的键映射的值

**语法:** 公共抽象 V get(对象键)

### **检查字典是否为空**

isEmpty():Java . util . dictionary . isEmpty()检查字典是否为空。

**语法:** 公共抽象布尔 isEmpty()

如果字典中没有键值关系，则返回 true 否则返回 false。

**从 Java 字典中删除键值**

remove(Object key):Java . util . dictionary . remove(Object key)删除用键映射的键值对。

**语法:** 公共抽象 V remove(对象键)

## **用 Java 实现字典**

```
import java.util.*; 
public class My_Class 
{ 
    public static void main(String[] args) 
    { 
       // Initializing a Dictionary 
        Dictionary edu = new Hashtable(); 
       // put() method 
        edu.put("1000", "Edureka"); 
        edu.put("2000", "Platfrom"); 
       // elements() method : 
        for (Enumeration i = edu.elements(); i.hasMoreElements();) 
        { 
            System.out.println("Value in Dictionary : " + i.nextElement()); 
        } 
        // get() method : 
        System.out.println("nValue at key = 3000 : " + edu.get("2000")); 
        System.out.println("Value at key = 1000 : " + edu.get("2000")); 
        // isEmpty() method : 
        System.out.println("nThere is no key-value pair : " + edu.isEmpty() + "n"); 
        // keys() method : 
        for (Enumeration k = edu.keys(); k.hasMoreElements();) 
        { 
            System.out.println("Keys in Dictionary : " + k.nextElement()); 
        } 
       // remove() method : 
        System.out.println("nRemove : " + edu.remove("1000")); 
        System.out.println("Check the value of removed key : " + edu.get("1000")); 
        System.out.println("nSize of Dictionary : " + edu.size()); 
}
 } 

```

**输出:**

字典中的值:Edureka 字典中的值:平台key 处的值= 3000:nullkey 处的值= 1000:平台 没有键-值对:字典中的假 键:1000 字典中的键:2000 删除:Edureka

至此，我们结束了这篇关于 Java 字典类的博客。如果您想了解更多，请查看 Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & [Spring](https://spring.io/) 。

有问题要问我们吗？请在这个“Java 字典”博客的评论部分提到它，我们会尽快回复您。