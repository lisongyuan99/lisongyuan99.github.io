---
title: Hexo 以及 NexT 主题的设置
date: 2020-10-19 13:24:26
tags: 
  - Hexo
categories: 
  - [前端, Hexo]
---

- 切换中文
- 添加备案信息
- 右上角添加 GitHub 章鱼猫
- 更改链接格式

<!--more-->

当前版本 Hexo 5.2.0, Hexo-cli 4.2.0 中，Hexo 的配置文件在 `_config.yml` 中，主题位置文件在 `_config.<主题名称>.yml` 中。

```bash
npm install hexo-theme-next
```

安装 NexT主题

新建 `_config.next.yml`  文件用于配置主题

## 切换中文

_config.yml

```yml
language: zh-CN
```

_config.next.yml

```yml
language: zh-CN
```

## 添加备案信息

_config.next.yml

```yml
footer:
  since: 2019
  powered: true
  beian:
    enable: true
    icp: 黑ICP备 20000491号-1
    gongan_id: 23010302000977
    gongan_num: 黑公网安备 23010302000977号
    gongan_icon_url: http://static.lsy99.cn/公安.svg
```

## 右上角 GitHub 章鱼猫

~~[Hexo博客NexT主题右上角添加fork me on github入口_野猿新一-CSDN博客](https://blog.csdn.net/mqdxiaoxiao/article/details/93796367)~~

~~` themes/next/layout/_layout.swig`~~

~~添加[GitHub Corners](https://tholman.com/github-corners/)~~

` _config.next.yml`

```yml
github_banner:
  enable: true
  permalink: https://github.com/yourname
  title: Follow me on GitHub
```



## 更改链接格式

`_config.yml`

```yml
permalink: :title/
```

## 其他

[Documentation | NexT](https://theme-next.js.org/docs/)