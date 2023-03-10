# 使用 Ansible Vault 保护您的秘密

> 原文：<https://www.edureka.co/blog/ansible-vault-secure-secrets>

技术的使用率越高，对安全的可能威胁就越大。典型的 Ansible 设置需要你输入“秘密”。这些秘密可以是任何东西，密码、API 令牌、SSH 公钥或私钥、SSL 证书等等。我们如何保护这些秘密的安全？Ansible 提供了一个名为 Ansible Vault 的功能。

在这篇博客中，我将演示如何使用 Ansible Vault，并探索一些保护数据安全的最佳实践。

本博客涉及的主题:

*   [什么是 Ansible Vault？](#What-is-Ansible-Vault)
*   [为什么要使用 Ansible Vault？](#Why-use-Ansible-Vault)
*   [创建加密文件](#Creating-Ansible-Vaults)
*   [编辑加密文件](#Editing-Encrypted-Files)
*   [查看加密文件](#Viewing-Encrypted-Files)
*   [重设金库密码](#Rekeying-Encrypted-Files)
*   [加密未加密文件](#Encrypting-Unencrypted-Files)
*   [解密加密文件](#Decrypting-Encrypted-Files)
*   [加密特定变量](#Encrypting-specific-variables)
*   [运行时解密加密文件](#Decrypting-Encrypted-Files-during-Runtime)
*   [使用金库 Id](#Using-Vault-Ids)

*如果你想掌握 DevOps，[这门](https://www.edureka.co/devops?qId=15528fae0b7b58fb1a3c599f1cbe9c02&index_name=prod_search_results_courses&objId=776&objPos=1)课程将是你的首选。*

## **什么是 Ansible Vault？**

将基础设施作为代码可能会带来将您的敏感数据暴露给外界的威胁，从而导致不必要的安全问题。Ansible Vault 是一个功能，可以让你保持所有的秘密安全。它可以加密整个文件，整个 YAML 剧本，甚至一些变量。它提供了一种工具，您不仅可以加密敏感数据，还可以将它们集成到您的行动手册中。

Vault 以文件级粒度实施，文件要么完全加密，要么完全不加密。它使用相同的密码加密和解密文件，这使得使用 Ansible Vault 非常用户友好。

## **为什么要使用 Ansible Vault？**

随着 Ansible 被用于自动化，剧本很有可能包含某些凭证、SSL 证书或其他敏感数据。将如此敏感的数据保存为纯文本不是一个好主意。一次错误的 GitHub 或笔记本电脑盗窃会给组织带来巨大的损失。这就是 Ansible vault 的用武之地。这是将基础设施作为代码的一种很好的方式，而不会损害安全性。

假设，我们有一个在 AWS 上提供 EC2 实例的剧本。您需要在行动手册中提供您的 AWS 访问密钥 id 和 AWS 密钥。出于显而易见的原因，您不会与他人共享这些密钥。你如何让他们不暴露？有两种方法——要么加密这两个变量并将其嵌入行动手册，要么加密整个行动手册。

这只是可以使用 ansible vault 的场景之一。我们既可以加密整个文件，也可以只加密一些可能包含敏感数据的变量，然后 Ansible 在运行时自动解密它们。现在我们可以安全地将这些值提交给 GitHub。

## **创建加密文件**

要创建一个加密文件，使用 **ansible-vault create** 命令并传递文件名。

```
$ ansible-vault create filename.yaml
```

系统会提示您创建一个密码，然后通过重新输入来确认。

![ansible vault create - Ansible Vault - Edureka](img/d4cf5c1eb469e29a2a79f1ccf0886e5a.png)

一旦您的密码被确认，一个新的文件将被创建并打开一个编辑窗口。默认情况下，Ansible Vault 的编辑器是 vi。您可以添加数据，保存并退出。

## ![secrets txt - Ansible Vault - Edureka](img/e6da0884a9176e645f198b6dd8d782e9.png)

你的文件被加密。

## ![edit output - Ansible Vault - Edureka](img/0daaef453b5e0e62ceaae9995bc9f0c9.png)

## **编辑加密文件**

如果你想编辑一个加密文件，你可以使用 **ansible-vault edit** 命令编辑它。

```
$ ansible-vault edit secrets.txt
```

其中 secrets.txt 是已经创建的加密文件。

系统会提示您输入保管库密码。文件(解密版本)将在 vi 编辑器中打开，然后您可以进行所需的更改。

![vault edit - Ansible Vault - Edureka](img/35caa4c325ae3321464e09f8e5db2081.png)

如果你检查输出，你会看到当你保存并关闭时，你的文本会被自动加密。

![edit output - Ansible Vault - Edureka](img/0daaef453b5e0e62ceaae9995bc9f0c9.png)

## **查看加密文件**

如果你只想查看一个加密的文件，你可以使用 **ansible-vault view** 命令。

```
$ ansible-vault view filename.yml 
```

你将再次被提示输入密码。

![vault view - Ansible Vault - Edureka](img/af075c60327811f4c9ec871192b302dc.png)

你会看到类似的输出。

## ![view output - Ansible Vault - Edureka](img/ed0b7c21ff2ccb1fcd9f206dcebeeb37.png)

## **重设金库密码**

当然，有些时候你会想要更改保险库密码。您可以使用 **ansible-vault rekey** 命令。

```
$ ansible-vault rekey secrets.txt
```

系统会提示您输入保管库的当前密码，然后输入新密码，最后确认新密码。

## ![rekey out - Ansible Vault - Edureka](img/c22e3bca6840bbe58dff6fc5b4e1f9ce.png)

## **加密未加密文件**

假设你有一个想要加密的文件，你可以使用 **ansible-vault encrypt** 命令。

```
$ ansible-vault encrypt filename.txt
```

系统将提示您输入并确认密码，您的文件将被加密。

## ![vault encrypt - Ansible Vault - Edureka](img/fd13ffc59e52fe1e7274fc9685caa2a1.png)

现在你可以看到文件内容了，它们都被加密了。

## ![encrypt output - Ansible Vault - Edureka](img/bcdd44f2c22444bec314d80f8a0085fb.png)

## **解密加密文件**

如果你想解密一个加密的文件，你可以使用 **ansible-vault 解密**命令。

```
$ ansible-vault decrypt filename.txt
```

像往常一样，它会提示您插入并确认保险库密码。

## ![vault decrypt - Ansible vault - Edureka](img/6b8dc96535822ee877e6bde23c7cc527.png)

## **加密特定变量**

使用 Ansible Vault 的最佳实践是仅加密敏感数据。在上面解释的示例中，开发团队不想与生产和试运行团队共享他们的密码，但是他们可能需要访问某些数据来执行他们自己的任务。在这种情况下，您应该只对您不想与他人共享的数据进行加密，让其余的数据保持原样。

Ansible Vault 只允许你加密特定的变量。为此，您可以使用**ansi ble-vault encrypt _ string**命令。

```
$ ansible-vault encrypt_string
```

系统会提示您插入并确认保管库密码。然后，您可以开始插入想要加密的字符串值。按 ctrl-d 结束输入。现在，您可以将这个加密的值分配给剧本中的一个字符串。

![vault encrypt string - Ansible Vault - Edureka](img/186cc76d71c91646a99f5d99cf29d137.png)

你也可以用一行代码完成同样的事情。

```
$ ansible-vault encrypt_string 'string' --name 'variable_name'
```

![vault encrypt string - Ansible Vault - Edureka](img/1956446973c2f730d46a5e94784c6dd9.png)

## **运行时解密加密文件**

如果你想在运行时解密一个文件，你可以使用**–ask-vault-pass**标志。

```
$ ansible-playbook launch.yml --ask-vault-pass
```

这将解密用于执行 launch.yml 行动手册的所有加密文件。此外，这只有在所有文件都用相同的密码加密的情况下才有可能。

![ask vault pass - Ansible Vault - Edureka](img/dc64af39dabcfbe161d7c7d7563d3ca3.png)

密码提示会变得很烦人。自动化的目的变得毫无意义。我们如何让它变得更好？Ansible 有一个名为“密码文件”的特性，它引用一个包含密码的文件。然后，您可以在运行时传递这个密码文件来实现自动化。

```
$ ansible-playbook launch.yml --vault-password-file ~/ .vault_pass.txt
```

![vault pass file - Ansible Vault - Edureka](img/6d97094824780dddb6f8656f515a4984.png)

拥有指定密码的单独脚本也是可能的。您需要确保脚本文件是可执行的，并且密码被打印到标准输出中，这样它才能正常工作，不会出现令人讨厌的错误。

```
$ ansible-playbook launch.yml --vault-password-file ~/ .vault_pass.py
```

## **使用金库 Id**

保险库 Id 是为特定保险库密码提供标识符的一种方式。Vault ID 有助于使用不同的密码加密不同的文件，以便在行动手册中引用。Ansible 的这个特性是随着 Ansible 2.4 的发布而出现的。在此版本之前，每次执行 ansible 剧本时只能使用一个保险库密码。

因此，现在如果你想执行一个使用不同密码加密的多个文件的可行剧本，你可以使用保险库 Id。

```
$ ansible-playbook --vault-id vault-pass1 --vault-id vault-pass2 filename.yml
```

至此，我们结束了这篇关于 Ansible Vault 的博客。赶上技术并充分利用它们是令人惊奇的，但不是通过在安全性上妥协。这是将基础设施作为代码(IaC)的最佳方式之一。

如果你觉得这篇文章有帮助，可以去看看由 Edureka 提供的 [DevOps 课程](https://www.edureka.co/devops?qId=15528fae0b7b58fb1a3c599f1cbe9c02&index_name=prod_search_results_courses&objId=776&objPos=1)。它涵盖了让 It 行业变得更加智能的所有工具。

*有问题吗？请将它发布在 [Edureka 社区](https://edureka.co/community)上，我们将会回复您。*