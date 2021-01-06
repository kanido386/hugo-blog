---
title: "音訊處理期末專題"
date: 2021-01-06T15:55:53+08:00
categories:
- 
tags:
- tag1
- tag2
slug: asp-final-project
thumbnailImage: https://images.unsplash.com/photo-1560849898-d058f7d93b23?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=2687&q=80
thumbnailImagePosition: left
coverImage: https://images.unsplash.com/photo-1560849898-d058f7d93b23?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=2687&q=80
coverCaption: ""
coverSize: partial
keywords:
-
#thumbnailImage: //example.com/image.jpg
---
用 Pure Data 打造吉他效果器！
<!--more-->
## 特別感謝
首先，非常幸運能夠和來自越南的朋友 Son Tran 同一組，沒有他，就不會有這段有趣的旅程！<br>
（他自彈自唱真的超好聽的，而且竟然還會做電子音樂！）<br>
（在這邊偷偷放他的 YouTube channel: <a href="https://www.youtube.com/channel/UCm6tcNSqAYVqZpA8pm4-T5A" target="_blank">MadSon TR</a> 🎧）

## Demo
強烈建議搭配後面的說明聽會比較知道在做什麼 😏<br>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/7F14-C7rrmg" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 課程內容簡介
這學期修了電機系張文輝教授開的<a href="https://timetable.nctu.edu.tw/?r=main/crsoutline&Acy=109&Sem=1&CrsNo=1078&lang=zh-tw" target="_blank">互動式音訊處理導論</a>，接觸到很多很酷的玩意兒：

1. 學一點聲音訊號處理的概念以後，用 MATLAB 做簡單的分析與處理
2. 認識<a href="https://zh.wikipedia.org/wiki/%E5%90%88%E6%88%90%E5%99%A8" target="_blank">合成器</a>的基本運作原理之後，用線上數位音樂工作站 <a href="http://www.audiosauna.com/" target="_blank">AudioSauna</a> 自製音色並用新音色做一首簡單的曲子
3. **<span style="color:black;">（本篇主角！）使用視覺化程式語言 <a href="http://puredata.info/" target="_blank">Pure Data</a> 做一些簡單的音訊處理</span>**
4. 用音訊編輯軟體 Adobe Audition 消除歌曲中的人聲
5. 用助教訓練好的 HMM 模型，做音樂的音值識別、拍號判定、樂譜追蹤，並為一段只有主旋律的譜生成和弦伴奏
6. 用一套叫 HTK 的自由軟體做一個簡單的歌手辨識系統
7. 認識「動態時間伸縮」的原理以後，直接拿助教寫好的 C 程式來做一個簡單的歌曲查詢系統

## 動機
期末的時候必須選個相關主題來發展成一個專題。<br>

我們原本打算是要做 source separation，也就是一種能夠把完整樂曲分離出 bass、鋼琴、吉他、鼓等獨立音訊的技術。<br>

但後來想說，既然之前實驗課有接觸過 Pure Data，再加上我們都有玩過吉他效果器，所以我們就想結合兩者，並兼合我們的創意，打造屬於我們的吉他效果器！（而且還不用花錢）

## 實作方法
### （一）研究別⼈是如何實作吉他效果器的
我們在查資料的過程中找到了 <a href="https://guitarextended.wordpress.com/audio-effects-for-guitar-with-pure-data/" target="_blank">Audio effects for guitar with Pure Data</a> 這一篇文章，裡頭有很多吉他效果器的實作及實際用吉他去測試效果器的 demo！<br>

只能說，網路世界無奇不有，這聽起來偏冷門的東西居然也找得到資源，酷斃了 😎

### （二）將那些⽅法盡可能內化成我們⾃⼰的能⼒
像海綿一樣，一直吸收、一直吸收，去讀懂為什麼他要這樣寫而不是那樣寫。<br>

如此一來，不僅讓我們更清楚該如何開始，也讓我們更加了解每個效果器的運作原理，一舉兩得！

### （三）利⽤我們對於吉他效果器的⾒解，打造屬於我們的吉他效果器
其實大部分還是參考那篇文章的做法居多xD<br>

雖然是這樣，但我們在過程中也更加熟悉了 Pure Data 的操作，若之後想嘗試同樣是視覺化程式語言但較為熱門的 Max/MSP，相信很快就能上手了吧！

### （四）考慮⽤ Pure Data Externals 的⽅式讓界⾯看起來更加簡潔
不過後來我們找到了 <a href="http://write.flossmanuals.net/pure-data/subpatches/" target="_blank">Subpatch</a> 的做法，它其實就是 Pure Data 界的 Function，可以自己定義在一個區塊當中你的 input／output 是什麼、要做哪些操作。<br>

什麼意思？<br>

比方說你現在不得不設計一部機器，需要餵給它的是好幾個單元的上課投影片和好多年份的考古題，你期望從這部機器當中獲得的僅僅是一張寫著好看分數的考卷，但過程中你卻得犧牲人生無數的可能性⋯⋯<br>

為了解釋 Function 的概念，扯遠了。<br>

拉回來。<br>

利用 Subpatch，可以方便我們管理圖形化的程式，除了能讓畫面看起來比較乾淨之外，也可以讓整個程式邏輯以及架構更有條理！

### （五）實際拿吉他測試我們的效果器，若有可以再改進的地⽅，就再改進
星期日 (2021.01.03) 晚上，我們去九舍地下二樓試我們的吉他效果器。<br>

提個外話，那邊的裝潢真的超棒的，走的是酒吧風、殘響效果又棒，若有酒保為我們調製上等的雞尾酒那就更完美了！<br>

再拉回來。<br>

原本我們是不抱持著什麼期待啦，想說市面上賣的效果器都不便宜，啊我們只不過是用程式語言來模擬出效果器，聲音是能有多好？<br>

沒想到！當我們打開「Wha-wha」的效果，Son Tran 刷了第一個和弦以後，我們都被嚇到了！那令人驚豔的聲響效果，真的會讓人誤以為此時此刻、這個地方有什麼專業樂團正在現場演出！<br>

我們從七點半一路弄到差不多快十一點，過程中調整了很多次程式，為的是讓聲音更符合我們的需求以及讓介面看起來比較不會那麼凌亂（雖然介面看起來還是很「科技風」就是了 😂）

## 結果分析
廢話不多說，直接給大家看我們的程式圖吧！

### 整體架構
<figure>
  <img src="https://i.imgur.com/5GYRnqu.png" style="width:43vw;" />
  <figcaption>使用者介面</figcaption>
</figure>

- `pd 某某某` 的小方塊就是前面所說的 Subpatch，除了 `pd file` 是用來開啟音檔並加以讀取的功能以外，其他的 `pd 某某某` 就都是吉他效果器了！
- 吉他效果器左邊一排的正方形框框是開關（Pure Data 稱它為 Toggle），打開代表說我要讓這個效果器處理我們的聲音，關掉的話就表示我們要讓聲音直接通過，不處理，即 `output = input`
- `adc~` (類比轉數位) 是我們的聲音輸入，我們選擇用錄音介面；`dac~` (數位轉類比) 則是輸出，不管是筆電內建的輸出或者是音箱都行，我們選擇用音箱，這樣聽起來比較震撼 😈
- `adc~` 和 `dac~` 後面的抖抖線意思是，通過這個有抖抖線的 Object 以後，它 output 出來的東西會是可以畫成波形圖的「訊號」，圖中黑線（Pure Data 稱它為 thin cable）代表控制資料的傳輸，藍線（Pure Data 稱它為 thick cable）代表訊號的傳輸
- 圖中一條一條的 slider 就是用來調整效果器參數的控制器（最下面的 slider 用來調控音量），藉由拉動 slider，就可以聽到聲音有趣的變化！（不然一成不變實在無趣）
- 後來我們決定把其他效果器的參數 slider 放進效果器 Subpatch 裡面，不然介面看起來會有點亂
- 中間偏右看起來像是按鈕的東西（Pure Data 稱它為 Bang），其功能是把參數設定到我們預設好的預設值，為的是方便回到預設值（有說跟沒說一樣），按下 Bang 以後，`s reset` (send) 就會幫我們把 Bang 的訊號傳到 `r reset` (receive) 的 output 給有數字的 Message，繼而引發更動 slider 的數值，於是乎，效果器的參數就回到預設值啦！

### Subpatch 小介紹
<figure>
  <img src="https://i.imgur.com/rPCYoPY.png" style="width:33vw;" />
  <figcaption>用 pd file 來簡單介紹</figcaption>
</figure>

- 剛剛說過，Subpatch 是 Pure Data 界的 Function！
- `inlet` 就是 input，`outlet` 就是 output
- 紅色圈起來的部分就是在區別究竟 input／output 是控制資料還是訊號
- input／output 之間的東西就是一些操作，本例在做打開音檔並讀取的動作
- 有了 Subpatch 的協助以後，開發的過程就更加愉悅了呢！

### Distortion 破音效果器
把訊號的振幅拉大再擷取一小部分，聽起來就會有種失真的破音效果，<a href="https://youtu.be/7F14-C7rrmg?t=77" target="_blank">像這樣</a>。
<figure>
  <img src="https://i.imgur.com/ziLZyCF.png" style="width:33vw;" />
  <figcaption>Distortion 破音效果器</figcaption>
</figure>

### Tremolo 顫音效果器
用一個低頻振盪器 (LFO) 來調變音量，讓音量呈現忽大忽小的效果，<a href="https://youtu.be/7F14-C7rrmg" target="_blank">聽起來像這樣</a>。
<figure>
  <img src="https://i.imgur.com/esTVil5.png" style="width:33vw;" />
  <figcaption>Tremolo 顫音效果器</figcaption>
</figure>

### Vibrato 抖音效果器
用一個低頻振盪器 (LFO) 來調變頻率，讓音高呈現忽高忽低的效果，<a href="https://youtu.be/7F14-C7rrmg?t=30" target="_blank">聽起來像這樣</a>。
<figure>
  <img src="https://i.imgur.com/O0g8FsR.png" style="width:38vw;" />
  <figcaption>Vibrato 抖音效果器</figcaption>
</figure>

### Wha-wha 娃娃效果器
細節頗複雜就不解釋了，其原理跟頻率有關。那為什麼叫娃娃效果器呢？<a href="https://youtu.be/7F14-C7rrmg?t=123" target="_blank">聽聽看就知道了</a>xD
<figure>
  <img src="https://i.imgur.com/n7iksIE.png" style="width:38vw;" />
  <figcaption>Wha-wha 娃娃效果器</figcaption>
</figure>

### Delay 延遲效果器
上面的 slider 控制聲音衰減的快慢（這就是為什麼要乘上一個介於 0 到 1 之間不包含 1 的值），下面的 slider 則是控制多久重複一次（不過每重複一次，聲音會越來越小聲），<a href="https://youtu.be/7F14-C7rrmg?t=169" target="_blank">讓我們來聽聽看它的效果吧</a>！
<figure>
  <img src="https://i.imgur.com/922G06G.png" style="width:38vw;" />
  <figcaption>Delay 延遲效果器</figcaption>
</figure>

### Reverb 殘響效果器
一種營造空間感的效果器。我們直接拿 Pure Data 內建的 `freeverb~` 來用，<a href="https://youtu.be/7F14-C7rrmg?t=210" target="_blank">聽起來像這樣</a>。
<figure>
  <img src="https://i.imgur.com/7Sjp3w0.png" style="width:38vw;" />
  <figcaption>Reverb 殘響效果器</figcaption>
</figure>

### Chorus 合聲效果器
製造一個和原來聲音有微小時間差和頻率差的聲音，然後再同時放。<br>

就像是一群人在合唱的時候，即使是唱同個旋律，也會因為進來的時間點有微小的差異、各自的不同音準，而形成一種亂中有序的感覺。<a href="https://youtu.be/7F14-C7rrmg?t=357" target="_blank">聽聽看吧</a>！
<figure>
  <img src="https://i.imgur.com/rmj9qr6.png" style="width:38vw;" />
  <figcaption>Chorus 合聲效果器</figcaption>
</figure>

## 參考來源
<a href="https://guitarextended.wordpress.com/audio-effects-for-guitar-with-pure-data/" target="_blank">Audio effects for guitar with Pure Data</a>

## 心得
前面其實已經講得差不多了，就用三個字來描述吧：「真有趣！」<br>
能創造出一個可以用五官感受的東西真的超有成就感的，很享受那個過程 🏝

## 最後
感謝教授開設這一門很有意思的課，感謝三位助教每堂實驗課的帶領，<br>
並再次感謝能與 Son Tran 合作了這整個學期，沒有你們，就沒有這一切！<br>
<br>
希望讀完這篇文章的您能夠有所收穫，我們下篇文見啦 😃