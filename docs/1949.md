# 如何在 Java 中迭代地图？

> 原文：<https://www.edureka.co/blog/iterate-maps-java/>

在这篇关于“在 Java 中迭代映射”的博客中，您将了解迭代[映射](https://www.edureka.co/blog/java-map-interface)的各种方法，并将分析这些方法，以便您可以根据自己的需求更容易地做出选择。博客由以下主题组成:

*   [Java 中的地图是什么？](#whatisamap)
*   [在 Java 中迭代地图](#iterate)
    *   [使用 For-Each 循环遍历条目](#foreach)
    *   [使用 keySet()和 values()方法使用 for-each 循环对键或值进行迭代](#keyset)
    *   [在 JAVA 8 中使用 stream()进行迭代](#stream)
    *   [使用 entrySet()](#entry)
    *   [通过地图使用迭代器](#iterator)

在开始迭代 Map 的方法之前，让我们先简要了解一下什么是 Java 中的 Map。

## **JAVA 中的地图是什么？**

Map 是 Java 中最重要的[数据结构之一。Java 映射接口 java.util.Map 表示键和值之间的映射，即](https://www.edureka.co/blog/data-structures-algorithms-in-java/) [Java 映射](https://www.edureka.co/blog/java-map-interface)可以存储键和值对，其中每个键都链接到一个特定的值。一旦存储在地图中，以后就可以只使用分配给该值的键来查找特定值。每个键最多只能映射到一个值。我们不能使用迭代器直接迭代地图，因为地图不是[集合](https://www.edureka.co/blog/java-collections/)，所以我们使用一些其他的方法来迭代地图，这将在本博客中详细描述。

**在 Java 中迭代地图** 让我们来看看 Java 中迭代地图的不同方式。

### **使用 For-Each 循环遍历条目**

当条目数量未知时，这种方法很有用。

```
</pre>
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

Map<Integer, String> customers = new HashMap<>();
customers.put(1, "Ajay");
customers.put(2, "Barkha");
customers.put(3, "Cathy");

System.out.println("Using foreach");
customers.forEach((id, name) -> {
System.out.println("Key : " + id + " value : " + name);
});

//{ autofold
}

}
//}
<pre>
```

**输出**

使用 foreach 键:1 值:Ajay 键:2 值:Barkha 键:3 值:Cathy

### **使用 keySet()和 values()方法使用 for-each 循环对键或值进行迭代**

**Map.keySet()** 方法返回此映射中包含的键的集合视图， **Map.values()** 方法返回映射中包含的值的集合视图。因此，当只需要映射中的键或值时，可以使用 [for-each 循环](https://www.edureka.co/blog/for-each-loop-in-java/)迭代键集或值。

```
import java.util.Map; 
import java.util.HashMap; 

class IterationDemo  
{ 
    public static void main(String[] arg) 
    { 
        Map<String,String> xyz = new HashMap<String,String>(); 

       //Enter value and url
        xyz.put("xyz", "Alphabet.org"); 
        xyz.put("Pronounce", "words.org"); 

        // using keySet() for iteration over keys 
        for (String name : xyz.keySet())  
            System.out.println("key: " + name); 

        // using values() for iteration over keys 
        for (String url : xyz.values())  
            System.out.println("value: " + url); 
    } 
}
```

**输出**键:发音键:xyz 值:words.org 值:Alphabet.org

### **在 Java 中迭代地图:在 JAVA 8 中使用 stream()**

```
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

        Map<Integer, String> students = new HashMap<>();
        students.put(1, "Anamika");
        students.put(2, "Bhaskar");
        students.put(3, "Rahul");

        System.out.println("");
        students.entrySet().stream().forEach(e ->
                System.out.println("Key : " + e.getKey() + " value : " + e.getValue())
        );

}
//}

```

**输出**

Key : 1 值:Anamika Key : 2 值:Bhaskar Key : 3 值:Rahul

### **使用 entrySet()**

```
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> students = new HashMap<>();
        students.put(1, "Anamika");
        students.put(2, "Bob");
        customers.put(3, "Mary");

    for (Map.Entry<Integer, String> entry : students.entrySet()) {
      System.out.println("Key : " + entry.getKey() + " value : " + entry.getValue());
    }

}
//}

```

**输出** 键:1 值:安娜卡键:2 值:鲍勃键:3 值:玛丽

### **通过映射使用迭代器**

```
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> Students = new HashMap<>();
        Students.put(1, "Anamika");
        Students.put(2, "Bob");
        Students.put(3, "Mary");

        Iterator<Map.Entry>Integer, String>> iterator = Students.entrySet().iterator();
        while (iterator.hasNext()) {
            Map.Entry entry = iterator.next();
            System.out.println("Key : " + entry.getKey() + " value : " + entry.getValue());
        }
//{ autofold
}

}
//}

```

**输出** 键:1 值:安娜卡键:2 值:鲍勃键:3 值:玛丽

在经历了所有这些方法之后，您现在可以根据需求选择您的方法了。至此，我们结束了这篇关于“用 Java 迭代地图”的博客。希望文章对你有帮助。

如果你想学习更多关于 Java 的知识，请查看 Edureka 的 [Java 培训](https://www.edureka.co/java-j2ee-training-course)，这是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。