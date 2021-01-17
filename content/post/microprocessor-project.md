---
title: "微處理機期末專題"
date: 2021-01-13T13:20:53+08:00
categories:
- 
tags:
- tag1
- tag2
slug: microprocessor-project
thumbnailImage: https://images.unsplash.com/photo-1514031231291-fee925070a61?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=1950&q=80
thumbnailImagePosition: left
coverImage: https://images.unsplash.com/photo-1514031231291-fee925070a61?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=1950&q=80
coverCaption: ""
coverSize: partial
keywords:
-
#thumbnailImage: //example.com/image.jpg
---
用 STM32 開發板做一台類似投籃機的遊戲機台！
<!--more-->
這次僅做簡單的紀錄。
## 開發過程寫的文件
### 專題提案
知道到底要做什麼是首要之務。<br>
<a href="https://github.com/kanido386/playground/blob/master/microprocessor-project/專題提案.pdf" target="_blank">這是專題提案～</a>

### 實作方向
開始行動前，如果能先有個大概方向，往往更有利於進度的推進。<br>
後來我又列出實作細節，非常 detailed 的那種，這不但讓我克服了拖延，也讓我因為能更容易地各個擊破而產生很大的成就感！<br>
<a href="https://github.com/kanido386/playground/blob/master/microprocessor-project/實作方向.pdf" target="_blank">這是實作方向～</a>

## 用影片來記錄
### 前一天測試
終於花非常多時間弄完有的沒的事情以後，來進行個測試。
<iframe width="560" height="315" src="https://www.youtube.com/embed/dAJFhHayooc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### demo當天再測試
在教授和助教們來評分以前，趕快再來測試一番，出了什麼差錯就功虧一簣了！
<iframe width="560" height="315" src="https://www.youtube.com/embed/M_ND80FLdWY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### 機台拆解
期末展結束以後要把所有器材還給助教，不得不拆解這個花我非常多心思的機台 😢<br>
剩下的紙箱、杯子留著也不能做什麼，只好回收掉⋯⋯
<iframe width="560" height="315" src="https://www.youtube.com/embed/jmL-ML8BDvc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 一些照片
<figure>
  <img src="https://i.imgur.com/4S5wvKm.jpg" style="width:30vw;" />
  <figcaption>來玩機台囉！</figcaption>
</figure>
<figure>
  <img src="https://i.imgur.com/vXYNK6y.jpg" style="width:30vw;" />
  <figcaption>挖掉杯子底部，讓球通過</figcaption>
</figure>
<figure>
  <img src="https://i.imgur.com/qbR9bUC.jpg" style="width:30vw;" />
  <figcaption>機台是放斜的，這樣可以讓球滾下來</figcaption>
</figure>
<figure>
  <img src="https://i.imgur.com/jPt5Qn1.jpg" style="width:30vw;" />
  <figcaption>這就是最麻煩無趣的部分：接線（機台裡面超亂）</figcaption>
</figure>

## 至少程式碼不會和我分開
<a href="https://github.com/kanido386/playground/tree/master/microprocessor-project" target="_blank">這是專案資料夾～</a><br>
只需要看 `/final-project/src/` 裡面的 code 就行囉！<br>
（邏輯的部分在 `main.c` 裡面～）<br>
<br>
原本我是用一個叫 SystemWorkbench 的 IDE 來開發，但後來發現，其實用 Visual Studio Code 來寫 code 會比較有效率，能不能同時縮排很多行 code 真的差非常多！<br>
（GitHub 上面呈現 code 的縮排看起來有點恐怖，就不要計較了啦 😂）<br>
<br>
<br>
今天的分享就到這邊，我們下篇文見吧 😃