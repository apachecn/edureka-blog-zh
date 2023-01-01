# 用 python 学习网页抓取的入门指南！

> 原文：<https://www.edureka.co/blog/web-scraping-with-python/>

**用 Python 进行网页抓取**

想象一下，你必须从网站上获取大量数据，并且你想尽可能快地完成它。如果不手动访问每个网站并获取数据，你会怎么做？ 嗯，“网刮”就是答案。网络抓取只是使这项工作更容易和更快。

在这篇关于使用 Python 进行 web 抓取的文章中，您将简要了解 Web 抓取，并通过演示了解如何从网站中提取数据。 我将涵盖以下主题:

## **为什么要用网页抓取？**

网络搜集用于从网站上收集大量信息。但是为什么一定要有人从网站上收集这么大的数据呢？为了了解这一点，l et 来看看网页抓取的应用:

*   **价格比较:**parse hub 等服务使用 web scraping 从在线购物网站收集数据，并使用它来比较产品的价格。
*   **电子邮件地址收集:**许多使用电子邮件作为营销媒介的公司，使用网络搜集来收集电子邮件 ID，然后发送批量电子邮件。
*   **社交媒体抓取:**网络抓取用于从 Twitter 等社交媒体网站收集数据，以了解流行趋势。
*   **研发:**网页抓取用于收集大量数据(统计、一般信息、温度等。)从网站上下载，对其进行分析并用于开展调查或研究& D.
*   **职位列表:**关于职位空缺、面试的详细信息从不同的网站收集，然后在一个地方列出，以便用户可以轻松访问。

## **什么是网页抓取？**

Web 抓取是一种用于从网站中提取大量数据的自动化方法。网站上的数据是非结构化的。Web 抓取有助于收集这些非结构化数据，并以结构化形式存储。有不同的方法来抓取网站，如在线服务、API 或编写自己的代码。在本文中，我们将看到如何用 python 实现 web 抓取。

[![Web Scraping - Edureka](img/e8e5a5fae28cb6880e83b87262cd5ee4.png)](/blog/wp-content/uploads/2018/11/Untitled-1.jpg)

## **网页抓取合法吗？**

谈到网络抓取是否合法，有些网站允许网络抓取，有些不允许。想知道一个网站是否允许网页抓取，可以看看网站的“robots.txt”文件。您可以通过将“/robots.txt”附加到您想要抓取的 URL 来找到该文件。对于这个例子，我正在抓取 Flipkart 网站。所以，要看“robots.txt”文件，的网址是【www.flipkart.com/robots.txt.】的的

Get in-depth Knowledge of Python along with its Diverse Applications [<button>Know More!</button>](https://www.edureka.co/python)

## **为什么 Python 对网页抓取有好处？**

这里列出了 Python 的一些特性，这些特性使它更适合网络抓取。

*   **易用性:** [Python 编程](https://www.edureka.co/blog/python-programming-language)代码简单。您不必添加分号“；”或花括号“{}”的任何位置。这使得它不那么凌乱，易于使用。
*   **庞大的库集合:** Python 拥有庞大的库集合，如 [Numpy](https://www.edureka.co/blog/python-numpy-tutorial/) 、 [Matlplotlib](https://www.edureka.co/blog/python-matplotlib-tutorial/) 、 [Pandas](https://www.edureka.co/blog/python-pandas-tutorial/) 等。，它为各种目的提供方法和服务。因此，它适用于 web 抓取和提取数据的进一步操作。
*   **动态类型:**在 Python 中，你不必为变量定义数据类型，你可以在任何需要的地方直接使用变量。这样可以节省时间，让你的工作更快。
*   **容易理解的语法:** Python 语法容易理解主要是因为阅读 Python 代码与阅读英文语句非常相似。它富有表现力，易于阅读，Python 中使用的缩进也有助于用户区分代码中不同的范围/块。
*   **小代码，大任务:**使用网页抓取来节省时间。但是你花再多时间写代码又有什么用呢？嗯，你不需要。在 Python 中，你可以编写小代码来完成大任务。因此，即使在编写代码时，您也节省了时间。
*   **社区:**写代码的时候卡住了怎么办？你不用担心。Python 社区有一个最大最活跃的社区，你可以在那里寻求帮助。

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

## **如何从一个网站上抓取数据？**

当您运行 web 抓取代码时，一个请求被发送到您提到的 URL。作为对请求的响应，服务器发送数据并允许您读取 HTML 或 XML 页面。然后，代码解析 HTML 或 XML 页面，找到数据并提取出来。

使用 python 通过 web 抓取提取数据，需要遵循以下基本步骤:

1.  找到你想要抓取的网址
2.  检查页面
3.  找到您想要提取的数据
4.  编写代码
5.  运行代码并提取数据
6.  以要求的格式存储数据

现在让我们看看如何使用 Python 从 Flipkart 网站提取数据。

*用这些学习 Python、深度学习、NLP、人工智能、机器学习 [**AI 和 ML 课程**](https://www.edureka.co/executive-programs/machine-learning-and-ai)NIT Warangal 的一个 PG 文凭认证项目。*

## **用于网页抓取的库**

众所周知，Python 有各种各样的应用，不同的库有不同的用途。在我们进一步的演示中，我们将使用以下库:

*   **Selenium** : Selenium 是一个 web 测试库。它用于自动化浏览器活动。
*   **Beautiful Soup**:Beautiful Soup 是一个解析 HTML 和 XML 文档的 Python 包。它创建解析树，有助于轻松提取数据。
*   **Pandas**:Pandas 是一个用于数据操作和分析的库。它用于提取数据并以所需的格式存储数据。

#### 订阅我们的 YouTube 频道获取新的更新..！