---
title: Mac电脑虚拟机Parallels Desktop安装Windows系统【效率工具指南】     
date: 2022-11-6 13:35:00               
tags: [Mac,Windows,Win10,macOS]                                                                               
---


本文首发于微信公众号「[效率工具指南](https://mp.weixin.qq.com/s/25I-M1tRAoxGRxl60PTseg)」
文/彭宏豪    

Hello 各位好，我是小豪。   

上周尝试给吃灰多年的 Kindle 刷安卓系统，照着网上的教程，其中有一个步骤，不得不在 Windows 系统上操作……  

因为这样，我也不得不在磁盘「**寸土寸金**」的 Mac 电脑上安装了 Windows 系统，因此今天的这篇文章，来简单分享一下 Mac 电脑安装 Windows 系统的方法。  

下图是虚拟机软件预估的 Win10 系统会占用的磁盘空间大小——21.47 GB，虽然我有 1 TB 空间，但还是肉疼。    


![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16673502888841.jpg)


我在 Mac 电脑上安装 Windows 系统的方法是：先安装虚拟机软件 Parallels Desktop，再在虚拟机软件中安装 Win10 镜像系统。   

除了这种方法，应该还有其他的方案，比如 Intel 芯片的电脑还支持的「双系统」，即在启动电脑时，可选择要使用的操作系统。   

不过我图方便，还是用了更为简单的「虚拟机 + 镜像系统」的方案。     

在开始之前，需要准备好 2 个东西——    

* 虚拟机软件 Parallels Desktop，可从官网下载，软件提供免费使用，过期后就需要付费，价格还比较高，当然你也可以从一些其他渠道下载（懂的都懂）；                
* Win10 镜像系统文件，格式为 iso，可从 msdn itellyou 下载。  

msdn itellyou 网址：   
https://msdn.itellyou.cn/      


下载 Parallels Desktop 后，就和普通的软件一样安装就好啦。    

打开 Parallels Desktop，选择「安装 Windows 或其它操作系统」。    

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677027509849.jpg)

如果你已经提前下好 Win10 镜像系统文件，Parallels 会扫描到本地已有的 iso 文件，并给出下图的提示「已找到安装映像」。     

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677028347619.jpg)

之后 Parallels 还会询问，你想把安装的 Windows 用于哪种用途，这里我选择「**生产力**」，猜测它是会根据我们选择的用途，给出不同的分配 Mac 磁盘空间和运行内存的方案。      

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16673500675834.jpg)

接着选择存放 Win10 系统的位置，名称和保存位置按默认的即可，记得勾选底部的「**安装前设定**」，否则无法顺利进入下一步。           

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16673502888841.jpg)


在打开的窗口，点击「配置」，选择「硬件 >> CPU 与内存」，选择「高级」，在弹出的窗口，将「虚拟机监控程序」更改为「Parallels」。    

后面的步骤我就没有截图了，按照提示进行操作，应该就能顺利安装 Win10 系统啦。       

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16673503936012.jpg)

## 虚拟机无法连接网络     

在 Parallels 虚拟机安装好 Win10 系统后，不确定是不是因为我用了特殊版的虚拟机软件，每次打开 Win10 系统都会遇到下面的提示：  

> 您的虚拟机将继续正常运作，但将无法连接网络。  

说人话就是，你在虚拟机中安装的 Win10 系统不能上网！  

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16676379886646.jpg)
   
对于这个问题，其实也有对应的解决方法：   

打开 Mac 的「访达」，点击顶部菜单栏的「前往」选项卡，选择「前往文件夹」。    

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677046261873.jpg)

在打开的窗口，粘贴下面的路径，打开 Parallels 安装位置的文件夹。     

`/Library/Preferences/Parallels/`

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677047183972.jpg)


打开的文件夹下有一个名为 `network.desktop.xml` 的文件，将这个文件**拖拽复制**一份到 Mac 桌面，然后使用 Mac 内置的「文本编辑器」或者电脑上安装的代码编辑器，例如 **VS Code** 打开复制的文件。     


![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677048535212.jpg)

打开文件后，找到 `<UseKextless>` 这一行代码，将中间的数字 -1 更改为 0，保存文件。     

接着将 Mac 桌面经过修改的文件，拖回到 `/Library/Preferences/Parallels/` 文件夹中，**替换已有的同名文件**。    

此时再重新打开虚拟机 Parallels，运行 Win10 系统，应该就不会再弹出「无法连接到网络」的提示啦。      

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677050328010.jpg)

✅ 虚拟机 Win10 系统可以正常连接到网络的标志： 

Win10 系统右下角的小电脑不会出现一个红色的叉号；或是打开 Edge 浏览器，可以正常访问网页。       

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16677055233076.jpg)


## 另外一个问题

除了前面的问题，我使用 Parallels 还遇到了另外一个错误提示：

> 无法将虚拟摄像头连接到 Win10 

这个问题目前我还没找到解决方法，而且我暂时也没有在虚拟机的 Win10 系统连接摄像头的需求，因此把这个问题搁着，也没啥大碍。    

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/11/06/16676385996234.jpg)


## 欢迎关注     

以上，就是本次想和你分享的内容，希望能够对你有一点帮助。     

![公众号：效率工具指南](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2021/05/28/gong-zhong-hao-wei-bu-er-wei-ma-dailogo.png)      


