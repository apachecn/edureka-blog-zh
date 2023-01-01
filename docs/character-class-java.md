# Java 中的 char:Java 中的 Character class 是什么？

> 原文：<https://www.edureka.co/blog/character-class-java>

在 Java 中，我们会遇到需要使用对象而不是原始数据类型的情况。为了实现这一点， [Java](https://www.edureka.co/java-j2ee-training-course) 为原语[数据类型](https://www.edureka.co/blog/data-types-in-java/) *char* 提供了包装类 *Character* 。在这篇关于 Java 中的 Char 的文章中，让我们详细了解一下。

本文将涵盖以下主题:

*   [Java 中的字符类](#CharacterclassinJava)
*   [转义序列](#Escapesequence)
*   [字符类的方法](#Methodsofcharacterclass)

我们开始吧！

## **Java 中的字符类**

*字符类*通常将所有原始类型 c *har* 的值包装到一个[对象](https://www.edureka.co/blog/java-objects-and-classes/)中。任何字符类型的对象都可以包含一个类型为 *char* 的字段。Character 类提供了许多有用的类(即静态的)[方法](https://www.edureka.co/blog/java-methods/)来处理角色。

使用角色[构造器](https://www.edureka.co/blog/constructor-in-java/) 创建角色对象

```
Character ch = new Character('a');

```

上面的语句创建了一个包含 char 类型的“a”的字符对象。character 类中只有一个构造函数需要 char 数据类型的参数。

接下来，在这篇关于 Java 中的 Char 的文章中，让我们看看 Java 中字符使用的一些转义序列。

## **转义序列**

前面有一个*反斜杠()*的字符通常称为转义序列。下面有一个表格可以帮助你理解这个概念。

| **转义序列** | **描述** |
| t | 此时在文本中插入一个制表符。 |
| n | 它在文本中插入一个新行。 |
| b | 此时在文本中插入一个退格键。 |
| r | 它在文本中插入一个回车。 |
| f | 此时，它会在文本中插入一个换页符。 |
| ' | 此时在文本中插入一个单引号字符。 |
| \" | 此时，它在文本中插入一个双引号字符。 |
| \ | 此时在文本中插入一个反斜杠字符。 |

既然你已经理解了转义序列，让我们继续理解 Java 中字符类提供的方法。

## **字符类的方法**

下表讨论了 character 类的几个重要的[方法](https://www.edureka.co/blog/java-methods/)。

| **方法** | **描述** |
| isWhitespace() | 它有助于确定指定的字符值是否为空白。 |
| isdigital() | 它有助于确定指定的 char 值是否为数字。 |
| isLetter() | 它有助于确定字符值是否是字母。 |
| isUpperCase() | 它有助于确定指定的 char 值是否为大写。 |
| isLowerCase() | 它有助于确定指定的 char 值是否为小写。 |
| toUpperCase() | 它返回指定字符值的大写形式。 |
| toLowerCase() | 它返回指定字符值的小写形式。 |
| toString() | 它返回一个表示指定字符值的字符串对象 |

接下来，在这篇关于 Java 中的 Char 的文章中，让我们看看上面讨论的方法的实际实现。

### **代码:**

```

import java.util.Scanner;
public class JavaCharacterExample1 {
public static void main(String[] args) {
// Ask the user for the first input.
System.out.print("First input:");
// Use the Scanner class to get the user input.
Scanner scanner = new Scanner(System.in);
// Gets the user input.
char[] value1 = scanner.nextLine().toCharArray();
int result1 = 0;
// Count the characters for a specific character.
for (char ch1 : value1) {
result1 = Character.charCount(ch1);
}
// Print the result.
System.out.print("Value: "+result1+"n");
System.out.print("Second input:");
char[] value2 = scanner.nextLine().toCharArray();
for (char ch2 : value2) {
int result2 = Character.hashCode(ch2);
System.out.print("The hash code for the character '"+ch2+"' is given as:"+result2+"n");
}
System.out.print("Third input:");
char[] value3 = scanner.nextLine().toCharArray();
for (char ch3 : value3) {
boolean result3 = Character.isDigit(ch3);
if(result3){
System.out.println("The character '" + ch3 + "' is a digit. ");
}
else{
System.out.println("The character '" + ch3 + "' is not a digit.");
}
System.out.print("Fourth input:");
char[] value4 = scanner.nextLine().toCharArray();
for (char ch4 : value4) {
boolean result4 = Character.isISOControl(ch4);
System.out.println("The fourth character '"+ch4+"' is an ISO Control:"+result4);
}
}
}
}

```

### **输出:**

```
First input:89
Value: 1
Second input:J
The hash code for the character 'J' is given as:74
Third input:5
The character '5' is a digit.
Fourth input:h
The fourth character 'h' is an ISO Control:false

```

至此，我们结束了这篇关于 Java 中 Char 的文章。我希望你理解了 Java 的基础知识。如果你找到了这篇关于“Java 中的 Char”的文章，请查看 Edureka 的  **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你踏上成为 java 开发者的每一步。除了这个面试问题，我们还为想成为 Java 开发者的学生和专业人士设计了一个课程。

有问题要问我们吗？请在这个“Java 中的字符*的评论区提出来，我们会尽快回复你。*