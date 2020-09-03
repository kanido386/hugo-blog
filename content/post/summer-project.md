---
title: "暑期專題"
date: 2020-09-03T18:52:58+08:00
categories:
- 
tags:
- tag1
- tag2
slug: summer-project
keywords:
-
#thumbnailImage: //example.com/image.jpg
---
2020 升大三的暑假，和康明軒教授、恩衍、育浚一起做了「音訊處理」的專題。
<!--more-->
（康明軒教授提供數學上的幫助、恩衍做降噪、育浚做其他也很有趣的聲音處理）
# 成果
先給大家聽聽看我最後上台發表的成果吧！
### 分析＆合成音色
| 樂器 | 待分析的音檔 | 合成出來 | 演奏音階 |
|:---:|:---:|:---:|:---:|
| 小號 | <a href="https://drive.google.com/file/d/1c4B6Thu5E5i0g3ySRfn2M6gAq13UJnkj/view?usp=sharing" target="_blank">01</a> | <a href="https://drive.google.com/file/d/1eNaZb4SIhUeP1-kB8wsLx38ekrbS_3Ls/view?usp=sharing" target="_blank">02</a> | <a href="https://drive.google.com/file/d/18yV-S-CPvI_Q_9xOVmpmue9fLbQF1Eyx/view?usp=sharing" target="_blank">03</a> |
| 雙簧管 | <a href="https://drive.google.com/file/d/1LsAohbiFXGa_KpjT2CsqmUGW1FZlz8t6/view?usp=sharing" target="_blank">04</a> | <a href="https://drive.google.com/file/d/1xjYuSMxfD97c0Wv5poHzIAlHz1N3LLd6/view?usp=sharing" target="_blank">05</a> | <a href="https://drive.google.com/file/d/1631sDcFSKs5NWkjumGGzHcNMIUjY8XoM/view?usp=sharing" target="_blank">06</a> |
| 管風琴  | <a href="https://drive.google.com/file/d/1I6LY-rCmSeiFL3lhrM8EwpxekmStVafd/view?usp=sharing" target="_blank">07</a> | <a href="https://drive.google.com/file/d/1ZNPWq6eJVD4L9owCd_PgC0s9_J7I5hYr/view?usp=sharing" target="_blank">08</a> | <a href="https://drive.google.com/file/d/1cDqbo_5fGCAQuSN2N5FRYS0N068QSJ1m/view?usp=sharing" target="_blank">09</a> |
### 改變音色
| 音樂 | 原音檔 | 小號 | 雙簧管 | 管風琴 |
|:---:|:---:|:---:|:---:|:---:|
| 生命之名 | <a href="https://drive.google.com/file/d/1OcF1t6QucHgnOVMcwNAnJmfuJRotJgZT/view?usp=sharing" target="_blank">10</a> | <a href="https://drive.google.com/file/d/1TKSwM6X4pYAfhoFKx3hysCSW33YeBCLI/view?usp=sharing" target="_blank">11</a> | <a href="https://drive.google.com/file/d/1QPD3pww866FZzO1y-eylMcWguLl1LS33/view?usp=sharing" target="_blank">12</a> |  |
| New Thang | <a href="https://drive.google.com/file/d/1VJSWuA2n6GoflmhA9hkpJtqQM5qP-AEh/view?usp=sharing" target="_blank">13</a> |  |  | <a href="https://drive.google.com/file/d/1OBh5F7fr53UW9dyRA4UNAgkcpkHEJVY4/view?usp=sharing" target="_blank">14</a> |

# 預備知識
### 音訊預處理
<span style="color:blue;">電腦如何將聲音訊號由類比轉成數位呢？</span><br>
先講為什麼要轉成數位好了。<br>
「電腦處理聲音」這件事情，其實就是在對聲音做運算，<br>
和類比也就是連續訊號相比，離散訊號的運算量小多了！<br>
所以在電腦處理聲音之前，必須先讓聲音變成離散資料。<br>
那該怎麼轉成數位呢？<br>
只要讓聲音經過 <span style="color:red;">取樣 (sampling)</span> 以及 <span style="color:red;">量化 (quantization)</span> 的過程就可以囉！<br>
<br>
在介紹取樣、量化之前，先給大家認識一下<span style="color:blue;">聲音檔案的重要參數</span>。<br>

- **<span style="color:black;">持續時間 (duration)</span>**：音檔總共有多少秒
- **<span style="color:black;">取樣頻率 (sampling rate)</span>**：一秒鐘要取多少個取樣點（聲音檔案通常會採用 48000 或 44100 赫茲，跟取樣定理有關）
- **<span style="color:black;">位元深度 (bit depth)</span>**：一個取樣點要用多少個位元紀錄（位元深度越大的話，會越精準，但相對而言，資料量也就越大！）
- **<span style="color:black;">聲道數 (channel)</span>**：其實就是我們常聽到的單聲道、雙聲道等等的
<br>

<span style="color:blue;">取樣＆量化</span><br>
<div style="padding:11px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/22d22a83403f9d39.png" style="width:550px; height:200px;" />
  <img src="https://ftp.bmp.ovh/imgs/2020/09/2c03857179f3c285.png" style="width:550px; height:200px;" />
</div>

- **<span style="color:black;">取樣 (sampling)</span>**：透過<span style="color:red;">取樣頻率</span>，也就是一秒鐘要取多少個取樣點，將<span style="color:red;">時間軸</span>上的資料離散化，得到一串取樣點（如上圖）
- **<span style="color:black;">量化 (quantization)</span>**：依照<span style="color:red;">位元深度</span>，也就是一個取樣點要用多少個位元紀錄，分別對每個取樣點做四捨五入，將<span style="color:red;">振幅軸</span>上的資料離散化，最後就會得到一串數列（如下圖）
<br>

訊號轉成數位了，那<span style="color:blue;">電腦如何處理聲音訊號呢？</span><br>
打個比方好了：<br>
在開始進行一個大任務之前，我們通常會先拆解成多個小行動，然後再各個擊破！<br>
處理聲音也是同樣道理，<br>
我們只要把一段音訊切成一個一個小<span style="color:red;">音框</span>，乘上<span style="color:red;">窗函數</span>重疊以後，就可以開始做後續的處理。<br>
<br>
<span style="color:blue;">切取音框</span><br>
<div style="padding:22px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/f6576ad5edcadf43.png" style="width:550px; height:200px;" />
</div>
在分析一段音訊的時候，我們通常是以<span style="color:red;">短時距分析</span>為主，<br>
因為聲音訊號在短時間之內是<span style="color:red;">相對穩定</span>的！<br>
所以我們通常會將音訊切成比較短的單位，稱為<span style="color:red;">音框</span> (frame)。<br>
那為了方便使用<span style="color:red;">快速傅立葉轉換</span>，我們通常會取 <span style="color:red;">2 的 n 次方</span>個取樣點當作一個音框。<br>
然後要注意，音框不能切太大或太小，這樣才能充分擷取音訊的特徵！<br>
那為了避免相鄰兩音框的特徵變化過大，一般會讓音框之間有一段<span style="color:red;">重疊</span>的區域，<br>
當然重疊的部分越多，對應的<span style="color:red;">運算量</span>也就越大！<br>
<br>
帶大家認識一下<span style="color:blue;">切取音框的重要參數</span>。<br>
<div style="padding:23px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/ce76456e87ee97c2.png" style="width:550px; height:200px;" />
</div>

- **<span style="color:black;">音框大小 (frame size)</span>**：每一個音框內所含有的取樣點個數
- **<span style="color:black;">音框重疊量 (frame overlap)</span>**：兩音框間重疊的取樣點個數
- **<span style="color:black;">音框跳距 (hop size)</span>**：兩音框起點距離的取樣點個數，相當於 <span style="color:red;">音框大小 - 音框重疊量</span>
- **<span style="color:black;">音框率 (frame rate)</span>**：每秒出現的音框數目，相當於 <span style="color:red;">取樣頻率 / 音框跳距</span>
<br>

<span style="color:blue;">套上窗函數</span><br>
<div style="padding:32px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/625f058dba3db937.png" style="width:600px; height:150px;" />
</div>
原本完整的聲音波形，<span style="color:red;">被音框硬生生地截斷</span>，頻譜將會產生誤差，該怎麼辦呢？<br>
我們只要透過乘上一個<span style="color:red;">中央高、兩側低的窗函數 (window function)</span>，<br>
讓音框內兩端的訊號達到 fade-in、fade-out 的效果，就可以增加音框左右兩端的<span style="color:red;">連續性</span>了！<br>
<br>

### 音色
<span style="color:blue;">聲音三要素</span><br>
<div style="padding:5px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/ede9088994b2a6b4.png" style="width:600px; height:150px;" />
</div>
待會只會介紹音色。<br>
<br>
什麼是<span style="color:blue;">音色</span>？<br>
音色是一個可以讓聆聽者<span style="color:red;">分辨</span>出聲音聽起來不同的聲音特性，<br>
藉由音色資訊，我們可以分辨出究竟現在聽到的聲音是人聲還是某種樂器聲，<br>
不受音高不同及音量大小的影響！<br>
<br>
<span style="color:blue;">哪些要素影響著音色呢？</span><br>

- ADSR Envelope
- Tremolo ＆ Vibrato
- 泛音列
- 可能還有其他 (?)

<span style="color:blue;">ADSR Envelope</span><br>
<div style="padding:7px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/d19848cbba1eb5ba.png" style="width:500px; height:300px;" />
</div>
它是什麼呢？<br>
它是描述 Attack、Decay、Sustain、Release 四階段的一個包絡！<br>
這樣講其實蠻抽象的，<br>
可以把它想像成聲音的 schedule，讓聲音的某個<span style="color:red;">參數隨著時間做改變</span>。<br>
那 Attack、Decay、Sustain、Release 又分別是什麼呢？<br>
觀察上圖：<br>

- **<span style="color:black;">Attack</span>**：一個參數從 0 到最大值所需要的<span style="color:red;">時間</span>
- **<span style="color:black;">Decay</span>**：一個參數從最大值降到 Sustain 所需要的<span style="color:red;">時間</span>
- **<span style="color:black;">Sustain</span>**：它比較特別，它是一個<span style="color:red;">程度</span>的參數，代表在 Release 之前維持的一個量
- **<span style="color:black;">Release</span>**：一個參數從 Sustain 降回 0 所需要的<span style="color:red;">時間</span>

這樣可能還是很抽象，沒關係，到 Ableton Live 的<a href="https://learningsynths.ableton.com/en/envelopes/change-over-time" target="_blank">合成器教學頁面</a>玩玩吧！<br>

<span style="color:blue;">Tremolo ＆ Vibrato</span><br>

- **<span style="color:black;">Tremolo</span>**：讓<span style="color:red;">音量</span>呈現忽大忽小的<span style="color:red;">顫音</span>效果，可以讓長音有起伏變化不再呆板，也可以讓每個音符呈現若隱若現的效果
- **<span style="color:black;">Vibrato</span>**：讓<span style="color:red;">音高</span>呈現忽高忽低的<span style="color:red;">顫音</span>效果，比方擦弦樂器可以靠<span style="color:red;">揉弦</span>來達到這種效果

<br>
<span style="color:blue;">泛音列</span><br>
泛音列是一系列頻率為<span style="color:red;">基音頻率 (fundamental frequency)  整數倍</span>的聲音，<br>
這些聲音都是純音，可以分別用正弦波來表示。<br>
那和音色有什麼關係呢？<br>
強烈推薦大家看 <a href="https://www.youtube.com/channel/UCVXstWyJeO6No3jYELxYrjg" target="_blank">NiceChord (好和弦)</a> 的 <a href="https://www.youtube.com/watch?v=0iJmDhNocaQ" target="_blank">一次搞懂「泛音列」！</a><br>
看完了一切都豁然開朗了呢 😎<br>

<span style="color:blue;">波形何以如此多元？</span><br>
<div style="padding:6px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/f615f911b624c2a1.png" style="width:500px; height:250px;" />
</div>
不同樂器，組成「一個音」的泛音列佔比都不太一樣。<br>
那剛剛提過，泛音列上的每個音都是純音，可以分別用正弦波來表示，<br>
然後再根據波的疊加原理，依照泛音列佔比，疊加出新的波形，<br>
疊加後的波形就是我們最後觀察到的波形！<br>
如上圖。<br>

<span style="color:blue;">再用聽的和看的來感受一次吧！</span><br>
<div style="padding:3px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/19b7c6548bc8fcfd.png" style="width:700px; height:250px;" />
</div>
以基頻為 220 赫茲的音來說明好了：<br>
先給大家聽 <a href="https://drive.google.com/file/d/1682sa4_ojGq4fpZ0Q_7bfccpb1Fwc9Ew/view?usp=sharing" target="_blank">220 赫茲的純音</a>。<br>
接著是 <a href="https://drive.google.com/file/d/1fRmcNPGGLnai-Nv9jP-VEZ28h1tZR4T1/view?usp=sharing" target="_blank">440 赫茲的純音</a>。<br>
然後我們再用一比一的比例，來調配出<a href="https://drive.google.com/file/d/1b60lT7gG-n7q8H-TaZKQsmHrWl6rtiUy/view?usp=sharing" target="_blank">新的音色</a>。<br>
新音色聽起來就像是「一個音」，但實際上卻是由兩個純音組合而成的！

<span style="color:blue;">泛音列與音色之間的關係</span>：<br>

- 基本頻率決定了一個音的音高
- 其他泛音與基頻的音量佔比決定了一個音的音色

# 所以，我是怎麼做出來的呀？
### 分析＆合成音色
<div style="padding:30px;">
  <img src="https://ftp.bmp.ovh/imgs/2020/09/ce7ecf082f96bce6.png" style="width:300px;" />
</div>

1. 用 `scipy.io.wavfile.read` ，將待分析的音檔讀進來
2. 用 `scipy.fftpack.fft` ，將原本 time domain 的 data 轉換到 frequency domain 上
3. 透過 `matplotlib.pyplot.plot` ，把圖給畫出來（如上圖，頻率取 0~1000）
4. 由圖可以觀察到基頻大概是 100 赫茲左右，也可以觀察到其泛音列的數值大小
5. 利用 `max` ，一個一個找出每個小區間內的最大值為何，即為圖中的明顯高起處
6. 由求出來的所有值，可以推算出基頻及其所有泛音列的數值大小佔比
7. 透過自己寫的 <a href="https://github.com/kanido386/playground/blob/master/2020-summer-project/timbre%20synthesizer/synthesizer.py" target="_blank">synthesizer</a>，依照上步驟的佔比，即可合成出該音色的聲音

### 改變音色（以一個音框來說明，單音音樂效果較佳！）

1. 用 `scipy.fftpack.fft` ，將該音框內的 data 轉換到 frequency domain 上
2. 透過自己獨創但效果很陽春 (?) 的方法運算以後，可以粗略找到基頻
3. 該<span style="color:red;">基頻及其整數倍的泛音</span>，透過剛剛分析出來的<span style="color:red;">佔比</span>來改變數值大小，即可轉換為新音色的音樂

# 感想
除了學到一些音訊處理的技巧以外，最大的收穫是，「態度」才是最重要的關鍵啊！<br>
目前在其他很多方面還是不夠及格，期望帶著這次的寶貴經驗，讓自己漸入佳境。

# 最後
再次感謝康明軒教授、恩衍、育浚，沒有你們，就沒有這一切！<br>
另外，也非常感謝柏毅給予我簡報上的指點，讓我學到一些很重要也很實用的簡報技巧！<br>
<br>
希望讀完這篇文章的您能夠有所收穫，我們下篇文見啦 😃<br>