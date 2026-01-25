---
# Page title
title: 第3章 索引

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 第3章 索引

# Page summary for search engines.
summary: Blah, blah, blah...

# Date page published
date: 2024-04-08

# Book page type (do not modify).
type: docs

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 3
---

## 1.重点
* <p>掌握索引的创建和优化方法  <p/>
* 掌握单字段索引、复合索引、多键索引、索引管理、查询优化

## 2.索引的概念
* 索引是对数据库**表中一列或多列的值进行排序的一种结构**
* 索引通常能够极大的提高查询的效率
* 索引的建立要花费系统时间，索引文件也会占用磁盘空间
    比如：书的目录、序号、学号等
    
* MongoDB索引的数据结构是B+树
