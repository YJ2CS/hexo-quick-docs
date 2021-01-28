---
title: nodejs环境配置
url: nodejs环境配置
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
no-photos: https://random.52ecy.cn/randbg.php?size=1&rid-nodejs环境配置
date: 2020-12-30T22:42:43.000Z
date updated: '2021-01-28T11:08:07+08:00'

---

> You must have a positive self perception in order to transcend anything.
> — <cite>Steve Maraboli</cite>

点击回到hexo项目的配置文档: [[hexo项目安装与配置]]

## 安装nodejs的包管理器nvm/n

在Linux上建议安装n:

Linux上安装nvm：这十分简便，见[nvm-sh/nvm: Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions - <https://github.com/](https://github.com/nvm-sh/nvm)>

在Windows上推荐使用nvm:[coreybutler/nvm-windows: A node.js version management utility for Windows. Ironically written in Go. - <https://github.com/](https://github.com/coreybutler/nvm-windows)>

## 使用nvm/n下载nodejs

对于nvm：

```shell
nvm ls
nvm uninstall 14.5.4
nvm install 14.5.4
nvm use 14.5.4
```

## npm 安装所有依赖

```cmd
npm i
```

## 测试环境安装是否成功

使用下面的这条命令，部署hexo的本地server，着能够测试你的环境是否全部安装完成，安装是否存在问题。

```bash
$ hexo clean && hexo s -debug
```

成功启动 <http://localhost:5000> ，打开且无报错

下面这条报错可以忽略，其他报错则需要自行排除bug

```bash
(node:11248) [DEP0066] DeprecationWarning: OutgoingMessage.prototype._headers is deprecated
```

- tips: 您可以选择全局安装hexo

  ```bash
  $ npm install -g hexo-cli
  ```

## 配置过程出现问题？

在配置过程中，可能会出现

- 部署本地server失败
- 无法访问nodejs网站，从而无法下载nodejs依赖

解决方法：您可以查看这一个步骤来尝试解决您的问题：[[自我bug排除和修复]]

至此，您已经初步配置好环境了。

## 结束语

到了这，您的相关环境就配置完成了，

下一步，您可以开始写下您的第一篇文章，见：[[写文章]]
