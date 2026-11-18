船舶捆裝貨物清點系統 V4（iPhone Safari 離線網頁版）

本版依使用者提供的 LI TUN TALLY CO., LTD. 空白 Daily Working Report Excel 整合。

主要更新：
- 清點紀錄支援重量輸入方式：單捆重量或整批總重量。
- PCS = 捆數；KGM = 公斤。
- 匯出 Excel 第一張工作表為 DAILY - 1，依 Hold 顯示 PCS／KGM。
- WORKED TO DAY = 所選日期清點；PREVIOUSLY = 所選日期之前的清點；G.TOTAL = 累計。
- Bay、貨物種類、規格、照片索引、破損紀錄保留在清點明細。
- 其餘原有離線清點、照片、破損紀錄、JSON 備份功能保留。
- AI 目前仍未連接雲端辨識服務；離線時人工清點可正常使用。

部署：
1. 先在舊版網站匯出 JSON 備份。
2. 解壓縮本 ZIP，將六個檔案上傳到 GitHub repository cargo-checking 根目錄並覆蓋。
3. Commit changes，等待 GitHub Pages 部署。
4. 用原本 iPhone Safari 網址重新開啟，首次更新需網路以刷新離線快取。
5. 不要清除 Safari 網站資料，否則可能遺失本機清點紀錄。

重量規則：
- 單捆重量：輸入每捆 KGM，系統乘以捆數。
- 整批總重量：直接輸入整批 KGM，不再乘以捆數。
- TON 與 KGM 分開統計，不互相換算。
