---
layout: post
title: "netServiceBrowserDidStopSearch 为什么不被调用"
description: "Bonjour 中 NSNetServiewBrowser 的 netServiceBrowserDidStopSearch 为什么一直没有被调用"
keyword: "Bonjour"
category: tips
tags: ["tips", "Bonjour"]
tagline: 
---
{% include JB/setup %}

#### netServiceBrowserDidStopSearch 一直没有被调用，为什么?
<br/>
当 NSNetServiceBrowser 开始寻找后，会不停的寻找，直到调用了 -stop 这个
方法。

NSNetServiceBrowser 会尝试寻找设定条件的服务，如果找到了一个服务之后并
不会停止寻找，而会继续寻找符合条件的其他服务。直到 -stop 这个方法被调
用。请根据自己业务的需要决定什么时候调用 -stop。



