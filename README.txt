船舶捆裝貨物清點系統（iPhone PWA）

檔案：
- index.html：手機清點網頁
- manifest.webmanifest：加入主畫面設定
- sw.js：離線快取
- icon-192.png / icon-512.png：圖示

重要：要啟用 iPhone Safari 的「加入主畫面」及 Service Worker 離線快取，必須先將這些檔案部署到 HTTPS 網址。不能只把 index.html 存在手機檔案中直接開啟，就期待 Service Worker 離線運作。

部署後 iPhone 使用方式：
1. 用 Safari 開啟 HTTPS 網址，第一次需有網路，等待頁面載入完成。
2. 點 Safari「分享」→「加入主畫面」→「加入」。
3. 從主畫面開啟「貨物清點」。之後已快取的頁面可離線開啟。
4. 清點資料存在此 iPhone 的 Safari IndexedDB 本機資料庫。
5. 定期使用「備份 JSON」保存完整資料；「匯出 Excel 相容 CSV」可用 Excel 開啟。

注意：
- 本版匯出的是 UTF-8 CSV（Excel 可開啟），不是原生 .xlsx。
- CSV 是清點明細；要做更完整統計可匯入提供的 xlsx 範本或用 Excel 樞紐分析表。
- 清除 Safari 網站資料、移除網站資料或更換手機可能造成資料遺失；請定期備份 JSON。
- 離線功能需首次在線成功載入並快取後才可使用。
- 這是本機單機版，不含跨手機同步、帳號或雲端備份。
