---
# Page title
title: 2024实验大作业

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 2024实验大作业

# Page summary for search engines.
summary: Blah, blah, blah...

# Date page published
date: 2024-04-28

# Book page type (do not modify).
type: docs

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 11
---
## 实验大作业目标

训练系统开发应用能力，自行解决实际问题的能力，以及为未来就业简历增加内容。

## 选题方向

实现特定功能的系统，其中大数据获取来源，包括交通、医疗、金融、知乎、微博、新闻、电影、影评、音乐、社交网络、物联网、图像、视频等。拟定的报告内容涉及的技术背景可以从上述领域中选取，或者选取自己熟悉的领域皆可。

## 材料提交要求

1.排版要求：内容宋体、小四，格式统一，排版清晰漂亮 <br>
2.电子文档内容参考软件著作权的书写方法（[见模版](https://pan.baidu.com/s/15KwMqxcVFi8D6BpMBKNQkA?pwd=abt7)），文档命名规则：学号-姓名.docx <br>
3.源代码文件夹命名“学号-姓名-源代码” <br>
4.文档和源码文件夹一起打包，打包后的格式：学号-姓名.zip <br>
5.打包的压缩包【学号-姓名.zip】发送给班长，纸质版文档第17周上课时，提交给班长。<br>
6.分享在阿里云部署后的演示链接，链接填入这里：[实验大作业演示链接](https://docs.qq.com/sheet/DQmZQTG9wREFJU3Ru?scene=a896b92c8e7086dee22e8937lpY3s1&tab=BB08J2)

## 实验方案

- 1.[领取阿里云云工开物，优惠卷300元](https://university.aliyun.com/?spm=5176.21213303.J_qCOwPWspKEuWcmp8qiZNQ.195.14332f3djd7wBs&scm=20140722.S_card%40%40%E6%B4%BB%E5%8A%A8%40%402997640.S_card0.ID_card%40%40%E6%B4%BB%E5%8A%A8%40%402997640-RL_%E4%BA%91%E5%B7%A5%E5%BC%80%E7%89%A9-LOC_search%7EUND%7Ecard%7EUND%7Eitem-OR_ser-V_3-P0_0)
- 2.技术方案
  - 方案1：本地获取数据，存入MongoDB，然后导出数据，数据上传至：文件存储NAS+云服务器ECS，在云服务器上展示自己的应用程序；
  - 方案2：本地获取数据，存入MongoDB，然后导出数据，数据上传至：文件存储NAS+云服务器ECS+函数计算FC，通过函数计算FC设计自己的应用；
- 3.[免费领取文件存储NAS，50GB，3个月](https://free.aliyun.com/?pipCode=nas&spm=5176.59209.J_5834642020.4.169276b94u5OFL)
- 4.[免费领取云服务器ECS，200元，3个月，注意：按使用量计算，超出收费](https://free.aliyun.com/?product=1351,1353,1355&spm=5176.59209.J_5834642020.4.169276b94u5OFL)
- 5.[免费领取函数计算FC，180元，3个月，注意：按使用量计算，超出收费](https://free.aliyun.com/?product=1351,1353,1355&spm=5176.59209.J_5834642020.4.169276b94u5OFL)
- 6.300元优惠卷可以根据使用情况进行使用
- 7.使用方法参考链接：
  - https://university.aliyun.com/activity/wintervacation
  - 同济子豪兄：https://www.bilibili.com/video/BV1DZ421B7J9
  - 老麦的工具库：https://www.bilibili.com/video/BV1Np421f7HE/
  - https://developer.aliyun.com/topic/freetier/nas
- 8.实验示例：
  - 示例1：python爬取审计署新闻数据或者爬取指定内容，将爬取的数据写入mongodb，导出数据存入文件存储NAS，在云服务器ECS端，通过python GUI实现可视化的数据增、删、查、改功能。其他可视化和数据分析功能根据爱好添加。
  - 示例2：python爬取互联网图片，写入mongodb，然后导出图像数据，存入文件存储NAS，通过函数计算FC对图片进行处理，有丰富的API，生成各式各样的图片进行展示。
- 9.还可以体验阿里云提供的其他服务，有兴趣的可以探索

> 特别提醒：文件存储NAS+云服务器ECS+函数计算FC，各种服务器使用完后，记得关闭!记得关闭!记得关闭! 可能按时间，或者按流量进行计算收费！！！！！！！

## 得分要点

1.独立完成报告内容，严禁抄袭，如若相互抄袭，抄袭者和被抄袭者都是低分。 <br>
2.完成如下基本功能模块，包含导入大量数据、修改数据、删除数据、查询数据等。也可增加其他功能。但至少要有4个功能模块。<br>
3.报告内容需涵盖所学内容的80%以上。<br>
4.开发的系统有创新性，融入自己的idea，高分，90-100之间。<br>
5.开发的系统转化为申请软件著作权，可指导完成申请，高分，90-100之间。<br>
6.完成预定的功能，系统增删改查基本能用，中分，80-90之间。<br>
7.只完成部分或未实现等，低分，70-80之间。
