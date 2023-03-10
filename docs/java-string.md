# Java 中的字符串——Java 中的字符串函数及示例

> 原文：<https://www.edureka.co/blog/java-string/>

**什么是 Java 字符串？**在 Java 中，字符串是表示一系列字符或字符值的对象。 *java.lang.String* 类用于创建一个 java 字符串对象。

创建字符串对象有两种方法:

1.  **通过字符串文字** : Java 字符串文字是用双引号创建的。比如:弦 s= 【迎宾】；
2.  **By new 关键字**:使用关键字“new”创建 Java 字符串。比如:String s =newString()； 它创建两个对象(在字符串池和堆中)和一个引用变量，其中变量“s”将引用堆中的对象。

现在，让我们来理解一下 Java 字符串池的概念。

**Java 字符串池:** Java 字符串池是指存储在堆内存中的字符串集合。在这种情况下，每当创建一个新对象时，String pool 首先检查该对象是否已经存在于池中。如果存在，那么相同的引用被返回到变量，否则新的对象将在字符串池中被创建，并且相应的引用将被返回。为了更好地理解，请参考图示:

![String-pool - Edureka](img/6e712fbfee2f997d3a722e1222339f2b.png)上图中，使用字面量创建了两个字符串，即“苹果”和“芒果”。现在，当用值“Apple”创建第三个字符串时，不是创建一个新对象，而是返回已经存在的对象引用。 这就是 Java 字符串池出现的原因。

在我们继续之前，我想补充的一个要点是，与 Java 中的其他数据类型不同，字符串是不可变的。所谓不可变，我们的意思是字符串是不变的，它们的值在创建后不能改变。因为字符串对象是不可变的，所以它们可以被共享。比如:

String str = " ABC "； 相当于 :

chardata[]= { ' a '，' b '，' c ' }；String str = new String(data)；

现在让我们看看字符串类 中的一些内置方法。

获得行业级项目认证&快速跟踪你的职业 [<button>看看吧！</button>](https://www.edureka.co/java-j2ee-soa-training)

## **Java S****tring 方法**

*   **Java String length()**:Java String length()方法告诉字符串的长度。它返回字符串中出现的字符总数。对于 考试ple:

```
public class Example{
public static void main(String args[]{ 
String s1="hello"; 
String s2="whatsup"; 
System.out.println("string length is: "+s1.length());  
System.out.println("string length is: "+s2.length()); 
}}

```

在这里，String length()函数将分别为 s1 和 s2 返回长度 5 和 7。

*   **Java St****ring** **comp****areTo** 是 String 类实现的*‘Comparable’*接口的方法。别担心，我们稍后将学习字符串接口。它返回正数、负数或 0。 例如:

```
public class CompareToExample{ 
public static void main(String args[]){ 
String s1="hello";
String s2="hello"; 
String s3="hemlo"; 
String s4="flag";
System.out.println(s1.compareTo(s2)); // 0 because both are equal
System.out.println(s1.compareTo(s3)); //-1 because "l" is only one time lower than "m" 
System.out.println(s1.compareTo(s4)); // 2 because "h" is 2 times greater than "f"
}} 

```

这个程序显示了各个字符串之间的比较。注意到Ifs>S2， it 返回一个正数IfS1<s

*   **Java String concat() :** The Java String concat() method combines a specific string at the end of another string and ultimately returns a combined string. It is like appending another string. For example:

    ```
    public class ConcatExample{
    public static void main(String args[]){
    String s1="hello";
    s1=s1.concat("how are you");
    System.out.println(s1);
    }}

    ```

    上面的代码返回“hellohow are you”。

*   **Java String IsEmpty()** :该方法检查字符串是否包含任何内容。如果 java 字符串为空，则返回 true，否则返回 false。例如:

    ```
    public class IsEmptyExample{ 
    public static void main(String args[]){ 
    String s1=""; 
    String s2="hello"; 
    System.out.println(s1.isEmpty());      // true
    System.out.println(s2.isEmpty());      // false
    }}

    ```

*   **Java String Trim()** : The java string trim() method removes the leading and trailing spaces. It checks the unicode value of space character (‘u0020’) before and after the string. If it exists, then removes the spaces and return the omitted string. For example:

    ```
    public class StringTrimExample{  
    public static void main(String args[]){  
    String s1="  hello   ";  
    System.out.println(s1+"how are you");        // without trim()  
    System.out.println(s1.trim()+"how are you"); // with trim()  
    }}  

    ```

    在上面的代码中，第一个打印语句将使用 trim()函数打印“hellohow are you ”,而第二个语句将打印“hello how are you”。

*   **Java String toLowerCase()** : The java string toLowerCase() method converts all the characters of the String to lower case. For example:

    ```
    public class StringLowerExample{
    public static void main(String args[]){
    String s1="HELLO HOW Are You?”;
    String s1lower=s1.toLowerCase();
    System.out.println(s1lower);}
    }

    ```

    上面的代码将返回“你好，你好”。

*   **Java String toUpper()** : The Java String toUpperCase() method converts all the characters of the String to upper case. For example:

    ```
    public class StringUpperExample{  
    public static void main(String args[]){  
    String s1="hello how are you";  
    String s1upper=s1.toUpperCase();  
    System.out.println(s1upper);  
    }}

    ```

    上面的代码将返回“你好，你好”。

*   **Java String ValueOf()** :该方法将不同类型的值转换成字符串。使用这种方法，您可以将 int 转换为 string，long 转换为 string，Boolean 转换为 string，char 转换为 string，float 转换为 string，double 转换为 string，object 转换为 string，char array 转换为 string。string valueOf()方法的签名或语法如下:公共静态字符串 valueOf(布尔 b) 公共静态字符串 valueOf(char c) 公共静态字符串 valueOf(char[] c) 公共静态字符串 valueOf(int i) 公共静态字符串 valueOf(long l) 公共静态字符串 valueOf(float f) 公共静态字符串 valueOf(double d) 公共静态字符串 valueOf(Object o)

让我们通过一个编程示例来理解这一点:

```
public class StringValueOfExample{
public static void main(String args[]){
int value=20; 
String s1=String.valueOf(value); 
System.out.println(s1+17);       //concatenating string with 10 
}}

```

在上面的代码中，它连接了 Java 字符串并给出了输出–2017。

*   **Java String replace()**:Java String replace()方法返回一个字符串，将所有旧字符或 CharSequence 替换为新字符。有两种方法可以替换 Java 字符串中的方法。

    ```
    public class ReplaceExample1{
    public static void main(String args[]){ 
    String s1="hello how are you"; 
    String replaceString=s1.replace('h','t'); 
    System.out.println(replaceString); }}

    ```

    在上面的代码中，它会将所有出现的‘h’替换为‘t’。上述代码的输出将是“tello tow are you”。 我们来看看 java 字符串中使用 replace 方法的另一种类型:**Java String replace(char sequence target， 字符序列替换) 方法**【t5 :

    ```
    public class ReplaceExample2{ 
    public static void main(String args[]){ 
    String s1="Hey, welcome to Edureka"; 
    String replaceString=s1.replace("Edureka","Brainforce"); 
    System.out.println(replaceString); 
    }}
    ```

    在上面的代码中，它会将所有出现的“Edureka”替换为“Brainforce”。因此，输出将是“嘿，欢迎来到 Brainforce”。

*   **Java String contains()** :The java string contains() method searches the sequence of characters in the string. If the sequences of characters are found, then it returns true otherwise returns false. For example:

    ```
    class ContainsExample{ 
    public static void main(String args[]){ 
    String name=" hello how are you doing"; 
    System.out.println(name.contains("how are you"));  // returns true
    System.out.println(name.contains("hello"));        // returns true  
    System.out.println(name.contains("fine"));         // returns false  
    }}
    ```

    在上面的代码中，前两个语句将返回 true，因为它匹配字符串，而第二个 print 语句将返回 false，因为字符串中不存在这些字符。

*   **Java String equals()**:Java String equals()方法根据字符串的内容(即 Java 字符串表示)来比较两个给定的字符串。如果所有字符都匹配，则返回 true，否则返回 false。例如:

    ```
    public class EqualsExample{ 
    public static void main(String args[]){ 
    String s1="hello"; 
    String s2="hello"; 
    String s3="hi";
    System.out.println(s1.equalsIgnoreCase(s2));   // returns true
    System.out.println(s1.equalsIgnoreCase(s3));   // returns false
    }
    }
    ```

*   **Java** **String equalsIgnoreCase():** This method compares two string on the basis of content but it does not check the case like equals() method. In this method, if the characters match, it returns true else false. For example:

    ```
    public class EqualsIgnoreCaseExample{ 
    public static void main(String args[]){ 
    String s1="hello"; 
    String s2="HELLO"; 
    String s3="hi";
    System.out.println(s1.equalsIgnoreCase(s2));   // returns true
    System.out.println(s1.equalsIgnoreCase(s3));   // returns false
    }}
    ```

    在上面的代码中，第一条语句将返回 true，因为无论大小写，内容都是相同的。然后，在第二个 print 语句中将返回 false，因为相应字符串中的内容不匹配。

*   **Java String toCharArray():** This method converts the string into a character array i.e first it will calculate the length of the given Java String including spaces and then create an array of char type with the same content. For example:

    ```
    StringToCharArrayExample{
    public static void main(String args[]){
    String s1="Welcome to Edureka";
    char[] ch=s1.toCharArray();
    for(int i=0;i<ch.length;i++){
    System.out.print(ch[i]);
    }}}

    ```

    上面的代码将返回“欢迎来到 Edureka”。

*   **Java StringGetBytes()** : The Java string getBytes() method returns the sequence of bytes or you can say the byte array of the string. For example:

    ```
    public class StringGetBytesExample {
    public static void main(String args[]){ 
    String s1="ABC";
    byte[] b=s1.getBytes(); 
    for(int i=0;i<b.length;i++){ 
    System.out.println(b[i]);
    }
    }}
    ```

    在上面的代码中，它将返回值 65 、66 、67。

*   **Java String IsEmpty()** :该方法检查字符串是否为空。如果字符串的长度为 0，则返回 true，否则返回 false。例如:

```
public class IsEmptyExample{
public static void main(String args[]) { 
String s1=""; 
String s2="hello";
System.out.prinltn(s1.isEmpty());     // returns true
System.out.prinltn(s2.isEmpty());     // returns false
}}

```

在上面的代码中，第一个 print 语句将返回 true，因为它不包含任何内容，而第二个 print 语句将返回 false。

*   **Java String endsWith()**:Java String endsWith()方法检查这个字符串是否以给定的后缀结尾。如果使用给定的后缀返回，则返回 true 否则返回 falsT5 e .F或 例如:

```
public class EndsWithExample{ 
public static void main(String args[]) {
String s1="hello how are you”; 
System.out.println(s1.endsWith("u"));       // returns true
System.out.println(s1.endsWith("you"));     // returns true   
System.out.println(s1.endsWith("how"));     // returns false
}}

```

这还不是结束。有更多的 Java 字符串方法可以帮助您简化代码。

继续，Java String 类实现了三个 **interfac** **es** ，即——*Serializable*和*C*h*ar sequence**。*

![StringInterface - Java String - Edureka](img/3b5620db316cb30d91f1ee5515a990ea.png)由于，Java 字符串是不可变的，也是最终的，所以每当我们做字符串操作的时候，都会创建一个新的字符串。由于字符串操作消耗资源，Java 提供了两个实用程序类: *StringBuffer* 和 *StringBuilder* 。让我们理解这两个实用程序类的区别:

*   StringBuffer 和 StringBuilder 是可变的类。StringBuffer 操作是线程安全和同步的，而 StringBuilder 操作不是线程安全的。
*   在单线程环境中，当多个线程处理同一个字符串和 StringBuilder 时，将使用 StringBuffer。
*   与 StringBuffer 相比，StringBuilder 的性能更快，因为没有同步开销。

我希望你们对 Java String 很清楚，它们是如何创建的，它们不同的方法和接口。我建议您尝试所有的 Java 字符串示例。 一定要看看我下一篇关于 [**Java 面试问题**](https://www.edureka.co/blog/interview-questions/java-interview-questions/) 的博客，这会帮助你在面试过程中脱颖而出。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/aqHhpahguVY](https://www.youtube.com/embed/aqHhpahguVY)

*既然您已经了解了 Java 的基础知识，那么就来看看 Edureka 的 **[Java 认证](https://www.edureka.co/java-j2ee-training-course)培训*** *吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这个“Java 字符串”博客的评论部分提到它，我们会尽快回复你，或者你也可以参加在阿姆利则的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-amritsar)*