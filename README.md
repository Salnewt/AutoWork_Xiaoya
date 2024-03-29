# AutoWork_Xiaoya 

小雅文档类自动刷课程序（WHUT登录）

可以实现对于[`小雅`](https://ccnu.ai-augmented.com/app/jx-web/)平台的`mp4`、`pdf`、`ppt`、`pptx`类型的任务完成自动化刷课任务，自动完成当月所有任务，旨在减少不必要的机械性重复操作。只进行了WHUT的登录界面适配，有需要的可以自取源代码修改。

- 实现：`Python 3.9.6 + pwinput + DrissionPage 4.0.0b20`
- 运行环境：`Windows`
- 不需要额外配置环境，可直接运行。
  - 其他平台可以下载`.py`源码自行编译

仓库包含内容：

1. 一份[Python程序源代码](AutoWork_Xiaoya.py)。
2. 一个从小雅网站上获取的favicon.ico [图标](favicon.ico)
3. 一份使用 pipenv + pyinstaller 打包的dist[文件夹](dist)

## 内容列表<!-- omit in toc -->
- [背景](#背景)
- [安装](#安装)
- [使用说明](#使用说明)
- [写在后面](#写在后面)

## 背景

可以用一张表情包来阐述整个工作的起因：

![怎么个事](why.jpg)

而当我去检查过期任务时，发现是一堆视频观看作业。就很不理解，为什么我上课听懂了的东西，需要我在课下再刷一遍视频，进行重复性相当之高的机械性操作，他甚至还会计入平时分。

而这类机械性操作的任务也会在平时分中占有不小的地位，也是让人十分费解的一点。因而便有了制作一个网页自动化程序来完成平台诸如mp4、pdf等根本不需要脑力付出的任务的完成。


工具目标：

1. 实现小雅账户的自动登录。
2. 自动检索任务并过滤已过期任务，并自动完成。
3. 对`mp4`任务进行自定义倍速播放，`pdf`、`ppt`、`pptx`任务进行自动点击完成。

## 安装

建议下载`Download.rar`压缩文件包
或者下载`dist`文件夹下的内容

解压后保证`exe`可执行文件与`configs.ini`、`setInfo.ini`在同一文件夹下。

## 使用说明

若正常下载，直接运行即可启动。

未对程序配置可视化窗口，启动后只有命令行窗口，会有相应的文本提示。

使用提示：
- **登录配置**：默认情况下并未设置账号密码，可以修改`setInfo.ini`中对应条目，来设置。但并未对ini文档进行额外的加密处理，因而存在一定的账号泄露风险。
- **建议**：只在`setInfo.ini`中填入`倍速`与`ID`，每次手动输入密码，可以提高安全性。
- **浏览器配置**：如果使用的并非Chrome浏览器，而是其他Chromium浏览器，如Edge，需要在`configs.ini`中修改`browser_path`一栏为自己浏览器的目标地址。**并非快捷方式地址**。具体操作在程序启动后无法找到浏览器会有提示。
- **浏览器弹窗问题**：程序并未配置灵活的对弹窗的提示，因而各种弹窗，需要手动处理，例如：
  - 首次启动的各种浏览器提示窗
  - 小雅平台未绑定验证的提示窗
- **密码错误问题**：当密码错误时，程序会在输入密码界面停留一分钟左右时间，等待用户完成输入。
- **过期任务**：在输入完账号密码之后会需要确认是否需要处理过期任务，输入除了`y/yes (大小写无所谓)`以外的的任意结果则表示不处理。

## 写在后面

一些废话而已，主要就是出事不负责，且用且珍惜，如果被追责我就删了【

小程序罢了，想着顺便试一下github的仓库怎么用，于是上传一下，小规模使用应该不成问题，如果有幸被传播【笑】~~【偷偷用别声张~~

这种随便来个计科的人都能写的东西，相信做的人应该很多，只是我想上传一下罢了。【【如果到时候小雅又整了什么反自动化机制那么没办法

鉴于选择学校那边不清楚华师的界面是什么情况，就没做适配。

如果发现bug，能联系上我的话，我会试着改改，或者源文件也在里面，也可以自己着手修改一下，也不难【
