# 如何打开安装在 Windows 上的 Cassandra 的 CQLSH

> 原文：<https://www.edureka.co/blog/how-to-open-cqlsh-of-cassandra-installed-on-windows/>

在我们启动 CQLSH 之前，请确保安装在 windows 上的 Cassandra 服务器正在运行。如果它运行良好，你会发现下图。

[![cassandra-cqlshimg2](img/30ab91ceddec8790d54f5086fddd0c4d.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg2.jpg)

要启动 cqlsh，我们需要在您的机器上安装 python。

请根据系统配置下载 Python 安装程序。

下面是我的系统配置。

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg3](img/c15be0559eddde1db7f53fa342373c5a.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg3.png)

如果您的系统是 32 位版本，请使用以下链接。

https://drive.google.com/file/d/0Bw3sqswQlMb4WFJndXBKNDVzSGs/edit?usp=sharing

如果您的系统是 64 位版本，请使用以下链接。

https://drive.google.com/file/d/0Bw3sqswQlMb4Y2x3ak1VQXFqQkE/edit?usp=sharing

由于我的系统是 64 位的，所以我下载了 64 位版本的 Python。

下载后双击，点击**运行。**

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg4](img/0b080b022543a927ad2e0e91abc8596b.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg4.png)

**点击下一步**

[![cassandra-cqlshimg5](img/4c8e147ef48abcc7cd93f6bc0a9c93a0.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg5.png)

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

当它询问目标文件夹时，让它使用默认文件夹，然后点击 **Next。**

[![cassandra-cqlshimg6](img/8cd12f914cab61a30c7d0efebde268b2.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg6.png)

单击下一步

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg7](img/0932c341a3c8e07847d29c65817b4f58.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg7.png)

让它安装

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg8](img/40d0b25c8cbc075be076c75d9ae856e3.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg8.png)

你会看到下图，最后点击完成

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg9](img/196f54e8a9d9d0c2278a00902133ab2b.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg9.png)

我们已经成功地在 Windows 上安装了 Python。

现在让我们为 Python 设置路径。

右键单击我的电脑，然后转到属性。

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg10](img/bfe2ae4b0c11d68e46f9fdfde5f74583.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg10.jpg)

在系统变量下选择变量路径并点击**编辑**

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg18](img/1e22ceba4617274f6ff631ede172ad7b.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg181.png)

追加"；C:Python27 "设置为如下图所示的路径值，并点击 **ok。**

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg12](img/f6cc97bb47eaedb8a6b184a20df89f32.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg12.png)

现在从下面的链接下载 Python 节俭模块。

https://drive.google.com/file/d/0Bw3sqswQlMb4UHpNSHJtMVdEY1U/edit?usp=sharing

下载后解压到 c 盘。

如果它被提取，你会在 C:中找到它，如下图所示。

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg13](img/b81ffd5fb6a6828eb8342cec20a3c0b4.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg13.png)

现在打开命令提示符，给出下面的命令。

cd C: hrift-0.9.1

python setup.py 安装

[![cassandra-cqlshimg14](img/f65475e0220a36cf8fb9121de1364ff0.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg14.png)

你会得到下面的图像。

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg15](img/5e50de8a1d1020ef1d932cb053db2213.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg15.jpg)

现在给出下面的命令来启动 cqlsh

cd c:卡桑德拉

python cqlsh localhost 9160

[![cassandra-cqlshimg16](img/99c104397c900072bb730dd131215277.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg16.png)

我们已经成功启动了安装在 windows 上的 Cassandra 的 cqlsh。

要检查它是否工作正常，请提供命令帮助并进行检查。

**如何打开安装在 Windows 上的 Cassandra 的 CQLSH**

[![cassandra-cqlshimg17](img/9db57241a46baa305b8bc11c27bd53d2.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/cassandra-cqlshimg17.png)

如果您收到上面的输出，那么我们已经成功地启动了 cqlsh。

**恭喜你！您已成功启动 CQLSH…！！**

![Edureka - logo](img/8f01e6cfc3dfbee50f9ca156a6dd9140.png)