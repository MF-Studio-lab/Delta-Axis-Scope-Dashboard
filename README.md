# Delta 軸控示波器儀表板

Delta DVP50MC11T-06 PLC 示波器波形與運動軌跡分析儀 v2.8

## 功能特色

- **多通道時序波形圖**：邏輯信號（PU射料、GCode_Run、G_Run_Busy、CV_Trace）+ 三軸位置（X/Y/Z）+ 推算合成速度
- **空間運動軌跡**：3D 立體軌跡 / XY 俯視圖切換，支援 XYZ 軸反轉
- **時間游標與單點狀態檢視**：滑桿、鍵盤←/→、播放動畫、波形點擊同步
- **關鍵事件日誌**：自動偵測數位/多狀態信號跳變，點擊可跳轉測量線
- **KPI 儀表板**：總採樣時長、各信號 ON 時長、最大/平均合成速度
- **CSV 匯入**：支援 DVP 示波器匯出格式，自動辨識欄位類型（數位/多狀態/位置）

## 線上 Demo

🔗 **GitHub Pages**：https://mf-studio-lab.github.io/Delta-Axis-Scope-Dashboard/

## 本地開啟

直接雙擊 `index.html` 或用任意靜態伺服器：

```bash
cd Delta-Axis-Scope-Dashboard
python3 -m http.server 8080
# 開啟 http://localhost:8080
```

## CSV 格式需求

- DVP 示波器匯出 CSV（含 Variable Name 標頭列）
- 第 1 欄為時間（HH:MM:SS 或秒數）
- 位置欄位名稱含：`C_X_Pos`、`C_Y_Pos`、`C_Z_Pos`（或同義詞）
- 數位信號自動偵測 0/1 欄位
- 多狀態整數信號自動偵測（如路徑號 1/2/3...）

## 技術架構

- **Plotly.js** (CDN) - 圖表渲染
- **Vanilla JS** - 無建置步驟，單一 HTML 檔案
- **CSS Variables** - 深色主題，響應式佈局

## 授權

MIT License