---
title: 命令行速成课
slug: Learn/Tools_and_testing/Understanding_client-side_tools/Command_line
---

{{LearnSidebar}}{{PreviousMenuNext("Learn/Tools_and_testing/Understanding_client-side_tools/Overview","Learn/Tools_and_testing/Understanding_client-side_tools/Package_management", "Learn/Tools_and_testing/Understanding_client-side_tools")}}

在你的开发过程中，你无疑需要在终端上（或者在“命令行”上，它们实际上是相同的）运行一些命令。本文介绍了终端、需要输入的基本命令、如何将命令链接在一起，以及如何添加自己的命令行界面 (CLI) 工具。

<table class="learn-box standard-table">
  <tbody>
    <tr>
      <th scope="row">预备条件：</th>
      <td>
        熟悉核心的 <a href="/zh-CN/docs/Learn/HTML">HTML</a>,
        <a href="/zh-CN/docs/Learn/CSS">CSS</a>, 和
        <a href="/zh-CN/docs/Learn/JavaScript">JavaScript</a> 语言。
      </td>
    </tr>
    <tr>
      <th scope="row">目标：</th>
      <td>
        要了解什么是终端/命令行，应该学习什么基本命令，以及如何安装新的命令行工具。
      </td>
    </tr>
  </tbody>
</table>

## 欢迎使用终端

终端是一个文本界面，用于执行基于文本的程序。如果你正在运行任何用于 web 开发的工具，那么几乎可以肯定的是，你必须打开命令行并运行一些命令来使用你所选择的工具 (你经常会看到这样的工具被称为 **CLI 工具**——命令行界面工具)。

大量的工具可以通过在命令行中输入命令来使用；许多是预先安装在你的系统上的，还有大量其他的可以从包注册表中安装。包注册表类似于应用程序商店，但 (主要) 面向命令行的工具和软件。我们将在本章后面学习如何安装一些工具，并在下一章中学习更多关于包注册表的知识。

对命令行最大的一个槽点是其极其缺乏用户体验。第一次使用命令行可能是一种令人望而生畏的体验：除了空白屏幕和闪烁的光标，几乎没有明显的帮助信息用于指导接下来的操作。

表面上看，它们并不友好，但实际上你可以使用它们做很多事情，我们保证，通过一些指导和练习，使用它们会变得更容易！这就是为什么我们提供这一章来帮助你开始适应这个看似不友好的开发环境。

### 终端从何而来？

终端起源于 20 世纪五六十年代，它最初的形式与我们今天使用的形式并不相似（我们应该感激这一点）。你可以在维基百科上的[终端](https://zh.wikipedia.org/wiki/%E7%B5%82%E7%AB%AF)词条中了解一些历史。

从那时起，终端一直是所有操作系统的一个不变特征——从台式电脑到云服务器，再到像树莓派 Zero 这样的微型计算机，甚至到手机。它提供了直接访问计算机底层文件系统和低级特性的途径，因此，如果你知道自己在做什么，它对于快速执行复杂任务非常有用。

它也非常适用于自动化——例如，编写一个命令即可立即更新数百个文件的标题，从“ch01-xxxx.png”更改为“ch02-xxxx.png”。如果你使用 Finder 或资源管理器的图形用户界面应用程序来更新文件名，将需要很长时间。

总而言之，终端不会很快消失。

### 终端像什么呢？

下面你可以看到一些不同类型的可以让你进入终端的程序。

下面的图片显示了 Windows 中的命令提示符，有很多种选项，从“cmd”程序到“powershell”，可以在开始菜单中输入程序名称来运行它们。

![一个原始的 Windows 命令行窗口和一个 Windows PowerShell 窗口](win-terminals.png)

下面是 macOS 终端应用程序。

![一个基础的原生 macOS 终端](mac-terminal.png)

### 你如何进入终端？

现在许多开发人员都在使用基于 Unix 的工具（例如终端以及通过终端可以访问的工具）。目前 存在于网络上的许多教程和工具都支持（但也令人遗憾地假定了）基于 Unix 的系统，但不用担心——它们可以在大多数系统上使用。在本节中，在本节中，我们将介绍如何在你选择的系统上访问终端。

#### Linux/Unix

如上所述，Linux/Unix 系统默认提供了一个终端，可以在应用程序列表中找到它。

#### macOS

macOS 有一个名为 Darwin 的系统，图形用户界面建立在其之上。Darwin 是一个类 Unix 系统，提供了终端和访问底层工具的功能。macOS Darwin 大多数情况下与 Unix 保持一致，足以让我们在本文中不必担心任何问题。

在 macOS 系统中，你可以在“应用程序/实用工具/Terminal”路径下找到终端。

#### Windows

与其他一些编程工具一样，长期以来在 Windows 上使用终端（或命令行）并不像在其他操作系统上那样简单或容易。但现在情况正在好转。

长期以来，Windows 一直有自己的类似终端的程序，称为 cmd（“命令提示符”），但这与 Unix 命令并不相同，相当于旧式的 Windows DOS 提示符。

在 Windows 上有程序可以提供更好的终端体验，例如 Powershell（[在此处查找安装程序](https://github.com/PowerShell/PowerShell)），以及 Gitbash（[Git for Windows](https://gitforwindows.org/) 工具集的一部分）。

然而，现代 Windows 系统的最佳选择是适用于 Linux 的 Windows 子系统（WSL）——一个兼容层，可让你直接从 Windows 10 中运行 Linux 操作系统，允许你在 Windows 中直接运行“真正的终端”，而无需使用虚拟机。

你可以直接从 Windows 商店免费安装它。你可以在[适用于 Linux 的 Windows 子系统文档](https://docs.microsoft.com/windows/wsl/)中找到所有所需的文档。

![一个适用于 Linux 的 Windows 子系统文档的截图](wsl.png)

至于在 Windows 上选择哪个选项，我们强烈建议尝试安装 WSL。你可以使用默认的命令提示符（`cmd`），许多工具都可以正常工作，但如果你能与 Unix 工具更好地保持一致，你会发现一切都更加容易。

#### 边注：命令行和终端的区别是什么？

通常情况下，这两个术语可以互换使用。严格来说，终端是一个软件，用于启动和连接到一个 shell。Shell 是你的会话和会话环境（例如，提示符和快捷键可能被自定义的地方）。命令行是闪烁光标以提示你输入命令的文字行。

### 你必须使用终端吗？

尽管命令行提供了大量的工具，但如果你使用类似于 [Visual Studio Code](https://code.visualstudio.com/) 这样的工具，有大量的扩展可以让你在不直接使用终端的情况下使用终端提供的一些功能。但是，你可能无法找到适用于你想要执行的所有任务的代码编辑器扩展——你最终还是要尝一尝使用终端的苦。

## 基本的内置终端命令

话不多说，让我们开始看看一些终端命令吧！下面是命令行可以做的一些事情，以及每种情况下相关工具的名称

- 在计算机文件系统中导航，完成基本的任务，例如创建、复制、重命名和删除：

  - 在目录结构中移动：`cd`
  - 创建目录：`mkdir`
  - 创建文件（并修改它们的元数据）：`touch`
  - 复制文件或目录：`cp`
  - 移动文件或目录：`mv`
  - 删除文件或目录：`rm`

- 下载在特定 URL 上的文件：`curl`
- 在大型文本中搜索文本片段：`grep`
- 分页查看文件的内容：`less`、`cat`
- 操作和转换文本流（例如将 HTML 文件中所有 `<div>` 标签更改为 `<article>`）：`awk`、`tr`、`sed`

> **备注：** 网上有许多深入介绍命令行的好教程——这只是一个简短的介绍！

让我们继续，看看在命令行上使用这些工具中的几个。在进一步操作之前，先打开终端程序！

### 在命令行中导航

当你访问命令行时，你将不可避免地需要导航到一个特定的目录“做一些事情”。所有的操作系统 (假设是默认设置) 都将在你的“home”目录中启动它们的终端程序，从那里你可能想要移动到其他地方。

`cd` 命令允许你更改目录。严格来说，`cd` 不是一个程序，而是一个内置命令。这意味着你的操作系统默认提供它，而且你也不会意外地删除它——谢天谢地！你不需要过多地担心某个命令是否是内置的，但是要记住，内置的命令在所有基于 Unix 的系统中都存在。

要更改目录，请在终端中键入 `cd`，然后输入要移动到的目录。假设该目录在你的主目录中，你可以使用 `cd Desktop` (请参见下面的屏幕截图).

![在不同窗口终端中运行 `cd Desktop` 命令的结果——终端位置移动到桌面](win-terminals-cd.png)

尝试在你的系统终端中运行：

```bash
cd Desktop
```

如果你想回到上一个目录，你可以使用两个点：

```bash
cd ..
```

> **注意：** 一个非常有用的终端快捷键是使用 <kbd>tab</kbd> 键自动完成你已知存在的名称，而不必输入整个名称。例如，在输入了上述两个命令之后，尝试输入 `cd D`，然后按下 <kbd>tab</kbd> 键——如果当前目录中存在 `Desktop` 目录，它会自动完成目录名称。接下来请记住这一点。

如果你要进入的目录嵌套得很深，你需要知道路径才能访问它。随着你对文件系统结构的熟悉程度越来越高，这通常会变得更容易，但如果你不确定路径，通常可以通过 `ls` 命令（见下文）或在资源管理器/Finder 窗口中单击来查看目录相对于当前位置的位置。

例如，如果你想进入名为 `project` 的目录内部的一个名为 `src` 的目录，并且该目录在 `Desktop` 上，你可以从你的主文件夹输入以下三个命令来到达该目录：

```bash
cd Desktop
cd project
cd src
```

但是这样非常浪费时间——相反，你可以输入一个命令，将路径中的不同项目用斜杠分隔，就像在 CSS、HTML 或 JavaScript 代码中指定图像或其他资源的路径一样：

```bash
cd Desktop/project/src
```

请注意，在路径中包含前导斜杠会使路径变成绝对路径，例如 `/Users/your-user-name/Desktop`。像上面那样省略前导斜杠会使路径相对于你的当前工作目录。这与你在 Web 浏览器中看到的 URL 完全相同。前导斜杠意味着"在网站的根目录"，而省略斜杠则意味着"该 URL 相对于我的当前页面"。

> **备注：** 在 Windows 上，你需要使用反斜杠而不是正斜杠，例如 `cd Desktop\project\src`——这可能看起来非常奇怪，但如果你想知道原因，请[观看这个 YouTube 视频片段](https://www.youtube.com/watch?v=5T3IJfBfBmI)，微软的一位主要工程师进行了解释。

### 列出目录内容

另一个内置的 Unix 命令是 `ls`（list 的缩写），它会列出你当前所在目录的内容。请注意，如果你使用的是默认的 Windows 命令提示符 (`cmd`)，这将不起作用——请使用 `dir`。

现在请在你的终端中运行以下命令：

```bash
ls
```

这将给你列出你当前工作目录中的文件和目录，但是信息非常简要——你只会得到每个项目的名称，而不知道它是文件还是目录，或其他任何信息。幸运的是，稍微改变一下命令用法就可以提供更多的信息。

### 介绍命令选项

大多数终端命令都有选项——这些选项是你添加到命令末尾的修饰符，它们使命令的行为略有不同。它们通常由命令名后的空格、后接破折号、后接一个或多个字母组成。

例如，请尝试运行以下命令，并查看结果：

```bash
ls -l
```

对于 `ls` 命令，`-l` 选项会给你提供一个列表，每行一个文件或目录，并显示更多信息。行的最左边的字母“d”标志着这是一个目录。这些是我们可以使用 `cd` 进入的目录。

下面是一个截图，顶部是一个“原始”的 macOS 终端，下面是一个带有一些额外图标和颜色——以使其看起来更加生动的自定义终端——它们都显示了运行 `ls -l` 的结果：

![一张原始的 macOS 终端和一张更加丰富多彩的自定义终端的截图，显示文件列表——这是运行 `ls -l` 命令的结果](mac-terminals-ls.png)

> **备注：** 要确切地了解每个命令有哪些可用选项，你可以查看其[手册页](https://en.wikipedia.org/wiki/Man_page)。这可以通过输入 `man` 命令，后跟要查找的命令的名称，例如 `man ls`。这将在终端的默认文本文件查看器中打开手册页（例如，在我的终端中是 [`less`](https://zh.wikipedia.org/wiki/Less_(Unix))），然后你应该能够使用箭头键或类似机制滚动页面。手册页详细列出了所有选项，这一开始可能有点吓人，但至少在需要时你知道它就在那里。完成查看手册页后，你需要使用文本查看器的退出命令（在 `less` 中是 "q"；如果不明显，你可能需要在网上搜索）退出手册页。

> **备注：** 要同时运行具有多个选项的命令，通常可以在破折号字符后面将它们全部放入单个字符串中，例如 `ls -lah` 或 `ls -ltrh`。请尝试查看 `ls` 的手册页，以确定这些额外选项的作用！

现在我们已经讨论了两个基本命令，请浏览一下你的目录，并尝试从一个位置导航到另一个位置。

### 创建，复制，移动，删除

在使用终端时，你可能会经常使用其他一些基本实用程序命令。它们非常简单，所以我们不会像前一对那样详细地解释它们。

在你创建的某个地方的测试目录中使用它们，这样你就不会意外地删除任何重要的内容，使用下面的示例命令作为指导

- `mkdir` —这将在你所在的当前目录中创建一个新目录，名称是你在命令名之后提供的。例如 `mkdir my-awesome-website` 将创建一个新目录叫 `my-awesome-website`。
- `rmdir` —删除指定目录，但仅当它为空时。例如`rmdir my-awesome-website`

  将删除我们在上面创建的目录。如果你希望删除一个非空的目录 (并删除其中包含的所有内容)，则可以使用`-r`选项（递归），但这很危险。确保以后在目录中不需要任何内容，因为它将永远消失。。

- `touch` —在当前目录中创建一个新的空文件。例如`touch mdn-example.md` 创建一个新的空文件叫做 `mdn-example.md`.
- `mv` —
例如，将文件从第一个指定的文件位置移动到第二个指定的文件位置`mdn-example.md mdn-example.txt`(这些位置被写成文件路径)。此命令移动一个名为`mdn-example.md`在当前目录中调用一个文件`mdn-example.txt` in the current directory.从技术上讲，文件正在被移动，但是从实际的角度来看，这个命令实际上是在重命名文件。

- `cp` — 类似于 `mv`, `cp`在指定的第一个位置和第二个位置创建文件的副本。例如
  `cp mdn-example.txt mdn-example.txt.bak`创建一个副本`mdn-example.txt` 叫做 `mdn-example.txt.bak`（当然，如果你愿意，你也可以叫它别的名字)。
- `rm` —删除指定的文件。例如，`rm mdn-example.txt` 删除单个文件叫做 `mdn-example.txt`.请注意，此删除是永久性的，不能通过桌面用户界面上的回收站撤消。

> **备注：** 许多终端命令允许你使用星号作为“通配符”字符，意思是“任何字符序列”。这允许你一次对可能大量的文件运行操作，所有这些文件都匹配指定的模式。作为一个例子，`rm mdn-*` 将删除所有文件开头`mdn-`. `rm mdn-*.bak` 会删除所有文件的开头`mdn-` 结束 `.bak`.

## 考虑终端有害吗？

我们之前提到过这一点，但为了明确起见，你需要小心使用终端。简单的命令不会带来太多危险，但是当你开始将更复杂的命令组合在一起时，你需要仔细考虑该命令将执行什么操作，并在最终在指定的目录中运行它们之前先尝试测试它们。假设你在一个目录中有 1000 个文本文件，你想遍历它们，并且只删除文件名中有特定子字符串的文件。如果不小心，可能会删除一些重要的内容，在此过程中丢失大量工作。

要养成的一个好习惯是在文本编辑器中编写你的 terminal 命令，弄清楚你认为它应该是什么样子，然后对目录进行备份，并首先尝试在该备份上运行命令，以测试它。

另一个好建议是，如果你不习惯在自己的机器上尝试终端命令，可以在 Glitch.com 上试试。除了是测试 web 开发代码的好地方外，这些项目还允许你访问终端，这样你就可以直接在该终端中运行所有这些命令，而且不会破坏你自己的机器。

![a double screenshot showing the glitch.com home page, and the glitch terminal emulator](glitch.png)

快速浏览特定终端命令的一个很好的资源是 [tldr.sh](https://tldr.sh/). 这是一个社区驱动的文档服务，类似于 MDN，但特定于终端命令。

在下一节中，让我们更进一步 (实际上是几个层次)，看看如何在命令行上将工具连接在一起，从而真正了解终端如何优于常规的桌面用户界面。

## 与管道命令连接在一起

当你开始使用。将命令链接在一起时，终端才真正成为自己的终端 `|` (pipe) 的象征。让我们看一个简单的例子来说明这意味着什么。

我们已经看了 `ls`, 它可以输出文件目录：

```bash
ls
```

但是如果我们想要快速计算当前目录中的文件和目录的数量会怎样呢`ls` 不能单独运行

还有另一个可用的 Unix 工具，称为`wc`. 它计算输入到其中的单词、行、字符或字节的数量。这可以是一个文本文件，下面的示例输出其中的行数

`myfile.txt`:

```bash
wc -l myfile.txt
```

但是它还可以计算输入到它的输出的行数。例如，下面的命令计算 ls 命令输出的行数 (如果单独运行，它通常会打印到终端)，并计算到终端的输出

```bash
ls | wc -l
```

因为 `ls` 在自己的行上打印每个文件或目录，这有效地为我们提供了目录和文件计数。

这是怎么回事？(unix) 命令行工具的一般原理是，它们将文本打印到终端 (也称为“打印到标准输出”或`STDOUT`). 很多命令也可以从流输入 (称为“标准输入”o) 中读取内容 `STDIN`).

管道操作符可以将这些输入和输出连接在一起，允许我们构建越来越复杂的操作，以满足我们的需要。一个命令的输出可以成为下一个命令的输入。在这种情况下，`ls` 通常会将其输出到`STDOUT`, 但是相反 `ls`输出被制成`wc`, 它将该输出作为输入，计算它包含的行数，然后将该计数输出到 STDOUT。

## 一个稍微复杂一点的例子

让我们看一些更复杂的东西。我们将首先尝试获取 MDN 的“获取”页面的内容 `curl` 命令 (可用于从 url 请求内容)[https://developer.mozilla.org/en-US/docs/Web/API/fetch](/zh-CN/docs/Web/API/fetch).

但是，这个 URL 是页面的旧位置。如果你在一个新的浏览器标签中输入它，你将 (最终) 被重定向到[https://developer.mozilla.org/enUS/docs/Web/API/fetch](/zh-CN/docs/Web/API/fetch).

因此，如果你使用 curl 请求 `https://developer.mozilla.org/docs/Web/API/fetch`，则不会得到输出。现在就试试：

```bash
curl https://developer.mozilla.org/en-US/docs/Web/API/fetch
```

我们想精确的告诉 `curl` 遵循重定向使用`-L` 标签。

让我们也看看标题 `developer.mozilla.org` 返回使用 `curl`'s `-I` 标签，并打印它发送到终端的所有位置重定向，通过管道输出 `curl` 到`grep` (我们将要求 grep 返回包含单词“location”的所有行)。

尝试运行以下代码，你将看到在到达最终页面之前，实际上发生了三次重定向

```bash
curl https://developer.mozilla.org/docs/Web/API/fetch -L -I | grep location
```

输出应该是这样的 (`curl` 首先会输出一些下载计数器之类的东西):

```bash
location: /en-US/docs/Web/API/fetch
location: /en-US/docs/Web/API/GlobalFetch/GlobalFetch.fetch()
location: /en-US/docs/Web/API/GlobalFetch/fetch
location: /en-US/docs/Web/API/fetch
```

尽管有些做作，我们可以把这个结果做得更深入一点，并变换 `location:` 行内容，将基本的起点添加到每个起点的开始，这样我们就可以打印出完整的 url。为此，我们将在混合中添加 awk(它是一种类似于 JavaScript、Ruby 或 Python 的编程语言，只是要老得多 !)

尝试运行这个：

```bash
curl https://developer.mozilla.org/docs/Web/API/fetch -L -I | grep location | awk '{ print "https://developer.mozilla.org" $2 }'
```

最终的输出应该是这样的

```bash
https://developer.mozilla.org/en-US/docs/Web/API/fetch
https://developer.mozilla.org/en-US/docs/Web/API/GlobalFetch/GlobalFetch.fetch()
https://developer.mozilla.org/en-US/docs/Web/API/GlobalFetch/fetch
https://developer.mozilla.org/en-US/docs/Web/API/fetch
```

通过组合这些命令，我们定制了输出以显示完整的 url，当我们请求时，Mozilla 服务器将通过这些 url 重定向`/docs/Web/API/fetch` URL.了解你的系统将在未来几年证明是有用的，你将了解这些单一服务工具是如何工作的，以及它们如何成为你解决小众问题的工具库的一部分。

## 添加工具

现在我们已经了解了系统自带的一些内置命令，让我们看看如何安装和使用第三方 CLI 工具。

目前，用于前端 web 开发的可安装工具的巨大生态系统主要存在于内部 [npm](https://www.npmjs.com), 与 Node.js 紧密合作的私有的包托管服务。随着时间的推移，你可以期望看到更多的包提供者。

[Installing Node.js](https://nodejs.org/en/) 还要安装 npm 命令行工具 (以及一个以 npm 为中心的补充工具 npx)，它提供了安装其他命令行工具的网关。js 和 npm 在所有系统上都能工作:macOS、Windows 和 Linux。

现在在你的系统上安装 npm，转到上面的 URL，下载并运行适合你的操作系统的 Node.js 安装程序。如果出现提示，请确保将 npm 作为安装的一部分。

![the node.js installer on windows, showing the option to include npm](npm-install-option.png)

尽管我们将在下一篇文章中讨论许多不同的工具，但我们将继续深入研究 [Prettier](https://prettier.io/). Prettier 是一种固执己见的代码格式化程序，它只有“很少的选择”。更少的选择往往意味着更简单。考虑到工具在复杂性方面有时会失控，“很少的选项”可能非常有吸引力。

### 在哪里下载我们的 CLI 工具？

在开始安装 Prettier 之前，有一个问题需要回答：“我们应该安装到哪里？”

用`npm` 我们可以选择在全局安装工具，因此我们可以在任何地方或本地访问当前项目目录。

每种方式各有利弊 — 而这张全局安装的利弊清单还远远不够详尽：

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col"><p>全局安装的优点</p></th>
      <th scope="col">全局安装的缺点</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>任何地方在你的终端</p></td>
      <td>可能与你项目的代码库不兼容</td>
    </tr>
    <tr>
      <td>只下载一次</td>
      <td>
        <p>
          你团队中的其他开发人员无法使用这些工具，例如，如果你通过 git
          这样的工具共享代码仓库。
        </p>
      </td>
    </tr>
    <tr>
      <td><p>使用较少的磁盘空间</p></td>
      <td>
        <p>
          与前一点相关的是，它使得项目代码更难复制
          (如果你在本地安装工具，可以将它们设置为依赖项并使用 npm 进行安装
          (<code>npm install</code>).
        </p>
      </td>
    </tr>
    <tr>
      <td><p>总是相同的版本</p></td>
      <td></td>
    </tr>
    <tr>
      <td><p>就像任何其他 unix 命令</p></td>
      <td></td>
    </tr>
  </tbody>
</table>

尽管缺点清单比较短，但是全局安装的负面影响可能要比好处大得多。然而，现在我们宁可追求简单，而采用全局安装来保持简单。在下一篇文章中，我们将进一步了解本地安装以及它们的优点。

### 下载 Prettier

对于本文，我们将安装 Prettier 作为全局命令行实用程序。

Prettier 是一款专门为前端开发人员设计的代码格式化工具，专注于基于 javascript 的语言，并增加了对 HTML、CSS、SCSS、JSON 等的支持。Prettier 能够：

- 省去了在所有代码文件中手动保持样式一致的认知开销;Prettier 可以自动为你完成此操作。
- 帮助 Web 新手以最佳方式完成他们的代码。
- 安装在任何操作系统上，甚至直接作为项目工具的一部分，以确保从事你的代码工作的同事和朋友使用你正在使用的代码风格。
- 配置为在保存时运行、在键入时运行，甚至在发布代码之前运行 (使用稍后将在模块中看到的其他工具）。

安装 node 之后，打开终端并运行以下命令来安装 prettier 程序：

```bash
npm install --global prettier
```

命令运行完成后，Prettier 工具现在可以在终端中的文件系统中的任何位置使用。

与许多其他命令一样，不带任何参数运行该命令将提供用法和帮助信息。现在试试这个

```bash
prettier
```

输出应该是这样的

```bash
Usage: prettier [options] [file/dir/glob ...]

By default, output is written to stdout.
Stdin is read if it is piped to Prettier and no files are given.

…
```

即使它很长，至少浏览一下使用信息也是值得的。它将帮助你更好地理解如何使用该工具。

### 尝试 Prettier

让我们快速演示一下 Prettier，这样你就可以看到它是如何工作的。

首先，在文件系统中容易找到的地方创建一个新目录。可能是一个叫做`prettier-test` 在你的 `Desktop`.

现在将以下代码保存在一个名为`index.js`, 在测试目录中：

```js
const myObj = {
a:1,b:{c:2}}
function printMe(obj){console.log(obj.b.c)}
printMe(myObj)
```

我们可以在代码基上运行得更好，以检查我们的代码是否需要调整。cd 到你的目录中，并尝试运行此命令：

```bash
prettier --check index.js
```

你的产出应该是：

```bash
Checking formatting...
index.js
Code style issues found in the above file(s). Forgot to run Prettier?
```

有些代码样式是可以修改的。没有问题。添加 `--write` option to the prettier 命令将修复这些问题，让我们专注于实际编写有用的代码。

现在尝试运行这个版本的命令：

```bash
prettier --write index.js
```

你可能得到这样的输出：

```bash
Checking formatting...
index.js
Code style issues fixed in the above file(s).
```

但更重要的是，如果你回头看你的 JavaScript 文件，你会发现它被重新格式化成这样：

```js
const myObj = {
  a: 1,
  b: { c: 2 },
};
function printMe(obj) {
  console.log(obj.b.c);
}
printMe(myObj);
```

根据你的工作流 (或你选择的工作流)，你可以将其作为流程的自动化部分。自动化确实是工具的优势所在;我们的个人偏好是那种无需配置任何东西就能“自动发生”的自动化。

使用 Prettier 有许多实现自动化的方法，尽管它们超出了本文的范围，但是有一些很好的在线资源可以提供帮助 (已经链接到其中一些)。你可以调用更漂亮的：

- 在将代码提交到 git 存储库之前，使用[Husky](https://github.com/typicode/husky).
- 当你在代码编辑器中点击“保存”的时候，无论是[VS Code](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode), [Atom](https://atom.io/packages/prettier-atom), 或[Sublime Text](https://packagecontrol.io/packages/JsPrettier).
- 作为持续集成检查的一部分，可以使用以下工具[Github Actions](https://github.com/features/actions).

我们个人的偏好是第二个当使用 say VS 代码时，Prettier 会启动并清理每次我们点击保存时需要做的格式化。关于以不同方式使用 Prettier，你可以在 [Prettier docs](https://prettier.io/docs/en/).

## 尝试其他的工具

如果你想尝试更多的工具，这里有一个简短的列表，很有趣的尝试：

- [`bat`](https://github.com/sharkdp/bat) — 一个更好的 `cat` (`cat` 用于打印文件内容）。
- [`prettyping`](http://denilson.sa.nom.br/prettyping/) — `ping`在命令行上，但是是可视化的 (ping 是检查服务器是否有响应的有用工具)。
- [`htop`](http://hisham.hm/htop/) —进程查看器，当某些东西使你的 CPU 风扇的行为像一个喷气发动机，并且你想要识别出错的程序时，它非常有用。
- [`tldr`](https://tldr.sh/#installation) —在本章前面提到的，但是可以作为命令行工具使用。

注意，上面的一些建议可能需要使用 npm 进行安装，就像我们使用 Prettier 所做的那样。

## 总结

这使我们结束了对终端/命令行的简短浏览。接下来，我们将更详细地介绍软件包管理器，以及如何使用它们。

{{PreviousMenuNext("Learn/Tools_and_testing/Understanding_client-side_tools/Overview","Learn/Tools_and_testing/Understanding_client-side_tools/Package_management", "Learn/Tools_and_testing/Understanding_client-side_tools")}}
