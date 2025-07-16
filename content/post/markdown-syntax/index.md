---
title: Markdown语法指南
date: 2023-09-07
description: 展示Hugo内容文件中基本Markdown语法和HTML元素格式化的示例文章
tags: 
    - markdown
    - css
    - html
    - themes
categories:
    - themes
    - syntax
---

本文提供了可在Hugo内容文件中使用的基本Markdown语法示例，同时展示了Hugo主题中基本HTML元素是否使用CSS进行装饰。

<!--more-->

## 标题

以下HTML `<h1>`—`<h6>`元素表示六个级别的章节标题。`<h1>`是最高级别，`<h6>`是最低级别。

# H1
## H2
### H3
#### H4
##### H5
###### H6

## 段落

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## 引用块

引用块元素表示从其他来源引用的内容，可选择包含引用信息（必须位于`footer`或`cite`元素内），也可包含内联修改如注释和缩写。

### 无来源引用块

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **注意** 您可以在引用块内使用*Markdown语法*。

### 带来源引用块

> 不要通过共享内存来通信，而要通过通信来共享内存。<br>
> — <cite>罗伯·派克[^1]</cite>

[^1]: 以上引语节选自罗伯·派克在2015年11月18日Gopherfest上的[演讲](https://www.youtube.com/watch?v=PAAkCSZUG1c)。

## 表格

表格不是Markdown核心规范的一部分，但Hugo开箱即支持表格功能。

   Name | Age
--------|------
    Bob | 27
  Alice | 23

### 表格中的内联Markdown

| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------------|
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

## 代码块
### 使用反引号的代码块

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```

### 使用四个空格缩进的代码块

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

### Diff代码块

```diff
[dependencies.bevy]
git = "https://github.com/bevyengine/bevy"
rev = "11f52b8c72fc3a568e8bb4a4cd1f3eb025ac2e13"
- features = ["dynamic"]
+ features = ["jpeg", "dynamic"]
```

### 单行代码块

```html
<p>A paragraph</p>
```

## 列表类型

### 有序列表

1. First item
2. Second item
3. Third item

### 无序列表

* List item
* Another item
* And another item

### 嵌套列表

* Fruit
  * Apple
  * Orange
  * Banana
* Dairy
  * Milk
  * Cheese

## 其他元素 — abbr, sub, sup, kbd, mark

<abbr title="图形交换格式">GIF</abbr>是一种位图图像格式。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按 <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> 结束会话。

大多数<mark>蝾螈</mark>是夜行性动物，以昆虫、蠕虫和其他小型生物为食。