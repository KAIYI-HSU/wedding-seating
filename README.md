# 互動式婚禮賓客座位表

一個單檔、純前端的互動式婚禮座位表網頁，讓賓客可透過姓名搜尋快速定位自己的座位。

🔗 **公開網址**：<https://kaiyi-hsu.github.io/wedding-seating/>

## 功能

- 🔍 **姓名搜尋**：輸入姓名即時過濾，選取後自動高亮對應桌位
- 🪑 **Hover 預覽**：滑鼠移到任一桌位即顯示該桌賓客名單
- 🎯 **桌位聚焦**：點擊桌位後其他區域暗化，突顯目標
- ⌨️ **鍵盤操作**：`↑` / `↓` 切換建議、`Enter` 選取、`Esc` 清除聚焦
- 📱 **響應式設計**：手機、平板、桌機皆可順暢使用

## 隱私

- 所有中文姓名已去識別化：**第二個字以 `O` 取代**（例：`王小明` → `王O明`）
- 原始未去識別化名單（`CSV`、原始座位圖）透過 `.gitignore` 排除，**不會進入公開 repo**

## 技術

單一 HTML 檔案，無需建置工具或 npm 相依：

- 純 HTML / CSS / JavaScript（`index.html`）
- Google Fonts：`Noto Serif TC`、`Cormorant Garamond`
- 部署：GitHub Pages（main 分支根目錄）

## 本地預覽

直接用瀏覽器開啟即可：

```bash
open index.html
```

或啟動本地伺服器：

```bash
python3 -m http.server 8000
# 瀏覽 http://localhost:8000
```

## 更新名單

編輯 `index.html` 中的 `RAW_GUESTS` 陣列，格式為 `["桌號key", "姓名"]`：

```js
const RAW_GUESTS = [
  ["main", "新郎新娘"],
  ["t2", "王O明"],
  // ...
];
```

桌位配置（座標、標籤）在 `TABLES` 陣列調整。

推送至 `main` 後 GitHub Pages 會於 1–2 分鐘內自動更新。

## 授權

私人婚禮用途，不提供對外授權。
