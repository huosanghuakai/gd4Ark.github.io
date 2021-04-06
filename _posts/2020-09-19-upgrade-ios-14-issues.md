---
title: 升级 IOS 14 的一些坑
categories:
  - 折腾
tags:
  - 折腾
abbrlink: 7b1778ee
date: 2020-09-19 15:37:23
---

## 前言

IOS 14 正式版已经发布差不多一个星期了，也看到社区不少人开始讨论新特性，我当然也要跟上脚步，于是也开始把我的 iPhone 和 iPad 更新了，但这过程中却是踩了不少的坑，先记录下来，让后来者少花一些时间。

## 先说结论

我最终成功更新的过程是：

1. 在 Windows 下载最新版本的 iTunes
2. 在 [异次元](https://www.iplaysoft.com/item/ios-ipsw-download) 下载 IOS 14 固件
3. 打开 `Service.msc` ，将 `Remote Desktop Services` 设置为启用和自动
4. Windows 连接手机热点，不要连接宽带网络
5. 在 iTunes 连接手机，按住 Shift 点击更新，选择固件，等待更新

PS：先备份好手机数据，以防万一！

## 过程

收到推送的当天晚上睡觉前我就在手机和平板上都点了更新，然而等我早上起床打算愉快地体验新系统时，却发现没有更新，进入更新界面才发现下载了不到一半，显示「正在预估剩余时间」，第二天晚上再试了一下，结果还是一样。

既然在手机上更新不了，那就在电脑更新，于是连接到 Mac，点击更新，到最后一步出现「iPad “4Ark 的 iPad” 的软件下载时被损坏，断开后再次连接...」，换了 Windows 也是一样的问题。

于是我自己在网上找 IOS 14 的固件，最初我打算在官方，想着系统固件还是官方的比较安全，结果发现最新版本还是停留在 IOS 13.7，于是在一个相对比较靠谱的 [异次元](https://www.iplaysoft.com/item/ios-ipsw-download) 里把 IOS 和 iPadOs 固件下载回来。

因为我是在 Windows 下载的，所以也就在 Windows 最新版的 iTunes 上面更新，连接上手机，按住 Shift 点击更新，选择固件，结果出现「未能更新iPhone，发生未知错误53」，在 [这里](https://discussionschinese.apple.com/thread/251504194) 找到了解决方案，主要是电脑上的网络不要连接宽带，而是连接移动网络的热点。

结果在更新过程中，一直停留在「正在准备iPhone以进行软件更新」十几分钟，根据以往的折腾经验，准备工作超过十分钟基本就是有问题的了，于是果然在 [这里](https://hcwang.pixnet.net/blog/post/40515550) 找到了解决方案，主要就是：打开 `Service.msc` ，将 `Remote Desktop Services` 设置为启用和自动，重启 iTunes，重新连接手机，这时候终于可以更新了。

## 写在最后

前两天还看到社区里的人都是手机上直接升级的，一睡醒就好了，怎么到我这里就一大堆问题 😩

但不管怎么说，这些问题我肯定不是第一个，更不可能是最后一个，本文就是为了让大家不要再浪费时间。

毕竟，周末美好时光，不能白白浪费嘛。