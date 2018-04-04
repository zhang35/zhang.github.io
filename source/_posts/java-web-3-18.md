---
title: Java投票网站初版
date: 2018-03-18 18:20:12
tags: java web
categories: Java Web
---

> 搭好[Spring+SpringMVC+Hibernate实现投票/调查问卷网站](https://www.jianshu.com/p/c68fd9fe4ead)的架子后，本想去尝试下其它东西，好在家腾君表示要把它完善下，能真正投入使用。
这才发现，还有太多东西要做，还有太多坑没踩。年后至今，三周过去了，终于合作完成了能凑合用的版本。家腾君表示：“吹了一年的牛B，终于能交差了。”


完善后的投票网站，目前效果如下：
<!-- more -->
### 前端（用户界面）
打开首页，点击进入投票页面。加了些jQuery美化插件：
![ios视觉差效果（飞机在飞有木有）](https://upload-images.jianshu.io/upload_images/6240664-ed7d33ae875b4cdd.gif?imageMogr2/auto-orient/strip)
![粒子效果](https://upload-images.jianshu.io/upload_images/6240664-272909d0be7b7a58.gif?imageMogr2/auto-orient/strip)

侧边导航：
![导航栏](https://upload-images.jianshu.io/upload_images/6240664-be9d05fec3600f0d.gif?imageMogr2/auto-orient/strip)

辅助填表，一键全优：
![一键全优](https://upload-images.jianshu.io/upload_images/6240664-ba35e36f3e5b9e43.gif?imageMogr2/auto-orient/strip)

表单验证。用户点击提交按钮后，检查答题情况，提示用户：
![提示未完成题目](https://upload-images.jianshu.io/upload_images/6240664-da82fc09fb9e6b33.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![提示用户投票是否有效](https://upload-images.jianshu.io/upload_images/6240664-a5a1312b5424a264.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/450)

防止重复投票（可由后台管理员开放）。完成一次投票后：
![投票成功](https://upload-images.jianshu.io/upload_images/6240664-53d49e3b952c49af.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/600)
再次投票会提示：
![投票失败](https://upload-images.jianshu.io/upload_images/6240664-496c8632d3680af2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/600)

### 后端（管理员界面）
输入密码，登录后台：
![登录界面](https://upload-images.jianshu.io/upload_images/6240664-a93c7364642fbd62.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/650)
![管理员界面](https://upload-images.jianshu.io/upload_images/6240664-b575da380c0ca4a2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

功能区如下：
![功能区](https://upload-images.jianshu.io/upload_images/6240664-1fbe4e1246c55049.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 每2s实时更新投票情况。
- “开放投票”按钮会刷新本轮投票情况，去除“无法重复投票”状态；
- “无限投票”开关打开时，永不限制重复投票；
- “下载文件”按钮会将结果导出为word文档，压缩为zip文件，提供下载；
- “过滤废票”开关打开后，会按规则去除无效票，改变统计结果。

点击人名，查看结果。如果打开“过滤废票”开关，会显示去除废票后的结果：
![查看详细结果](https://upload-images.jianshu.io/upload_images/6240664-b5daecc9202dc003.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

下载结果。如果打开“过滤废票”开关，会得到去除废票后的结果：
![下载得到“测评结果.zip”文件](https://upload-images.jianshu.io/upload_images/6240664-ffa1f989c5bc0ebf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/720)
![解压得到按部门分类目录结构](https://upload-images.jianshu.io/upload_images/6240664-5cc47f3b23179c99.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![得到自动生成的word文件xxx.doc](https://upload-images.jianshu.io/upload_images/6240664-01a9c388468d39cb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

以上。

几乎全是“面向搜索引擎”的编程。后面会继续完善，慢慢总结所用知识。
项目源码：[https://github.com/zhang35/QuizWeb.git](https://link.jianshu.com/?t=https%3A%2F%2Fgithub.com%2Fzhang35%2FQuizWeb.git)
