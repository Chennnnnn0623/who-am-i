
# 360° 全景網頁（Starter Kit）

這個資料夾已經幫你準備好最基本的 360° 全景網頁。
你只需要把 `images/pano.jpg` 換成自己的 360° 全景照片（equirectangular 2:1 比例），就能在網頁中拖曳觀看。

---

## 你需要做什麼（步驟）

1) 準備圖片  
   - 使用 360° 相機拍攝，或用軟體拼接成 **等距矩形 equirectangular** 圖片。  
   - 推薦比例：**2:1（例如 4096x2048、8000x4000）**。  
   - 檔名建議直接取代 `images/pano.jpg`。

2) 放入專案  
   - 將你的圖片覆蓋到：`images/pano.jpg`。  
   - 不需要修改程式碼就能顯示。

3) 啟動本機預覽（避免瀏覽器檔案存取限制）  
   選一種方式：  
   - **Python 3（Windows / macOS / Linux）**  
     在這個資料夾開啟終端機（或命令提示字元），輸入：  
     ```bash
     python -m http.server 5500
     ```  
     然後用瀏覽器開啟：`http://localhost:5500`  
   - **Node.js（使用 npx serve）**  
     ```bash
     npx serve -l 5500
     ```  
     打開：`http://localhost:5500`  
   - **VS Code：Live Server 外掛**  
     右鍵 `index.html` →「Open with Live Server」。

4) 使用方法  
   - 滑鼠拖曳旋轉視角，滾輪縮放。  
   - **雙擊** 全螢幕；再次雙擊退出。  
   - 手機上可用手勢操作。

---

## 常見問題（Troubleshooting）

- **畫面黑或出現錯誤**：請確認已用「本機伺服器」開啟（不是直接雙擊 `index.html`），並觀察瀏覽器主控台訊息（F12）。  
- **圖片比例不是 2:1**：視角會被拉扯或無法正常顯示，請輸出 2:1 的 equirectangular 圖。  
- **圖片太大很慢**：可以壓到 4096x2048 或 6000x3000。  
- **想換檔名或路徑**：編輯 `index.html` 中 `panorama: "images/pano.jpg"` 的路徑即可。

---

## 上線部署（選擇其一）

- **GitHub Pages / Netlify / Vercel**：這是純靜態網頁，上傳整個資料夾即可。  
- 確認你的網站能連到 Pannellum CDN（本範例使用 jsDelivr）。

---

## 版權與第三方
- 全景引擎：Pannellum（MIT License），本範例以 CDN 方式載入。  
- 本 Starter Kit 僅供教學與示範，請自行替換圖片與內容。
