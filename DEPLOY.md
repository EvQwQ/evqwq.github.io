# 部署到 GitHub Pages

## 步骤 1：创建 GitHub 仓库

1. 登录 GitHub (https://github.com)
2. 点击右上角 "+" → "New repository"
3. 仓库名填写：`yourusername.github.io`（将 yourusername 替换为你的 GitHub 用户名）
4. 选择 "Public"（公开）
5. 点击 "Create repository"

## 步骤 2：推送代码到 GitHub

```bash
cd myblog
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

## 步骤 3：启用 GitHub Pages

1. 在仓库页面，点击 "Settings"
2. 左侧菜单选择 "Pages"
3. "Source" 选择 "Deploy from a branch"
4. "Branch" 选择 "main" 和 "/ (root)"
5. 点击 "Save"

等待几分钟，访问 `https://yourusername.github.io` 即可看到你的博客！

## 更新博客

创建新文章：
```bash
hugo new content posts/文章标题.md
```

编辑文章后重新构建并推送：
```bash
hugo --minify
git add .
git commit -m "更新博客"
git push
```

## 本地预览

```bash
hugo server -D
```
然后在浏览器打开 http://localhost:1313
