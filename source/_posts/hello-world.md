---
layout: vue
title: Vue Cli
date: 2020-11-04 20:35:53
tags: Vue.js
categories: Vue
---
圖一
![](https://i.imgur.com/aNwSDtY.png)
<!--more-->
圖二
![](https://i.imgur.com/2M2CLCy.png)

我們在開發的過程中，會使用很多的檔案，例如jpg、png檔案等等，我們也可能有撰寫javaScript程式碼，使用到ES6的語法，在比較舊的瀏覽器就沒辦法運行，我們也可能會撰寫sass或是scss這種預處理器，還有.vue的檔案，.vue的檔案簡單來說一個檔案就是一個元件，這個元件包含了html、js、css，把這三個都結合在一起在開發上也比較容易。
(圖二)左邊是我們撰寫的檔案，右邊則是輸出的可以運行的檔案，因為我們沒辦法直接讀取像是sass、scss、.vue，所以會建立一個main.js，把所有檔案都進行關聯，除此之外還會建立一個loader，它會把所有檔案都載進來，最後還有一個output輸出檔案的位子，Webpack要做的事情就是，把這些loader跟main.js產生關聯性，再藉由Webpack編譯，雖然左邊的檔案沒辦法直接運行它，但是進行編譯之後呢，輸出之後就是瀏覽器可以運行的版本。
圖三
![](https://i.imgur.com/3YbT69U.png)

簡單來說，Webpack就是把我們開發中使用的工具和套件全部整合在一起，並且使用npm的方式來運行。

![](https://i.imgur.com/Hwd3OXK.png)
## SPA

簡單來說就是由前端模擬的路由，那麼(路由)我們可以想像成一個網址，目前我們看到的網頁都是由後端決定的路由，SPA呢就是由前端所決定的路由，會在/後面加上#字號，#字號後面的user，就是我們實際運行的網址，實際上呢也只會切換#字號後面的網址，頁面也會跟著做更換；通常後端決定的路由在網頁切換的時候會有一個閃爍的感覺，如果使用前端決定的路由，更能提升使用者體驗
![](https://i.imgur.com/0I2f0yJ.png)

![](https://i.imgur.com/G7i5GJK.png)



## 安裝 Node.js
目前有許多前端開發環境都是基於 Node.js，如 Gulp、Webpack、Parcel...，或是任何主流框架（Vue、React、Angular）的 CLI 也都是基於此服務。本次要介紹的 Vue Cli 自然也不例外。

進入官網安裝 [Node.js](https://nodejs.org/en/)，請打開終端機或命令提示字元，輸入 `node -v` 後按 Enter，看是否有顯示版本號。

![](https://i.imgur.com/tMn6b6n.gif)

> Mac 請按 command+空白鍵，輸入「terminal」打開終端機
> Win 請按 開始 > 執行 > 輸入「cmd」打開命令提示字元
Win10 執行視窗快速鍵為 win + R:

![](https://i.imgur.com/xM3UOZG.jpg)

![](https://i.imgur.com/fEKbeaR.png)

在版本號較新的 Win10 也可在左下搜尋欄輸入 cmd 打開命令提示字元:

![](https://i.imgur.com/UsXljox.jpg)

請確保 Node.js 在第 9 版以上（官方建議：`8.11.0+`）。

## Vue CLI 安裝

![](https://i.imgur.com/6uhIFx9.png)
`npm install -g @vue/cli` 是使用全域的環境建立vue。

![](https://i.imgur.com/yMyJDBy.png)
到了這裡基本上Vue CLI就已經下載完成，Vue CLI的運行方式有兩種，第一種是使用指令的方式終端機(terminal)，另一種是使用vue ui的方式，在這裡我們使用ui的方式來運行。

![](https://i.imgur.com/govrlEi.png)

第一次開發的話進來基本上不會有內容，再來點擊新增

![](https://i.imgur.com/qcddG6a.png)

![](https://i.imgur.com/WuZKKWy.png)

![](https://i.imgur.com/EFgn5e4.png)

![](https://i.imgur.com/W2SUt8U.png)
這邊是課程建議開啟的功能:

Babel:在撰寫js的時候很常使用ES6的語法，為了確保這些語法在所有的瀏覽器能夠正確運行。


TypeScript: js的預處理器。

Router:建議直接在Vue CLI的部分直接啟用，在之後使用上也比較方便，會直接給一個初始的loader環境，以後實作就不用手動開啟。

Vuex:資料狀態管理的工具

CSS Pre-processors:CSS的預處理器。

Linter/Formatter:檢查程式碼有沒有排整齊，建議開啟。

最後面兩個是測試工具

![](https://i.imgur.com/h6IsXJ9.png)

History Mode 切記不要開啟，當開啟之後呢，私服器必須做額外的設定才能運行(開了老師不會幫我們改作業)。
![](https://i.imgur.com/TBBnPmj.png)
直接新增不儲存

![](https://i.imgur.com/ry3yPxI.png)
開發使用的話大多使用前兩個

![](https://i.imgur.com/yw5EEs9.png)
node_modules:這是我們所安裝的套件包含sass(scss)、.vue檔案這些功能都是安裝在這裡

public:這個資料夾是公開的資料夾，這個資料夾的內容都不會被編譯，像是.png、.jpg的檔案就很適合放在這裡面

![](https://i.imgur.com/HBll11c.png)
雖然不會被編譯，但index.html呢實際上編譯的時候，會做一些些調整，像我們編譯完會進行一些插入，css、js就會插入到html裡面

![](https://i.imgur.com/Vj11447.png)
再來我們還會有更目錄下的檔案，就是我們運行的環境

package.json:安裝套件所記錄的檔案
