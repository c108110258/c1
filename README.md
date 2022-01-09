# 軟體工程FINALPROJECT

# 摘要
### 疫情影響，必須遠距上課，在家自習學習狀況不佳。
### 預計要能夠開發出可以輔助課業，且具有教學與解答問題的AI家教機器人。

## 主要功能：
* ### 鏡頭掃描
* ### 語音辨識
* ### 教科書題庫解答
* ### 數學解題程序
### 輔助功能：
* ### 針對弱點出題
* ### 課文教學
* ### 家長監控

## 研究動機
* ### 疫情影響，在家學習、線上上課，無法有效監督學生學習進度，教學效果也不好。
* ### 家教機器人教導學生課業，幫助學生完成作業，提高在家學習的品質。

## 研究目的
* ### 題目辨識-讀取題目辨識文字。
* ### 數學解題-針對數學問題解答。
* ### 教科書解答與解析-引用出版社之解答與解析，針對數學以外題目提供學習。
* ### 課文教學-引用出版社之電子書，提供學生在有問題的地方進行影片教學。

---------------------------------------
# 文獻回顧與文獻探討
![image](https://user-images.githubusercontent.com/92836676/147935788-3c45823f-a704-4d7f-a26d-e7086929d803.png)
![image](https://user-images.githubusercontent.com/92836676/147935765-7da73ac4-c77d-47d8-a333-1cfda4c1d7b0.png)

#### 以解數學題來講，市面上的解題程式大多大同小異，APP上有「Photomath」、「Microsoft Math Solver」，網站則有「Mathway」可供使用，基本功能都有支援掃描、手寫、鍵盤三種方法讓使用者輸入題目來 做使用，除了算出答案之外，也會有詳解，不過有些類型的題目就只有直接算出答案，沒有詳解可以看。

# 研究步驟
* ### 系統架構圖
#### 當使用者想要知道如何解題時，點擊螢幕選擇語音或是鏡頭辨識，機器人就會依據使用者要求，透過鏡頭或語音讀取題目，接著程式就會根據題目，透過程式運算得出解答與步驟，將解題步驟透過螢幕與語音傳遞給使用者。而後透過鏡頭擷取使用者作答過程，一步步判斷使用者作答狀況，達到學習解答的目的。
#### 家長透過WIFI連線的方式，連上機器人的前鏡頭，觀看學生的即時影像。

![image](https://user-images.githubusercontent.com/92836676/147932473-8b8a6962-f701-4e64-a929-75cd7fae273b.png)

* ### 鏡頭識別
#### 圖像識別系統是使用OpenCV中的OCR(光學字元辨識)，我們引用的是Pytesseract，只要使用者將圖片拍照匯入程式中他就能將圖片轉成文字檔，也可以將使用者書寫的文字識別進電腦裡，這技術精準度很高也支持多個語言的轉換，目前此軟體是由Google進行維護。
![image](https://user-images.githubusercontent.com/92836676/147932442-ef2af85e-bfd6-4710-96f3-dc13e11d215c.png)

* ### 語音識別
#### 語音識別系統是使用Google API，雖然它的音檔較大，而且需要連接網路才可使用，不過網路越快，辨識的速度也就越快，再加上它可以偵測多國語言而且準確率很高，不太會造成用戶的困擾。
![image](https://user-images.githubusercontent.com/92836676/148095905-32b340dd-df0e-42b0-bbc4-b4b3f09bfb0d.png)

* ### 題庫應用
#### 題目資料庫透過網路，蒐集各教科書商的題庫，因應學生所使用的教科書。
![image](https://user-images.githubusercontent.com/92836676/148095949-46b48e03-eb36-4906-a557-c0d6ac7a1db7.png)

* ### 題庫出題
#### 在學生使用AI家教做題目時，程式會蒐集學生答題該科目的正確率 ，在出題上會有較多的錯誤題目出題在此單元。
![image](https://user-images.githubusercontent.com/92836676/147932301-0ea2a97f-6fc9-4c13-b868-5a7637d6da24.png)

* ### 數學解題
#### 使用mathAI的優點有以下，可透過圖片來做題；能辨識字符多，能因應多種題型；精度高，適應性強。缺點則有，辨識複雜數學題準確率較低；如過前面計算過程出錯會導致後續計算錯誤。
![image](https://user-images.githubusercontent.com/92836676/147932317-9c2a419f-07a3-48e6-bbb1-3b93080ad0a1.png)
<img src="https://user-images.githubusercontent.com/92836676/147932323-4867e342-3a33-42ae-9375-5fb65dbc821d.png"  width="250" height="200">

* ### 家長監控
#### 使用Python加上OpenCV的功能，來使用家教機器人上的鏡頭，以網路來連接，家長可以透過手機，及時觀察學生的狀況。
<img src="https://user-images.githubusercontent.com/92836676/147932333-2d870899-4b8c-4a86-a43b-f4a8311478f8.png"  width="500" height="400">

* ### 課文教學
#### 整合出版社提供的電子書，讓學生對課文有疑問時可以查看。
![image](https://user-images.githubusercontent.com/92836676/148096092-81806db1-cdc7-41d6-8b8e-f3c93ebbf27b.png)

# 預期成果
![image](https://user-images.githubusercontent.com/92835373/148681709-8fddfd0f-d8b8-4c53-9ae5-fc42b2102bb5.png)

# 進度規劃
<img src="https://user-images.githubusercontent.com/92836676/147935366-05f598c3-9d57-45d6-8bce-7acc35bdc4df.png"  width="600" height="300">

---------------------------------------

# 參考文獻
* mathAI：https://github.com/Roujack/mathAI
* OpenCV：https://medium.com/ching-i/python-opencv-%E8%AE%80%E5%8F%96%E9%A1%AF%E7%A4%BA%E5%8F%8A%E5%84%B2%E5%AD%98%E5%BD%B1%E5%83%8F-%E5%BD%B1%E7%89%87-ee3701c454da
* COR：https://dotblogs.com.tw/RYNote/2021/01/14/105447
* Google API 語音辨識：https://www.oxxostudio.tw/articles/201509/web-speech-api.html
* ROYBI機器人：https://www.epochtimes.com/b5/21/6/20/n13035239.htm
* Photomath：https://agirls.aotter.net/post/52065
* Microsoft Math Solver：https://math.microsoft.com/zh
* Mathway：https://www.pkstep.com/archives/22122
* NUWA科技：https://www.nuwarobotics.com/zh-hant/
* Kebbi Air S：https://www.esentra.com.tw/product/kebbi-air-s/
---------------------------------------
