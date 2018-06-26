---
title: 氧 OS 也能使用公交卡
date: 2018-05-15 09:32:23
categories:
  - Tips
tags:
  - 一加
  - 氧OS
  - 公交卡
---

{% note info %}
本文最后更新于 2018年5月24日 可能会因为没有更新而失效。如已失效或需要修正，请留言！
{% endnote %}

两个月前，我换了一加 5T，算是 48 年入国军了吧，不过等于 7 看样子会有刘海，无爱，放弃；而 5T 的 835 性能又很足够，造型也很讨我喜欢。

买来后果断刷了氧 OS 使用，确实没让我失望，内置 Google 框架，使用很流畅。前两天，因为想尝试着体验一下全球上网和公交卡功能，刷成了氢 OS 8.1 稳定版，但是是 dirty flash。开机后检查各项软件，果然，电话闪退无法使用。在设置中找边所有地方也没找到全球上网，不过还好，卡券里的公交卡功能可用，没算是白刷。但是这修改过的氢的界面用起来还是各种别扭，还预装了许多中国特色软件。于是打算把公交卡功能搬到氧 OS 中使用。

在氢中提取了一加商店，在刷回氧以后，可以装上，但是只能下载不能自动安装，需要在手机目录中找到 ``apk`` 文件手动安装。
按照常规操作，安装卡券和一加公交卡插件以后，在负一屏添加卡券部件，打开之后，点击加号，就会开始扫码添加会员卡。但这不是我们想要的，氢中点击加号有公交卡选项，而氧中屏蔽了这一入口。这时有两个方法可以解决。<!--more-->

## 方法一 ADB

打开 USB 调试，在 ``adb.exe`` 的文件夹中打开 ``PowerShell`` 或者 ``Command Line``，输入 ``adb shell`` 之后手机提示授权。
{% img /uploads/2018/05/Screenshot_20180524-131155.jpg 540 %}
授权之后电脑端提示变为 ``OnePlus5T:/$``。
![](/uploads/2018/05/adb.png)
输入 ``am start -n cn.oneplus.wallet/cn.oneplus.wallet.activity.NewCardActivity``，回车，此时在手机上就打开了添加公交卡的界面。
![](/uploads/2018/05/shell.png)
{% img /uploads/2018/05/Screenshot_20180524-131302.jpg 540 %}

## 方法二 QuickShortcutMaker

此方法最为简单快捷，无需借助电脑。
安装打开 QuickShortcutMaker，找到公交卡，选择第一项，尝试运行即可打开开卡界面。
{% img /uploads/2018/05/Screenshot_20180531-142204.jpg 540 %}

在成功开卡之后，在负一屏就能看到已经开启的公交卡了，点击卡片可以直接充值。
{% img /uploads/2018/05/Screenshot_20180515-100212.jpg 540 %}
{% img /uploads/2018/05/Screenshot_20180515-100440.jpg 540 %}