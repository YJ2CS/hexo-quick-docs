---
title: 出现bug的自我检查修复
url: 出现bug的自我检查修复
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
no-photos: https://random.52ecy.cn/randbg.php?size=1&rid-出现bug的自我检查修复
date: 2020-12-28T20:38:44.000Z
date updated: '2021-02-27T10:45:26+08:00'

---

您可能是从[[安装与配置]]跳转过来的。

## 初始化server失败-使用 npm-check 更新项目依赖

使用 npm-check 更新项目依赖是一个常用的自我排除问题方法。

在网站项目根目录运行

安装 npm-check

```cmd
npm i -g npm-check
```

检查更新

```bash
npm-check -u
```

输出如下：

```bash
? Choose which packages to update. (Press <space> to select)

 Update package.json to match version installed.
❯◯ chalk     ^1.1.3   ❯  2.4.2   https://github.com/chalk/chalk#readme
 ◯ cheerio   ^0.22.0  ❯  0.22.0  https://github.com/cheeriojs/cheerio#readme
 ◯ debug     ^2.3.3   ❯  4.1.1   https://github.com/visionmedia/debug#readme
 Space to select. Enter to start upgrading. Control-C to cancel.

```

**使用 `↑` `↓` `空格space` 选中要更新的包，`Ctrl + C` 取消更新，`回车` 就是执行更新。**

## 清理全部生成文件 hexo clean

这是排除大部分bug时使用的命令,有时候还能够解决一些报错。十分的玄学。究其原因，是npm糟糕的依赖安装系统导致的。

```bash
hexo clean
```
