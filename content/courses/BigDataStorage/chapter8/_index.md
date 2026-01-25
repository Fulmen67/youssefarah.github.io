---
# Page title
title: 第8章 分布式文件存储

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 第8章 分布式文件存储

# Page summary for search engines.
summary: Blah, blah, blah...

# Date page published
date: 2024-06-03

# Book page type (do not modify).
type: docs

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 8
---

- 关系型数据库读取上传要2步性能差
- MongoDB的存储基本单元是BSON文档对象，字段值可以是二进制类型，支持一条记录存储；
- 文件内容直接保存到MongoDB(非路径)，可充分发挥分布式特性
- MongoDB对单个文件有限制，最大不超过16MB，可直接存储；当文件大于16MB时，就需要通过GridFS实现。