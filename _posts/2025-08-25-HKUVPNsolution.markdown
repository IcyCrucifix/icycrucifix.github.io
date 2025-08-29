---
layout:     post
title:      "解决方案·HKUVPN遵循官方指南设置依然无法登陆"
date:       2025-08-29 11:09:00
author:     "Jeffery"
header-img: "img/HKU Grand Hall.HIF"
catalog: true
tags: [HKU, macOS, Mac]
---

> 此文的成功解决是在macOS系统下，Windows/iOS等系统可参考解决方案，但也许会有少量差异（欢迎有Windows Linux Android系统机器的同学找我联系补充..感谢）

## 如果你不知道：HKUVPN的作用是什么？

HKU有部分系统，例如Faculty of Science相关课程选课时可能会需要的的Science Online Application System (OASS) 仅有HKU校园网可以完全访问。对于不在校园内的学生&教职员工而言，学校提供的解决方案便是让其连接HKUVPN，使学生在校外也能够访问这些系统

## 学校方面：

这里是HKU官方的操作指南： [HKUVPN User Guide](https://its.hku.hk/kb/user-guide-on-making-hkuvpn-connection-with-mfa/)

***实则漏洞显著***

如果你依照步骤下载了Cisco并尝试用connect+PIN登陆，你也许会经历无数次「登陆失败」。虽然系统显示也许是账号/密码错误，但这本来也不是真正的问题。

## 补全操作：

User Guide中把Cisco的登陆这一步放在了Microsoft Authenticator 前，然而如果你真的不先搞定Authenticator，你就真的（大概率）只会登陆失败。

真正需要做的事是在登陆前先去Microsoft Authenticator的App（或其他端。我个人使用的是手机App）先去登陆自己的connect邮箱。也许会各种卡，显得像你没成功登陆进去。但只要你清后台重进之后你的uid@connect.hku.hk邮箱在Authenticator中即可。

这时候你再去登陆Cisco，就可以直接登入下一步，让你填写一次性代码。此时你再去Authenticator App中点入你的帐号，把你的一次性密码代码填入即可。

**然后不出意外你就可以连上了！恭喜！** 
