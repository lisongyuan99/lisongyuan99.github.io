---
title: 开始使用 Hexo
date: 2020-10-18 17:55:33
tags: 
  - Hexo
categories: 
  - [前端, Hexo]
---

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 [Markdown](http://daringfireball.net/projects/markdown/)（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

<!--more-->

## 步骤

1. 安装，初始化hexo环境
   
   ```bash
   npm install -g hexo-cli
   hexo init [folder]
   ```
   
2. 新建一个页面

   ```bash
   hexo new page --path /front-end/hexo/hexo-start
   ```

   将新建  `/source/_posts/front-end/hexo/hexo-start.md` 文件

   部署后的url是 `年/月/日/front-end/hexo/hexo-start` ，可通过调整 _config.yml设置

3. 调试

   ```bash
   hexo server
   ```

   默认 localhost:4000

