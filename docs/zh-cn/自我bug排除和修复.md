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
date updated: '2021-01-28T11:08:35+08:00'

---

您可能是从[[hexo项目安装与配置]]跳转过来的。

## 增加proxy

您可能在某些地区无法下载node，于是您可能要增加一个代理：

### nvm增加proxy

nvm设置代理

```shell
nvm proxy 127.0.0.1:7890
nvm install 14.5.4
```

### n增加proxy

## 安装 nrm

```cmd
npm i -g nrm
```

### nrm查看下载镜像源

```cmd
nrm ls
```

### nrm切换镜像源

```cmd
nrm use taobao
```

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

## 安装node js相关依赖时出现了问题

当您安装了错误的node依赖，或者您遇到了未知bug，可以尝试**重新安装node依赖**

linux中:

```bash
rm -rf node_modules/ && npm i
```

windows中:
删除node_modules文件夹并执行

```bash
npm i
```

## git push过程中出现了问题-单次提交文件体积过大

当您尝试git push到远程仓库，发现单次提交文件体积过大，提交失败，可以尝试以下解决方案

_git 远程仓库设置_

```bash
# 关闭ssl的安全验证
git config http.sslVerify "false"
# 增大缓冲池 `Buffer`
git config --global http.postBuffer 524288000
```

524288000代表B，524288000B也就是500MB。这个值得大小，可以根据项目酌情设置。
