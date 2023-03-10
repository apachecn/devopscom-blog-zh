# repex–简化了正则表达式管理

> 原文：<https://devops.com/repex-versioning-complexity/>

## 我们的版本复杂性

[Cloudify](http://getcloudify.org/) 是一家 Python 商店。

我们的 REST 服务是 Python。

我们的[工作流引擎](http://getcloudify.org/guide/3.1/guide-workflows.html)是 Python。

我们的[插件](http://getcloudify.org/guide/3.1/guide-plugin-creation.html)是 Python。

我们有不同的版本格式和不同的依赖关系，不同类型的文件在版本更新时需要改变。

至少可以说，这很复杂。我们不想在处理版本更新时手动管理超过 60 个回购。

为什么不是 sed？

*   塞德是个婊子，不是吗？不可维护，不可管理。虽然这仅仅是我的观点，但是处理成百上千的文件，在没有任何安全网的情况下在不同的上下文中进行每个更改，使得 sed 成为您应该远离的东西。
*   sed 不可配置。

为什么不是金贾？

使用 Jinja 模板，虽然安全，但很快就退出了 windows，因为我们需要 repos 开箱即用，否则我们将迫使用户更改模板，以便他们可以使用我们的产品。

## 解决方案

我们求助于 Regex。是的，有 [regex 问题](http://regex.info/blog/2006-09-15/247)。你可能对这句名言很熟悉:

–有些人在遇到问题时会想:“我知道，我会使用正则表达式。”现在他们有两个问题。

虽然这可能是真的，但这也取决于你如何使用正则表达式。

我相信我们已经做得很好了。

**重复**

我们开发了 [repex](https://github.com/cloudify-cosmo/repex) 。

repex 允许您指定需要以 YAML 格式执行的更改的结构:

```
variables:  replace: 3.1.0-m2  version: 3.1.0-m4paths:  - description: demo thing    path: repex/tests/resources/mock_VERSION    match: '"version": "3.1.0-m2"'    replace: "{{ .replace }}"    with: "{{ .version }}"    to_file: repex/tests/resources/mock_VERSION.test    validate_before: true    must_include:      - date      - commit      - version  - description: handles core modules version in all core repositories    type: setup.py    path: cloudify-.*    excluded:      - my/excluded/path    match: version=('|")(\d+)(\.\d+){1,2}(dev|(\w+\d+)?)('|")    replace: (\d+)(\.\d+){1,2}(dev|(\w+\d+)?)    with: "{{ .python_core_version }}"
```

你定义一个你想要迭代的路径列表，提供你想要搜索的路径，你想要替换的路径，你想要替换的路径，以及更多的参数，然后你就可以开始了。

例如，上述配置中的第一个对象将:

*   在路径 repex/tests/resources/mock _ VERSION(regex)中查找文件
*   在该文件中，查找“版本”:“3 . 1 . 0-m2 ”`( regex)
*   仅当在匹配阶段找到字符串并且在文件中找到字符串“日期”、“提交”和“版本”时，才尝试用 3.1.0-m3 替换 3.1.0-m2。
*   写入输出文件 repex/tests/resources/mock _ version . test

第二个对象将:

*   在“cloudify-”下查找“setup . py ”( regex)文件。*` (regex)而不是在' my/excluded/path '下。
*   查找` version=('|")(\d+)(\。\d+){1，2}(dev|(\w+\d+)？)(' | " '(regex)在文件中找到。
*   替换`(' |")(\d+)(\。\d+){1，2}(dev|(\w+\d+)？)(' | " '(regex)带有一个未进行硬编码的变量，因此必须使用 API 提供。

## 保护层

repex 试图提供多层保护和舒适:

**安全！**

*   您可以首先“匹配”您想要匹配的任何内容，这样您就可以确定您只是在您希望处理的确切上下文中替换了某些内容。如果“validate_before”为真，则只有找到一个或多个匹配项时，才会进行替换。
*   您可以通过将文件列在“must_include”下来验证只有包含非常具体的字符串的文件才会被处理。
*   您可以将不需要搜索的文件或目录列在“已排除”下，从而将其排除在外。

但是不要误解，正则表达式就是正则表达式。你犯了错，就要为此付出代价。repex 给你的只是把所有东西都组织在一个地方的能力，有一些保护层来防止你犯一些小错误。

**舒适**

您可以在一个可管理的 YAML 中声明您想要寻址的每个目录或文件。

当然，我们需要创建某种命名约定，这样我们就不必单独配置每个文件。

**接受变量，包括硬编码的和通过 API 的**

repex 最强的特性之一是它支持使用变量进行字符串替换。上面的例子包含了一个`{{ .version }}`变量。

API 允许你提供变量的字典，这些变量将被放置在占位符中。您可以在`variables`部分硬编码一个变量，或者使用 API 发送一个要使用的变量字典。如果一个变量在 YAML 中被硬编码，并且您使用 API 发送一个同名的变量，它将覆盖硬编码的变量。此外，变量替换时将进行验证，以确保它已被替换。

**功能 API**

该 API 提供了三个基本功能。我不想重写 repex 的文档..所以参考[这个](https://github.com/cloudify-cosmo/repex#basic-functions)就可以了。

基本上，这三个函数允许您决定处理变更的粒度级别。它将允许您在更换过程的不同阶段执行操作。

例如，我们并没有真正使用 API 的最高级别，它只是迭代 YAML 中的所有对象。我们编写了一个 [Cloudify 特定的包装器](https://github.com/cloudify-cosmo/version-tool)，可以用作参考实现。它可以在每次替换后进行验证。因此，举例来说，在每一个蓝图特定的替换之后，我们运行一个蓝图相对于我们的 DSL 解析器是有效的验证。

Repex 在 [PyPI](https://pypi.python.org/) 上可用。您可以通过运行以下命令来安装它:

**pip 安装 repex**

我们可能会在某个时候为 repex 提供一个 CLI。此外，还可以实现一个日志记录特性，允许生成 JSON 格式的日志消息，以便可以传输它们进行分析。

在过去五个月左右的时间里，我们在整个构建过程中使用了 repex，事实证明它非常有用。我们现在可以跟踪整个版本更新过程，并通过查看一个 YAML 文件和一个执行日志文件来轻松识别问题。我们计划使用 repex 来替换其他类型的数据(不仅仅是版本)。

我们将感谢反馈，更好的是，拉请求。

希望这对你有用。