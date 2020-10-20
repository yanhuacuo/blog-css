# blog-css


``````
https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/footer.min.css

https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/buttons.min.css

https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/plugins.min.css

https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/friend.min.css

https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/my.css

https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/font.css
``````


# config

``````
inject:
  head:
  # - <link rel="stylesheet" href="/xxx.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.2/footer.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.2/buttons.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.2/plugins.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.2/friend.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.2/my.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.2/font.css">  
``````


# Mathjax实现：

``````
npm uninstall hexo-renderer-marked --save
npm install hexo-renderer-kramed --save
npm uninstall hexo-math --save
npm install hexo-renderer-mathjax --save
``````

- https://github.com/yanhuacuo/blog-css/blob/main/renderer.js

``````
function formatText(text) {
  // Fit kramed's rule: $$ + \1 + $$
  // return text.replace(/`\$(.*?)\$`/g, '$$$$$1$$$$');
  return text;
}
``````

- https://github.com/yanhuacuo/blog-css/blob/main/inline.js
``````
//  escape: /^\\([\\`*{}\[\]()#$+\-.!_>])/,
  escape: /^\\([`*\[\]()#$+\-.!_>])/,
  
....

//em: /^\b_((?:__|[\s\S])+?)_\b|^\*((?:\*\*|[\s\S])+?)\*(?!\*)/,
em: /^\*((?:\*\*|[\s\S])+?)\*(?!\*)/,
``````

# 表头

``````
---
title: Hello World
tags: 旧事
categories: 散文 
date: 2020年10月17日
updated: 2020年10月17日
comments: true
description: 
keywords: 回忆
top_img: /img/pic/05.jpg
mathjax: false
katex: false
aside: false
aplayer:
highlight_shrink: true
---
``````

# 依赖

``````
  "dependencies": {
    "hexo": "^5.0.0",
    "hexo-deployer-git": "^2.1.0",
    "hexo-generator-archive": "^1.0.0",
    "hexo-generator-category": "^1.0.0",
    "hexo-generator-index": "^2.0.0",
    "hexo-generator-search": "^2.4.1",
    "hexo-generator-tag": "^1.0.0",
    "hexo-renderer-ejs": "^1.0.0",
    "hexo-renderer-kramed": "^0.1.4",
    "hexo-renderer-mathjax": "^0.6.0",
    "hexo-renderer-pug": "^1.0.0",
    "hexo-renderer-stylus": "^2.0.1",
    "hexo-server": "^2.0.0",
    "hexo-wordcount": "^6.0.1"
  }
``````


# 文章表头

``````
---
title: 远方
tags: 旧事
categories: 散文 
date: 2020年10月17日
updated: 2020年10月17日
comments: true
description: 
keywords: 回忆
top_img: https://upimage.alexhchu.com/2020/10/17/6368b36b0e8dc.jpg
mathjax: false
katex: false
aside: false
aplayer:
highlight_shrink: true
---

一直都没有从旧梦中醒来，总觉得这场假期会有尽头。
![pic](https://upimage.alexhchu.com/2020/10/17/81c9b9b291f66.jpg)
``````
