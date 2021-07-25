---
layout: post
title: 一张报纸引起的布局思考
tags: css
date: 2021-7-25
---
# 思考背景
+ 早上看到一份报纸，突发灵感如何实现这种布局呢？🤔

<img src="{{site.url}}/assets/img/newpapers/IMG_20210724_063838.jpg" alt="newspaper" style="zoom:40%;" />

## 过程
1. 像文本流之类的用浮动可以做，但是有问题。用浮动来解决问题会出现很多麻烦
> 浮动要用很多盒子来解决。

2. 我们有什么新的属性呢？
3. 有的！多列属性（Multi-column Layout Module）
4. 来看语法:

| columns                      | CSS3 | 无   | 设置或检索对象的列数和每列的宽度。复合属性 |
| ---------------------------------------------- | ---- | ---- | ------------------------------------------ |
| column-width               | CSS3 | 无   | 设置或检索对象每列的宽度                   |
| column-count               | CSS3 | 无   | 设置或检索对象的列数                       |
| column-gap                   | CSS3 | 无   | 设置或检索对象的列与列之间的间隙           |
| column-rule                 | CSS3 | 无   | 设置或检索对象的列与列之间的边框。复合属性 |
| column-rule-width     | CSS3 | 无   | 设置或检索对象的列与列之间的边框厚度。     |
| column-rule-style     | CSS3 | 无   | 设置或检索对象的列与列之间的边框样式。     |
| column-rule-color     | CSS3 | 无   | 设置或检索对象的列与列之间的边框颜色。     |
| column-span                 | CSS3 | 无   | 设置或检索对象元素是否横跨所有列。         |
| column-fill                 | CSS3 | 无   | 设置或检索对象所有列的高度是否统一。       |
| column-break-before | CSS3 | 无   | 设置或检索对象之前是否断行。               |
| column-break-after   | CSS3 | 无   | 设置或检索对象之后是否断行。               |
| column-break-inside | CSS3 | 无   | 设置或检索对象内部是否断行。               |

> 注意: column-break-before,column-break-after, column-break-inside。chorme兼容性比较差，要加浏览器前缀！ie 10以上支持！

+ 实例代码 [codepen](https://codepen.io/cai_kai/pen/KKmZPwx)
<iframe height="500" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/cai_kai/embed/KKmZPwx?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/cai_kai/pen/KKmZPwx">
  </a> by 山子安 (<a href="https://codepen.io/cai_kai">@cai_kai</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


+ [兼容性比较](https://caniuse.com/?search=column)
> 多列布局的后面三个断行兼容性比较差，要加前缀！ie 6-9不支持！

# 总结
+ 目前关于colmns布局做的网站没怎么看到，这个语法我在很多网站都没怎么找到。但是做一些杂志和报纸一类的比较适合！