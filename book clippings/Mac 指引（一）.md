![](_resources/Mac 指引（一）image0.jpg)

我个人的习惯是周末一定要睡足，这样周一到周五都会精力充沛，可惜最近这两个周末一直奔波在外，十分疲惫，所以昨晚把支付宝的钱打足以后，便倒头昏睡过去。一觉醒来已
经天光大亮，打开手机一看，账户空空如也！妥了，于是踏踏实实去上班袅。

今晚估计很多媒体自媒体都要发文章分析光棍节和300亿的事情，在 Mac 君看来，这事和我只有半根鸡毛的关系，因为：  
1、300亿的军功章上有你的一份也有我的一份  
2、荷包又瘪了那么一点点

所以，Mac 君是断然不会凑那个热闹的，谁爱写谁去写吧。

最近 MacTalk 这个平台又增加了很多新读者，于是我再次收到了很多 Mac 相关的「新」问题，比如：

「为什么把界面右上角的红色按钮叉掉，程序还没有关闭？」  
「为什么选中文件后回车打不开文件？」  
「妈妈开始菜单不见袅！」  
……

诸如此类，做为一个同时具备人文情怀和工匠精神的 Mac
用户，看到这些问题，我表现出了不明觉厉、喜大普奔和人艰不拆的复杂情感，问题无法一一回复，所以我决定写个相对系统的「Mac
指引」的系列，给各位一个交代，今天是第一篇「就愿意挖坑怎么着吧」。

对新用户来说，用好 Mac 就三板斧：

1、理解 OS X 的基本结构和特点  
2、掌握多手势和快捷键，少量即可，多多益善  
3、用好工具，否则就算是把屠龙刀，搁庸人手里也是废铁一块，还得嫌沉

一、理解 OS X 的基本结构和特点  
  
OS X本身是基于类 Unix 内核的 Darwin 构建的，整个系统的设计思想、内核、文件系统、命令行都和 Unix 一脉相承，所以具备
Linux/Unix 经验的同学上手会非常快，也会感觉很顺畅。没有相关经验的也不用伤心，看完这个系列，你们操作起来一样会快得让自己不好意思。

1、用户目录  
  
OS X 采用了 Unix 的多用户系统，所有用户的目录都在/Users目录下，这里面的“/”，表示根目录。用户登录系统后，自己的用户目录下一般有「公共、图
片、文稿、下载、音乐、影片、站点、桌面、资源库（资源库在10.7 Lion以后的版本中已经被隐藏，通过终端可以找到）」，当然，这是 OS X
为用户做了国际化，打开终端（在 Finder 左边栏点击，应用程序–>实用工具–>终端，后续我们会介绍如何使用 Launcher 快速打开应用程序），输入l
s，你会看到真正的目录名称：Desktop、Documents、Downloads、Library、Movies、Music、Pictures、Public
、Sites 等。继续在终端中输入cd /，切换到根目录，键入ls，这样基本就可以看到Unix目录的全貌。

所以在 OS X 中，无需纠结于 C 盘 D 盘、数据与程序的分离，因为它们本身就是分离的。没有特殊需求，不需要再进行分区，所有的数据都可以放在你的用户目录
下，如果你觉得系统提供的目录不够，可以自行增加目录。关于数据文件，根据自己的喜好分门别类进行组织即可，也可以一股脑扔到
Documents（文稿）目录下，需要什么文件，通过 Ctrl + Space
快捷键呼出Spotlight，一问便知（在工具部分会做介绍）。其他图片音像文件，按照系统提供的目录放置即可，简单明了不费脑。

2、Finder 和 Dock——资源管理  
  
Finder 是 OS X 的资源管理器，原型来自早期的 Mac OS 系统，最初功能十分简陋。

我最早开始用 Mac 的时候，发现 Finder 既不支持页签，也不支持剪切，最令人发指的是，如果你想调整 Finder 的窗口大小，只能把鼠标移到窗口的右
下角进行拖拽操作。当然在我知道了事实真相后，立刻觉得这并不是最令人发指的，因为所有的程序窗口都是这么设计的！那时我就想，苹果的设计人员也有脑子进水的时候。「
有时候，我会觉得苹果标榜的“think different”的意思就是像精神病一样地去考虑问题」。

当然，系统发展到现在，除了 Finder 依然不支持剪切外，功能已经非常丰富了。Finder 提供了多种资源浏览方式，比如图标、列表、分栏、CoverFlo
w等，左边栏是个人收藏和设备信息。你可以把常用的文件夹拖放到左边栏个人收藏区域，便于快速访问。近期新增的功能包括「我的所有文件、AirDrop无线共享、Ta
g、页签」等功能。Finder 对所有文件提供了 QuickLook （快速预览）功能，想知道是什么效果的，选中一个 PDF 或 MP4，单击空格键即可。

在 Finder 中选中文件回车是对文件重命名，想打开文件可以用鼠标双击，或者快捷键 command + o。

那为什么不提供文件剪切的功能呢？如何不使用插件实现剪切操作呢？下一篇揭晓答案。

最后说说 Dock。Dock 是一个工具栏，一般在窗口的底部，相当于资源访问的快捷方式，除了对程序的快速访问，还提供了Stack（栈）的功能。把需要快速访问
的资源文件夹拖放到Dock中，在 Dock
右键点击相关文件夹，把显示内容改为网格，然后点击Dock中的文件夹，效果如下，同样可以QuickLook，也可以回车直接打开文件。

【待续】

* * *

光棍节福利：

CleanMyMac 2 是 Mac 上著名的系统清理软件。相关网址，http://macpaw.com/cleanmymac，现在  @ibuick
为国内 Mac 用户申请了一个6折优惠的购买折扣，原价257元折扣后154元。如果同时购买 Gemini
这个系统重复文件清理软件，则可以获得更多优惠。我个人是CleanMyMac 2的正版用户，推荐购买。

@ibuick 是《OS X Mountain Lion高手进阶》的作者，当然他这本书比《MacTalk**人生元编程》贵多了……你们懂的

点击{阅读原文}购买CleanMyMac 2，或者复制链接到电脑上购买。

  

[阅读原文](https://sites.fastspring.com/macpaw/instant/cleanmymac2?source=ibuick&c
oupon=ibuickcomspecialoffer10102013&campaign=ibuickcomemail&utm_source=ibuickc
om&utm_medium=emailoffer&utm_campaign=affiliate_ibuickcom_ibuickcomemailoffer#
wechat_redirect)

