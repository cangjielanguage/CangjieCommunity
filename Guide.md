# 一篇文章带你了解仓颉所有开发套件获取及安装

## 1 概览

**仓颉编程语言通用版本(服务端等领域开发)**

[仓颉官网下载链接](https://cangjie-lang.cn/download)（STS版本通道已经开放下载）

[仓颉官方文档](https://cangjie-lang.cn/docs)（STS版本通道文档已经公开）

**HarmonyOS NEXT 仓颉语言开发者预览版(鸿蒙原生应用开发)**

[HarmonyOS NEXT 仓颉语言开发者预览版申请链接](https://developer.huawei.com/consumer/cn/activityDetail/cangjie-beta/)

[DevEco Studio NEXT Developer Beta2-Cangjie Plugin 下载链接](https://developer.huawei.com/consumer/cn/download/) （HarmonyOS NEXT 仓颉语言开发者预览版申请通过后可见）

## 2 仓颉编程语言通用版本开发环境搭建（以 Windows 平台为例）

### 2.1 下载 VScode 以及 仓颉语言 VScode 插件

IDE下载这里不做赘述，在仓颉官网中下载[仓颉VScode插件](https://cangjie-lang.cn/download)，并解压缩

![image.png](https://raw.gitcode.com/Cangjie/CangjieCommunity/attachment/uploads/07ff8af9-4ad3-4771-88d9-309dfad7e4ea/image.png 'image.png')

### 2.2 下载仓颉编程语言通用版本SDK

在仓颉官网中下载[仓颉SDK](https://cangjie-lang.cn/download)，并解压缩

![image.png](https://raw.gitcode.com/Cangjie/CangjieCommunity/attachment/uploads/2f1f48b7-737b-409e-ae35-35512a2cffba/image.png 'image.png')

### 2.3 配置环境

![配置环境](picture/03.png)

![配置环境](picture/04.png)

路径层次如下图：

![配置环境](picture/05.png)

### 2.4 初始化工程

`Ctrl + Shift + P` 打开VScode功能搜索栏，输出 `Cangjie`，选择 `Create Cangjie Project`

![配置环境](picture/06.png)

根据提示初始化仓颉项目（CJNative），如下图名为 demo 的仓颉工程

![配置环境](picture/07.png)

配置文件字段详细说明详见[仓颉编程语言通用版本官方文档](https://gitcode.com/Cangjie/CangjieDocs/overview) （通过申请后可见）《仓颉语言工具使用指南》-仓颉语言命令行工具使用指南-包管理工具-模块配置文件说明

![配置环境](picture/08.png)

### 2.5 编译运行

右上角三角按钮编译运行，或使用`cjpm run`运行

![配置环境](picture/09.png)

恭喜您编译运行了第一仓颉程序

### 2.6 相关资源

[仓颉编程语言入门教程](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101718903607800132)

## 3 仓颉鸿蒙应用开发环境搭建（以 Windows 平台为例）

### 3.1 下载 DevEco Studio NEXT Developer Beta2 以及 DevEco Studio NEXT Developer Beta2-Cangjie Plugin.

IDE下载这里不做赘述，点击[DevEco Studio-Cangjie Plugin Beta2 下载链接](https://developer.huawei.com/consumer/cn/download/) （HarmonyOS NEXT 仓颉语言开发者预览版申请后可见）

![配置环境](picture/10.png)

### 3.2 配置环境

打开 DevEco Studio 选择 `Customize`，选择 `All settings...`

![配置环境](picture/12.png)

选择 `Plugins`，选择 `install Plugin from Disk...`

![配置环境](picture/13.png)

选中下载的 DevEco Studio NEXT Developer Beta2-Cangjie Plugin 压缩包，进行安装

![配置环境](picture/14.png)

安装结束后点击 Restart IDE，完成安装

![配置环境](picture/15.png)

### 3.3 初始化工程

回到创建工程界面，选择 `Create Project`

![配置环境](picture/11.png)

选择 `[Cangjie]Empty Ability`

![配置环境](picture/16.png)

工程初始化成功

![配置环境](picture/17.png)

### 3.4 编译运行

手机系统镜像要求：NEXT.0.0.31及以后
IDE模拟器已支持仓颉

### 3.5 相关资源

[HarmonyOS NEXT Developer Beta2 - 仓颉（仓颉鸿蒙应用开发文档）](https://developer.huawei.com/consumer/cn/doc/cangjie-guides-V5/2_1_u5feb_u901f_u5165_u95e8-V5)（HarmonyOS NEXT 仓颉语言开发者预览版申请后可见）

[仓颉UI开发入门课程](https://developer.huawei.com/consumer/cn/training/course/slightMooc/C101720786490569532)（HarmonyOS NEXT 仓颉语言开发者预览版申请后可见）