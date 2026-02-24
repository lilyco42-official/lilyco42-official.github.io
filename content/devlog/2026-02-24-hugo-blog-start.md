+++
date = '2026-02-24T15:49:17+08:00'
draft = false
title = 'Hugo 博客启动'
tags = ["Hugo", "博客搭建", "开发日志"]
categories = ["开发日志"]
description = "从 0 开始搭建个人开发博客"
+++

## 🎯 今日目标

把 Hugo 博客成功跑起来，并理解基本结构。

---

## ✅ 完成内容

- 安装 hugo extended
- 使用 Stack 主题
- 修复 SCSS 构建错误
- 本地运行成功
- 创建第一篇 devlog

现在可以通过：
hugo server -D


在本地访问博客。

---

## ❌ 遇到的问题

### 1️⃣ SCSS 无法构建

报错：


this feature is not available in your current Hugo version


原因：

使用了普通版 Hugo，需要 extended 版本。

解决：


scoop install hugo-extended


---

### 2️⃣ avatar 配置导致模板报错

helper/image 期望字符串路径，但我使用了对象配置。

最终改为：
#hugo.toml
[params.sidebar]
subtitle = "开发日志型博客"
avatar = "img/avatar.png"

avatar = "img/avatar.png"


并放入：


assets/img/avatar.png


---

## 🧠 学到的东西

- Hugo 分为普通版和 extended 版
- Stack 主题依赖 Hugo Pipes
- static 目录用于放不会被处理的资源
- archetype 可以用于生成文章模板

---

## 🚀 下一步计划

- 配置 GitHub Pages 自动部署
- 自定义首页
- 设计开发日志文章模板
- 添加 About 页面