---
title: gulp安裝流程
date: 2021-2-28 18:03:35
tags: gulp
categories: gulp
---

# gulp 環境安裝流程

## 影片教學(請不會使用 gulp 的新手，直接看這部)
<!-- more -->
{%youtube mZnMsYVHUkA %}

### 步驟一：安裝 [Node.js](https://nodejs.org/en/)，請打開終端機或命令提示字元，輸入 `node -v` 後按 Enter，看是否有顯示版本號

![](https://i.imgur.com/tMn6b6n.gif)

PS1：Mac 請按 command+空白鍵，輸入「terminal」打開終端機
PS2：Win 請按 開始 > 執行 > 輸入「cmd」打開命令提示字元
Win10 執行視窗快速鍵為 win + R:
![](https://i.imgur.com/xM3UOZG.jpg)

![](https://i.imgur.com/fEKbeaR.png)


在版本號較新的 Win10 也可在左下搜尋欄輸入 cmd 打開命令提示字元:
![](https://i.imgur.com/UsXljox.jpg)


### 步驟二：在終端機安裝 gulp，繼續輸入指令 `npm i gulp@4 -g` 按 Enter 安裝，輸入 `gulp -v` 查詢是否有回報版本號。

### 步驟三：下載此[資料夾](https://github.com/hexschool/web-layout-training-gulp)，並解壓縮
![](https://i.imgur.com/OYjJLXH.jpg)



### 步驟四：移動到該資料夾，cd 移動到該資料夾，如果移動成功，win 輸入指令`dir`、Mac 輸入指令 `ls`，可以觀看該資料裡的檔案列表，如下 Win 截圖。
![](https://i.imgur.com/Xl4ShdL.png)

### 步驟五：輸入指令 `npm install` 安裝插件

### 步驟六：輸入指令 `gulp `執行

### 步驟七：若步驟六執行成功，會打開瀏覽器，看到下方畫面，就代表你全部都成功了！


![](https://i.imgur.com/QvvDPZS.png)


## 步驟八：如果你都做完了，要將網頁部署到 GitHub Pages ，請上傳 dist 資料夾，流程請觀看[影片，從 40 秒開始觀看](https://www.youtube.com/watch?v=pa4Ydm7WT9k&feature=youtu.be)留意相關細節，



## QA

### 步驟一 常見問答
Q：windows 安裝 node.js 以後，輸入 node -v 沒顯示版本號怎麼辦？？
A：請重新開機再嘗試

Q：Windows 的命令提示字元怎麼快速開啟？
A：請到 開始 > 執行 > 輸入 `cmd` 就可直接開啟


### 步驟二 常見問答
Q：我是 Mac，安裝沒有成功怎麼辦？
A：指令請換成 `sudo npm i gulp@4 -g`


![](https://i.imgur.com/GJOw1fE.png)
