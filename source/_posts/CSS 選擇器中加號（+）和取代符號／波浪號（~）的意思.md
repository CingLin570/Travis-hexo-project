---
title: CSS 選擇器中加號（+）和取代符號／波浪號（~）的意思
date: 2021-2-14 11:05:53
tags: css
categories: css
---
# CSS中的加號(+)

讓我們先來看一下加號，加號影響的是同一階層（siblings）的標籤，例如，div + p指的是直接影響到div後的p，而div和p是屬於同一層的
為了方便大家理解，我們直接來看一下範例吧！
<!-- more -->
我們的html結構長這樣：

```html
<div>
    <p>One</p>
    <div>Two</div>
    <p>Three</p>
</div>

<div>
    <div>Four</div>
    <div><p>Five</p></div>
    <p>Six</p>
    <p>Seven</p>
</div>
```
接著，我在STYLE的地方，加入如下的CSS:

```css
div + p{
            font-size:50px;
        }
```

這時候有哪些字體會變大呢？結果如下：
我們可以看到Three和Six都變大了，之所以Three和Six會變大，是因為CSS是選擇div + p，所以所有在同一階層（siblings）的情況下，如果是div接著碰到的p，都會受到影響。

<iframe height="265" style="width: 100%;" scrolling="no" title="CSS中的加號(+)" src="https://codepen.io/pvzfeusk/embed/OJbWogd?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/pvzfeusk/pen/OJbWogd'>CSS中的加號(+)</a> by 胡謦麟
  (<a href='https://codepen.io/pvzfeusk'>@pvzfeusk</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

# CSS中的取代符號(~)

那麼取代符號（~）呢？（註：我查了一下google才知道這個符號叫做取代符號）。

取代符號其實和加號用法很類似，只是加號只會影響到下一個同階層的元素，但是取代符合則是影響到下一個同階層的所有元素。用中文說實在非常難解釋...，還是讓我們看一下例子。

我們用一樣的HTML結構，只是現在把CSS換成如下：

```css
div ~ p{
            font-size:50px;
        }
```

這時候的結果會長這樣子：

<iframe height="265" style="width: 100%;" scrolling="no" title="CSS中的取代符號(~)" src="https://codepen.io/pvzfeusk/embed/PobWdJV?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/pvzfeusk/pen/PobWdJV'>CSS中的取代符號(~)</a> by 胡謦麟
  (<a href='https://codepen.io/pvzfeusk'>@pvzfeusk</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

這時候連Seven也跟著變大了，Seven之以跟著變大是因為seven同樣是在div之後的p（碰到的第二個p），在上面加號的例子中，div + p只會影響到div之後的第一個p，不會影響到後續的p，但如果使用的是div~p，則div後面的p都能夠有影響。

總結來說，
p+p：同一層中，p後面的第一個p；
p~p：同一層中，p後面的所有p。
