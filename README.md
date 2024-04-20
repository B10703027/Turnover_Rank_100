# 成值排行  
Gooaye EP424: 「整個族群都在動的時候，這個一般我們都把它視為是真的，就是市場上有一些資金要去買單」  
這組程式碼可以**將當日成交值前100名的股票針對族群進行分類，快速看出目前大盤金流的去處**。若有族群單一個股入榜，也可以留意同族群其他類股的走勢。  
  
除了族群金流以外，該組程式碼也有提供以下DataFrame:  
1. 成值前20名的個股: 當下最熱門的股票  
2. 創高創量股: 良好的突破需要有大資金進駐，而能夠上成值排行的個股通常都有各式資金進駐，較不易受單一資金來源控制。創高放量、搭配族群動能通常會有不錯的延續性  
3. 投信連買股: 列出投信近幾日連續買超、上成值排行的個股，投信連買通常被市場認為是不錯的訊號  

DataFrame中也有下列features可以判斷動能的延續性:  
1. 當月營收YoY
2. 投信連買天數
3. 內外盤比
---
### Data Source
1. 成值前100的個股資料: 該資料集需要XQ或XQ-based的看盤軟體做輸出，找出「成交重心股」輸出至excel後再轉為csv檔  
   (備註: 需要以下欄位 -> 商品代碼、商品名稱、成交、漲幅%、總量、內外盤比圖、估計量、成交值)
2. 所有個股前一日的投信、營收相關資料，可以從XQ下載後以 "投信、月營收資料處理.ipynb" 進行資料清洗
---
### How to use
確認資料來源、路徑無誤，用 "main.ipynb" 一鍵輸出即可
