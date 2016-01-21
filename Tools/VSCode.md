+++
Categories = ["Tools"]
author = "sincerelywy"
comments = true
date = "2016-01-21T15:09:32+08:00"
draft = false
image = ""
menu = ""
share = true
slug = "vscode"
tags = ["tools","vscode"]
title = "VS Code使用记录"

+++

# VS Code使用记录

记录修改VS Code的配置以及快捷键。会不停的补充。

<!--more-->

## 1. 行号、字体和自动换行

```json
// Place your settings in this file to overwrite the default settings
{
    "editor.fontFamily": "Consolas",
	"editor.fontSize": 14,
    "editor.wrappingColumn": 0
}
```

wrappingColumn表示多少个字符后换行，0的话表示根据窗口显示进行换行，也就是自动换行。

## 2. 打开多个VS Code

使用快捷键`Ctrl + Shift + N`，这样不会关闭原来已经打开的实例，可以查看多个文档或者目录。对应关闭的快捷键是`Ctrl + Shift + W`。