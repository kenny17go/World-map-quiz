# 世界地圖國家測驗 | World Map Country Quiz

互動式世界地圖國家位置測驗，支援**繁體中文 / 英文 / 日文**名稱，可依大洲篩選，並提供學習模式與測驗模式。

## 功能

- **測驗模式**：隨機出題（國家名稱三語顯示），在地圖上點選位置。答對顯示正確，答錯會高亮正確國家。
- **學習模式**：點選或滑鼠移到國家即可查看「繁中 / 英文 / 日文」名稱，方便先記憶再測驗。
- **大洲篩選**：全部 / 亞洲 / 歐洲 / 非洲 / 北美洲 / 南美洲 / 大洋洲。
- 分數統計與「顯示答案」、「下一題」功能。

## 使用方式

### 本機開啟（推薦）

因為瀏覽器安全限制，**請勿直接雙擊 `index.html`**。請用本地伺服器開啟：

```bash
# 方法 1：Python
cd world-map-quiz
python -m http.server 8080

# 方法 2：Node.js
npx serve .
```

然後瀏覽器開啟：http://localhost:8080

### 上傳到 GitHub Pages

1. 建立新的 GitHub repository
2. 把本資料夾內容全部推上去（`index.html`、`data/`、`README.md`）
3. 到 Settings → Pages → Source 選擇 main branch（或 docs 等）
4. 等待部署完成後即可線上使用

## 資料來源

- 國家邊界：Natural Earth 1:110m Admin 0 Countries（public domain）
- 國家名稱：stefangabos/world_countries（繁中、英文、日文）

## 技術

- 純前端：HTML + Leaflet.js
- 地圖資料已打包在 `data/` 資料夾，載入快速，不需從遠端抓大檔
- 底圖使用 **OpenStreetMap**（免費、不需 API Key）。若要完全離線可註解掉 tileLayer，只保留國家多邊形。

## 授權

地圖與名稱資料皆為公開授權，本專案程式碼可自由使用與修改。
