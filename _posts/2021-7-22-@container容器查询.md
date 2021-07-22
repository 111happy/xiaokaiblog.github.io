---
layout: post
title: '@container容器查询'
tags: css
math: false
date: 2021-7-22
---

# 历史
+ 2017.6  		有开发者讨论
+ 2017 		EQCSS.js
+ 2017-2019		草案提出（开发者讨论） 	
+ 2021.3 		第一个版本chrome 支持@container和contain
+ 最低：Chromium 91.0.4459.0 并#enable-container-queries通过chrome://flags.

# 代码实例
<iframe height="500" style="width: 100%;" scrolling="no" title="grid@container" src="https://codepen.io/cai_kai/embed/ZEeZBKO?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/cai_kai/pen/ZEeZBKO">
  grid@container</a> by 山子安 (<a href="https://codepen.io/cai_kai">@cai_kai</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

+ 代码详解
```css
/* 父容器里面我们要使用contain属性来声明父容器 */
.container {
    contain: layout inline-size style;
}
/* 含义: 创建一个新的块，让浏览器与布局分割开 */
@container (max-width: 1100px){
    xx {
        xx
    }
}
/* 含义: 用法和媒体查询一样，我们可以结合新的布局grid与容器查询生动形象！😋 */
```
> [contain官方含义](https://drafts.csswg.org/css-contain-1/#:~:text=2.%20Strong%20Containment%3A%20the%20contain%20property)

# 优缺点
+ 缺点：兼容性太高。（目前）
+ 优点：可以更细致化的处理
+ 响应式问题。不根据视口，只关注容器自身，便于开发。在前端框架组件中符合高内聚低耦合的设计思想。

![兼容性]({{ site.url }}/assets/img/@container/Snipaste_2021-07-22_20-04-16.png)