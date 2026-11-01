# Beyblade X Tournament Manager（網頁版）

這是一個可部署到 HTTPS 網址的手機優先網頁程式，支援 iPhone Safari 及加入主畫面。

## 功能
- 選手登記
- 瑞士輪配對（盡量避免重複對戰）
- 比賽計分：Xtreme Finish 3 分、Over Finish 2 分、Burst Finish 2 分、Spin Finish 1 分
- 每場先取得 4 分勝出
- 排名及 CSV 匯出
- 同一瀏覽器本機保存賽事資料
- 加入主畫面後可離線開啟已載入的程式介面

> 注意：目前版本採用瑞士輪式配對及 Buchholz 排名參考，並非官方賽事管理平台的認證軟件。不同賽事的配對、排名細則請以主辦方規章為準。賽事資料只保存在該裝置/瀏覽器，不會自動同步到其他裝置。

## 最簡單部署方式：GitHub Pages（免費）

你需要一個 GitHub 帳戶。部署完成後會得到一條 `https://...github.io/...` 網址。

1. 在 GitHub 建立一個新的 Repository（儲存庫），例如命名為 `beyblade-x-tournament`。
2. Repository 可設為 **Public**，然後建立。
3. 將本資料夾內的全部檔案上傳到 Repository 根目錄：
   - `index.html`
   - `manifest.webmanifest`
   - `service-worker.js`
   - `icon-192.png`
   - `icon-512.png`
4. 在 Repository 頁面進入 **Settings → Pages**。
5. 在 **Build and deployment** 選擇 **Deploy from a branch**。
6. Branch 選 `main`，資料夾選 `/(root)`，按 **Save**。
7. 等待 GitHub Pages 完成部署。回到 Pages 頁面，開啟顯示的網址。

## iPhone 加入主畫面

1. 用 iPhone 的 **Safari** 開啟部署後的 `https://...github.io/...` 網址。
2. 點 Safari 的「分享」圖示（方框向上箭頭）。
3. 選擇 **加入主畫面（Add to Home Screen）**。如未見到該項目，向下捲動分享選單。
4. 按「加入」。之後可從主畫面圖示開啟程式。

## 重要資料提醒
- 賽事資料保存在目前 iPhone 的 Safari 網站資料中，不會自動同步至其他手機或電腦。
- 不要清除 Safari 的網站資料；每場賽事結束後建議按「匯出 CSV」備份。
- 若要在另一部裝置繼續同一場賽事，現版本沒有雲端同步/匯入功能。

## 更新程式
日後替換 `index.html` 等檔案並推送到 GitHub，重新載入網頁即可。若仍顯示舊版，可關閉主畫面程式後重新開啟，或在 Safari 重新載入。
