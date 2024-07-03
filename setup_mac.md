## 安装仓颉工具链

在以上“精选项目”板块点击进入“CangjieSDK-Mac-Beta”项目页面，可以看到下图中的文件列表。

<img src="https://raw.gitcode.com/Cangjie/CangjieCommunity/attachment/uploads/89102e18-05af-4bb2-9b4a-8f2b582e2431/0.png"  width="50%">

仓颉工具链适配了 x86_64 和 m 系列芯片，根据您所使用的设备情况下载相应的工具链包。

在适当位置解压，您将看到下图中的文件列表，其中的 `envsetup.sh` 脚本用于配置仓颉运行环境，但当前 Mac版本工具链没有签名，未避免系统误报，我们需要用文本编辑器打开 `envsetup.sh` 文件，在 39 行之后添加一行内容： `xattr -dr com.apple.quarantine ${CANGJIE_HOME}/*`，参见下图中有背景高亮的部分。



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