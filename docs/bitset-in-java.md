# java 中的 bitest:关于 java 中的位集方法，您需要知道的一切

> 原文：<https://www.edureka.co/blog/bitset-in-java/>

Java 认证是程序员最关心的认证之一。主要原因是 Java 提供了极大的灵活性和不同的特性来简化各种任务。本文将向您介绍一个这样的特性，即 Java 中的“**位集”。本文将关注以下几点:**

*   [Java 中的位集是什么？](#WhatareBitsetsinJava?)
*   [Bitset Java 方法](#BitsetJavaMethods)

那么让我们从接下来讨论的第一个话题开始，

## **Java 中的位集是什么？**

比特集表示具有值 0 或 1 的 N 比特的固定大小序列。零表示值为假或未设置。一表示值为真或已设置。位集大小在编译时是固定的。 Bitset 是 java.util 包中定义的类。它是保存位值的特殊类型的数组。它实现了一个位向量。 当需要更多比特时，它的大小会自动增长。

这个类为我们提供了两种类型的构造函数来从整数和字符串中形成位集。那两个是:

*   **Bitset( ):** 它是一个无参数的构造函数，用来创建默认对象。
*   **Bitset(int size):** 它是一个单构造函数，具有整数参数，以形成 Bitset 类的实例，整数参数的初始大小表示位数。

**例如:**

```

 import java.util.BitSet;
public class BitSetJavaExample
{
public static void main(String args[])
{
int n=8;
BitSet p = new BitSet(n);
for(int i=0;i<n;i++)
p.set(i);
System.out.print("Bits of p are set as : ");
for(int i=0;i<n;i++)
System.out.print(p.get(i)+" ");
BitSet q = (BitSet) p.clone();
System.out.print("nBits of q are set as : ");
for(int i=0;i<n;i++)
System.out.print(q.get(i)+" ");
for(int i=0;i<3;i++)
p.clear(i);
System.out.print("nBits of p are now set as : ");
for(int i=0;i<n;i++)
System.out.print(p.get(i)+" ");
System.out.print("nBits of p which are true : "+p);
System.out.print("The Bits of q which are true : "+q);
BitSet r= (BitSet) p.clone();
p.xor(q);
System.out.println("Output of p xor q= "+p);
p = (BitSet) r.clone();
p.and(q);
System.out.println("Output of p and q = "+p);
p = (BitSet) r.clone();
p.or(q);
System.out.println("Output of p or q = "+p);
}
}

```

**输出**

![Output - Bitsets in Java - Edureka](img/3327794d688bf7cbb6fa15383440b9fc.png)

现在让我们更进一步，看看本文讨论的下一个主题 Java 中的位，

## **BITSET JAVA 方法和描述**

### **Bitset 和( )方法 **

此方法用于使用指定的参数对目标位集执行逻辑 AND 运算。set 的值只有在初始位集和相应的位集都具有真值时才为真。

**语法:**public void and(bit set set)

**举例:**

```

import java.util.BitSet;
public class BitSetAndExample2
{
public static void main(String[] args)
{
// create 2 bitsets
BitSet bitset1 = new BitSet();
BitSet bitset2 = new BitSet();

// assign values to bitset1
bitset1.set(1);
bitset1.set(2);
bitset1.set(3);
bitset1.set(6);
bitset1.set(7);

// assign values to bitset2
bitset2.set(10);
bitset2.set(20);
bitset2.set(30);
bitset2.set(40);
bitset2.set(60);

// print the sets
System.out.println("bitset1: " + bitset1);
System.out.println("bitset2: " + bitset2);

// perform and operation between two bitsets
bitset1.and(bitset2);
// print the new bitset1
System.out.println("result bitset: " + bitset1);
}
}
```

**输出:**

![Output - Bitsets in Java - Edureka](img/894d1ffbe3b7d147a3c5cf1e56b94f8b.png)

### **Bitset andNot()方法**

此方法用于清除位集中的整个位，其对应的位已经在指定的位集中设置。

**语法-**public void and not(bit set set)

**举例:**

```

import java.util.BitSet;
public class BitSetAndNotExample2
{
public static void main(String[] args)
{
BitSet bitset1 = new BitSet();

bitset1.set(60);
bitset1.set(61);
bitset1.set(62);
bitset1.set(63);
bitset1.set(64);
// print the sets
System.out.println("bitset1: " + bitset1);

// perform andNot operation between bitset and null throw exception
bitset1.andNot(null);
// print the new bitset1
System.out.println("result bitset after andNot: " + bitset1);
}
}
```

**输出:-**

### **![output - Edureka](img/6308ff88fe9f0cc813266f77fa877e08.png)**

### **Bitset cardinality()方法**

此方法用于仅返回位集中为真的位数。

**语法-**public int cardinality()

**例题**

```

import java.util.BitSet;
public class BitSetCardinalityExample1
{
public static void main(String[] args)
{
// create a bitset
BitSet bitset = new BitSet();

// assign values to bitset
bitset.set(10);
bitset.set(11);
bitset.set(12);
bitset.set(15);
bitset.set(16);

// print the sets
System.out.println("bitset: " + bitset);
int trueBits = bitset.cardinality();
// print bitset cardinality
System.out.println("number of true bits: " + trueBits);

bitset.clear(2);
System.out.println("bitset after clear index 2: " + bitset);
trueBits = bitset.cardinality();
// print bitset cardinality after clear index 2
System.out.println("number of true bits after clear index 2: " + trueBits);

}
}
```

**输出-**

### **![output - Bitset In Java - Edureka](img/38a6c3fd4335d0a4937ff871bf0cf3a0.png)**

### **BitSet clone()方法**

此方法用于将位集克隆为新的位集。该位集等于当前的原始位集。克隆位集具有与原始位集完全相同的真值。

**语法-** 公共对象克隆()

**举例***–*

```

import java.util.BitSet;
public class BitSetCloneExample1
{
public static void main(String[] args)
{
BitSet bitsetOriginal = new BitSet(15);
bitsetOriginal.set(12);
bitsetOriginal.set(13);
bitsetOriginal.set(15);
bitsetOriginal.set(16);
bitsetOriginal.set(18);
//print current bitset
System.out.println("Current bitset: "+bitsetOriginal);
// making clone of current bitset
Object bitsetClone = bitsetOriginal.clone();
//print clone bitset
System.out.println("Clone bitset: "+bitsetClone);
}
}
```

**输出**

**![output - Bitset In Java - Edureka](img/fbc311a8ec62d13f60dec57ab4225604.png)**

### **BitSet equals()方法**

JAVA bitset 的这个方法用于将当前的 bitset 对象与指定的 bitset 对象进行比较。

当且仅当指定的位集对象不为空，并且位集对象的集合应该具有与该位集完全相同的位集到真值集合时，位集比较的结果返回真。

**语法-** 公共布尔等于(对象 obj)

**举例***–*

```
</pre>
import java.util.BitSet;

public class BitSetEqualsExample1
{
public static void main(String[] args)
{
// creating bitset
BitSet bitset = new BitSet(15);

Object obj = new BitSet(15);

bitset.set(10);
bitset.set(11);
bitset.set(12);
bitset.set(13);
bitset.set(14);

((BitSet) obj).set(10);
((BitSet) obj).set(11);
((BitSet) obj).set(12);
((BitSet) obj).set(13);
((BitSet) obj).set(14);

// print current bitsets
System.out.println("bitset:" + bitset);
System.out.println("object:" + obj);
boolean bol = bitset.equals(obj);
if(bol==true) {
System.out.println("BitSet is equal to specified Object");
}
else {
System.out.println("BitSet is not equal to specified Object");
}
}
}
<pre>

```

**输出**

### **![output - Bitset In Java - Edureka](img/76e3509df2767def019900f72278dea1.png)**

### **BitSet 是一个空方法**

如果此位集不包含设置为 true 的位，则此方法返回 true。

**语法-** 公共布尔 isEmpty( )

**例子**

```

import java.util.BitSet;

public class BitSetIsEmptyExample1
{
public static void main(String[] args)
{
BitSet bitset1 = new BitSet(15);
BitSet bitset2 = new BitSet(15);

bitset1.set(11);
bitset1.set(12);
bitset1.set(13);
bitset1.set(14);

System.out.println("bitset1: "+bitset1);
System.out.println("bitset2: "+bitset2);

//returns false as bitset1 is not empty
boolean b1 = bitset1.isEmpty();
//returns true as bitset2 is empty
boolean b2 = bitset2.isEmpty();

System.out.println("bitset1 isEmpty: "+b1);
System.out.println("bitset2 isEmpty: "+b2);
}
}

```

**输出**

**![output - Bitset In Java - Edureka](img/75232a8ccf62bc3005bdd4f836fbbdb5.png)**

### **BitSet length()方法**

此方法返回该位集的逻辑大小。长度上升到最高设置位的索引加 1。如果位组不包含任何位，则返回零。

**语法-** public int length( )

**举例-**

```

import java.util.BitSet;

public class BitSetLengthExample1
{
public static void main(String[] args)
{
BitSet bitset1 = new BitSet(15);
BitSet bitset2 = new BitSet(15);
BitSet bitset3 = new BitSet(15);

bitset2.set(11);
bitset2.set(12);
bitset2.set(13);
bitset2.set(14);

bitset3.set(12);
bitset3.set(14);
bitset3.set(16);
bitset3.set(18);
bitset3.set(0);
bitset3.set(2);

System.out.println("bitset1: "+bitset1);
System.out.println("bitset2: "+bitset2);
System.out.println("bitset3: "+bitset3);

int length1 = bitset1.length();
int length2 = bitset2.length();
int length3 = bitset3.length();
System.out.println("length of bitset1: "+length1);
System.out.println("length of bitset2: "+length2);
System.out.println("length of bitset3: "+length3);
}
}
```

**输出-**

### **![output - Bitset In Java - Edureka](img/1b85cf754e2be9b97076b0c4106a2862.png)**

### **BitSet intersects()方法**

该方法根据参数位集是否与位集相交来返回布尔值 true 或 false。如果该位集中的位集也为真，则返回真。

**语法-** 公共布尔交集(BitSet set )

**例子**

```

import java.util.BitSet;

public class BitSetEntersectsExample2
{
public static void main(String[] args)
{
BitSet bitset = new BitSet(15);

bitset.set(11);
bitset.set(12);
bitset.set(13);
bitset.set(14);

System.out.println("bitset: "+bitset);
// perform andNot operation between bitset and null throw exception
boolean b = bitset.intersects(null);
System.out.println("intersected result between bitset and null: "+b);
}
}
```

**输出-**

![output - Bitset In Java - Edureka](img/77bbe08cca523ffcd92f2a1ffd87c179.png)

借助于按位运算符，我们可以实现各种运算，如与、或、非、异或等。他们的工作规模较小。它们可以应用于任何整数类型。按位运算符在比特级进行运算。它们速度更快，需要的内存更少。许多加密算法也在比特级别工作。

伙计们，到了。这就把我们带到了这篇关于 Java 中的位的文章的结尾。我希望你喜欢这条信息。查看值得信赖的在线学习公司 Edureka 的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证旨在为您提供 Java 编程的良好开端，并培训您核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。