---
title: hexo-next-theme-项目特性
url: hexo-next-theme-项目特性
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
no-photos: 'https://random.52ecy.cn/randbg.php?size=1&rid-hexo-next-theme-项目特性'
date: 2020-12-29T23:58:33.000Z
date updated: '2020-12-30T00:12:22+08:00'

---

> Feeling grateful to or appreciative of someone or something in your life actually attracts more of the things that you appreciate and value into your life.
> — <cite>Christiane Northrup</cite>

项目特性分为已选和可选部分，前半段我将介绍这些已选部分，

它们是已经在template中配置好的，您可以直接使用，无需再行配置。

### 添加feed支持(已选)

在 Hexo **根目录**下的 `_config.yml` 文件中，新增以下的配置项：

```yaml
feed:
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
  content_limit: 140
  content_limit_delim: ' '
  order_by: -date
```

执行 `hexo clean && hexo g` 重新生成博客文件，然后在 `public` 文件夹中即可看到 `atom.xml` 文件，说明你已经安装成功了。

## 项目可选功能配置

### 修改permalink，可修改为短链接(可选,不建议)

使用短链接后，链接是短了，可你也不能从url上判断出来这个网页有什么内容了，这个看你怎么想了。

安装插件：

```cmd
npm install --save hexo-abbrlink
```

在根目录_config.yml中修改permalink

```yaml
permalink: :abbrlink.html #:year/:month/:day/:title/
permalink_defaults:
#alg: crc32  # 算法：crc16(default) and crc32
#rep: hex    # 进制：dec(default) and hex
#短链接
abbrlink:
  alg: crc16   #算法： crc16(default) and crc32
  rep: hex   #进制： dec(default) and hex: dec #输出进制：十进制和十六进制，默认为10进制。丨dec为十进制，hex为十六进制

```
