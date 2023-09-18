---
title: '股票投資組合 - C# WinForm'
date: '2023-03-01'
---

# 個人股票投資組合

## Database Tables Design
![image](https://i.imgur.com/oT5XkwG.png)

## 使用套件

* 資料庫存取: Dapper
* 物件映射轉換: Automapper
* Json相關套件: System.Text.Json
* HttpClient: System.Net.Http
* Email發送: Mailkit

## 功能

### 1. 會員功能
    1.1 註冊功能, 加密密碼 (Bcrypt), 存到資料庫
    1.2 忘記密碼, 發送驗證信, 更換密碼.
    1.3 登入驗證

### 2. 主要頁面
    2.1 投資個股投資情況總覽 [包含損益總和]
    2.2 損益計算 [不同種類證交稅不同 e.g. ETF]
    2.3 搜尋 - 以關鍵字過濾組合內的股票
    2.4 每五秒會自動去API拿最新的資料 (如果存在)

### 3. 新增股票
    3.1 可選是否需要計算損益 [已購買 OR 需要觀察]
    3.2 選取股票欄位可透過輸入 AutoComplete

### 4. 刪除或編輯股票
    4.1 可將股票的股價或持有數量或持有日做調整 [發放股利調整成本價]
    4.2 刪除不要的股票