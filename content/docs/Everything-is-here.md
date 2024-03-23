---
title: "Everything Is Here"              # 标题
description: Describes commo.            # 描述
lead: 将编辑HUGO blog的方法技巧进行了整理       # 导言
date: 2024-03-23T10:44:56+08:00          # 日期
#thumbnail: "img/placeholder.png"         # 缩略图
authorbox: false                         # 作者框
sidebar: false                           # 侧边栏
pager: false                             # 分页器
tags:                                    # 标签
  - hugo
  - blog
categories:
  - 教程
---

在Hugo中，通常`content`文件夹用于存储您网站的内容，而`docs`和`post`这样的文件夹可能被用于组织不同类型或不同主题的内容。
<!--more-->
以下是通常情况下这两个文件夹的作用：

1. **docs 文件夹**：
    - `docs` 文件夹通常用于存储网站的文档内容，比如用户手册、指南、教程等。
    - 这个文件夹可以用于组织网站的长篇文章或结构化的文档内容，例如对产品的详细介绍、使用指南等。
    - 您可以根据您网站的需要，在`docs`文件夹下创建子文件夹来更好地组织不同主题或类型的文档内容。

2. **post 文件夹**：
    - `post` 文件夹通常用于存储网站的博客文章或新闻类内容。
    - 在这个文件夹中，您可以存放各种短篇文章、新闻更新或博客帖子，用于展示最新的内容。
    - Hugo通常会将`post`文件夹中的内容按照发布日期自动排序，使最新的文章显示在前面。

这些文件夹的名称和具体用途实际上取决于您的Hugo网站的结构和主题，您可以根据自己的需要进行调整和定制。


## doc中文章的说明区
### 入门中的说明区
```
title: Getting started                   # 标题
description: This article helps .        # 描述
lead: This article helps you ge.         # 导言
date: 2022-01-24T14:00:00.000Z           # 日期
tags:                                    # 标签
  - "Installation"                      
authorbox: false                         # 作者框
sidebar: false                           # 侧边栏
pager: false                             # 分页器
weight: 1                                # 权重，这篇文章上方的标题栏中第一个
menu: main                               # 菜单，这篇文章显示在了上方的标题栏中
```

### 定制化中的说明区
```
title: Customization                      # 标题
description: Describes common Mainr.      # 描述
lead: Describes common Mainroad th.       # 导言
date: 2022-01-24T14:00:00.000Z            # 日期
thumbnail:                                # 缩略图
  src: "img/placeholder.png"                # 图片路径
  visibility:                               # 图片可见性
    - list                                  # 列表
authorbox: false                          # 作者框
sidebar: false                            # 侧边栏
pager: false                              # 分页器
weight: 2                                 # 权重，这篇文章上方的标题栏中第二个
menu: main                                # 菜单，这篇文章显示在了上方的标题栏中
```

### 常见问题中的说明区
```
title: Frequently asked questions (FAQ)   # 标题
description: Browse this FAQ page to .    # 描述
date: 2022-01-24T14:00:00.000Z            # 日期
authorbox: false                          # 作者框
sidebar: false                            # 侧边栏
pager: false                              # 分页器
weight: 3                                 # 权重，这篇文章上方的标题栏中第三个
menu:                                     # 菜单，这篇文章显示在了上方的标题栏中
  main:                                   # 主菜单
    name: FAQ                             # 名称，这篇文章在上方的标题栏中显示名称为FAQ
```

## post中文章的说明区
### 基本元素中的说明区
```
title: Basic HTML Elements                # 标题：基本HTML元素
description: Example test article that .  # 描述
date: 2018-04-16                          # 日期
categories:                               # 分类
  - "Development"  
tags:                                     # 标签
  - "HTML" 
  - "CSS" 
  - "Basic Elements"  
menu:                                     # 菜单，这篇文章显示在了上方的标题栏中
  main:  # 主菜单
    name: Basic Elements                  # 名称，这篇文章在上方的标题栏中显示名称为Basic Elements
    weight: 4                             # 权重，这篇文章上方的标题栏中第四个
```

### 使用Hugo入门中的说明区
```
title: Getting Started with Hugo          # 标题
date: 2014-04-02                          # 日期
tags:                                     # 标签
  - "go"  # Go
  - "golang"  # Go语言
  - "hugo"  # Hugo
  - "development"  # 开发
categories:                               # 分类
  - "Development"  # 开发
  - "golang"  # Go语言
```

### (Hu)go模板入门中的说明区
```
title: "(Hu)go Template Primer"           # 标题
date: 2014-04-02                          # 日期
thumbnail: "img/placeholder.png"          # 缩略图：占位图像路径
tags:                                     # 标签
  - "go"  # Go
  - "golang"  # Go语言
  - "templates"  # 模板
  - "themes"  # 主题
  - "development"  # 开发
categories:                               # 分类
  - "Development"  # 开发
  - "golang"  # Go语言
```

## 其他
### 关于中的说明区
```
title: About
date: 2024-03-22T23:00:00.000Z
authorbox: false
sidebar: false
menu: main                                # 菜单，这篇文章显示在了上方的标题栏中最后
```

---

## 内容编辑方式
### 分段
使用一行空行进行分段。注意：代码中换行，不影响显示效果。


### 倾斜
*一对星号包围的内容将显示为倾斜*


### 加粗
 **两组星号包围的内容将加粗**

### 网址
方括号里填代替网址的描述，圆括号内填网址，描述将显示为红色。
 [Hugo](https://gohugo.io/) static

```[Hugo](https://gohugo.io/) static```

### 等宽显示代码块
通常用于文字中。

在两组反引号（``）之间包含内容，则该内容将被视为代码块，并且将以等宽字体显示，通常在网页或文本编辑器中，这样的内容会以代码块的形式呈现，以便于区分普通文本和代码。
`hugo server -D`

### 代码块的显示
如果您在两组``````之间包含内容，则该内容将被视为代码块，并根据您的环境或网站的设置来呈现。

代码块的种类有toml/sh/html

### 从其他来源引入的内容
大于号加空格，将显示一条引文，这条引文在显示时前面将多出一条红色竖线。

> 这是一条引文。

当有多行前面都有大于号加空格时，多行也将被视为一条引文，显示为一行。
> 这是引文第一行。
> 这是第二行。

###
三条连续横杠将绘制一条分隔线，横线前后要加上空行

---

### 无序序列
一个星号加空格将创建一条无序列表，以点作为分隔。也可以只有一条序列！
* 这是一条无序序列

### 有序序列
数字加点加空格，将创建一条有序序列。创建多条序列时，数字都写1，以便于在中间插入序列。
1. 这是有序序列
1. 这是有序序列。

### 表格
```
| ID  | Make      | Model   | Year |
| --- | --------- | ------- | ---- |
| 1   | Honda     | Accord  | 2009 |
| 2   | Toyota    | Camry   | 2012 |
| 3   | Hyundai   | Elantra | 2010 |
```

| ID  | Make      | Model   | Year |
| --- | --------- | ------- | ---- |
| 1   | Honda     | Accord  | 2009 |
| 2   | Toyota    | Camry   | 2012 |
| 3   | Hyundai   | Elantra | 2010 |

使用冒号进行对齐；
分隔线左侧加冒号，左对齐；
分隔线右侧加冒号，右对齐；
分隔线两侧加冒号，居中对齐
```
| Tables      | Are           | Cool         |
|:----------- |:-------------:| ------------:|
| align: left | align: center | align: right |
| align: left | align: center | align: right |
| align: left | align: center | align: right |
```

| Tables      | Are           | Cool         |
|:----------- |:-------------:| ------------:|
| align: left | align: center | align: right |
| align: left | align: center | align: right |
| align: left | align: center | align: right |

表格中支持加粗、倾斜等效果
```
| Inline     | Markdown  | In                | Table      |
| ---------- | --------- | ----------------- | ---------- |
| *italics*  | **bold**  | ~~strikethrough~~ | `code`     |

```
| Inline     | Markdown  | In                | Table      |
| ---------- | --------- | ----------------- | ---------- |
| *italics*  | **bold**  | ~~strikethrough~~ | `code`     |

