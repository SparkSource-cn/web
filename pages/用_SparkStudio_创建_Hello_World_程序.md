---
layout: page
title: SparkSource Tutorial
description: examples that teaches how to use SparkSource
---

想必大家都已经从
[试用版下载](http://www.sparksource.cn/html_ch/trial_download.html)
下载了 Spark Studio 的试用版。可是，这是一个创新的程序，虽然我们做出了非常易学的
设计和流程，还是有很多人提问：到底 SparkStudio 该怎么用？

今天，我们就手把手地和大家一起创建我们自己的第一个程序：Hello Wrold!

我们以 GNU/Linux 版本为例。通过 SparkSource 官网下载的文件是

>spark_studio_linux.zip

文件不大，解压之后有三个文件：

```
create_shortcut.sh
spark_studio_installer.deb
spark_studio_installer.sh
```

第一个文件是创建桌面快捷方式的脚本，我们先不用管。第二个文件是我们熟悉的软件包，
其中包含了 Spark Studio 的全部内容。原则上软件包可以使用以下命令之一安装：

```
1. kpkg -i spark_studio_installer.deb
2. aptitude install spark_studio_installer.deb
```

不过，为了便于管理，我们提供了第三个安装脚本。在安装之前先修改权限，打开终端，进
入刚才的解压目录，执行命令

```
sudo chmod 755 spark_studio_installer.sh
```

然后执行命令

```
./spark_studio_installer.sh
```

上面这条安装命令，会把 Spark Studio 安装在指定目录，并把其执行路径加入到环境变量
中。执行命令时，会需要输入 sudo 用户名密码。安装完成之后，在任意路径下输入

```
SparkStudio
```

就可以看到 SparkStudio 的界面，Spark Studio 的两个窗口：主窗口和控件窗口。
图1-SparkStudio 主窗口
图2-SparkStudio 控件窗口

在主窗口 -> File -> Create，会出现一个 Project Information 弹出窗口
图3-project infromation 弹出窗口
在此窗口可以点击输入区域选择项目存放路径，手动输入项目名称、主题和皮肤。点击 OK
确定之后，项目文件结构就确定了。这时，我们就可以在此项目下构建我们的第一个人机交
互程序——你好，世界！

在控件窗口 -> Text -> click + sign on the top，我们添加两个字符显示界面
一个是“你好，世界！”（Hello，world！）
一个是“显示”（show）

主题和皮肤建立项目时已经设置为默认，作为示例，这里就不改了。不过，这些时随时可以
改动的。字体和颜色也是可以添加和修改的。

更多内容，请点击 Spark Studio 的 Help -> Beginner，这里有 Hello World 的详细步骤。
祝你的世界更美好！

请同时参看：
 - [在 SparkSource 中运用 Shader](在_SparkSource_中运用_Shader.html)
 - [SparkSource 图形引擎示例](SparkSource_图形引擎示例.html)
 - [SparkSource 的图形引擎助你高效开发 3D 应用](SparkSource_的图形引擎助你高效开发_3D_应用.html)
