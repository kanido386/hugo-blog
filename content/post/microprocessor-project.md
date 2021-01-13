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
  <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7dc537d8-b0ba-4252-bf7e-51963853ed81/IMAG1522.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210113%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210113T044346Z&X-Amz-Expires=86400&X-Amz-Signature=f08f626474ad91091a617df68c75b76f47d7410634375d8b16b7b8990d7672fe&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22IMAG1522.jpg%22" style="width:30vw;" />
  <figcaption>來玩機台囉！</figcaption>
</figure>
<figure>
  <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d1cf5f10-8b56-4bfe-86b9-fad53c4fb031/IMAG1523.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210113%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210113T044514Z&X-Amz-Expires=86400&X-Amz-Signature=b4409192f047fec7ed6f18db72a8a0df9f2950b0587cf7d8b9103e2763c34790&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22IMAG1523.jpg%22" style="width:30vw;" />
  <figcaption>挖掉杯子底部，讓球通過</figcaption>
</figure>
<figure>
  <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7fb0edfb-022d-4706-9200-c8cd27e21216/IMAG1524.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210113%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210113T044604Z&X-Amz-Expires=86400&X-Amz-Signature=f97b0eb51121c8eb28cc4e17914484e270cf9c36dcb8bec74b2a6fb41e72235b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22IMAG1524.jpg%22" style="width:30vw;" />
  <figcaption>機台是放斜的，這樣可以讓球滾下來</figcaption>
</figure>
<figure>
  <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/36caef15-113e-4e6b-8781-da21977c6996/IMAG1526.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210113%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210113T044631Z&X-Amz-Expires=86400&X-Amz-Signature=f14e86873067180feb7bddd104a15510dc4b7dcc82b8871e6c1a0bef9c965d57&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22IMAG1526.jpg%22" style="width:30vw;" />
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