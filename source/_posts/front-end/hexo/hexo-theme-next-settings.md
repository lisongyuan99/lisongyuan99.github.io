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

