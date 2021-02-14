---
title: CSS 選擇器中大於符號是什麼意思?
date: 2021-2-14 17:23:55
tags: css
categories: css
---

# CSS大於符號

CSS選擇器中的大於（>）是什麼意思？
在編輯網頁CSS的時候，有時候我們會看到大於（>）的符號，究竟這個符號代表什麼意思呢？

這個符號其實相當容易理解，你可以把它想成直接的小孩(direct descendant/child)，而平常比較容易看到的空格（space）則是所有小孩的意思。

這是什麼意思呢？讓我們看個範例比較容易理解。
<!-- more -->
假設我先寫一個html文件，如下：

```html
<div class="container">
    <div>This is the first child</div>
    <div><p>This is the second child</p></div>
    <p>This is the third child</p>
</div>
```
接下來，我們分別套用不同的CSS來看看會有什麼不同的效果。

<iframe height="265" style="width: 100%;" scrolling="no" title="LYbxMVy" src="https://codepen.io/pvzfeusk/embed/LYbxMVy?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/pvzfeusk/pen/LYbxMVy'>LYbxMVy</a> by 胡謦麟
  (<a href='https://codepen.io/pvzfeusk'>@pvzfeusk</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

因為大於（>）只會影響到直接的小孩，所以在container之後，直接碰到p的只有third，所以結果就是只有third的字體會變大。


接下來，我們試試看常用的「空格（space）」，我把css改成：

<iframe height="265" style="width: 100%;" scrolling="no" title="CSS 大於符號" src="https://codepen.io/pvzfeusk/embed/bGBgOEz?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/pvzfeusk/pen/bGBgOEz'>CSS 大於符號</a> by 胡謦麟
  (<a href='https://codepen.io/pvzfeusk'>@pvzfeusk</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

因為沒有指定要直接的小孩，所以只要是container裡面，所有p的標籤的字體都會變大，結果如下：

最後，如果我在css的地方只選擇container呢，像這樣的話：

<iframe height="265" style="width: 100%;" scrolling="no" title="CSS 類別選擇器" src="https://codepen.io/pvzfeusk/embed/qBqRLZm?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/pvzfeusk/pen/qBqRLZm'>CSS 類別選擇器</a> by 胡謦麟
  (<a href='https://codepen.io/pvzfeusk'>@pvzfeusk</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

希望這樣的說明，能夠幫助大家更瞭解css中大於這個符號的意思。

CSS-Tricks的這一張圖清楚的說明了>和空格的差異：

![](https://i.imgur.com/935Lbrj.png)