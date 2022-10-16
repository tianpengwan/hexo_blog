---
title: 思维导图软件幕布导出Markdown【效率工具指南】                                
date: 2022-10-11 15:03:00               
tags: [幕布,思维导图软件,Markdown,插件]                                                                                   
---  

本文首发于微信公众号「[效率工具指南](https://mp.weixin.qq.com/s/ZWxbw10b_I-M_Q0stszXYw)」                 
文/彭宏豪      


Hello 各位好，我是小豪。    

继之前写过[石墨文档批量导出](https://mp.weixin.qq.com/s?__biz=MzAxMjY0NTY5OA==&mid=2649920142&idx=1&sn=88f4acce321bb7917a7313c85e6148d8&chksm=83a896a3b4df1fb53feead145913aba5803f69bf5a37504f1c3c901caf0c424dc7e293e4b4ec&token=237325951&lang=zh_CN#rd)之后，今天我想对许久没更新的思维导图软件「幕布」动手了——**从幕布中批量导出 Markdown 文件**，预防之后幕布可能关停带来的数据丢失。         

先来看一下从幕布导出前后的对比：   

下图左侧是导出前的幕布文件，右侧是导出后在 Markdown 编辑器 MWeb 打开的 Markdown 文件。   

对比了导出前后的文件，发现导出的部分 Markdown 文件存在**文本丢失**的问题，这个问题会出现在某一行文本带有**粗体**样式的时候，导出的 Markdown 只保留了粗体样式中的文本。          

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/10/11/16654635347301.jpg)

不过我发现，**文本丢失的问题，目前只出现在创建时间比较早的文档上**，我猜测是在幕布推出 Markdown 功能之前创建的文档，导出时所在的行如果带有粗体样式，就会发生内容丢失，而如果是之后创建的文档，就不会出现这个问题。          


上面在幕布中创建的读书笔记，是纯粹的文本内容，为了更全面地了解这个导出工具的能力，我还测试了**导出带有图片**的幕布文件。   

下图是带有图片的幕布文件导出前后的对比：  

导出的 Markdown 文件会生成一个压缩包，里面带有原文件中附带的图片，因此使用 MWeb 打开的 Markdown 文件(下图右侧)，图片也能正常显示，但有个小小的不足——幕布中插入的 gif 动画会变成一张静态的 jpg 图片。             

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/10/11/16654657992107.jpg)

总体而言，我对这个导出工具还是比较满意的，虽然多少存在一些问题，但能把我放在幕布中的大部分内容导出，我就很满意了。    

## 幕布导出器 - Mubu Dumper  

前面用到的幕布批量导出 Markdown 工具，就是下图的浏览器插件：**幕布导出器 - Mubu Dumper**。

这个插件目前只上架到了 Chrome Web Store，还没上架 Edge 的插件商店。        

有意思的是，我还留意到了这个插件名称下方的域名 `xmind.app`，用过国内另外一款思维导图软件 XMind 的朋友，想必对这个域名并不陌生。   

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/10/11/16654667162953.jpg)

浏览器插件「幕布导出器 - Mubu Dumper」安装地址：   
https://chrome.google.com/webstore/detail/%E5%B9%95%E5%B8%83%E5%AF%BC%E5%87%BA%E5%99%A8-mubu-dumper/nhpebeoohnmbgeigmojaebjfliekikkb/related 


安装插件后，在浏览器打开网页版的幕布，点击浏览器右上角的插件图标，在弹出的面板，可以选择导出 所有文件、单个文件夹或是单个文件。       

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/10/11/16654678724168.jpg)

勾选☑️ 文件之后，点击下方的「导出」按钮，在弹出的二级菜单，可以选择导出的文件格式：  

默认导出 xmind 格式的文件，不过下方也提供了更通用的 Markdown 格式。      

这里之所以提供了 Markdown 格式，不确定是不是只提供 xmind 格式的话，会让人看起来是在「明目张胆」地撬幕布的墙角，所以出于体面一些的考虑，这里也提供了更通用的 Markdown 格式。     

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/10/11/16654683129332.jpg)

不过，撬别人墙角，在国内很多产品都可以看到，不独有 XMind 一家：   

* 国内很多模仿 XMind 的思维导图软件：支持导入 xmind 文件    
* 国内很多模仿 Figma 的设计软件：支持导入 Figma 文件      
* 国内很多模仿 Visio 的绘图软件：支持导入 Visio 文件    

不仅如此，有些产品的「帮助文档」中，还明目张胆地列出了如何将其他产品的文件导入自己产品的方法，你说会有多少人注意到呢？       

绝大多数用户都不会在意这些事情，因为这些下三滥的操作多了，原本不正确的事情也会变成是理所当然。   

![](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2022/10/11/16654689727150.jpg)


看到这里，你说：       


情怀有用吗？    
体面有用吗？
体面能当饭吃吗？   
产品理念有用吗？     
团队气质有用吗？     

在没有赚到钱让产品或团队可持续地活下来，扯那么多虚的，有用吗？    

少谈情怀，多干正事。        



## 欢迎关注     

以上，就是本次想和你分享的内容，希望能够对你有一点帮助。     

![公众号：效率工具指南](https://article-picbed-1302715071.cos.ap-guangzhou.myqcloud.com/2021/05/28/gong-zhong-hao-wei-bu-er-wei-ma-dailogo.png)       

