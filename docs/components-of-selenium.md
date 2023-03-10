# Selenium Suite 的各种组件是什么？

> 原文：<https://www.edureka.co/blog/components-of-selenium>

如果你问一个懒惰的测试者他们最喜欢的测试工具，很大概率你会得到“ ***[硒](https://www.edureka.co/blog/what-is-selenium/)*** ”作为答案。这是因为它是 web 应用程序自动化测试的完美工具。在这篇文章中，让我们看看是什么样的各种硒成分使它如此受欢迎。你可以从 [Selenium 在线课程](https://www.edureka.co/selenium-certification-training)中了解更多。

本文涵盖以下主题:

*   [硒简介](#IntroductiontoSelenium)
*   [硒成分](#SeleniumComponents)
    *   [硒 IDE](#SeleniumIDE)
    *   [硒 RC](#SeleniumRC)
    *   [硒网驱动](#SeleniumWebDriver)
    *   [硒栅](#SeleniumGrid)

我们开始吧！

## **硒简介**

Selenium 是一个开源工具，用于自动化在 web 浏览器上执行的测试用例或使用任何 web 浏览器进行测试的 web 应用程序。 等等，在你忘乎所以之前，让我重申一下，只有对 web 应用程序的测试才有可能使用 Selenium。我们既不能测试任何桌面软件应用程序，也不能使用 Selenium 测试任何移动应用程序。 所以它是一个支持[交叉浏览](https://www.edureka.co/blog/cross-browser-testing-using-selenium/)和自动化网络应用的开源工具！

现在让我们看看硒由哪些不同的成分组成。

## **硒成分**

Selenium 主要由一套工具组成，包括:

*   [硒 IDE](#SeleniumIDE)
*   [硒 RC](#SeleniumRC)
*   [硒网驱动](#SeleniumWebDriver)
*   [硒栅](#SeleniumGrid)

![Selenium Suite - Selenium WebDriver Architecture - Edureka](img/a463c4d6d80454e3390a18a35b87dc8d.png)

让我们更详细地了解这些工具的功能。

### **硒 IDE**

Selenium IDE(集成开发环境)主要是一个 Firefox 插件。它是 Selenium 套件中最简单的框架之一。它允许我们记录和回放脚本。如果您希望使用 [Selenium IDE](https://www.edureka.co/blog/selenium-ide) 创建脚本，您需要使用 Selenium RC 或 Selenium WebDriver 来编写更高级和健壮的测试用例。

在 Selenium IDE 中，测试用例的执行非常慢，与其他组件相比，测试用例的报告生成步骤并不好。它不支持并行或远程执行的测试用例执行。

硒 IDE 的一些缺点是:

1.  它将测试用例的执行限制在 Firefox 浏览器上。

2.  它不支持基于移动设备的测试，比如 iPhone/Android 测试。

3.  与其他组件相比，测试用例的执行非常慢，报告生成步骤也不好。

接下来，我们来看看什么是硒 RC。

### **硒 RC**

Selenium RC，也称为 Selenium 1，在 WebDriver merge 带来 Selenium 2 之前的很长一段时间里是主要的 [Selenium 项目](https://www.edureka.co/blog/selenium-projects/)。它主要依靠 JavaScript 实现[自动化](https://www.edureka.co/blog/automation-testing-tutorial/)。它支持 Ruby，PHP， [Python](https://www.edureka.co/blog/python-programming-language) ，Perl 和 C#，Java，Javascript。它支持几乎所有的浏览器。

***注:**硒 RC 正式弃用。*

Selenium RC 的其他一些特性:

*   它基于 JavaScript。它不支持录制/回放功能。

*   它基于客户端/服务器架构，这意味着->无论何时您想要执行测试用例/测试脚本，您都需要手动启动服务器。

*   它支持测试用例的并行执行，以及借助 Selenium Grid 的远程执行。

Selenium RC 的缺点是，无论何时您想要执行测试用例，您都应该手动启动 Selenium 独立服务器。为了克服这个问题，引进了[硒线切割机](https://www.edureka.co/blog/how-to-find-elements-in-selenium/)。

### **硒网驱动**

Selenium WebDriver 是一个浏览器自动化框架，它接受命令并将其发送到浏览器。它是通过特定于浏览器的驱动程序实现的。它直接与浏览器通信并控制它。Selenium WebDriver 支持各种编程语言，如-[Java](https://www.edureka.co/blog/java-tutorial/)、C#、 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 、 [Python](https://www.edureka.co/blog/python-tutorial/) 、Perl、 [Ruby](https://www.edureka.co/blog/ruby-on-rails-tutorial/) 。还有 [Javascript。](https://www.edureka.co/blog/top-10-javascript-frameworks/)

Selenium WebDriver 支持以下功能:

1.  ***操作系统支持***——Windows、Mac OS、Linux、Solaris
2.  ***浏览器支持***——Mozilla Firefox、Internet Explorer、Google Chrome 12.0.712.0 及以上、Safari、Opera 11.5 及以上、Android、iOS、HtmlUnit 2.9 及以上。

如果你想了解更多关于 Selenium WebDriver 的知识，请参考这篇关于 [***Selenium 教程***](https://www.edureka.co/blog/selenium-tutorial) 的文章。现在让我们了解最后一个组件，即硒网格。

### **硒栅**

[硒格](https://www.edureka.co/blog/selenium-grid-tutorial)是和硒 RC 一起使用的工具。它用于在不同的机器上针对不同的浏览器并行运行测试。这意味着——在运行不同浏览器和操作系统的不同机器上同时运行多个测试。您也可以参考这篇关于 Selenium Grid 的文章，从更广的角度理解这些概念。

所以这都是关于硒的成分。到此，我们来结束这篇文章。 我希望你理解这些概念，并帮助你增加知识的价值。现在，如果你想对硒有更多的了解，你可以看看我们的 ***[其他关于硒的文章](https://www.edureka.co/blog/category/software-testing/)* 。**

*如果您发现这篇“Selenium Components 文章* *”、* *相关内容，请查看 Edureka 提供的 ***[Selenium 认证培训](https://www.edureka.co/selenium-certification-training)**** *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在 Selenium Components 文章的评论部分提到它，我们会尽快回复您。*