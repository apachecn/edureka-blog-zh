# 使用 Sqoop 从 Oracle 到 HDFS

> 原文：<https://www.edureka.co/blog/hdfs-using-sqoop/>

1.从以下链接下载 Oracle Expresss 版本，并将其解压缩。

https://docs.google.com/a/edureka.in/file/d/0B2-rlCGKD40NNW5BcHZMTkdtcmc/edit

[![61](img/357e0d978a7067cba1063fe5f75711b4.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/612.png)

2.解压缩后，您会发现一个 Oracle XE Edition 的可执行文件，如下图所示。

[![62](img/9c13a5ee8151e224abe231dd7c2e4e58.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/621.png)

3.双击 OracleXEUniv 在您的系统上安装 Oracle 数据库，然后单击 Run。

[![63](img/248809a393ce8db0b5a4748fafaee547.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/631.png)

4.点击下一步

[![64](img/065f71c0e4c175fe7c0ff96c8ff263f1.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/641.png)

5.接受许可协议，然后单击下一步。

[![65](img/928f823568c64774378cc3059741e848.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/651.png)

6.默认情况下，oracle 将 system 作为数据库名称。让我们输入密码

对于这个数据库。

输入密码–>系统

确认密码–>系统

单击下一步:

[![66](img/dbb1ccada769e9d212682730ea7eee01.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/661.png)

7.点击安装

[![67](img/f294b154bd45062c5654291a68cf9dc9.png) ](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/671.png) [ ![68](img/bc9b551e40c4e1e0336a668b475a3e32.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/681.png)

8.点击完成

[![69](img/b4a77ed4a0c1946e4a2cb2bc9e73a0cb.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/691.png)

9.让我们编辑文件夹中的 sqlnet.ora 文件

c:Oracle xepporacleproduct . 2.0 server network admin

当你打开它，你会发现下面的内容。

[![70](img/cb15c5e633661805eb7afdb44e0eb23d.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/701.png)

编辑它，如下图所示

[![71](img/cb44b6cdfbbe4d1c3c23de88f9017fc7.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/712.png)

10.让我们启动 Oracle 的 SQL 命令行。

转到开始菜单->所有程序-> Oracle 数据库 10g 快捷版->

运行 SQL 命令行并双击它。

[![72](img/aad207f4e8559ad4bd8cf1e6c31c4bcb.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/721.png)

11.您将获得 Oracle 数据库的命令行界面。

[![73](img/aed2b0226d0e72f552438fcbc51109a6.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/731.png)

12.让我们连接到 Oracle 数据库。

用户名:系统

密码:系统

[![74](img/fcdff17f36aecab4f01e8da8e09c4c0f.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/741.png)

您将收到成功连接的消息。

13.让我们创建一个简单的表。

命令:

创建表 emp (id 号)；

[![75](img/c7dbd657d36f940b56d211815198d4ad.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/751.png)

14.让我们使用 insert 命令在其中插入一些值。

命令:

插入 emp 值(2)；

[![76](img/fa0bc589d1169eddf5381390727a6835.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/761.png)

15.让我们使用 Select 命令检查数据是否被插入到表中。

命令:

select * from emp

[![77](img/5f256e415bd454e0b7a8ee92957e1d7d.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/771.png)

16.让我们提交数据。

命令:

提交；

[![78](img/cc52ca965e58b2ec17ba20af26d3e347.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/781.png)

17.为了将数据从 Oracle 数据库导入到 Sqoop，我们需要添加

Oracle 连接器(ojdbc6_g.jar)。

你可以从下面的链接下载这个 jar。

https://docs.google.com/a/edureka.in/file/d/0B2-rlCGKD40Nekw3ZXBRWUU5Y1E/edit

18.打开 Cloudera cdh3，使用 FileZilla 将 Oracle connector 迁移到 Cloudera cdh3(到桌面)。

使用以下链接了解如何将文件从 Windows 移动到 cloudera cdh3 vm。

https://www.edureka.co/blog/transfer-files-windows-cloudera-demo-vm/

19.一旦 Oracle 连接器出现在 Cloudera Cdh3 桌面上，就将其移动到

通过执行以下命令来执行 sqoop:

命令:

sudo CP/home/cloudera/Desktop/OJ DBC 6 _ g . jar/usr/lib/sq OOP/lib/

[![79](img/833cd353de25d53f4a5c0977597e0d23.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/791.png)

20.通过执行以下命令，将目录更改为 Sqoop:

命令:

cd /usr/lib/sqoop/

[![80](img/9892125e15cabe7342214e4383e89b87.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/801.png)

21.在 Windows 上打开命令提示符(CMD)并检查 **IPv4 地址**

通过执行

以下命令:

命令:

用于查看本机的 IP 信息

[![81](img/f7af649bb1ad54417cee4157606ee178.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/811.png)

22.通过执行以下命令，将 Oracle 数据库中的表 emp 的数据导入 hdfs

命令:

命令所需的项目:

IPv4 地址–您的 IPv4 地址。我的情况是 192.168.46.1

数据库名称–系统

表名–EMP

用户名-系统

密码-系统

输出目录–可以是任何目录。我用过 sqoopoutput1

命令:

sudo bin/sqoop 导入–连接 jdbc:oracle:thin:system/

系统@192.168.46.1:1521:xe

–用户名 system-P–表 system . EMP–列“ID”–目标目录/

sqoopoutput1 -m 1

[![83](img/925291c3eb40297b64406466292f112b.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/831.png)

23.当命令成功执行时，您将收到消息

检索的记录如下图所示。

[![84](img/7446670bef59190fa7790e9d4a6e928f.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/841.png)

24.打开浏览器并转到以下 URL:

URL:http://localhost:50070/DFS health . JSP

点击浏览文件系统

[![86](img/2ddde88447b8f6611fa474724de84285.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/861.png)

25.点击 sqoopoutput1 目录

[![87](img/d6fd55ab89af9e596af8d6916baa2732.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/871.png)

26.点击零件-m-00000 文件:

[![88](img/74842a73e72fe4c059f4aaf601975c0c.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/881.png)

27.下面是从 Oracle 数据库导入的数据:

[![89](img/04ceb073e7f1d4b5908b647d12b5cda3.png)](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/891.png)

恭喜你！您已成功从 Oracle 数据库导入数据

使用 Sqoop 到 HDFS..！