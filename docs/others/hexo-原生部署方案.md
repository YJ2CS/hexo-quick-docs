---
title: hexo-原生部署方案
url: hexo-原生部署方案
author: YJ2CS
avatar: '/cdn/avatar.webp'
authorLink: YJ2CS.github.io
authorAbout: 愿青年摆脱了冷气，只是向前走！
authorDesc: 愿青年摆脱了冷气，只是向前走！
comments: true
categories:
  - 文章
tags:
  - 悦读
no-photos: 'https://random.52ecy.cn/randbg.php?size=1&rid-hexo-原生部署方案'
date: '2021-02-27T10:30:34+08:00'
date updated: '2021-02-27T10:30:34+08:00'

---

> I keep asking myself these three questions.. What do you have? What do you want? What will you give up?
> &mdash; <cite>Jack Ma</cite>

## 使用hexo原生的在线部署服务

使用hexo原生的在线部署服务,生成网页并且在线部署,可以部署到GitHub Pages或者其他pages服务

```bash
hexo g -d
```

合并清理命令：

```bash
hexo clean && hexo g -d
```

## 一键发布 deploy脚本

新建`hexo-publish.bat`,内容为

```bash
hexo g -d
```

实际操作过程只是执行了`hexo g -d`命令
