---
title: 写作后发布到服务器中
url: 写作后发布到服务器中
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
no-photos: https://random.52ecy.cn/randbg.php?size=1&rid-写作后发布到服务器中
date: '2021-02-27T10:40:08+08:00'
date updated: '2021-02-27T10:48:52+08:00'

---

> I keep asking myself these three questions.. What do you have? What do you want? What will you give up?
> — <cite>Jack Ma</cite>
如果您在本地更新了文章想要发布,或者是对 Hexo 更换了主题,或者是修改了 Hexo 的配置、添加了插件等，

可以使用 git 命令添加文件夹上传至 Github，然后等待几分钟后，Vercel 便会自动将 Github 仓库里的最新提交进行解析部署，

然后成功后会发一封邮件至绑定邮件提醒博客已经更新（可关闭），然后去自己的博客网站就可以看见自己做的修改或者最新的文章已经能看见了。

## git命令
使用git 命令添加文件夹上传至 Github
```shell
git add --all
git commit -m 'new commit 2021-02-01-10-48'
git push 
```

## git push过程中出现了问题-单次提交文件体积过大

当您尝试git push到远程仓库，发现单次提交文件体积过大，提交失败，可以尝试以下解决方案

```bash
# 关闭ssl的安全验证
git config http.sslVerify "false"
# 增大缓冲池 `Buffer`
git config --global http.postBuffer 524288000
```

524288000代表B，524288000B也就是500MB。这个值得大小，可以根据项目酌情设置。
