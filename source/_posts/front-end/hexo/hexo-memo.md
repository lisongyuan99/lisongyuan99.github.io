---
title: Hexo 备忘录
date: 2020-10-19 17:17:32
tags: 
  - Hexo
categories: 
  - [前端, Hexo]
---

各种疑难杂症

- 端口号

<!--more-->

## QQ联网错误

Hexo 占用4000端口调试，QQ 也使用4000端口会导致无法登录

使用该语句调试

```bash
hexo s -p 40000
```

或修改 `node_modules/hexo-serve/index.js`

```js
port: 40000
```



