# Java 中的替换:你需要知道的一切

> 原文：<https://www.edureka.co/blog/replace-in-java/>

替换一个数字或一串字符是一件有趣的事情，无论是 [Java](https://www.edureka.co/blog/java-tutorial/) 、 [Python](https://www.edureka.co/blog/python-tutorial/) 还是任何其他编程语言。然而，在本文中，我们将按照以下顺序关注 Java 中的替换:

*   [更换类型](#types)
*   [替换](#replace)
*   [ReplaceAll](#replaceall)
*   [replace first](#replace-first)

## **Java 中替换的类型**

替换 Java 字符串有三种方法。

*   替换
*   ReplaceAll(全部替换)
*   替换优先

![Replace in Java](img/1ebba2dd90ef6924482a727cdd99861a.png)

借助这些选项，您可以替换字符串中的任何字符。

## **在 Java 中替换**

**String replace():** 这个方法通过用一个新字符替换每个出现的字符，返回一个新的字符串作为输出。

**语法:**

`public Str replace(char oldC, char newCh)`

**参数:**

`oldCh − old character`

`newCh − new character`

**返回值:**

这会将字符串中的 oldCh 替换为 newCh。

**代码:**

```
public class Ex1 {
    public static void main(String args[]) {
        String S1 = new String("the quick fox jumped");
        System.out.println("Original String is ': " + S1);
        System.out.println("String after replacing 'cat' with 'dog': " + S1.replace("cat", "dog"));
        System.out.println("String after replacing all 't' with 'a': " + S1.replace('t', 'a'));

    }
}
```

**输出:**

`Original String is ': the cat jumped``String after replacing ‘cat' with 'dog': the dog jumped`T5`String after replacing all’t’ with 'a': ahe quick fox jumped`

## 全部替换

**Java String replace all():**该方法返回一个新的字符串，替换所有匹配正则表达式的字符序列和替换字符串。

**语法:**

`public Str replaceAll(String regex, String replacement)`

**参数:**

`regx: regular expression` 

**代码:**

```
public class Ex2 {
    public static void main(String args[]) {
        String str = "Java web replace method";
        //remove white spaces
        String str2 = str.replaceAll("s", "");
        System.out.println(str2);
    }
}
```

**输出:**

`Javewebreplacemethod`

## **ReplaceFirst**

**Java String replace first():**该方法替换匹配正则表达式的任何给定字符串的第一个子串。

**语法:**

`public Str replaceFirst(String rgex, String replacement)`

**参数:**

`rgex − the regular expression to which given string needs to matched. `

`replacement − the string that replaces regular expression.`

**代码:**

```
public class Ex3 {
    public static void main(String args[]) {
        String str = "This is an example of replace";
        //Only Replace first 'i' with '7' 
        String str1 = str.replaceFirst("i", "7");
        System.out.println(str1);
    }
}
```

**输出:**

`Th7s is an example of replace.`

就这样，我们到了这篇文章的结尾。我希望您了解了如何替换字符串和字符。

*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 [Hibernate](https://www.javatpoint.com/hibernate-tutorial) & Spring。*

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。