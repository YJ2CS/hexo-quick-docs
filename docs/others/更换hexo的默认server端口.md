---
title: 更换hexo的默认server端口
url: 更换hexo的默认server端口
author: YJ2CS
avatar: /custom/avatar.webp
authorLink: YJ2CS.github.io
authorAbout: 愿青年摆脱了冷气，只是向前走！
authorDesc: 愿青年摆脱了冷气，只是向前走！
comments: true
categories:
  - 文章
tags:
  - 悦读
no-photos: 'https://random.52ecy.cn/randbg.php?size=1&rid-更换hexo的默认server端口'
date: 2020-12-30T00:07:35.000Z
date updated: '2020-12-30T00:07:48+08:00'

---

hexo的默认server端口是4000，其与中国大部分软件使用的端口都冲突(主要是腾讯系，包括foxmail)

所以建议更改默认的server端口,

具体的方法如下：

## 每次启动server都使用指定命令

```cmd
hexo s -p 5000 -debug
```

## 永久方法(推荐)：在根目录_config.yml文件中加入配置

在根目录_config.yml文件中加入下列配置：(推荐在最后一行)（template已经配置好了）

```yaml
server:
  port: 5000
  compress: true
  header: true
```
