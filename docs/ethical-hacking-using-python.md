# 关于使用 Python 进行道德黑客攻击，您需要知道的是

> 原文：<https://www.edureka.co/blog/ethical-hacking-using-python/>

在有道德的黑客中，编写漂亮的脚本并自动化任何结构化的过程是常见的做法，范围从小型网络扫描到广域网数据包嗅探。近年来，Python 已经成为这类任务的首选语言，这是有充分理由的。在这篇关于使用 Python 进行道德黑客的文章中，我们将讨论让这两个人如此出色的原因

以下是我们将要讨论的主题清单:

*   [什么是道德黑客？](#what-is-ethical-hacking)
*   [Python 是什么？](#what-is-python)
*   [为什么使用 Python 进行道德黑客攻击？](#python-and-hacking)
*   [使用 Python 的简单字典攻击](#demo)

## **什么是道德黑客？**

黑客这个术语可以追溯到很久以前。确切地说，这一切都始于麻省理工学院的*铁路俱乐部*，这里首次创造了术语“*黑客”*和“*黑客”*。到现在快 50 年了，黑客已经演变成了当今时代的一门学科。随着人们对数据保护和数据隐私意识的增强，如今黑客行为已被视为一种非法活动。如果被抓住，根据造成的伤害程度，你很有可能会被起诉一段时间。尽管如此，为了保护自己免受各种黑客的攻击，雇佣道德黑客已经成为组织间的普遍做法。[道德黑客](https://www.edureka.co/blog/how-to-become-an-ethical-hacker/)被赋予在黑帽黑客发现之前，为某个组织发现并修复安全漏洞的责任。浏览我们的[道德黑客课程](https://www.edureka.co/ceh-ethical-hacking-certification-course)，探索更多关于道德黑客的知识。本课程将向您传授黑客使用的最新黑客技术、工具和方法。

## **Python 是什么？**

[![Python Logo - Python cheat sheet for beginner-Edureka](img/1f832a49255567a01424e2bf3684583c.png) ](/blog/wp-content/uploads/2018/10/Python-Logo-Python-cheat-sheet-for-beginner.png) [Python](https://www.edureka.co/blog/python-tutorial/) 是一种通用脚本语言，因其简单性和强大的库而在专业人士和初学者中广受欢迎。Python 具有惊人的通用性，几乎可以用于任何类型的编程。从构建用于完成普通任务的小规模脚本，到大规模系统应用——Python 可以在任何地方使用。事实上，NASA 实际上使用 Python 为他们的设备和太空机械编程。

Python 还可以用来处理文本、显示数字或图像、求解科学方程、保存数据。简而言之，Python 在幕后用于处理大量您可能需要或在设备上遇到的元素。

## **为什么要用 Python 做伦理黑客？**

Python 之所以广受欢迎，主要是因为它拥有超级强大且易于使用的库。当然 Python 有很棒的可读性，而且它真的很简单，但是没有什么比这些库让你作为开发人员的工作变得超级简单更好的了。这些库在各种领域都有用途，例如，人工智能有[*py torch*](https://www.edureka.co/blog/pytorch-tutorial/)和 [*Tensorflow*](https://www.edureka.co/blog/tensorflow-tutorial/) 而数据科学有 [*熊猫*](https://www.edureka.co/blog/python-pandas-tutorial/) 、 [*Numpy*](https://www.edureka.co/blog/python-numpy-tutorial/) 、[*Matplotlib*](https://www.edureka.co/blog/python-matplotlib-tutorial/)。

同样，Python 在道德黑客方面也很出色，原因如下:

*   Pulsar、NAPALM、NetworkX 等漂亮的 python 库使开发网络工具变得轻而易举
*   有道德的黑客通常开发小脚本，python 作为一种脚本语言为小程序提供了惊人的性能
*   Python 有一个庞大的社区，因此任何与编程相关的疑问都会被社区迅速解决
*   学习 Python 也为你打开了另外几个[职业机会](https://www.edureka.co/blog/python-career-opportunities-your-guide-to-a-career-in-python-programming)

## **演示:使用 Python 的字典攻击**

让我给你们做一个小演示，展示一个有道德的黑客如何在日常工作中使用 Python。假设您正在扫描一个 FTP 服务器和一个客户端之间的 3 次握手，并且您也成功地这样做了。但是你们可能已经知道了，密码从来没有真正以纯文本的形式存储过。它们在被存储到数据库之前总是被散列，并且通常散列本身被比较用于验证目的。让我们创建一个小的 [Python](https://www.edureka.co/blog/python-programming-language) 程序，它可以用来使用字典攻击方法破解密码。

```
import hashlib

flag = 0

pass_hash = input("md5 hash: ")

wordlist = input("File name: ")
try:
	pass_file = open(wordlist,"r")
except:
	print("No file found :(")
	quit()

for word in pass_file:

	enc_wrd =word.encode('utf-8')
	digest =hashlib.md5(enc_wrd.strip()).hexdigest()
	# print(word)
	# print(digest)
	# print(pass_hash)
	if digest.strip() == pass_hash.strip():
		print("password found")
		print("Password is " + word)
		flag = 1
		break

if flag == 0:
	print("password not in list")

```

**60 分钟讲解使用 Python 的道德黑客|道德黑客| Edureka |网络安全直播**

[https://www.youtube.com/embed/ANgGnXPou5A](https://www.youtube.com/embed/ANgGnXPou5A)

好了，伙计们，这篇“使用 Python 进行道德黑客攻击”的文章到此结束。这是我发表的一长串道德黑客博客中的一个。关于网络安全的更多信息，你可以看看我的其他[博客](https://www.edureka.co/blog/?s=cybersecurity)。如果你对这篇文章有任何疑问，请在下面的评论区留下你的评论，或者今天就参加我们在乌代普尔举办的[网络安全培训。](https://www.edureka.co/cybersecurity-certification-training-udaipur)

如果您希望学习网络安全，并在网络安全领域建立丰富多彩的职业生涯，那么请查看我们的 [***网络安全认证培训***](https://www.edureka.co/cybersecurity-certification-training) ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解网络安全，并帮助您掌握该主题。

*你也可以看看我们新推出的课程 **[CompTIA Security+认证](https://www.edureka.co/comptia-security-plus-certification-training)** 课程，这是 Edureka & CompTIA Security+首次与官方合作的课程。它为您提供了一个获得全球认证的机会，该认证侧重于安全和网络管理员不可或缺的核心网络安全技能。*

<article class="maincontentblog">*Got a question for us? Please mention it in the comments section of “Ethical Hacking using Python” and we will get back to you.*</article>

<article>Learn Cybersecurity the right way with Edureka’s [cyber security masters](https://www.edureka.co/masters-program/cybersecurity-training) programand defend the world’s biggest companies from phishers, hackers and cyber attacks.</article>