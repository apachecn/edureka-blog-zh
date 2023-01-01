# Python 请求:您需要知道的一切

> 原文：<https://www.edureka.co/blog/python-requests/>

Python requests bag almost 400,000 downloads everyday. This number is evident enough to understand about the popularity of this [python library](https://www.edureka.co/blog/python-libraries/). In recent years, python programming language has become the most desired programming language for many developers. The concepts and libraries like requests is one of the many reasons for developers to transition from other programming languages to python. In this blog, we will go through the following topics:

*   [什么是 Python 请求？](#1)
*   [为什么使用 Python 请求？](#2)
*   [如何安装 Python 请求？](#3)
*   [制作获取&帖子请求](#4)
*   [在 URL 中传递参数](#5)
*   [状态代码](#6)
*   [响应内容](#7)
*   [多部分文件上传](#8)
*   [cookie 和标题](#9)
*   [会话对象](#10)
*   [错误和异常](#11)

## **什么是 Python 请求？**

Python requests was written by Kenneth Reitz and licensed under apache 2.0\. It is a human friendly HTTP library as it is mentioned on the official documentation page. It is easy to use and basically used for making all sorts of HTTP requests. Following are a few advanced features that requests comes with:![requests logo-python requests-edureka](img/4ee5cf203e1430a189b1f089b6715cde.png)

1.  保持活动和连接池
2.  国际域名和网址
3.  具有 cookie 持久性的会话
4.  浏览器风格的 SSL 验证
5.  自动内容解码
6.  基本/摘要认证
7.  优雅的键/值 cookies
8.  自动减压
9.  Unicode 响应正文
10.  HTTPs 代理支持
11.  多部分文件上传
12.  流媒体下载
13.  连接超时
14.  分块请求

These are all the advanced features of python requests library, lets try to understand why do we use python requests in the first place.

## **为什么使用 Python 请求？**

When it comes to why do we use python requests? the reason is pretty simple. While using python requests, you don’t have to manually add the queries to your urls and form-encode post data. It makes our job easier when making http requests of any kind.Now that we are familiar with python requests and why we use them in python, lets try to understand how are we going to install requests on our project or system.

## **如何安装 Python 请求？**

The installation part is very easy as well. If you have the pipenv setup installed on your system, you can simply run the following command in the terminal.

$ pip 安装请求

This will install the requests library on your system. There is one more approach to install requests. If you are using pycharm, you can add requestson the project interpreter in the settings. It serves the same purpose as the terminal in case of installing the library on our project.Now that we are through with the installation, lets try to understand how we will make get and post requests in python.

## **如何提出获得&帖子的请求？**

Get request is basically used to request the data from the server. Following is the syntax to make a get request.

```

import requests

res = requests.get('url')

#res is the response object here.

```

Post request is used to submit the data to be processed to the server. Following is the syntax to make a post request.

```

import requests

payload = {'key1': 'value1'}

res = requests.post('url' , data= payload)

```

Now that we know how we can make get and post requests, lets take a look at how we can pass parameters to the url using the get request.

## **在 Url 中传递参数**

Passing parameters in a url is as simple as making a get request. Following is an example to pass parameters to url.

```

import requests

payload = {'key1': 'value1' , 'key2': 'value2'}

res = requests.get('url', params= payload)

print(res.url)

#this will print the url with the parameters passed through the get request.

```

## **状态代码**

我们也可以检查状态代码，下面是检查状态代码的代码:

```

import requests

res = requests.get('url')

print(res.status_code())

```

If the code returns 200, it means there is no error and the request is all well. If we make a bad request, the code will return code like 404 or 505 which will raise an http error.

## **响应内容**

We can also read the contents of the server’s response. The library will automatically decode the content from the server.

```

import requests

res = requests.get('url')

print(res.content)

```

Requests 还有一个内置的 json 解码器。

```

import requests

res = requests.get('url')

print(res.json())

#this will get the response in a json format

```

## **多部分文件上传**

It is very easy to upload multi-part files using requests.

```

import requests

files = {'file' : open('filename', 'rb')}

res = requests.post('url' , files= files)

print(res.text)

```

For sending multiple files we will specify multiple files in the files parameter.

## **cookie 和标题**

We can view the server’s response headers and cookies using the response object. Following is the code to view the server’s headers.

```

import requests

res = requests.get('url')

print(res.headers)

```

We can pass custom headers to the url as well. Lets take a look at the code.

```

import requests

headers = {'key1' : 'value1'}

res = requests.get('url', headers= headers)

print(res.headers)

```

Requests does not change its behavior based on custom headers. They are simply passed onto the final request. **cookies **can also be viewed using the response object.

```

import requests

#to pass our own cookies we can use the cookies parameter

cookies = dict(cookies= 'working')

res = requests.get('url' , cookies= cookies)

print(res.text)

```

Cookies 在 RequestCookieJar 中返回，它的作用就像一个字典，但也提供了更完整的接口，适合在多个域或路径上使用。

## **会话对象**

The session object allows you to persist certain parameters across the requests.

*   跨会话实例发出的所有请求保持 cookies
*   使用 urllib3 连接池
*   显著的性能提升
*   会话对象拥有主请求 API 的所有方法

Following is the code to persist some cookies across requests.

```

s = requests.session()

s.get('url')

res = s.get('url')

print(res.text)

```

## **错误和异常**

Following are the errors and exceptions that are raised in a python request.

*   如果出现网络问题，请求将引发 ConnectionError 异常。
*   当存在不成功的状态代码时，Response.raise_for_status()将引发 HTTP 错误。
*   如果超时，它将引发超时异常
*   如果请求超过配置的最大重定向数，将引发 TooManyRedirects 异常。

In this blog we have discussed the python requests module in which we have various advanced features. We discussed installation and making a get and post request with the response content and other concepts in requests library in python. Python requests module is one of the many extraordinary out of the box features of [python programming language](https://www.edureka.co/blog/introduction-to-python/). You can kickstart your learning by enrolling in [edureka’s python certification training](https://www.edureka.co/data-science-python-certification-course) and discover the possibilities of python programming language.*Have any queries? mention them in the comments section, we will get back to you.*