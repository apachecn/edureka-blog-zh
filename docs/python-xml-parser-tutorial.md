# 如何用 Python 解析和修改 XML？

> 原文：<https://www.edureka.co/blog/python-xml-parser-tutorial/>

我们经常需要解析用不同语言编写的数据。 [Python 编程](https://www.edureka.co/blog/python-programming-language)提供了大量的库来解析或拆分用其他语言编写的数据。在这篇 Python XML 解析器教程中，您将学习如何使用 Python 解析 XML。

以下是本教程涵盖的所有主题:

[什么是 XML？](#whatisxml) [Python XML 解析模块](#modules)[XML . etree . element tree 模块](#xml.etree)

*   [使用 parse()函数](#etreeparse)
*   [使用 fromstring()函数](#fromstring)
*   [寻找感兴趣的元素](#findingelements)
*   [修改 XML 文件](#modifying)
*   [添加到 XML](#adding)
*   [从 XML 中删除](#deleting)

[xml.dom.minidom 模块](#xml.dom)

*   [使用 parse()函数](#domparse)
*   [使用 fromString()函数](#domfromstring)
*   [寻找感兴趣的元素](#domfindingelements)

所以让我们开始吧。:)

## **什么是 XML？**

XML 代表可扩展标记语言。它在外观上类似于 [HTML](https://www.edureka.co/blog/what-is-html/) ，但是，XML 用于数据表示，而 HTML 用于定义正在使用的数据。XML 专门设计用于在客户机和服务器之间来回发送和接收数据。看一下下面的例子:

**举例:**

```
<?xml version="1.0" encoding="UTF-8"?> <metadata> <food>
 <item name="breakfast">Idly</item>
 <price>$2.5</price>
 <description>  Two idly's with chutney
   </description>
 <calories>553</calories> </food> <food>
 <item name="breakfast">Paper Dosa</item>
 <price>$2.7</price>
 <description>  Plain paper dosa with chutney
    </description>
 <calories>700</calories> </food> <food>
 <item name="breakfast">Upma</item>
 <price>$3.65</price>
 <description>  Rava upma with bajji
    </description>
 <calories>600</calories> </food> <food>
 <item name="breakfast">Bisi Bele Bath</item>
 <price>$4.50</price>
 <description>  Bisi Bele Bath with sev
    </description>
 <calories>400</calories> </food> <food>
 <item name="breakfast">Kesari Bath</item>
 <price>$1.95</price>
 <description>  Sweet rava with saffron
    </description>
 <calories>950</calories> </food> </metadata> 

```



上面的例子显示了一个我命名为“Sample.xml”的文件的内容，我将在本 Python XML 解析器教程中对所有即将到来的例子使用相同的内容。

## **Python XML 解析模块**

Python 允许使用两个模块解析这些 XML 文档，即 xml.etree.ElementTree 模块和 Minidom(最小 dom 实现)。解析意味着从文件中读取信息，并通过识别特定 XML 文件的各个部分将信息拆分成片段。让我们进一步看看如何使用这些模块来解析 XML 数据。

### **xml.etree.ElementTree 模块:**

这个模块帮助我们将 XML 数据格式化为树形结构，这是分层数据最自然的表现形式。元素类型允许在内存中存储分层数据结构，并具有以下属性:

| 财产 | 描述 |
| 标签 | 它是一个字符串，表示存储的数据类型 |
| 属性 | 由许多存储为字典的属性组成 |
| 文本字符串 | 包含需要显示的信息的文本字符串 |
| 尾串 | 如果需要，也可以有尾串 |
| 子元素 | 由许多存储为序列的子元素组成 |

ElementTree 是一个包装元素结构的类，允许与 XML 相互转换。现在让我们尝试使用 [python 模块](https://www.edureka.co/blog/python-modules/)解析上面的 XML 文件。

使用“ElementTree”模块有两种方法来解析文件。第一个是通过使用 ***parse()函数*** 而第二个是 ***fromstring()函数*** 。parse()函数解析以文件形式提供的 XML 文档，而 fromstring 解析以字符串形式(即在三重引号内)提供的 XML 文档。

#### **使用 parse()函数:**

如前所述，这个函数获取文件格式的 XML 来解析它。看一下下面的例子:

**举例:**

```
import xml.etree.ElementTree as ET
mytree = ET.parse('sample.xml')
myroot = mytree.getroot()
```

如您所见，您需要做的第一件事是导入 xml.etree.ElementTree 模块。然后，parse()方法解析“Sample.xml”文件。getroot()方法返回“Sample.xml”的根元素。

当您执行上面的代码时，您将不会看到返回的输出，但是不会有指示代码已成功执行的错误。要检查根元素，只需使用如下的 print 语句:

**例如:**

```
import xml.etree.ElementTree as ET
mytree = ET.parse('sample.xml')
myroot = mytree.getroot()
print(myroot)
```

**输出:** <元素“元数据”在 0x033589F0 >

上面的输出表明我们的 XML 文档中的根元素是“元数据”。

#### **使用 fromstring()函数:**

您也可以使用 fromstring()函数来解析您的字符串数据。如果您想这样做，请将 XML 作为三重引号内的字符串传递，如下所示:

```
import xml.etree.ElementTree as ET
data='''<?xml version="1.0" encoding="UTF-8"?>
<metadata>
<food>
    <item name="breakfast">Idly</item>
    <price>$2.5</price>
    <description>
   Two idly's with chutney
   </description>
    <calories>553</calories>
</food>
</metadata>
'''
myroot = ET.fromstring(data)
#print(myroot)
print(myroot.tag)
```

上述代码将返回与上一个代码相同的输出。请注意，用作字符串的 XML 文档只是“Sample.xml”的一部分，我使用它是为了更好地显示。您也可以使用完整的 XML 文档。

您还可以通过使用“tag”对象来检索根标记，如下所示:

**举例:**

```
print(myroot.tag)
```

**输出:**元数据

您还可以通过指定想要在输出中看到的字符串部分来分割标签字符串输出。

**举例:**

```
print(myroot.tag[0:4])
```

**输出:**元

如前所述，标签也可以有字典属性。要检查根标签是否有任何属性，您可以使用“attrib”对象，如下所示:

**例如:**

```
print(myroot.attrib)
```

**输出:** {}

如您所见，输出是一个空的[字典](https://www.edureka.co/blog/dictionary-in-python/)，因为我们的根标签没有属性。

**了解我们在顶级城市/国家的 Python 培训**

| **印度** | **美国** | **其他城市/国家** |
| [班加罗尔](https://www.edureka.co/python-programming-certification-training-bangalore) | [纽约](https://www.edureka.co/python-programming-certification-training-new-york-city) | [英国](https://www.edureka.co/python-programming-certification-training-uk) |
| [海德拉巴](https://www.edureka.co/python-programming-certification-training-hyderabad) | [芝加哥](https://www.edureka.co/python-programming-certification-training-chicago) | 伦敦 |
| [德里](https://www.edureka.co/python-programming-certification-training-delhi) | 亚特兰大 | [加拿大](https://www.edureka.co/python-programming-certification-training-canada) |
| [钦奈](https://www.edureka.co/python-programming-certification-training-chennai) | [休斯顿](https://www.edureka.co/python-programming-certification-training-houston) | [多伦多](https://www.edureka.co/python-programming-certification-training-toronto) |
| [孟买](https://www.edureka.co/python-programming-certification-training-mumbai) | 洛杉矶 | [澳大利亚](https://www.edureka.co/python-programming-certification-training-australia) |
| [浦那](https://www.edureka.co/python-programming-certification-training-pune) | [波士顿](https://www.edureka.co/python-programming-certification-training-boston) | 阿联酋 |
| 加尔各答 | [迈阿密](https://www.edureka.co/python-programming-certification-training-miami) | [迪拜](https://www.edureka.co/python-programming-certification-training-dubai) |
| 艾哈迈达巴德 | [旧金山](https://www.edureka.co/python-programming-certification-training-san-francisco) | [菲律宾](https://www.edureka.co/python-programming-certification-training-philippines) |

#### **寻找感兴趣的元素:**

根也由子标签组成。要检索根标记的子标记，可以使用以下方法:

**举例:**

```
print(myroot[0].tag)
```

**输出:**食物

现在，如果您想要检索根的所有第一个子标签，您可以使用 for 循环迭代它，如下所示:

**举例:**

```
for x in myroot[0]:
     print(x.tag, x.attrib)
```

**输出:**

项目{ '名称':'早餐' } 价格{} 描述{} 卡路里{}

返回的所有项目都是食物的子属性和标签。

要使用 ElementTree 从 XML 中分离出文本，可以使用 text 属性。例如，如果我想检索第一个食物项目的所有信息，我应该使用下面这段代码:

**举例:**

```
for x in myroot[0]:
        print(x.text)
```

**输出:**

懒懒地 $2.5 两份带酸辣酱的懒懒地 553

如您所见，第一项的文本信息已经作为输出返回。现在，如果您想显示所有商品及其特定价格，您可以使用 get()方法。这个方法访问元素的属性。

**例如:**

```
for x in myroot.findall('food'):
    item =x.find('item').text
    price = x.find('price').text
    print(item, price)
```

**输出:**

懒懒地 2.5 美元纸 Dosa 2.7 美元 Upma 3.65 美元比西贝莱巴斯 4.50 美元凯萨里巴斯 1.95 美元

上面的输出显示了所有需要的商品以及它们的价格。使用 ElementTree，您还可以修改 XML 文件。

#### **修改 XML 文件:**

XML 文件中的元素是可以操作的。为此，可以使用 set()函数。让我们首先看看如何向 XML 添加内容。

#### **添加到 XML:**

以下示例显示了如何向项目描述中添加内容。

**举例:**

```
for description in myroot.iter('description'):
     new_desc = str(description.text)+'wil be served'
     description.text = str(new_desc)
     description.set('updated', 'yes')

mytree.write('new.xml')
```

write()函数帮助创建一个新的 xml 文件，并将更新后的输出写入该文件。但是，您也可以使用相同的功能修改原始文件。执行上述代码后，您将能够看到一个新文件已经用更新后的结果创建。

![set()-Python XML Parsing Tutorial-Edureka](img/1059d8756c25e573eab1c3422a49f7c2.png)

上图显示了修改后的食品描述。要添加新的子标记，可以使用 SubElement()方法。例如，如果您要将新的专业标签添加到第一个闲置项目，您可以执行以下操作:

**举例:**

```
ET.SubElement(myroot[0], 'speciality')
for x in myroot.iter('speciality'):
     new_desc = 'South Indian Special'
     x.text = str(new_desc)

mytree.write('output5.xml')
```

**输出:**

![SubElement-Python XML Parsing Tutorial-Edureka](img/86484fbf6835bdc5c2cfa222f6f5113d.png)

如您所见，在第一个食品标签下添加了一个新标签。通过在[]括号中指定下标，您可以在任何需要的地方添加标签。现在让我们来看看如何使用这个模块删除项目。

##### **从 XML 中删除:**

要使用 ElementTree 删除属性或子元素，可以使用 pop()方法。该方法将删除用户不需要的属性或元素。

**举例:**

```
myroot[0][0].attrib.pop('name', None)

# create a new XML file with the results
mytree.write('output5.xml')
```

**输出:**

![pop-Python XML Parsing Tutorial-Edureka](img/926465136369477142e48e2dfd9c4ebd.png)

上图显示 name 属性已经从 item 标签中删除。要删除完整的标记，可以使用相同的 pop()方法，如下所示:

**举例:**

```
myroot[0].remove(myroot[0][0])
mytree.write('output6.xml')
```

**输出:**

![elementpop-Python XML Parsing Tutorial-Edureka](img/14fca528fbd04bcb0ea95842978bc80e.png)

输出显示食品标签的第一个子元素已被删除。如果您想要删除所有标签，您可以使用 clear()函数，如下所示:

**例如:**

```
myroot[0].clear()
mytree.write('output7.xml')
```

**输出:**

当执行上述代码时，food 标签的第一个子标签将被完全删除，包括所有子标签。到目前为止，我们一直在使用 Python XML 解析器教程中的 xml.etree.ElementTree 模块。现在让我们看看如何使用 Minidom 解析 XML。

## **xml.dom.minidom 模块:**

这个模块基本上是精通 DOM(文档对象模块)的人用的。DOM 应用程序通常从将 XML 解析成 DOM 开始。在 xml.dom.minidom 中，这可以通过以下方式实现:

### **使用 parse()函数:**

第一种方法是通过提供要解析的 XML 文件作为参数来利用 parse()函数。例如:

**举例:**

```
from xml.dom import minidom
p1 = minidom.parse("sample.xml");
```

一旦执行了这个操作，您就能够分割 XML 文件并获取所需的数据。您也可以使用这个函数解析一个打开的文件。

**举例:**

```
dat=open('sample.xml')
p2=minidom.parse(dat)
```

在这种情况下，存储打开文件的变量作为参数提供给 parse 函数。

### **使用 parseString()方法:**

当您希望提供要作为字符串进行解析的 XML 时，可以使用此方法。

**例如:**

```
p3 = minidom.parseString('<myxml>Using<empty/> parseString</myxml>')
```

您可以使用上述任何一种方法解析 XML。现在让我们尝试使用这个模块来获取数据。

#### **寻找感兴趣的元素:**

在我的文件被解析后，如果我试图打印它，返回的输出会显示一条消息，说明存储解析数据的变量是 DOM 的一个对象。

**举例:**

```
dat=minidom.parse('sample.xml')
print(dat)
```

**输出:**

**使用 GetElementByTagName 访问元素:**

**举例:**

```
tagname= dat.getElementsByTagName('item')[0]
print(tagname)
```

如果我尝试使用 GetElementByTagName 方法获取第一个元素，我将看到以下输出:

**输出:**

请注意，只返回了一个输出，因为为了方便起见，我使用了[0]下标，在后面的例子中会删除它。

要访问属性的值，我必须使用 value 属性，如下所示:

**举例:**

```
dat = minidom.parse('sample.xml')
tagname= dat.getElementsByTagName('item')
print(tagname[0].attributes['name'].value)
```

**输出:**早餐

要检索这些标记中的数据，您可以使用 data 属性，如下所示:

**举例:**

```
print(tagname[1].firstChild.data)
```

**输出:**纸张 Dosa

还可以使用 value 属性拆分和检索属性值。

**举例:**

```
print(items[1].attributes['name'].value)
```

**输出:**早餐

要打印出菜单中所有可用的项目，您可以遍历这些项目并返回所有项目。

**举例:**

```
for x in items:
    print(x.firstChild.data)
```

**输出:**

懒懒地纸 Dosa Upma 比西贝莱巴斯凯萨里巴斯

要计算菜单上的项目数量，您可以使用 len()函数，如下所示:

**举例:**

```
print(len(items))
```

**输出:** 5

输出指定我们的菜单由 5 个项目组成。

这就把我们带到了 Python XML 解析器教程的结尾。我希望你已经明白了一切。

***Make sure you practice as much as possible and revert your experience.*  **

*有问题吗？请在“Python XML 解析器教程”博客的评论部分提到它，我们会尽快回复您。要了解更多信息，你可以报名参加我们的[Python 编程](https://www.edureka.co/masters-program/python-developer-training)硕士课程。*

*要深入了解 Python 及其各种应用，您可以注册参加实时 [**Python 课程**](https://www.edureka.co/python-programming-certification-training) ，该课程提供全天候支持和终身访问。*