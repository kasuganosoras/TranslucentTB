# TranslucentTB

[![Build status](https://ci.appveyor.com/api/projects/status/9yym3vr6s5gc7vk3/branch/master?svg=true)](https://ci.appveyor.com/project/sylveon/translucenttb/branch/master)
[![Join on Discord](https://img.shields.io/discord/304387206552879116.svg)][Discord]
[![Join on Gitter](https://badges.gitter.im/TranslucentTB/Lobby.svg)][Gitter]
[![Total downloads](https://img.shields.io/github/downloads/TranslucentTB/TranslucentTB/total.svg)](https://github.com/TranslucentTB/TranslucentTB/releases)
[![Liberapay patrons](https://img.shields.io/liberapay/patrons/TranslucentTB.svg)](https://liberapay.com/TranslucentTB/)

一个轻量级（仅需要几 MB 的内存，几乎不占用 CPU）的实用程序，使 Windows 10 任务栏变成透明或者半透明。

您可以在下面的几张图片中预览软件的效果:

![blur](https://i.imgur.com/r4ZJjnL.png) ![transparent](https://i.imgur.com/eLGTtwp.png) ![acrylic](https://i.imgur.com/M15IPJW.png)

## 功能介绍

- 高级的 **颜色选择工具** 支持透明颜色，并且可以实时预览任务栏的效果
- **任务栏效果** (选择一种类型，除正常状态外，其他状态均可定制。):
  - **模糊**: 可以将任务栏变成模糊效果。
  - **透明**: 将任务栏变成完全透明的。
  - **正常**: 正常的任务栏效果 (就像没有运行 TranslucentTB 一样)
  - **纯色**: 完全不透明的任务栏。
  - **毛玻璃**: 仅限于 Windows 10 1804 版本以上支持，效果类似于 Windows 登录界面背景。
- **动态改变模式** (这些效果可以组合使用，每个效果都提供自定义选项):
  - **最大化窗口**: 如果当前窗口最大化，则将任务栏更改为其他外观。
  - **开始菜单**: 在开始菜单打开时更改任务栏外观。
  - **微软小娜**: 在打开微软小娜（如果禁用了小娜，则在打开搜索框）时改变任务栏外观。
  - **时间线或任务视图**: 当时间线（或旧版本上的任务视图）打开时更改任务栏外观。
- 可以 **显示或隐藏 Aero 特效** 按钮。可以定制为 **任意窗口** 或者 **动态改变**。

您可以在这里看到它的效果：[简单动态图介绍](https://gfycat.com/TidyFelineCrownofthornsstarfish) 以及 [详细动态图介绍](https://gfycat.com/ConsciousCriminalDassie)。

## 下载

您可以直接在 [Microsoft Store](https://www.microsoft.com/store/apps/9PF4KZ2VN4W9) 里下载本软件，并且可以支持自动同步设置等功能。

如果您想直接下载，您可以在 [Release 页面](https://github.com/TranslucentTB/TranslucentTB/releases) 下载本软件。

如果您想体验包含最新特性的构建版本，您可以在 [AppVeyor page](https://ci.appveyor.com/project/sylveon/translucenttb) (`Configuration: Release` > `Artifacts` > `TranslucentTB-setup.exe`) 下载构建的文件。请注意，这些构建的版本可能不能正常使用，或者存在未完成的功能，请您自行承担使用的风险。

## 设置开机启动

如果您希望设置 TranslucentTB 为开机启动，请在任务栏的 TranslucentTB 图标上右键，选中 "开机时启动" 选项。如果它是灰色的并且不可点击，说明 TranslucentTB 已被任务管理器或组织禁止开机启动。

## 赞助我们

[我们有一个 Liberapay！](https://liberapay.com/TranslucentTB/) 如果您喜欢 TranslucentTB 并愿意支持我们的工作，请捐赠我们。

## 安全

有些杀毒软件可能会将此程序标记为病毒。并不是这样，超过20万用户安全下载了这个程序。我们的源代码是开放的，您可以自己编译它，我欢迎任何的代码安全审查。

说到编译代码……

## 从源代码构建

您可以选择一个可用的分支。但是，建议使用 “master” 分支，因为这里的代码是最稳定的，并且已经通过了同行评审。

通过 [git](https://git-scm.com):

```sh
$ git clone -b [您想选择的分支] https://github.com/TranslucentTB/TranslucentTB
Cloning into 'TranslucentTB'...
remote: Counting objects: 909, done.
remote: Compressing objects: 100% (40/40), done.
remote: Total 909 (delta 44), reused 61 (delta 35), pack-reused 834
Receiving objects: 100% (909/909), 383.94 KiB | 2.78 MiB/s, done.
Resolving deltas: 100% (624/624), done.
```

您还可以通过点击分支文件列表的 `Clone or download` 按钮来下载代码的 Zip 压缩文件。

现在您已经拥有了源代码，接下来您需要 Visual Studio 2017. [您可以在这里获得社区免费版本](https://www.visualstudio.com/vs/community/).
并安装以下功能:

- C++ 桌面开发
- .NET 桌面开发

您还需要安装以下各个组件：

- VC++ 2017 工具集（最新版本首选）
- Windows 10 SDK（10.0.17134.0）
- .NET Framework 4.6.2 SDK
- .NET Framework 4.6.2 目标包

您还需要 [Windows C 语言编译器](http://releases.llvm.org/download.html) 以及 [Inno Setup](http://jrsoftware.org/isdl.php).

<!-- markdownlint-disable MD033 -->
当您安装完成时，请打开 `TranslucentTB.sln`，然后按下 <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>B</kbd> 来构建解决方案。
<!-- markdownlint-enable MD033 -->

输出将位于 debug 或 release 文件夹中（取决于当前激活的解决方案配置）。

要生成桌面安装程序，请运行 desktopinstallerBuilder 项目。

要构建 Microsoft 应用商店应用程序包，请使用应用商店配置构建解决方案。

## 贡献

如果您想贡献代码，所有人都欢迎！ 如果您正在考虑一个主要功能，需要指导，或想要提出一个想法，请不要犹豫，立即在 [Discord] 或 [Gitter] 提出，您也可以在此处提出一个 Issues。 主要贡献者通常在 [Discord] 和 [Gitter] 以及 GitHub，所以我们应该很快回复。
目前我们还没有计划将其扩展到任务栏之外。

在贡献时，请尊重代码库代码风格。简单示例：

- 括号应该写在单独的一行：

  ```cpp
  // Bad!
  if (condition) {
      statement;
  }
  
  // Bad!
  if (condition) statement;
  
  // Bad!
  if (condition)
      statement;
  
  // Good!
  if (condition)
  {
      statement;
  }
  ```

- The only exception to this rule is the opening brace of a class, enumeration, namespace or structure, in which K&R braces apply:

  ```cpp
  class Foo {
      // content
  };
  
  struct Bar {
      // content
  };
  
  namespace Baz {
      // content
  }

  enum Foobar {
      // content
  };
  ```

- lvalue, rvalue and pointer qualifiers are next to the variable name:

  ```cpp
  std::wstring &foo;
  std::wstring &&bar;
  std::wstring *baz;
  ```

- 缩进样式是 4 个空格的大制表符，您的编辑器应该使用这个 repo 的 `.editorconfig` 自动执行它。

在尝试调试主程序时，一开始可能会让人感到困惑，因为 header 中列出要启动的两个项目是 storepackage 和 desktopinstallerbuilder。只需右键单击TranslucentTB 项目并选择 “设置为启动项目”。

## 致谢

TranslucentTB 是由一个团队完成的，这个团队由许多人组成:

- [@ethanhs](https://github.com/ethanhs),
- [@sylveon](https://github.com/sylveon),
- [@MrAksel](https://github.com/MrAksel),
- [@denosawr](https://github.com/denosawr),
- [@PFCKrutonium](https://github.com/PFCKrutonium),
- 其余非核心的 [代码贡献者](https://github.com/TranslucentTB/TranslucentTB/graphs/contributors)!

感谢 [@dAKirby309](https://github.com/dAKirby309) 制作了图标，您可以在 [DeviantArt 的个人资料](https://dakirby309.deviantart.com/) 上了解更多关于他的信息。

使用的颜色选择器来自 [这篇伟大的文章](https://www.codeproject.com/Articles/9207/An-HSV-RGBA-colour-picker).
我们对它进行了一些现代化的改造，使其适应高 DPI 的显示器，速度更快 (以及硬件加速) 的绘图，并允许输入任何有效的 HTML 颜色代码或[名称](https://www.w3schools.com/colors/colors_names.asp).

我们用于安装程序截图的图片来自 [Michael D Beckwith](https://unsplash.com/photos/M-nHIqkO4-o) 的 [Unsplash](https://unsplash.com/).

我们使用 [Inno Setup Dependency Installer](https://github.com/stfx/innodependencyinstaller) 来安装 Visual C++ 的可再发行组件。

### 类似的程序

如果您正在寻找的东西不仅仅是修改任务栏，那么有几个程序。

[Taskbar Tools](https://github.com/Elestriel/TaskbarTools) 是一个用 C# 编写的类似程序。 但是它似乎没有在维护。

您可能已经从类似于 StartIsBack，Start10 和现已解散的 Classic Shell 等程序中看到了类似的半透明功能。所有这些都是很棒的程序，但我不需要替换功能，所以我写了这个。
TranslucentTB 还允许在任务栏上进行更多可自定义，具有这些程序所没有的动态 Windows，动态效果和动态启动等功能。存储和内存占用也较小。

### 开源协议

本软件是免费的，并且使用 GPLv3 协议开源，有关更多信息，请阅读 [LICENSE.md](LICENSE.md) 文件。

[Discord]: https://discord.gg/w95DGTK
[Gitter]: https://gitter.im/TranslucentTB/Lobby
