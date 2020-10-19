---
title: Hexo 一键部署到云服务器
date: 2020-10-18 22:35:49
tags: 
  - Hexo
categories: 
  - [前端, Hexo]
---

 多分支备份源文件，部署到 Github Pages

<!--more-->

## 步骤

1.  搭建远程裸仓库

   [搭建Git服务器 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600/899998870925664)

2. git用户提权

   ```bash
   chmod 740 /etc/sudoers
   vim /etc/sudoers
   ```
   添加git一行

   ```
   ## Allow root to run any commands anywhere
   root    ALL=(ALL)     ALL
   git     ALL=(ALL)     ALL
   ```

   ```
   chmod 400 /etc/sudoers
   ```

3. 添加文件夹，Hexo 生成静态文件的位置

   ```bash
   mkdir /srv/hexo
   chown -R git:git /srv/hexo
   chmod -R 755 /srv/hexo
   ```

4. 添加 hooks 脚本

   ```bash
   vim /var/repo/hexo.git/hooks/post-receive
   ```

   加入脚本中，收到提交之后把默认分支的工作空间复制到 `/srv/hexo`

   ```
   #!/bin/bash
   git --work-tree=/srv/hexo --git-dir=/var/repo/hexo.git checkout -f
   ```

   更改权限

   ```bash
   chown -R git:git /var/repo/hexo.git/hooks/post-receive
   chmod +x /var/repo/hexo.git/hooks/post-receive
   ```

5. 本地 `_config.yml` 添加部署仓库分支

   ```yml
   deploy:
   - type: git
     repo: git@github.com:<用户名>/<用户名>.github.io.git
     branch: gh-pages
   - type: git
     repo: git@<服务器地址>var/repo/hexo.git
     branch: master
   ```

