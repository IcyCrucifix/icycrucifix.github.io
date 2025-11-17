---
layout:     post
title:      "解决方案·如何通过Surge简单完成VPN的应用分流以同时访问校园网站和ChatGPT"
date:       2025-11-16 20:09:00
author:     "Jeffery"
header-img: "img/HKU Grand Hall.HIF"
catalog: true
tags: [HKU, 解决方案]
---

> 本来想用Shadowrocket的，然而发现我好像不知道怎么用小火箭做分流。

## 如果你不知道：为什么要分流？

众所周知，ChatGPT等较为好用的GenAI工具即便是在香港也不能直连访问，需要翻墙。然而翻墙后经常出现无法访问Moodle, .hku.hk后缀等网站的问题。对此（我个人认为）最好的解决方案就是进行分流，使ChatGPT/Atlas能够通过代理路线访问，同时让学校网站保持原有的直连状态。

此处以Surge举例。因为别的我不会。

## Surge：

这里是Surge的官方网站 (macOS版本）： [Surge](https://nssurge.com)

***Windows系统也有，反正知道是这个Surge别找错就好了。***


## 操作：

**如果你不喜欢看图文喜欢看视频，这里有一个老师的视频可供参考。内容基本一致，因为我也是学他的。**
[点这里](https://www.youtube.com/watch?v=Pbwkq5X0nTU)

### 0. 节点

如果你没有节点，我个人在用[flyingbird](flyingbird.pro)

在你的节点网站中也许可以找到Surge复制配置文件一类的选项，如果有 请复制。

### 1. Surge部分

在你下载好Surge并按指示完成初步Setup后，可以这样安装配置：

如图，点击更多-配置

![SurgeMore](/img/in-post/SurgeMorePage.png)

![FromURL](/img/in-post/SurgefromURL.png)

将你刚刚复制的配置粘贴至此，然后让一步步继续添加即可。

如下图，双击后点击应用。

![ApplyURL](/img/in-post/SurgeURLapply.png)

然后你便成功添加了你的节点配置。

### 2. 如何分流

分流的本质直白些讲就是对不同的网址设立不同的规则，让他们能够走不同的路径。核心在于修改/添加规则。

如果你的节点是自建节点，那么你可以直接边栏点击规则，左下角加号添加规则。页面如下图

![SurgeAddRules](/img/in-post/SurgeRuleSet.png)

**但如果你是订阅制节点，那你将无法这么修改规则。**

对于订阅制节点，最简单的处理方式：

对于macOS，如下图这样在Finder中打开配置：

![ManualRuleSet](/img/in-post/SurgeManualRuleSet.png)

或者直接选择用文本编辑器打开，像这样更改规则：

![SurgeChangeRules](/img/in-post/RuleChangesSurge.png)

在**[Rule]**下增加规则即可。例如我这里写了：

    DOMAIN-SUFFIX,hku.hk,DIRECT
    DOMAIN-SUFFIX,youtube.com,DIRECT

Domain Suffix意为所有有这些后缀的网站均遵循这条/些规则，Direct为直连。

完成这部设置后保存你刚刚编辑完的配置文件即可。

然后（也许需要？）重启一下Surge，然后在边栏的概览中打开系统代理&增强模式。

**然后你就可以一边使用Atlas一边流畅访问学校网页了！**
