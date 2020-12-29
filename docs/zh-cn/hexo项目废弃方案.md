---
title: hexo项目废弃方案
url: hexo项目废弃方案
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
no-photos: 'https://random.52ecy.cn/randbg.php?size=1&rid-hexo项目废弃方案'
date: 2020-12-30T00:09:38.000Z
date updated: '2020-12-30T00:12:03+08:00'

---

## 使用 Markdown-Toolbox工具管理您的文档(可选，不建议，有更好方案)

安装:

```cmd
pip install Markdown-Toolbox
```

有问题不要发issue，因为这项功能在Windows上十分不稳定

安装python依赖

```shell
pip install -r requirements.txt
```

启动命令:

```cmd
MarkdownToolbox
或
Markdown-Toolbox
```

启动失败修复命令：

```cmd
pip install Markdown-Toolbox --force-reinstall
```

## hexo-admin后台管理插件(可选，不建议，有安全风险)

```cmd
npm install --save hexo-admin
```

在本地的server中，浏览器的地址栏添加`/admin`

例如，

```text
http://localhost:5000/admin
```

### 用户重置admin登录密码

如果您第一次使用这项功能或者忘记了登录密码，您需要重置登录密码

在根目录中的_config.yml，删除以下内容:

只需删除:

```cmd
admin:
	username:*********
	password_hash:**********
	secret:***********
```

更改为:

```cmd
admin:
	otherconfig.......
```

更多配置，请见文档： hexo-admin后台管理插件doc

- [使用 hexo-admin 後台管理工具](https://ed521.github.io/2019/08/hexo-admin/)

- [Hexo-Admin博客后端管理工具](https://thistgg.github.io/2017/03/23/Hexo-Admin%E5%8D%9A%E5%AE%A2%E5%90%8E%E7%AB%AF%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7/)

## hexo-git-backup插件(可选)

```cmd
npm install --save hexo-git-backup
```

使用命令

```shell
hexo b
or
hexo backup
```
