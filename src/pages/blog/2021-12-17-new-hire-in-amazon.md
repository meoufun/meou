---
templateKey: blog-post
title: New Hire in Amazon
date: 2021-12-17T03:37:43.528Z
description: New Hire in Amazon
featuredpost: true
featuredimage: /img/amazon-badge.png
tags:
  - Amazon
---
入职 Amazon 差 13 天就满半年了，总体上来说还是符合预期。单就可以带薪学英语和 transfer 到海外这两点就可以忽略其他的劣势。目前还在家中办公，基本上上午 10 点上班，下午 6 点下班，有时会早起开会，不过这在国际公司中也比较常见。在入职的这段时间里，总共还额外放了 3 天假，其原因嘛，主要是大老板觉着我们 Prime Day，Black Friday 以及 Q4 太辛苦了。

第一个月我主要是在 embark 公司文化等培训（主要为了让你更快融入），同时也体会到了一个美国公司在包容性、低碳和创新等方面的重视。记忆犹新的一次是在 commit code 时因为包含 black 这个单词而要求调整，国内基本上不会出现这种情况，我们主要是为了大多数人的利益，至于少数根本无暇顾及，这也体现了一个文明发达社会所秉承的人文关怀，至于 Policy Correst 是否正确我们在此不会讨论。

---

## 前端项目介绍

我所在的团队之前使用的前端技术栈主要是 Backbone.js 和 React，也没有做到前后端分离。最初开始阅读 Backbone.js 这部分业务代码时，常常为了调试一个简单 feature 而花上几天的时间，也不由得深深体会到 React 解决的问题。下面我就之前前端的设计做一些介绍：

首先，own 的所有应用技术栈主要分为三大类：纯 Backbone.js，纯 React, Backbone.js + React 混合。

### 整体设计

Match 页面路由请求后，直出 js 模板，在前端获取 js 模板并注入相应数据插入到页面目标 DOM 节点中。当然这一套完全在适应 Amazon UI 只有 ssr 组件这一限制下做出的。整体就是渲染了 ssr 组件，实则是 csr 体验。

### 通信机制

在含有 Backbone.js 的应用中采用事件流来进行组件间的通信，除此以外事件系统还使用了两套：Backbone.js 自带的 Event 和 Amazon UI 的 Event。整体阅读和调试代码时的体验就是事件满天飞，使得追踪数据变更变得异常困难。此时，不得不惊叹单向数据流动所带来的简便，尤其是在我们的应用不断膨胀。

### 开发模式

不知道是否有 Amazon 团队的前端应用是否可以在 local 上 run 起来，我们团队的前端应用只能在 cloud desktop 上 run，然后通过文件同步工具从 local 同步到 cloud desktop 上。一开始还是比较不习惯，不过现在觉着 local vs cloud 没有太大差别，就是 apollo 经常挂掉，起初修下环境就要以天记，现在总结了一些经验，因为环境引起的问题基本可以忽略不计了。

---

其实在 Amazon 基本没有纯 FE 的工作，常规的 Operation things 不会少做，比如说我在这半年期间，就解过几个种类的 risks。目前是不要求我开发后端，可是能够阅读 Java 代码这个也是必须要掌握的技能。后面想要 transfer 到海外，那么 transform role 成 SDE，Java 也必须要重视起来。

如果你也期望拥有不同体验，欢迎加入 Amazon。
