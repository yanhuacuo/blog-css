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
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/footer.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/buttons.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/plugins.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/friend.min.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/my.css">
  - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yanhuacuo/blog-css@1.0/font.css">  
``````


Mathjax实现：

``````
npm uninstall hexo-renderer-marked --save
npm install hexo-renderer-kramed --save
npm uninstall hexo-math --save
npm install hexo-renderer-mathjax --save
``````

https://github.com/yanhuacuo/blog-css/blob/main/renderer.js

``````
function formatText(text) {
  // Fit kramed's rule: $$ + \1 + $$
  // return text.replace(/`\$(.*?)\$`/g, '$$$$$1$$$$');
  return text;
}
``````

https://github.com/yanhuacuo/blog-css/blob/main/inline.js
``````
//  escape: /^\\([\\`*{}\[\]()#$+\-.!_>])/,
  escape: /^\\([`*\[\]()#$+\-.!_>])/,
  
....

//em: /^\b_((?:__|[\s\S])+?)_\b|^\*((?:\*\*|[\s\S])+?)\*(?!\*)/,
em: /^\*((?:\*\*|[\s\S])+?)\*(?!\*)/,
``````
