---
date: 2014-08-31 00:14:31+00:00
layout: post
title: 黑莓BlackBerry World错误ID 40820的解决办法
categories: 杂记
tags: 黑莓 40820
---

我的黑莓是9930 Bold，最近两天使用BlackBerry World安装、卸载应用或者进入My World都会报错，错误代码为：40820

![](/album/other/app40820.jpg)

去黑莓官网查询，官网给出的原因及解决方案有很多种，详情可以查看官网：[点这里去官网](http://btsc.webapps.blackberry.com/btsc/viewdocument.do?noCount=true&externalId=KB28188&sliceId=1&dialogID=599906&cmd=displayKC&docType=kc&isLoadPublishedVer=&stateId=599907&docTypeID=DT_SUPPORTISSUE_1_1&ViewedDocsListHelper=com.kanisa.apps.common.BaseViewedDocsListHelperImpl)

具体到自己，我排除了其它可能，怀疑是网络的问题导致的，在关掉wifi链接后问题就消失了，所以问题就出在wifi上，但是wifi是可以正常访问，在电脑上可以正常访问BlackBerry World。所以问题的原因就定位在了手机的wifi设置上，最后发现是由于前两天用手机链接VPN，所以在手机WiFi配置中做了相应设置，但是VPN不能正常访问，而又没有删除该设置，所以导致手机访问BlackBerry World出错，删除掉该设置后，恢复正常。