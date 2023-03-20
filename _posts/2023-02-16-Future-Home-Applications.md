---
layout: post
title: innovative Project proposal
author: [frank570570]
category: [Lecture]
tags: [jekyll, ai]
---

This homework is to propose an innovative Projects and describe the key features, list all Design Considerations and the required technologies, then draw the System Block Diagram.


### Homework Report
**Contents:**<br>
* **應用與功能說明**
  - Specify the future home application, and Describe the key features
  - Describe the key features which may be applied to the home space (kitchen, living room, play room, study room, bed room)
* **設計考量與所需相關技術**
  - List all design considerations and the required technologies
* **系統方塊圖**
  - Draw a System Block Diagram

---

### 超級書桌
### 應用功能說明
1. 回到家自動丟下背包自動幫我把所有裝置放到我需要的位置，讓我可以在上個廁所的時間內完成預備作業
2. 自動幫我把需要充電的物品充電，並放置好預備位置
3. 語音切換多種模式 : 說我想要休息了、要工作了.....會幫我自動調整好裝置的位置，桌椅高低，整理好物品讓我
4. 連接網路，可以用homekit等手機app進行操控需求的模式
5. 影響辨識功能:辨識書包拉鍊位置，拉開拉鍊，判斷書包中的物體是甚麼，如果未辨認成功則不移動，如果辨認成功為需要移動的物體則將它的位置移到預先設定的位置
6. 需要充電的物體:書桌已知充電器在哪裡(由書桌收的或記得的)自動插上插頭並將需要充電的電器充電
7. 自動記錄系統:每當所有物品位置維持不動超過3小時，於下一次使用時間通知是否紀錄位置，這樣下一次需要擺放這個位置時就可以直接按 
8. 光學感測器:當更改書桌的物體位置時，一但有物體碰觸則中斷，避免造成傷害
9. 自動調整檯燈照度

### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:手機遙控，語音控制
2. 移動方式:對書桌安裝馬達、機器手臂
3. 供電方式:插電
4. 聯網方式:WiFi或BT to 手機
4. 作業系統：採用Android OS

**所需相關技術：**
1. 滑軌式機器手臂(可辨識插孔並準確插入、移動物體) ＆ 軟式夾具
2. 物體辨識分類：Jetson-Nano + IMX219
3. 聲音辨識:將人聲辨識並進行任務
4. 光學感測器:避免誤傷、辨識出現今物體位置並記錄
5. 聲音感測器:感測人聲
6. 記憶體記錄位置
7. 智慧燈泡連接：AWS Alexa介接, 或藍牙命令操控燈光
8. 照度感測: ADC界面讀取光敏電阻(GL5516)


### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/FutureHome_kitchen_robot.png?raw=true)


---
## Design Methodology (設計方法)
* Top-Down Design  ：由上層應用分析再區分出下層個別功能及所需軟硬體設計
* Bottom-Up Design ：由底層軟硬體元件往上組合出上層所需應用功能

---
## Market Analysis (市場分析)
![](https://blog.hubspot.com/hs-fs/hubfs/tam-sam-som.png?width=1200&name=tam-sam-som.png)

---
### TAM of Future Home Products
The Target Market size (TAM) of Future Home Products is the number of household.<br>

---
### Taiwan Student = 421.2 萬人 ， 中產階節約67.8%
* [Number of Srudent in the Taiwan ]([https://www.statista.com/statistics/183635/number-of-households-in-the-us/]([http://www.stat.org.tw/data/asoctopic/109%E5%AD%B8%E5%B9%B4%E5%AD%B8%E6%A0%A1%E5%9F%BA%E6%9C%AC%E6%A6%82%E6%B3%81%E7%B5%B1%E8%A8%88%E7%B5%90%E6%9E%9C%E6%8F%90%E8%A6%81%E5%88%86%E6%9E%90.pdf])<br>
* [台灣中產階級比例]([https://joelin.cc/?p=1763]

### American Student = 7660萬
* [Number of Srudent in the US ]([https://zh.wikipedia.org/zh-tw/%E7%BE%8E%E5%9B%BD%E6%95%99%E8%82%B2]



-

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


