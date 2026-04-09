# Changelog

## 2026-04-09 — Initial Build & Deploy

### 新增
- 部署到 GitHub Pages：https://glen200392.github.io/teapot-hike-2026/
- 建立 `.gitignore`、`README.md`

### 功能修改
- **即時功能去日期鎖定**：公車狀態、行程「現在」標記、天氣逐小時區間改為全程使用裝置當下時間（原本鎖定 2026-04-12）
- **天氣逐小時標題**：改為動態顯示實際時間區間（`接下來逐小時 HH:00–HH:00`）

### UI / 響應式設計
- **桌面 sidebar layout**（≥768px）：底部 nav 轉為左側欄（200px），`position:fixed`
- **Fluid typography**：`html { font-size: clamp(14px, 13px + 0.5vw, 18px) }`，所有 `rem` 字體隨 viewport 比例縮放
- **Fluid sidebar**：`clamp(160px, 16vw, 240px)`，側欄寬度比例連動
- **桌面內容網格加寬**：總覽 4 欄、裝備 3 欄、地圖 4 欄、天氣卡片左右分欄

### Bug 修復
- 修復行程頁載入失敗：`isDay` 變數已刪除但仍被引用，導致 `ReferenceError`

### 內容
- 移除所有「7 人同行」相關文字（HTML、zh/en i18n、行程說明）

### 文件
- 新增 `ROADMAP.md`：通用版 `hike-planner` 規劃
