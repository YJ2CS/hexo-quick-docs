---
title: markdown语法
url: markdown语法
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
no-photos: 'https://random.52ecy.cn/randbg.php?size=1&rid-markdown语法'
date: 2020-12-31T19:40:29.000Z
date updated: '2020-12-31T19:41:01+08:00'

---

> I know for sure that what we dwell on is who we become.
> — <cite>Oprah Winfrey</cite>

Obsidian 是基于Markdown格式的笔记和知识库管理程序。

我们目前支持以下MD语法：

---

### 标题
```text
# 这是标题 1
## 这是标题 2
### 这是标题 3 
#### 这是标题 4
##### 这是标题 5
###### 这是标题 6
```
# 这是标题 1
## 这是标题 2
### 这是标题 3 
#### 这是标题 4
##### 这是标题 5
###### 这是标题 6

---

### 重点
```text
*本行文字为斜体*

_这行也是斜体_

**本行文本为粗体**

__这行也是粗体__

_您 **可以** 合并两种效果_
```
*本行文字为斜体*

_这行也是斜体_

**本行文本为粗体**

__这行也是粗体__

_您 **可以** 合并两种效果_

---

### 清单
```text
- 项目 1
- 项目 2
  - 项目 2a
  - 项目 2b

1. 项目 1
1. 项目 2
1. 项目 3
   1. 项目 3a
   1. 项目 3b
```
- 项目 1
- 项目 2
  - 项目 2a
  - 项目 2b

1. 项目 1
1. 项目 2
1. 项目 3
   1. 项目 3a
   1. 项目 3b

--- 

### 图像
```text
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

---

### 链接
```text
http://obsidian.md - automatic!
[Obsidian](http://obsidian.md)
```
http://obsidian.md - automatic!

[Obsidian](http://obsidian.md)

---

### 块引用
```text
> 人类面临着越来越复杂和紧迫的问题，如何有效地处理这些问题，关系到社会的稳定和持续进步。

\- Doug Engelbart, 1961
```
> 人类面临着越来越复杂和紧迫的问题，如何有效地处理这些问题，关系到社会的稳定和持续进步。

\- Doug Engelbart, 1961

---

### 内联代码
```text
一行文本中 `单引号` 内的文本将被格式化为代码。
```
一行文本中 `单引号` 内的文本将被格式化为代码。


---

### 代码块

第一组反引号后指定的语言支持语法突出显示。 我们使用prismjs突出显示语法，可以 [在此站点](https://prismjs.com/#supported-languages)找到支持的语言列表

````text
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
````

````text
    Text indented with a tab is formatted like this, and will also look like a code block in preview. 
````

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
    
    Text indented with a tab is formatted like this, and will also look like a code block in preview. 
    

---

### 任务列表
```text
- [x] 支持 #标签, [链接](), **格式**
- [x] 需要列表语法 (支持无序和有序列表)
- [x] 这是一个完成的项目
- [ ] 这是一个未完成的项目
- [ ] 点击复选框可以切换任务的进展情况
```
- [x] 支持 #标签, [链接](), **格式**
- [x] 需要列表语法 (支持无序和有序列表)
- [x] 这是一个完成的项目
- [ ] 这是一个未完成的项目
- [ ] 点击复选框可以切换任务的进展情况

---

### 表格

您可以通过组合单词列表并用连成字符 `-` 分割行，然后用竖线 `|` 分隔列来创建表格：
```text
表头1 | 表头2
------------ | ------------:
单元格1中的内容 | 单元格2中的内容
第1列中的内容 | 第2列中的内容
```
表头1 | 表头2
------------ | ------------:
单元格1中的内容 | 单元格2中的内容
第1列中的内容 | 第2列中的内容

---
```text
可以有冒号对齐表格 | 另一个长标题示例
:----------------|-------------:
使用`:`的效果 | 这是右对齐效果
```
可以有冒号对齐表格 | 另一个长标题示例
:----------------|-------------:
使用`:`的效果 | 这是右对齐效果


---

### 删除线
```text
用两个波浪号包含任何单词 (例如 ~~这个~~) 将被标注删除线。
```
用两个波浪号包含任何单词 (例如 ~~这个~~) 将被标注删除线。

---

### 脚注
```text
这是一个简单的脚注效果，[^1] 这是一个较长的脚注。[^bignote]

[^1]: 有意义！

[^bignote]: 这里有多个段落和代码。

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

```
这是一个简单的脚注效果，[^1] 这是一个较长的脚注。[^bignote]

[^1]: 有意义！

[^bignote]: 这里有多个段落和代码。

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

---

```text
您还可以使用内部脚注。 ^[请注意，尖帽子符号在括号以外才生效]
```
您还可以使用内部脚注。 ^[请注意，尖帽子符号在括号以外才生效]

### 数学公式
```text
$$\begin{vmatrix}a & b\\
c & d
\end{vmatrix}=ad-bc$$
```
$$\begin{vmatrix}a & b\\
c & d
\end{vmatrix}=ad-bc$$


## Obsidian 特定格式

### 高亮文本
```text
使用两个等号包含 ==需要高亮的文本==.
```
使用两个等号包含 ==需要高亮的文本==.

### 内部链接
```text
使用双层方括号包含文本，可以链接到页面： [[内部链接]].
```
使用双层方括号包含文本，可以链接到页面： [[内部链接]].

### 内部嵌入

使用感叹号和内部链接的格式来嵌入其它文件 (阅读有关 [[嵌入文件]] 的更多信息).
```text
![[index]]
```
![[index]]


## 开发者笔记

因为使用了稍微个性的语法组合，我们努力在不破坏任何现有格式的情况下获得最大的功能。它是一个广泛的通用标记，增加了一些GitHub 风格的Markdown(GFM)功能， LaTex支持，以及我们选择的嵌入语法。您可以在 [[嵌入文件]] 页面了解到更多信息。
