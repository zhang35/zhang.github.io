---
title: 量化考评网站初版
date: 2018-08-29 11:27:12
tags: 量化考评 web 购物车 成长曲线 评语 angular.js gulp bower jade 
categories: 前端开发
description: 量化考评网站前端部分。用到angular.js、gulp、bower、jade等技术,实现绩效填写、购物车增减条目、成长曲线、评语等功能
---

在李成海大神搭的架子下，完成了量化考评网站前端部分。用到angular.js、gulp、bower、jade等技术，感谢成海指导。

7月31日，初版于单位内网上线，功能如下。

## 用户入口

### 登录页面
![](https://upload-images.jianshu.io/upload_images/6240664-b0c2cd0849c662d5.gif?imageMogr2/auto-orient/strip)

### 考评页面
#### 选择部门、日期
![](https://upload-images.jianshu.io/upload_images/6240664-f756bd0f28ed4e38.gif?imageMogr2/auto-orient/strip)

#### 填写一日工作
![](https://upload-images.jianshu.io/upload_images/6240664-d0427d18b4cfe357.gif?imageMogr2/auto-orient/strip)

- 类似**购物车**功能，增减或直接修改数目，可实时看到得分结果。

- 当数目输入不合法时（字母，负数等），自动替换为0。

- 加分数目和减分数目均为0时，得分将被清空，不做统计。

#### 快速导航按类别定位

![](https://upload-images.jianshu.io/upload_images/6240664-bec3804745bcb7c8.gif?imageMogr2/auto-orient/strip)

自动按类别生成导航菜单。

#### 提交今日工作
![](https://upload-images.jianshu.io/upload_images/6240664-87e70757d27b353d.gif?imageMogr2/auto-orient/strip)

显示今日总得分，提交后显示明细。

#### 防止重复提交
![](https://upload-images.jianshu.io/upload_images/6240664-0c9d275ec06260ad.gif?imageMogr2/auto-orient/strip)
显示“今日已提交！”，提交按钮变灰。

工作记录限制每天提交一次，一经提交不可更改。

### 绩效搜索页面

![](https://upload-images.jianshu.io/upload_images/6240664-e20b8baabb85eb13.gif?imageMogr2/auto-orient/strip)

查看个人绩效，可按得分类型、评语类型、起止日期等筛选。

### 成长曲线页面
![](https://upload-images.jianshu.io/upload_images/6240664-136572835a30c463.gif?imageMogr2/auto-orient/strip)

查看个人成长曲线，由每日得分构成。可按部门、起止日期筛选。

## 领导入口
### 登录页面
![](https://upload-images.jianshu.io/upload_images/6240664-a65371827291a9c3.gif?imageMogr2/auto-orient/strip)

### 绩效搜索页面
#### 检索人员绩效
![](https://upload-images.jianshu.io/upload_images/6240664-c5023d334565727a.gif?imageMogr2/auto-orient/strip)

检索所属人员绩效，可按部门、姓名、得分类型、评语类型、起止日期等筛选。

#### 填写评语
![](https://upload-images.jianshu.io/upload_images/6240664-9bc00a179361b7a4.gif?imageMogr2/auto-orient/strip)

领导可对某条绩效添加评语。普通用户将能在绩效搜索页面看到评语。

### 成长曲线页面
![](https://upload-images.jianshu.io/upload_images/6240664-384477faedc03d77.gif?imageMogr2/auto-orient/strip)

查看所属人员成长曲线，可按部门、姓名、起止日期等筛选。

## 结语 
网站后端由成海开发，使用springboot脚手架，效率极高地提供了数据增删查改的接口，这是后面需要学习的东西。

借此体验了前后端分离的合作开发模式：在阿里云服务器上搭建测试网站和数据库服务，在GitHub上共同管理代码。

源码可在我的GitHub上找到：https://github.com/zhang35
