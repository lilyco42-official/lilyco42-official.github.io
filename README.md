# lilyco42-official.github.io
个人经验撰写存放处
gh repo create 
仓库名称:用户名.github.io
类型：公开
scoop 安装 hugo
scoop install  hugo-extended
 tips:只有 Hugo extended 才能编译 SCSS。
🚀 第一步：确认 Hugo 正常

在当前终端运行：

hugo version

你应该看到：

hugo v0.156.0
🚀 第二步：在当前仓库初始化 Hugo

⚠️ 你现在已经在 GitHub Pages 仓库里
所以 不要 hugo new project（否则会多一层目录）

直接执行：

hugo new site . --force

意思是：

在当前目录生成 Hugo 结构
🚀 第三步：安装主题（我们用开发者最爱的 Stack）
git submodule add https://github.com/CaiJimmy/hugo-theme-stack.git themes/stack

然后打开：

hugo.toml

改成：

baseURL = "https://lilyco42-official.github.io/"
languageCode = "zh-cn"
title = "Lilyco42 DevLog"
theme = "stack"
🚀 第四步：启动本地预览
hugo server -D

浏览器打开：

http://localhost:1313

你会看到博客已经跑起来了 🎉

✍️ 第五步：创建你的第一篇开发日志

执行：

hugo new posts/elysia-image-board-day01.md

打开这个文件，把内容改成：

---
title: Day 01 - 项目初始化
date: 2026-02-24
draft: false
tags: ["Elysia", "Bun", "开发日志"]
---


保存后刷新网页 ✅

🧪 第六步：生成静态文件
hugo

会生成：

/public
🌍 第七步：推送上线 GitHub Pages
git add .
git commit -m "init hugo blog"
git push

几秒后访问：

https://lilyco42-official.github.io

博客就上线了 🎉



以后只要：

① 启动博客
hugo server -D
② 创建新日志
hugo new posts/day02-auth.md
③ 写今天干了什么
④ 发布
hugo
git add .
git commit -m "day02"
git push

