# 📸 PTT Beauty Crawler (PTT 表特版圖片下載器 - 防擋版)

這是一個基於 Python 的自動化爬蟲工具，用於練習 `requests` 與 `BeautifulSoup` 的網頁解析技術。
針對 PTT 的連線限制，本專案實作了 Session 會話管理與隨機延遲機制，能有效穩定地進行資料抓取。

## 🛠️ 技術棧 (Tech Stack)
* **Python 3.9+**
* **Requests**: 使用 `Session` 保持連線，模擬真實瀏覽器行為。
* **BeautifulSoup4**: 解析 HTML DOM 結構。
* **Random & Time**: 實作隨機等待時間 (Random Delay)，降低被伺服器阻擋的風險。

## 🚀 功能特色
* ✅ **自動繞過驗證**: 在 Headers 中設定 Cookie 自動通過 PTT 18 歲驗證。
* ✅ **防禦機制 (Anti-Blocking)**: 
    * 引入隨機延遲 (Random Sleep)，模擬真人閱讀速度。
    * 實作重試邏輯 (Retry Logic)，遇 `ConnectionResetError` 自動暫停並重連。
* ✅ **智慧分類**: 下載的圖片會依照「文章標題」自動建立對應資料夾。

## ⚠️ 免責聲明
本專案僅供程式技術交流與教育用途，請勿用於大量惡意請求或商業用途。
