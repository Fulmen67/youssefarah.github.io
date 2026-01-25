---
# Page title
title: 第10章 权限控制

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 第10章 权限控制

# Page summary for search engines.
summary: Blah, blah, blah...

# Date page published
date: 2025-11-11

# Book page type (do not modify).
type: docs

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 10
---

- 10.1 基于角色与权限控制原理
- 10.2 启动角色权限控制功能
- 10.3 MongoDB默认提供角色
- 10.4 用户管理
- 10.5 角色管理

---
**知识点**
- 理解权限控制的概念和原理
- 掌握权限控制的常见命令

---
**知识运用背景**
- **到目前为止，数据库都处于“裸奔”的状态，任何用户都可以连接到任何数据库并进行CRUD操作；**
- **像关系型数据库一样，不同的用户应该有不同的权限来操作数据；**
- **MongoDB提供了一套权限控制的API来实现这样的需求；**
- **权限控制的基本情况：**
  1. mongodb是没有默认管理员账号，所以要先添加管理员账号，再开启<mark>权限认证</mark>。
  2. 切换到<mark>admin数据库</mark>，添加的账号才是管理员账号。
  3. 用户只能在用户所在数据库登录，包括管理员账号。
  4. mongo的用户是以<mark>数据库为单位</mark>来建立的，每个数据库有自己的管理员。
  5. 管理员可以管理所有数据库，但是不能直接管理其他数据库，要先在admin数据库认证后才可以。
  >注：帐号是跟着库走的，所以在指定库里授权，必须也在指定库里验证



