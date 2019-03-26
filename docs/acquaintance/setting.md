# 前言

GitBook 的配置存储文件为 `book.json`。该文件可以配置本书的基本信息与安装插件等，具体配置都是可选的，如果不配置则默认输出。

```json
{
	"title": "",
	"author": "",
	"description": "",
	"language": "",
	"gitbook": "",
	"root": "",
	"links": {
	},
	"plugins": [
	],
	"pluginsConfig": {
	}
}

```

# title

设置书本的标题

```json
{
    "title" : "How to use GitBook"
}
```

# author

作者的相关信息

```json
{
  "author" : "GitBook Author"
}
```

# description

本书的简单描述

```json
{
  "description": "记录 GitBook 的基本使用"
}
```

# language

GitBook 使用的语言, 版本 `v2.6.4` 中可选的语言如下：

```
en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw
```

配置使用简体中文

```json
{
  "language" : "zh-hans"
}
```
# gitbook

指定使用的 `gitbook` 版本
```json
{
  "gitbook": "3.2.3",
  "gitbook": ">=3.0.0"
}
```
# root

指定存放 GitBook 文件（除了 book.json）的根目录

```json
{
  "root": "."
}
```

对于软件项目，你可以使用子目录（如 `docs/`）来存储项目的文档，目录结构如下：

```
.
├── book.json
└── docs/
    ├── README.md
    └── SUMMARY.md
```

在 `book.json` 中配置：

```json
{
    "root": "./docs"
}
```

# links

在左侧导航栏添加链接信息

```json
{
  "links" : {
      "sidebar" : {
          "Home" : "https://gitbook.com"
      }
  }
}
```

# styles

自定义页面样式， 默认情况下各generator对应的css文件

```json
{
  "styles": {
      "website": "styles/website.css",
      "ebook": "styles/ebook.css",
      "pdf": "styles/pdf.css",
      "mobi": "styles/mobi.css",
      "epub": "styles/epub.css"
  }
}
```

例如使`<h1> <h2>`标签有下边框，可以在 `website.css` 中设置

```css
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
```
# plugins

配置使用的插件

```json
{
  "plugins": [
      "disqus"
  ]
}
```

添加新插件之后需要运行`gitbook install`来安装新的插件  

GitBook默认带有5个插件：
* highlight
* search
* sharing
* font-settings
* livereload

如果要去除自带的插件， 可以在插件名称前面加 `-`

```json
{
  "plugins": [
      "-search"
  ]
}
```
# pluginsConfig

配置插件的属性

```json
{
  "pluginsConfig": {
      "disqus": {
          "shortName": "XXXXXXX"
      }
  }
}
```

# structure

指定 Readme、Summary、Glossary 和 Languages 对应的文件名，下面是这几个文件对应变量以及默认值：

| 变量 | 含义和默认值 |
|:----:|:----:|
|`structure.readme` | `Readme file name (defaults to README.md)` |
|`structure.summary` | `Summary file name (defaults to SUMMARY.md)`|
|`structure.glossary`| `Glossary file name (defaults to GLOSSARY.md)` |
|`structure.languages`| `Languages file name (defaults to LANGS.md)`|

# .gitignore

在 GitBook 中，你可以在根目录增加 `.gitigonre` 或 `.bookignore` 或 `.ignore` 来进行忽略文件。这样，GitBook 就不对读取该文件了，下面是
文件内容示例，可以忽略 `test.md` 文件和 `bin` 目录下的所有文件：

```
# This is a comment

# Ignore the file test.md
test.md

# Ignore everything in the directory "bin"
bin/*
```