# 其它环境中的 Git
从头至尾读到了这里，你肯定已经掌握了不少使用 Git 命令行操作的知识。

你学会了操作本地文件，通过网络连接你的仓库，以及与他人进行有效率的合作。 但是故事并未就此结束。


## 图形界面

Git 的原生环境是终端。

在那里，你可以体验到最新的功能，也只有在那里，你才能尽情发挥 Git的全部能力。

但是对于某些任务而言，纯文本并不是最佳的选择；有时候你确实需要一个可视化的展示方式。

不同的界面是为不同的工作流程设计的，每种工具都有其特定的目的和意义，
没有什么事情是图形界面客户端可以做而命令行客户端不能做的；命令行始终是你可以完全操控仓库并发挥出全部力量的地方。

### gitk 和 git-gui 
在安装 Git的同时，你也同时装好了它提供的可视化工具，gitk 和 git-gui。

- `gitk` 是一个历史记录的图形化查看器。

    你可以把它当作是基于`git log` 和 `git grep` 命令的一个强大的图形操作界面。

    当你需要查找过去发生的某次记录，或是可视化查看项目历史的时候，你将会用到这个工具。

    使用 Gitk 的最简单方法就是从命令行打开。 只需 cd 到一个 Git 仓库，然后键入：

        $ gitk [git log options]

    Gitk 可以接受很多命令行选项，其中的大部分都直接传给底层的`git log`去执行了。 `--all` 可能是这其中最有用的一个, 它告诉 gitk 去尽可能地从任何引用查找提交并显示，而不仅仅是从`HEAD`。

- git-gui 则主要是一个用来制作提交的工具。

    打开它的最简单方法也是从命令行启动：
        
        $ git gui

gitk 和 git-gui 就是针对某种任务设计的工具的两个例子。 
它们分别为了不同的目的（即查看历史和制作提交）而进行了精简，略去了用不到的功能。

### Mac 和 Windows 上的 GitHub 客户端

GitHub发布了两个面向工作流程的Git客户端：Windows 版和 Mac 版。

GitHub 的 Windows 客户端可以从 https://windows.github.com 下载。

Mac 客户端可以从 https://mac.github.com 下载。 

### 其它图形界面

除此之外，还有许许多多其它的图形化 Git 客户端：

 Git 的官方网站整理了一份时下最流行的客户端的清单： http://git-scm.com/downloads/guis


## Visual Studio中的Git

从 Visual Studio 2013 Update 1 版本开始，Visual Studio 用户可以在他们的IDE中直接使用内嵌的 Git 客户端。

Visual Studio 现在拥有一套着眼于任务的强大 Git 操作界面。 它包括线性的历史视图、diff 视图、远程仓库操作命令，以及其它很多功能。

## Visual Studio Code中的Git

Visual Studio Code内置git支持。需要安装git version 2.0.0 (or newer).
通过安装插件，实现更多功能。
参考： https://code.visualstudio.com/Docs/editor/versioncontrol

## Eclipse 中的 Git
Eclipse 附带了一个名为 Egit 的插件，它提供了一个非常完善的 Git 操作接口。 这个插件可以通过切换到 Git 视图来使用。

## Bash 中的 Git
如果你是一名 Bash 用户，Git附带了几个Shell的插件，但是这些插件并不是默认打开的。

首先，你需要从 Git 源代码中获得一份 `contrib/completion/git-completion.bash` 文件的拷贝。将这个文件复制到一个相对便捷的目录，例如你的 Home 目录，并且将它的路径添加到 `.bashrc` 中。Bash会把命令自动补全。 在适当的情况下，这项功能适用于Git所有的子命令、命令行参数、以及远程仓库与引用名。

要添加你自己的提示符（prompt），只需从 Git 源版本库复制 `contrib/completion/git-prompt.sh`文件到你的 Home 目录(或其他便于你访问与管理的目录)， 并在 `.bashrc` 里添加这个文件路径。

这两个脚本都提供了很有帮助的文档；浏览 `git-completion.bash` 和 `git-prompt.sh` 的内容以获得更多信息。

`git for windows`已经自动开启了这两个脚本功能，打开`git bash`即可使用。

## Zsh 中的 Git
Git 还为Zsh提供了一个 Tab补全库。 复制 `contrib/completion/git-completion.zsh` 到你的 home目录，然后在 `.zshrc` 中 source 即可。相对于Bash，Zsh 的接口更加强大。
该功能可用于 Git 命令、它们的参数和在仓库中内容的名称（例如 refs 和 remotes），还有文件名和其他所有 Zsh 知道如何去补全的项目。

在提示符自定义方面，Zsh 很好地兼容了Bash，并允许你同时使用一个右侧提示符。 

Zsh 本身已足够强大，但还有一些专门为它打造的完整框架，使它更加完善。其中之一名为 "oh-my-zsh"，你可以在 https://github.com/robbyrussell/oh-my-zsh 找到它。 `oh-my-zsh` 的扩展系统包含强大的 Git Tab 补全功能，且许多提示符 "主题" 可以展示版本控制数据。

## Powershell 中的 Git

Windows 中的普通命令行终端 (cmd.exe) 无法自定义 Git 使用体验，但是如果你正在使用 Powershell，那么你就十分幸运了。

安装[oh-my-posh](https://github.com/JanDeDobbeleer/oh-my-posh)，需要先安装`posh-git`模块。

# 总结

你已经学会了如何从日常工具中发挥 Git 的强大力量，以及从自己的程序中访问 Git 仓库的方法。