---
title: "如何搭建 Hugo 博客"
date: 2026-03-18T13:30:00+08:00
draft: false
categories: ["技术", "教程"]
tags: ["hugo", "github-pages"]
---

本文将详细介绍如何使用 Hugo 搭建一个漂亮的博客，并部署到 GitHub Pages。

## 什么是 Hugo？

Hugo 是一个用 Go 语言编写的静态网站生成器，以**极速构建**著称。它使用 Markdown 格式编写内容，通过主题模板生成 HTML 页面。

## 安装 Hugo

### Windows
```bash
winget install Hugo.Hugo
```

### macOS
```bash
brew install hugo
```

## 创建新站点

```bash
hugo new site myblog
cd myblog
git init
```

## 添加主题

```bash
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo "theme = 'ananke'" >> hugo.toml
```

## 创建文章

```bash
hugo new content posts/hello.md
```

## 本地预览

```bash
hugo server -D
```

访问 http://localhost:1313 预览。

## 部署到 GitHub Pages

1. 创建仓库 `username.github.io`
2. 启用 GitHub Actions
3. 推送代码

更多细节请参考官方文档。
