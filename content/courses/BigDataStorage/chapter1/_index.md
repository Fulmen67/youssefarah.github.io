---
# Page title
title: 第1章 初识MongoDB

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 第1章 初识MongoDB

# Page summary for search engines.
summary: Blah, blah, blah...

# Date page published
date: 2018-09-09

# Book page type (do not modify).
type: docs

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 1
---

## 1.安装步骤
- 下载地址：https://www.mongodb.com/download-center/community  版本4.4或更高版本；
- 或者网盘下载：https://pan.baidu.com/s/15KwMqxcVFi8D6BpMBKNQkA?pwd=abt7 提取码: abt7
- 安装方法参考：https://www.runoob.com/mongodb/mongodb-window-install.html
- 安装过程中不要勾选MongoDB Compass（可视化环境），MongoDB单独安装。
## 2.配置数据和日志文件目录（自定义）
- 创建数据目录：D:\mongodb\data\db
- 创建日志目录：D:\mongodb\data\log
- 创建日志文件：D:\mongodb\data\log\mongodb.log
## 3.安装成功与否测试
- 启动服务器：C:\Program Files\MongoDB\Server\4.4\bin>.\mongod.exe --dbpath d:\mongodb\data\db
- 看到日志倒数第二行：waiting for connections on port 27017
- 浏览器输入：http://localhost:27017/    显示It looks like you are ...
出现上述情况，说明安装正常
