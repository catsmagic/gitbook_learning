# **文件结构**

* README.md
* SUMMARY.md
* package.json
* _book文件夹
* book.json
* bookignore文件夹
* 章节文件夹

---

## 1. README.md & SUMMARY.md

由gitbook init 自动生成的文件，README进行文档介绍，SUMMARY进行章节目录的编写。

本书SUMMARY.md如下：

```
# Summary

* [Introduction](README.md)
* [Chapter 0 前言](chapter0/README.md)
* [Chapter 1 环境配置](chapter1/README.md)
* [Chapter 2 文件结构](chapter2/README.md)
* [Chapter 3 基本语法](chapter3/README.md)

```

## 2. package.json

继续进行npm init 自动生成的文件，文件名从字面意思上看，应该为打包所有文件为电子书的意思。

通过文件里的scripts的设置，可以进行命令的等效。如**npm run** serve = **gitbook** serve。

```
"scripts": {
    "serve": "gitbook serve",
    "build": "gitbook build",
    "install": "gitbook install",
    "clean": "gitbook clean",
    "lint": "gitbook lint",
    "ls": "gitbook ls",
    "new": "gitbook new",
    "pdf": "gitbook pdf",
    "summary": "gitbook summary",
    "serve:watch": "gitbook serve --watch"
  }
```

## 3. _book文件夹

通过serve或build自动打包生成的含html等静态文件的文件夹，**gitbook的输出结果**。

build仅生成相关文件。

serve命令同时生成网页预览，一般在4000端口，在serve关闭前无法对电子书进行更改。

## 4. book.json

用户自己创建的电子书配置文件，内容在gitbook官网上有示例，有待摸索。

## 5. bookignore文件夹

用户自己创建的文件，文件中的内容在打包成电子书时将不被考虑，似注释作用？

注：JSON语言不允许注释。

## 6. 章节文件夹

用户在根目录下自己创建的文件夹，里面放置章节内容。

在SUMMARY.md中设置章节链接时，文件路径为 **章节文件夹/文件.md。**
