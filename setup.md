# 开发环境搭建指导

在[项目主页](https://gitcode.com/Cangjie)的“精选项目”板块，给出了仓颉通用工具链的三大平台版本，以及仓颉 VSCode 插件（各平台通用，支持工程创建、语法高亮和 LSP 等）

<img src="https://cdn-img.gitcode.com/ba/aa/53b110a391aafc08eecd643471f645c9576312673bfe6ce27b22d9e3ccfa9b58.png"  width="50%">

下面**以 Windows 平台为例**，介绍仓颉开发环境的搭建方法，Mac 平台请参阅：[Mac 开发环境搭建指导](setup_mac.md)

## 安装仓颉工具链

在以上“精选项目”板块点击进入“CangjieSDK-Win-Beta”项目页面，可以看到下图中的文件列表。

<img src="https://cdn-img.gitcode.com/db/ee/0306dbeedfe83fba9aa3f24d08c5c02a7dc38ec9ad3f9bc7adde13e41a0949b7.png"  width="50%">

这里有两种格式的安装包，您可以根据需求或使用习惯选择下载。

### exe 安装包

如果我们下载了 `exe` 格式的安装包，则直接双击执行，根据提示点选操作，很快就能完成安装（过程中关于 `CANGJIE_HOME` 和 `PATH` 的设置，建议保持默认选项，否则在使用前还需要手动配置环境变量）。

<img src="https://cdn-img.gitcode.com/db/de/2d73bde7e9af8211b80b77c49ee544dc0ba4d6f91d16be9de9222f27cd91ff45.png"  width="50%">

为了验证工具链是否正确安装，请在命令行窗口中执行 `cjc -v`，如果输出了版本号，说明此工具链可用。

<img src="https://cdn-img.gitcode.com/db/fc/db774f1c9024c169a7ae79a665bd630d24e00c4c8b01c40174ba3956302533db.png"  width="50%">

### zip 安装包

如果我们下载了 `zip` 格式的安装包，请解压到适当位置，下图是解压后的目录内容。

<img src="https://cdn-img.gitcode.com/be/af/b1134eaf75c9eead572df080e6773849a25c814efc5604d893efa0d7eaf92072.png"  width="50%">

在需要使用仓颉工具链的环境中，请执行以上 `envsetup` 脚本（根据命令行环境选用一种脚本格式，如在 powershell 环境，可执行 `envsetup.ps1`），它将临时配置相关环境变量、让当前环境可以引用仓颉工具链。

<img src="https://cdn-img.gitcode.com/af/ec/0a692fe3011c5e340afed37842c82edd3410fc0a44062b3d727acd2eb09356a1.png"  width="50%">

这种安装配置方式，不会影响系统全局环境，方便实现多版本共存/切换等。

## 安装仓颉 VSCode 插件

现阶段，使用仓颉通用版本做 PC 或服务器程序开发，推荐使用 VSCode 作为 IDE。

在主页`精选项目`板块点击进入`CangjieVScodePlugin-Beta`项目页面，可以看到下图中的文件列表。

<img src="https://cdn-img.gitcode.com/ed/ea/e4d0e4aad3096c79d1994029db147e8bf663aa08b76c42bdf9bb24ccc98afc80.png"  width="50%">

下载其中的 `Cangjie-vscode-0.51.4.tar.gz` 压缩包，解压后会得到一个名为 `Cangjie-0.51.4.vsix` 的文件。

打开 VSCode 软件，按下图中标记的位置和顺序点击。

<img src="https://cdn-img.gitcode.com/bf/cb/317bfc5973629533b738fac477698931799695de80047339c2dd2690c3aa208d.png"  width="50%">

在弹出的窗口中选择刚刚解压出的 `vsix` 文件，并点击 `Install` 按钮。

<img src="https://cdn-img.gitcode.com/de/bd/51de2bdb1a39f984ed5f8029646cc5b132de1ded5cc561a424c6478f8ed50a49.png"  width="50%">

随后就能在 VSCode 插件列表中看到已安装的仓颉插件。

<img src="https://cdn-img.gitcode.com/df/bf/63d4f7060b52fd9f5e39a3391650b973c0f8e813c551da10006ad6a143fde831.png"  width="50%">

这样，在 VSCode 中编写仓颉程序，就具备了语法高亮等功能支持。

<img src="https://cdn-img.gitcode.com/fd/dd/8f8d85dd35cf954ee246ee570f1c260471f7ac3ebc7d26aaa7d90c82848349c9.png"  width="50%">