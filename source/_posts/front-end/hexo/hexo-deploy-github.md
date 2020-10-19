---
title: Hexo 一键部署 Github Pages
date: 2020-10-18 18:37:20
tags: 
  - Hexo
categories: 
  - [前端, Hexo]
---

建立远程仓库添加 hooks 一键部署

<!--more-->

## 步骤

1. Github 新建 `<用户名>.github.io` 仓库

2.  新建 `gh-pages` 分支

3.  `settings->Github Pages`  选择  `gh-pages` 分支

4.  配置 `-config.yml`

   ```yml
   deploy:
   - type: git
     repo: git@github.com:<用户名>/<用户名>.github.io.git
     branch: gh-pages
   ```

5. 一键部署

   ```bash
   hexo deploy
   ```

## 补充

使用 master dev 分支存储源文件