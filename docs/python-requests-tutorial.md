# Python 请求教程:用 Python 获取和发布请求

> 原文：<https://www.edureka.co/blog/python-requests-tutorial/>

## **用 Python 请求教程**

在这篇关于 Python 请求教程的文章中，我将向你解释请求模块的所有基础知识，以及你如何使用 Python 发送 HTTP/1.1 请求。到本博客结束时，你将能够使用 Python 执行 web 抓取。在这篇文章中，我将涉及以下主题:

*   [什么是 Python 请求？](#z1)
*   [如何在 Python 中安装请求模块？](#z2)
*   [如何进行 GET 请求？](#z3)
*   [下载有请求的图像](#z4)
*   [如何提出发文请求？](#z5)
*   [如何在请求中插入标题&cookie？](#z6)
*   [什么是会话对象？](#z7)
*   [结论](#z8)

让我们从这个“请求教程”博客开始，首先看看请求模块到底是什么。

## **什么是 Python 请求？**

Requests 是一个 Python 模块，可以用来发送各种 HTTP 请求。这是一个易于使用的库，具有许多功能，从在 URL 中传递参数到发送自定义头和 SSL 验证。在本教程中，您将学习如何使用这个库在 Python 中发送简单的 HTTP 请求。

请求允许您发送 HTTP/1.1 请求。您可以使用简单的 Python 字典添加头、表单数据、多部分文件和参数，并以相同的方式访问响应数据。

## **如何在 Python 中安装请求模块？**

要安装请求，只需:

```
$ pip install requests
```

或者，如果你一定要:

```
$ easy_install requests
```

## **如何进行 GET 请求？**

使用 Requests 发送 HTTP 请求相当简单。首先导入模块，然后发出请求。看看这个例子:

```
import requests
req = requests.get('https://www.edureka.co/')

```

So, we are storing the information somewhere, correct?Yes, Response object stores the information.Let’s say, for example, you want the encoding of a web-page so that you can verify it or use it somewhere else. We can do this using the **req.encoding **property as well.An added plus is that you can also extract many features like the status code for example (of the request). This can be done using the **req.status_code** property.

```
req.encoding # returns 'utf-8'
req.status_code # returns 200

```

我们还可以访问服务器发回的 cookies。这是使用 **req.cookies，**完成的，就这么简单！ 同样，你也可以得到响应头。这是通过使用 **req.headers.** 完成的

请注意， **req.headers** 属性将返回一个不区分大小写的响应头字典。那么，这意味着什么呢？

这意味着**req . headers[' Content-Length ']**、**req . headers[' Content-Length ']**和**req . headers[' Content-Length ']**都将只返回 **'Content-Length'** 响应头的值。

我们还可以检查所获得的响应是否是一个格式良好的 HTTP 重定向(或者不是),它可以使用 **req.is_redirect** 属性自动处理。这将根据获得的响应返回**真**或**假**。

您还可以使用另一个属性获得发送请求和获得响应之间的时间间隔。猜猜看。没错，就是 **req.elapsed** 属性。

还记得您最初传递给 **get()** 函数的 URL 吗？由于许多原因，它可能不同于响应的最终 URL，这也包括重定向。

为了查看实际的响应 URL，您可以使用 **req.url** 属性。

```
import requests
req = requests.get('http://www.edureka.co/')

req.encoding # returns 'utf-8'
req.status_code # returns 200
req.elapsed # returns datetime.timedelta(0, 1, 666890)
req.url # returns 'https://edureka.co/'

req.history 

req.headers['Content-Type']
# returns 'text/html; charset=utf-8'

```

难道你不认为获取网页的所有信息是件好事吗？但是，问题是您最有可能想要访问实际的内容，对吗？

如果你访问的内容是文本，你总是可以使用 **req.text** 属性来访问它。请注意，内容随后将只被解析为 unicode。您可以像我们之前讨论的那样，使用 **req.encoding** 属性来传递用于解码该文本的编码。

在非文本回复的情况下，您可以非常轻松地访问它们。事实上，当你使用 **req.content.** 时，它是以二进制格式完成的。这个模块会自动为我们解码 **gzip** 和 **deflate** 传输编码。当您直接处理媒体文件时，这非常有用。此外，您还可以使用 **req.json()** 函数访问 JSON 编码的响应内容，如果它存在的话。

非常简单而且非常灵活，对吗？

同样，如果需要，你也可以通过使用 **req.raw 从服务器获得原始响应。**请记住，你必须在请求中传递 **stream=True** 才能根据需要获得原始响应。

但是，你用请求模块从网上下载的一些文件可能会很大，对吗？在这种情况下，一次性将整个响应或文件加载到内存中是不明智的。但是，建议您使用 **iter_content(chunk_size = 1，decode_unicode = False)** 方法分块下载文件。

因此，这个方法一次迭代 **chunk_size** 字节数的响应数据。当请求中的 **stream=True** 时，这种方法将避免只为了大的响应而一次将整个文件读入内存。

请注意， **chunk_size** 参数可以是整数，也可以是 **None** 。但是，当设置为整数值时，chunk_size 确定应该一次读入内存的字节数。

当 **chunk_size** 被设置为 **None** 并且 **stream** 被设置为 **True** 时，数据将在到达时被读取，无论块的大小如何。但是，当 **chunk_size** 设置为 **None** 并且 **stream** 设置为 **False** 时，所有数据将仅作为单个数据块返回。

View Upcoming Batches For Python Certification Course Now! [<button>Read Now</button>](https://www.edureka.co)

接下来，在这个“请求教程”博客中，让我们看看如何使用请求模块下载图像。

## **使用请求模块下载图像**

因此，让我们使用我们所学的请求模块在 Pixabay 上下载下面的森林图片。下面是实际图像:

![Requests Tutorial - Edureka](img/64dd74b71ad078a5a941d888d9fdfd53.png)

这是下载图像所需的代码:

```
import requests
req = requests.get('path/to/forest.jpg', stream=True)
req.raise_for_status()
with open('Forest.jpg', 'wb') as fd:
for chunk in req.iter_content(chunk_size=50000):
print('Received a Chunk')
fd.write(chunk)

```

注意， **'path/to/forest.jpg'** 是实际的图片 URL。你可以把任何其他图片的 URL 放在这里来下载其他的东西。这只是一个例子，给定的图像文件大小约为 185kb，您已经将 **chunk_size** 设置为 50，000 字节。

这意味着“接收到一个块”消息应该在终端中打印**四次**。最后一个块的大小将只有 39350 字节，因为在前三次迭代之后仍待接收的文件部分是 39350 字节。

请求还允许你在 URL 中传递参数。当您在网页上搜索一些结果(如教程或特定图像)时，这尤其有用。您可以使用 GET 请求中的关键字 **params** 将这些查询字符串作为字符串字典提供。看看这个简单的例子:

```
import requests

query = {'q': 'Forest', 'order': 'popular', 'min_width': '800', 'min_height': '600'}
req = requests.get('https://pixabay.com/en/photos/', params=query)

req.url
# returns 'https://pixabay.com/en/photos/?order=popular_height=600&q=Forest&min_width=800'

```

在这篇“请求教程”博客的下一篇文章中，让我们来看看如何发出帖子请求！

## **如何提出发文请求？**

发出 POST 请求和发出 GET 请求一样简单。你只是使用了 **post()** 函数而不是 **get()** 。

当您自动提交表单时，这很有用。例如，下面的代码将下载整个维基百科关于纳米技术的页面，并将其保存在您的 PC 上。

```
import requests
req = requests.post('https://en.wikipedia.org/w/index.php', data = {'search':'Nanotechnology'})
req.raise_for_status()
with open('Nanotechnology.html', 'wb') as fd:
for chunk in req.iter_content(chunk_size=50000):
fd.write(chunk)

```

## **如何在请求中插入标题&cookie？**

如前所述，您可以使用 **req.cookiess** 和 **req.headers** 来访问服务器发回给您的 cookie 和标头。请求还允许您随请求发送自己的自定义 cookies 和标题。比方说，当您想要为您的请求设置一个自定义用户代理时，这是很有帮助的。

要给请求添加 HTTP 头，您可以简单地将它们以 **dict** 的形式传递给 **headers** 参数。同样，您也可以使用传递给 cookie参数的 **dict** 将自己的 cookie 发送到服务器。

```
import requests

url = 'http://some-domain.com/set/cookies/headers'

headers = {'user-agent': 'your-own-user-agent/0.0.1'}
cookies = {'visit-month': 'February'}

req = requests.get(url, headers=headers, cookies=cookies)

```

饼干罐也可以存放饼干。 他们提供了一个更完整的接口来允许你在多个路径上使用那些 cookies。

看看下面这个例子:

```
import requests

jar = requests.cookies.RequestsCookieJar()
jar.set('first_cookie', 'first', domain='httpbin.org', path='/cookies')
jar.set('second_cookie', 'second', domain='httpbin.org', path='/extra')
jar.set('third_cookie', 'third', domain='httpbin.org', path='/cookies')

url = 'http://httpbin.org/cookies'
req = requests.get(url, cookies=jar)

req.text

# returns '{ "cookies": { "first_cookie": "first", "third_cookie": "third" }}'

```

接下来在这个“请求教程”博客中，让我们来看看会话对象！

## **什么是会话对象？**

有时在多个请求中保留某些参数是很有用的。会话对象正是这样做的。例如，它将跨使用同一会话的所有请求持久保存 cookie 数据。

会话对象使用 **urllib3 的**连接池。这意味着底层 TCP 连接将被对同一主机发出的所有请求重用。

这可以显著提升性能。还可以将 Requests 对象的方法用于 Session 对象。

当您想要在所有请求之间发送相同的数据时，会话也很有帮助。例如，如果您决定将带有所有请求的 cookie 或用户代理标头发送到给定的域，则可以使用会话对象。

这里有一个例子:

```
import requests

ssn = requests.Session()
ssn.cookies.update({'visit-month': 'February'})

reqOne = ssn.get('http://httpbin.org/cookies')
print(reqOne.text)
# prints information about "visit-month" cookie

reqTwo = ssn.get('http://httpbin.org/cookies', cookies={'visit-year': '2017'})
print(reqTwo.text)
# prints information about "visit-month" and "visit-year" cookie

reqThree = ssn.get('http://httpbin.org/cookies')
print(reqThree.text)
# prints information about "visit-month" cookie

```

如您所见，**“visit-month”**会话 cookie 与所有三个请求一起发送。然而,“visit-year”cookie 只在第二次请求时发送。第三个请求中也没有提到“visit-year”cookie。这证实了一个事实，即单个请求上的 cookies 或其他数据集不会与其他会话请求一起发送。

## **结论**

本教程中讨论的概念应该有助于您通过传递特定的头、cookies 或查询字符串向服务器发出基本请求。

当你试图搜集一些网页信息时，这将非常方便。现在，一旦你弄清楚了 URL 的模式，你也应该能够从不同的网站自动下载音乐文件和壁纸。

在阅读了这篇关于使用 Python 的请求教程的博客后，我敢肯定你想了解更多关于 Python 的知识。想要了解更多关于 Python 的知识，你可以参考下面的博客:

1.  **[Python 教程——Python 编程初学者](https://www.edureka.co/blog/python-tutorial/)**
2.  **[用于数据科学的 Python](https://www.edureka.co/blog/learn-python-for-data-science/)**
3.  [**你应该学习 Python 的 10 大理由**](https://www.edureka.co/blog/10-reasons-why-you-should-learn-python)

我希望你喜欢这篇关于请求教程的帖子。如果你对本教程有任何疑问，请在评论中告诉我，或者现在就加入我们的 [Python 认证课程](https://www.edureka.co/python-programming-certification-training)。

**Python 初学者教程| Edureka**



[https://www.youtube.com/embed/jJkEc9d1Rwg?rel=0&showinfo=0](https://www.youtube.com/embed/jJkEc9d1Rwg?rel=0&showinfo=0)*This video covers all the basics of Python.*