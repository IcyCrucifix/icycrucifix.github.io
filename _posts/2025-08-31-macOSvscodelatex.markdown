---
layout:     post
title:      "教程·macOS环境下VScode配置LaTeX"
date:       2025-08-31 00:03:00
author:     "Jeffery"
header-img: "img/VScodeBG.jpg"
catalog: true
tags: [macOS, VScode, 教程]
---

## Pt.0

***如果你并不知道LaTeX是什么：***

这里是官方介绍。[Wikipedia](https://en.wikipedia.org/wiki/LaTeX) | [Baidu](https://baike.baidu.com/item/LaTeX/1212106)

**如果你并非macOS用户：**

这里有一份也许更加适合你的教程：[Latex：超详细新手安装latex：TexLive环境+VScode编辑器--啥都发的小c](https://www.bilibili.com/video/BV1y8411P7qs?vd_source=a788835c5f092ff579ff6cbc4b103d78)

## Pt.1 MacTex

如果你也有学习过小c的视频，那你大概率会发现她视频里所说的ISO文件在macOS上想像她那样顺畅打开几乎不可能。

*所以换一种方法。*

首先，你需要去下载MacTex。[链接一站直达官网](https://www.tug.org/mactex/)

完成后，将刚刚下载下来的MacTeX.pkg点击并Install即可。

## Pt.2 VScode方面

在一切开始之前，你首先需要下载VScode。如果你并没有，[请点击这里跳转官网下载](https://code.visualstudio.com)。

这里不多赘述关于VScode的基础设置，按VScode自己的引导走即可。

下载完、打开并完成基础设置后，你需要安装LaTeX 及 LaTeX Workshop两个扩展。

点击VScode左列工具栏从上往下数第六个（四个方块）即可进入扩展商店。如下图搜索LaTeX并把**前两个扩展**分别点击安装即可。

![VScodeLaTeXextentions](img/VScodeLaTeXsettings.png)

### 到这里实则基础配置就已经完成了

## Pt.3 试试看

在以上步骤全部完成后，打开VScode并新建一个.tex文件

如果你完全没有接触过LaTeX语法，可以复制输入以下代码：

    \documentclass[]{report}

    \title{Writing with LaTeX}
    \author{Your Name}
    \begin{document}

    \maketitle 
    \textbf{Hello LaTeX!}

    \end{document}

然后在你的VScode右上方一列图表中找到「查看LaTeX PDF文件」

即。下图中左4


或者直接按option+command+V也可以。

这时候你的VScode右侧应该会出现一个和你文件名相同的.pdf，第一也应该是标题+作者+日期。下滑后可以看见Hello LaTeX字样。

如果你也得到了此结果，那么恭喜你配置成功。

## End
