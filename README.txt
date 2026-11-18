船舶捆裝貨物清點系統（iPhone Safari 離線網頁版）

檔案：
- index.html：手機清點網頁
- manifest.webmanifest：加入主畫面設定
- sw.js：離線快取（本次版本 v2）
- icon-192.png / icon-512.png：圖示

本版功能：
- 單捆登記及批次登記
- Hold、Bay、貨物種類、規格、長度、捆數、每捆件數
- 單捆重量可留白，TON 與 KG 分開統計
- 每次按「儲存清點紀錄」自動保存本機日期時間，並在明細顯示
- Excel 原生 .xlsx 匯出，含清點明細及 Hold、Bay、貨物種類、規格、長度統計
- CSV 匯出及 JSON 備份／還原
- IndexedDB 本機保存、Service Worker 離線快取

部署方式：
1. 將 ZIP 解壓縮。
2. 把裡面的六個檔案放在 GitHub repository cargo-checking 的最外層（root）。
3. 若舊版檔案已在 GitHub，使用新檔案覆蓋同名檔案並 Commit changes。
4. GitHub repository → Settings → Pages，Source 選 Deploy from a branch；Branch 選 main，資料夾選 /(root)，按 Save。
5. 等待 GitHub Pages 顯示網站已發布，再用 iPhone Safari 開啟 HTTPS 網址。
6. 第一次開啟時保持網路，等待頁面及離線快取完成；Safari 分享 → 加入主畫面。

重要：
- 離線功能需先在線成功開啟一次，讓 Service Worker 快取完成。
- 清點資料存在該 iPhone 的 Safari 網站本機資料庫；清除網站資料或換機可能遺失，請定期備份 JSON。
- Excel 匯出會產生 .xlsx 檔，包含「清點明細」及「統計報表」兩個工作表。
- 每筆時間是按下儲存按鈕當下的 iPhone 本機時間。
- 此版本為單機本機儲存，不會自動同步到其他手機。
