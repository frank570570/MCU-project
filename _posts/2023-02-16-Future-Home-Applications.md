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

### 桌面整理機器人
### 應用功能說明
1. 回到家自動丟下背包自動幫我把所有裝置放到我需要的位置，讓我可以在上個廁所的時間內完成預備作業
2. 自動幫我把需要充電的物品充電，並放置好預備位置
3. 語音切換多種模式 : 說我想要休息了、要工作了.....會幫我自動調整好裝置的位置，桌椅高低，整理好物品讓我
4.  

### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:垂直升降式手臂 or 懸吊式手臂
2. 移動方式:兩輪 or 滑軌懸吊
3. 供電方式:鋰電池
4. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 滑軌式機器手臂 ＆ 軟式夾具
2. 食物辨識分類：Jetson-Nano + IMX219
3. 電子鼻：氣味感測與辨識 MQ2

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/FutureHome_kitchen_robot.png?raw=true)

---
## 早晨喚醒系統
### 應用功能說明
1. 照度偵測
2. 藍牙手環監測睡眠品質,並保存睡眠動態紀錄
3. 手勢偵測與遙控
3. 鬧鐘喚醒功能：播放預設音檔.Wav, 或播放網路電台(PAM8403+8ohm speaker)
4. 遙控電動窗簾：紅外線遙控 (IR-LED)
5. 操控燈光：智慧燈泡＋手勢辨識 (TinyML)

### 設計考量與相關技術
**系統設計考量：**<br>
1. 感測方式:照度,手環動態及手勢
2. 供電方式:音箱用有線電源,手環用電池
3. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 照度感測: ADC界面讀取光敏電阻(GL5516)
2. 睡眠品質監測：藍牙穿戴式手環(ESP32+MPU6050), 運用三軸加速器偵測睡眠動態
3. 手勢偵測：MPU6050感測手勢動作之三軸加速器數值, 利用TinyML進行AI手勢辨識
4. 網路電台播放：ESP32 Internet Radio player
5. 智慧燈泡連接：AWS Alexa介接, 或藍牙命令操控燈光

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_morning_alarm_system.png?raw=true)

---
## 互動伴學機器人
### 應用功能說明
1. 外語學習
2. 學齡前遊戲互動

### 設計考量與相關技術
**系統設計考量：**<br>
1. 移動方式：球形滾動
2. 供電方式：鋰電池
3. 互動方式：LCD顯示模組 + 語音輸出入 + 肢體動作 + 指頭操作
4. 作業系統：採用Android OS

**所需相關技術：**
1. 影像物件識別： 執行 CSL-YOLO模型進行辨識(Jetson Nano)
2. 語音辨識與輸出： Speech Recognition & Text-To-Speech (AppInventor 2)
3. 外語教學：AI對答
4. 指頭操作：觸控 & 吸盤式電磁頭
5. 互動教具：字卡, 跳棋, ...

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_companion_robot.png?raw=true)

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
### Taiwan Households = 8.93M (台灣 9百萬戶）
* [Total number of households in Taiwan from 2010 to 2020(in 1,000s)](https://www.statista.com/statistics/330804/taiwan-national-total-number-of-households/#:~:text=By%20the%20end%20of%202020,households%20in%20the%20previous%20year.)

### Japan Households = 57.2M (日本 5千7百萬戶)
* [Number of Households in Japan](https://www.helgilibrary.com/indicators/number-of-households/japan/) 

### South Korea Households = 19.9M (南韓 2千萬戶)
* [Number of Households in South Korea](https://www.helgilibrary.com/indicators/number-of-households/south-korea/)

---
### American Households = 129.93M (美國 1.3億戶)
* [Number of households in the U.S. from 1960 to 2021(in millions)](https://www.statista.com/statistics/183635/number-of-households-in-the-us/)<br>
* [The average American household consisted of 2.51 people in 2021.](https://www.statista.com/statistics/183648/average-size-of-households-in-the-us/)<br>

-

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


