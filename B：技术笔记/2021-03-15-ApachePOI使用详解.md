---
title: Apache POI使用详解
date: 2021-03-15 12:07:00
updated: 2021-03-15 12:07:00
summary: 介绍Apache软件基金会的开放源码函式库Apache POI是如何对Microsoft Office格式档案进行读写操作。
---

# 1、什么是Apache POI？

Apache POI 是用Java编写的免费开源的跨平台的 Java API，Apache POI提供API给Java程式对Microsoft Office格式档案读和写的功能。POI为“Poor Obfuscation Implementation”的首字母缩写，意为“可怜的模糊实现”。

Apache POI 是创建和维护操作各种符合Office Open XML（OOXML）标准和微软的OLE 2复合文档格式（OLE2）的Java API。用它可以使用Java读取和创建,修改MS Excel文件.而且,还可以使用Java读取和创建MS Word和MSPowerPoint文件。Apache POI 提供Java操作Excel解决方案（适用于Excel97-2008）。

POI 子模块与处理文档对应关系

| 模块 | 对应文档类型          |
| ---- | --------------------- |
| HSSF | Microsoft Excel       |
| XSSF | Microsoft Excel OOXML |
| HWPF | Microsoft Word        |
| HSLF | Microsoft PowerPoint  |
| HDGF | Microsoft Visio       |