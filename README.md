# lisongyuan99.github.io

master: 博客的源文件

gh-pages: 部署文件

`_config.yml`

``` yml
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site
title: 李西西的屎山
subtitle: ''
description: ''
keywords:
author: 李西西
language: zh-CN
timezone: ''

# URL
## If your site is put in a subdirectory, set url as 'http://example.com/child' and root as '/child/'
url: https://blog.lsy99.cn
root: /
# permalink: :year/:month/:day/:title/
permalink: posts/:title/
permalink_defaults:
pretty_urls:
  trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
  trailing_html: true # Set to false to remove trailing '.html' from permalinks

# Directory
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render:

# Writing
new_post_name: :title.md # File name of new posts
default_layout: post
titlecase: false # Transform title into titlecase
external_link:
  enable: true # Open external links in new tab
  field: site # Apply to the whole site
  exclude: ''
filename_case: 0
render_drafts: false
post_asset_folder: true
relative_link: false
future: true
highlight:
  enable: true
  line_number: true
  auto_detect: false
  tab_replace: ''
  wrap: true
  hljs: false
prismjs:
  enable: false
  preprocess: true
  line_number: true
  tab_replace: ''

# Home page setting
# path: Root path for your blogs index page. (default = '')
# per_page: Posts displayed per page. (0 = disable pagination)
# order_by: Posts order. (Order by date descending by default)
index_generator:
  path: ''
  per_page: 10
  order_by: -date

# Category & Tag
default_category: uncategorized
category_map:
tag_map:

# Metadata elements
## https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
meta_generator: true

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD
time_format: HH:mm:ss
## updated_option supports 'mtime', 'date', 'empty'
updated_option: 'mtime'

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10
pagination_dir: page

# Include / Exclude file(s)
## include:/exclude: options only apply to the 'source/' folder
include:
exclude:
ignore:

# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: next

# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
- type: git
  repo: git@github.com:lisongyuan99/lisongyuan99.github.io.git
  branch: gh-pages
- type: git
  repo: git@175.24.31.49:/var/repo/hexo.git
  branch: master
- type: baidu_url_submitter

# 内置搜索
search:
  path: search.xml
  field: post
  content: true
  format: html

disable_baidu_transformation: true
index_with_subtitle: true

# 自动 nofollow
nofollow:
  enable: true
  field: site

# 站点地图
sitemap:
  path: sitemap.xml
baidusitemap:
  path: baidusitemap.xml

# emoji
githubEmojis:
  enable: true
  className: github-emoji
  inject: true

baidu_url_submit:
  count: 1 ## 提交最新的一个链接
  host: blog.lsy99.cn ## 在百度站长平台中注册的域名
  token:  ## 请注意这是您的秘钥， 所以请不要把博客源代码发布在公众仓库里!
  path: baidu_urls.txt ## 文本文档的地址， 新链接会保存在此文本文档里
```

注意更改百度token



`_config.next.yml`

``` yml
# scheme: Muse
# scheme: Mist
scheme: Pisces
# scheme: Gemini
language: zh-CN
footer:
  since: 2019
  powered: false
  beian:
    enable: true
    icp: 黑ICP备 20000491号-1
    gongan_id: 23010302000977
    gongan_num: 黑公网安备 23010302000977号
    gongan_icon_url: /images/beian-icon.svg
  icon:
    # name: fa fa-user
    animated: true
    # color: "#808080"

# 何时显示菜单栏
sidebar:
  # display: post
  display: always

# 侧边菜单栏
menu:
  home: / || fa fa-home
  archives: /archives/ || fa fa-archive
  tags: /tags/ || fa fa-tags
  categories: /categories/ || fa fa-th
  about: /about/ || fa fa-user
  # sitemap: /sitemap.xml || fa fa-sitemap
  # schedule: /schedule/ || fa fa-calendar

# 侧边栏头像
avatar:
  url: /images/avatar.png
  # 圆的
  # rounded: true
  #旋转
  # rotated: true

# 侧边栏 社交
social:
  GitHub: https://github.com/lisongyuan99 || fab fa-github
  E-Mail: mailto:lsy114514@hotmail.com || fa fa-envelope
  # Weibo: https://weibo.com/yourname || fab fa-weibo
  # Google: https://plus.google.com/yourname || fab fa-google
  # Twitter: https://twitter.com/yourname || fab fa-twitter
  # FB Page: https://www.facebook.com/yourname || fab fa-facebook
  # StackOverflow: https://stackoverflow.com/yourname || fab fa-stack-overflow
  # YouTube: https://youtube.com/yourname || fab fa-youtube
  # Instagram: https://instagram.com/yourname || fab fa-instagram
  # Skype: skype:yourname?call|chat || fab fa-skype
social_icons:
  enable: true
  icons_only: false
  transition: true


# Github 章鱼猫
github_banner:
  enable: true
  permalink: https://github.com/lisongyuan99
  title: Follow me on GitHub

# 阅读进度条
reading_progress:
  enable: true
  # color: "#FC6423"
  color: "#222222"
  height: 2px

# 回到顶部
back2top:
  enable: true
  scrollpercent: true
  # sidebar: true

# tag从井号换图标 
tag_icon: true

# 谷歌日历
# calendar:
#   calendar_id: 
#   api_key: 
#   orderBy: startTime
#   showLocation: false
#   offsetMax: 72
#   offsetMin: 4
#   showDeleted: false
#   singleEvents: true
#   maxResults: 250

toc:
  number: false

# Local search
# Dependencies: https://github.com/next-theme/hexo-generator-searchdb
local_search:
  enable: true
  # If auto, trigger search by changing input.
  # If manual, trigger search by pressing enter key or search button.
  trigger: auto
  # Show top n results per article, show all results by setting to -1
  top_n_per_article: 1
  # Unescape html strings to the readable one.
  unescape: false
  # Preload the search data when the page loads.
  preload: false

# 查看大图
fancybox: true
vendors:
  fancybox: //cdn.jsdelivr.net/gh/fancyapps/fancybox@3/dist/jquery.fancybox.min.js
  fancybox_css: //cdn.jsdelivr.net/gh/fancyapps/fancybox@3/dist/jquery.fancybox.min.css

favicon:
  small: /images/favicon/favicon-16x16.png
  medium: /images/favicon/favicon-32x32.png
  apple_touch_icon: /images/favicon/apple-touch-icon.png
  safari_pinned_tab: /images/favicon/safari-pinned-tab.svg
  android_manifest: /images/favicon/manifest.json
  ms_browserconfig: /images/favicon/browserconfig.xml

# 数据统计
google_analytics:
  tracking_id: 
  only_pageview: false
  
baidu_analytics: 
```

注意添加 Google 和百度的id