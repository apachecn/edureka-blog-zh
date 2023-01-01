# 关于 PHP 中的文件处理，你需要知道的

> 原文：<https://www.edureka.co/blog/file-handling-in-php/>

实际上，PHP 脚本需要处理从磁盘文件、SQL 结果集、XML 文档和许多其他类型的数据中检索到的数据。PHP 有许多访问这些数据源的内置函数。让我们按以下顺序理解 PHP 中的文件处理:

*   [打开文件](#open)
*   [关闭文件](#close)
*   [读取文件](#read)
*   [写文件](#write)
*   [其他文件处理&目录操作](#other)

## **PHP 中的文件处理:打开文件**

函数的作用是打开一个文件。第一个参数包含要打开的文件的名称，第二个参数告诉应该以何种模式打开文件。函数的作用是:创建一个指针，指向所提到的文件。

**举例:**

`<?php` `// a file is opened using fopen() function` `$file = fopen(“demo.txt”,'w');`

在 PHP 中打开文件的模式有:

| **模式** | **描述** |
| **r** | 只读。文件指针从文件的开始处开始 |
| **r+** | 读/写。文件指针从文件的开头开始 |
| **w** | 只写。它打开并清除文件的内容；或者创建一个新文件(如果它不存在) |
| **w+** | 读/写。它打开并清除文件的内容；或者创建一个新文件(如果它不存在) |
| **答** | 追加。它打开并写到文件的末尾，如果文件不存在，则创建一个新文件 |
| **a+** | 读取/追加。它通过写到文件末尾来保留文件内容 |
| **x** | 只写。创建新文件。如果文件已经存在，则返回 FALSE 和一个错误 |
| **x+** | 读/写。创建新文件。如果文件已经存在，则返回 FALSE 和错误 |

## **PHP 文件处理:关闭文件**

函数的作用是:关闭一个打开的文件指针所指向的文件。它将文件作为必须关闭的参数，并关闭该文件。

**注:**

*   如果一个文件是通过 fwrite()函数写入的，则必须首先使用 fclose()函数关闭该文件，并且您必须读取该文件的内容。

*   fclose()对远程文件不起作用。它只对服务器文件系统可访问的文件有效。

**举例:**

`<?php` `$file= fopen("demo.txt", "r");` `// the file is closed using fclose() function` `fclose($file);` 

继续 PHP 中的文件处理，下一部分是读取文件。

## **读取文件**

PHP 的文件操作 API 非常灵活:它允许您从本地文件系统或远程 URL 按行、字节或字符将文件读入字符串或数组。

*   **fread()**:fread()函数用于读取数据的内容。第一个参数是文件指针，另一个是以字节为单位的文件大小。

`<?php` `$file= "demo.txt";` `$file = fopen( $file, 'r' );` `$filedata = fread( $file, 300 );` `// reads the first 300 bytes of the file`

*   **feof()** 函数可用于检查是否到达“文件结束”(eof)。这非常有用，因为我们可以遍历一个未知长度的文件。我们可以在任何模式下对每个文件都这样做。

`<?php``$file = fopen(“demo.txt”,”r”) or exit (“ERROR: cannot open file”);``while(!feof($file))``{``echo fgets($file)``}``fclose($file);``?>`

*   函数的作用是:从文件中读取一个字符。

`<? php``$file = fopen("demo.txt", "r") or exit("ERROR: cannot open file");``while(!feof($file))``{``echo fgetc($file);``}``fclose($file);``?>`

*   **file_get_contents():** 在 PHP 中读取本地磁盘文件，使用 file_get_contents()函数。该函数接受磁盘文件的名称和路径，并将整个文件一次性读入一个字符串变量。

`<?php``//read file into string``$str = file_get_contents(‘demo.txt’) or die(‘ERROR: cannot find file’);``echo $str;`

*   从文件中读取数据的另一种方法是 PHP 的 file()函数。它接受文件的名称和路径，并将整个文件读入一个数组，数组中的每个元素代表文件的一行。我们使用 foreach 循环遍历数组来访问数组的元素。

`<?php``//read file into an array``$arr=file(“demo.txt”) or die(“ERROR: cannot find file”);``foreach($arr as $line)``{``echo $line;``}``?>`

*   **读取远程文件:****file _ get _ contents()**和 **file()** 都支持使用 HTTP 或 FTP 协议从 URL 读取数据。它将网页的 HTML 文件读入一个数组。

`<?php``//read file into array``$arr= file (“https://www.google.com”) or die (“ERROR: cannot find file”);``foreach($arr as $line)``{``echo $line;``}``?>`

**注意:** 在网络连接缓慢的情况下，以“块”的形式读取远程文件会更有效，从而最大化可用网络带宽的效率。 **fgets()** 函数可以从文件中读取特定数量的字节。

`<?php``//read file into array (chunks)``$str=””;``$file=fopen(“http://www.google.com”) or die(“ERROR: cannot open file”);``while(!feof($file))``{``$str=fgets($fgets($file,512);``//it opens only 512 bytes of data``}` `fclose($file);``echo $str;`

## **写文件**

*   函数的作用是写一个文件。fwrite()的第一个参数包含要写入的文件名，第二个参数是要写入的字符串。

`<?php``$file = fopen("demo.txt", "w") or die("ERROR: cannot open file");``$text = "this is the first linen";``fwrite($file, $text);``fclose($file);`

*   **PHP 改写:**【demo . txt】包含部分数据。所有现有的数据将被删除，我们从一个空文件开始。

`<?php``$file = fopen("demo.txt", "w") or die("ERROR: cannot open file");``$text = "this is the first linen";``fwrite($file, $text);``fclose($file);`

*   **file _ put _ contents():**file _ put _ contents()函数接受一个文件名和要写入文件的数据。

`<?php``//write string to file``$data=”this is n the n first line n”;``file_put_contents(“output.txt”,$data) or die(“ERROR: cannot write file”);``echo “data written to file”;`

## **其他文件处理和目录操作**

*   **计算文件大小:**filesize()函数以字节为单位计算文件的大小。它以文件名作为参数。

`<?php``// get file size``if (file_exists(“demo.txt”)) {``echo “File is “ . filesize(“demo.txt”) . “bytes.”;``} else {``echo “Named file does not exist. “;``}``?>`

*   **查找绝对文件路径:**realpath()函数用于获取文件的绝对文件路径。

`<?php``// get file path``if (file_exists(“demo.txt”)) {``echo “File path: “ . realpath(“demo.txt”);``} else {``echo “Named file does not exist. “;``}``?>`

**注意:** 我们也可以使用 pathinfo()函数。它返回一个包含文件路径、名称和扩展名的数组。

`<?php``// get file path info as array``if (file_exists(“demo.txt”)) {``print_r(pathinfo(“demo.txt”));``} else {``echo “Named file does not exist. “;``}``?>`

*   **检索文件属性:**我们可以使用 stat()函数获得特定文件的详细信息，包括其所有权、权限、修改和访问次数。它将此信息作为关联数组返回。

`<?php``// get file information``if (file_exists(“demo.txt”)) {``print_r(stat(“example.txt”));``} else {``echo “Named file does not exist. “;``}``?>`

*   **检查方式:** 我们可以借助 is_readable()、is_writable()和 is_executable()函数来检查一个文件是否可读、可写或可执行。

`<?php``// get file information``// output: 'File is: readable writable'``if (file_exists(“demo.txt”)) {``echo “File is: “;``// check for readable bit``if (is_readable(“example.txt”)) {``echo “ readable “;``}``// check for writable bit``if (is_writable(“demo.txt”)) {``}``if (is_executable(“demo.txt”)) {``}``echo “Named file does not exist. “;``?>`

*   **检查是否是文件:** 如果传递给 is_dir()函数的参数是目录，则返回 true。如果传递给 is_file()函数的参数是一个文件，则该函数返回 true。

`<?php``// test if file or directory``if (file_exists(“demo.txt”)) {``if (is_file(“demo.txt”)) {``echo “It's a file.”;``}``else {``echo “ERROR: File does not exist.”;``}``?>`

*   **复制文件:**copy()函数将文件从一个位置复制到另一个位置。它将文件源和目标路径作为两个参数

`<?php``// copy file``if (file_exists(“demo.txt”)) {``if (copy(“demo.txt”, “new_demo.txt”)) {``echo “File successfully copied.”;``} else {``echo “ERROR: File could not be copied.”;``}``} else {``echo “ERROR: File does not exist.”;``}`

*   **重命名文件或目录:**rename()函数用于重命名或移动文件(或目录)。I 将新旧路径名作为参数。

`<?php``// rename/move file``if (file_exists(“demo.txt”)) {``if (rename(“demo.txt”, “../new_demo.txt”)) {``echo “File successfully renamed.”;``} else {``echo “ERROR: File could not be renamed.”;``}``} else {``echo “ERROR: File does not exist.”;``}``// rename directory``if (file_exists('mydir')) {``if (rename('mydir', 'myotherdir')) {``echo 'Directory successfully renamed.';``echo 'ERROR: Directory could not be renamed.';``} else {``echo 'ERROR: Directory does not exist.';``}`

*   **删除文件或目录:**unlink()函数用于删除文件。它将文件名作为参数。

`<?php``// delete file``if (file_exists(“demo.txt”)) {``if (unlink(“demo.txt”)) {``echo “File successfully removed.”;``} else {``echo “ERROR: File could not be removed.”;``}``} else {``echo “ERROR: File does not exist.”;``}`

*   **锁定和解锁文件:** 函数的作用是:在读取或写入文件之前锁定文件，使其不能被其他进程访问。这样做可以降低数据损坏的可能性，如果两个进程试图在同一时刻将不同的数据写入同一文件，可能会发生数据损坏。第一个参数接受文件名。flock()的第二个参数指定锁的类型:LOCK_EX 为写操作创建一个排他锁，LOCK_SH 为读操作创建一个非排他锁，LOCK_UN 销毁锁。

`<?php``//open and lock file``//write string to file``//unlock and close file``$data=”This is n the n first line”;``$file=fopen(“demo.txt”,”w”) or die(“ERROR: cannot open file”);``flock($file,LOCK_EX) or die(“ERROR: cannot lock file”);``fwrite($file,$data) or die(“ERROR: cannot write file”);``flock($file,LOCK_UN) or die(“ERROR: cannot unlock file”);``fclose($file);``echo “data written to file”;`

读写文件是任何 PHP 开发人员都应该知道如何完成的基本任务；本文涵盖了这些任务以及更多内容。它首先演示了如何读取本地和远程文件，以及如何创建新文件或向现有文件追加数据。然后介绍了 PHP 下的目录操作，并解释了 PHP 的许多文件和目录函数。

至此，我们结束了 PHP 文章中的文件处理。我希望文件处理不应该是一个问题。C 查看 Edureka 提供的 [**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。

有问题吗？请在“PHP 中的文件处理”的评论部分提到它，我会回复你。