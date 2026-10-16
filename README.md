# 𓃥 白六筆畫微觀訊息 (3D Stroke Micro-View Animation)

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?logo=github)](https://kuochili-ops.github.io/Big-message/)
[![Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js)](https://threejs.org/)
[![WebGL](https://img.shields.io/badge/WebGL-Interactive-blue)](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)

**𓃥 白六筆畫微觀訊息** 是一款基於 Three.js 與 WebGL 的單頁互動式 3D 文字視覺化應用。透過 1024x1024 高解析度 Mask 精準筆畫採樣，實現鏡頭深入 3D 文字深色筆畫核心的極致放大穿梭效果。演繹完成後自動後退全景，呈現具備實體 Z 軸厚度的立體文字陣列，並支援 3D 手勢旋轉、無損 WebGL 自動錄影與帶有狀態參數的網址分享。

👉 **線上即時體驗：** [https://kuochili-ops.github.io/Big-message/](https://kuochili-ops.github.io/Big-message/)

---

## ✨ 核心特色 (Key Features)

- **🔍 純黑墨跡核心精準採樣 (Strict In-Stroke Core Sampling)**
  採用 1024x1024 獨立黑白 Mask 畫布與多重安全半徑二次校驗，100% 確保鏡頭推進時精準聚焦於文字筆畫內部深處，絕不偏離至邊框或空白區域。

- **📦 無邊框純 3D 質感厚度 (Pure 3D Extruded Geometry)**
  捨棄傳統底板，採用雙層 3D 多重切角疊加（Double-Layer Offset Extrusion），展現具備實體 Z 軸厚度與多重金屬質感光澤的立體文字。

- **🎨 多款主題邊框顏色 (Live Theme Switching)**
  提供**暖金 (Golden)**、**琥珀銅 (Copper)**、**翡翠綠 (Emerald)**、**琉璃藍 (Sapphire)**、**紫羅蘭 (Amethyst)** 與 **玫瑰紅 (Rose)** 六種經典質感配色，並同步更新控制面板 UI 色系。

- **📐 動態視距與自適應拉退 (Dynamic Camera Retreat)**
  結尾展開階段自動計算 3D 空間中文字陣列的總寬度，若文字較多，鏡頭會以平滑對數曲線（Logarithmic Smooth Retreat）自動向後退遠，確保所有文字 100% 完整容納於畫面中。

- **📹 WebGL 自動錄影與下載 (Auto Video Recording)**
  結合 WebGL `canvas.captureStream()` 技術，支援一鍵高清錄影。演繹完成時，系統會自動儲存並發起 WebM/MP4 影片檔下載。

- **🔗 帶狀態參數的網址分享 (URL State Sharing)**
  支援 URL Query 參數（`?text=...&color=...`），複製或分享連結時能完整保存「訊息內容」與「邊框配色設定」，開開即刻還原相同視覺設定。

- **🕹️ 手勢與滑鼠全景互動 (OrbitControls)**
  演繹結束後自動解鎖 3D 控制器，支援單指/滑鼠旋轉全景、雙指縮放與平移觀賞。

---

## 🛠️ 技術架構 (Tech Stack)

- **Core Library:** Three.js (r128)
- **Interactive Controls:** THREE.OrbitControls
- **2D Processing & Sampling:** HTML5 Canvas API (Context 2D ImageData Masking)
- **Recording Engine:** MediaStream Recording API (`captureStream`)
- **Deployment:** Single-file HTML (Zero Build Tool Dependency), GitHub Pages

---

## 🚀 快速上手 (Quick Start)

本專案採用極簡單檔案架構（Single-file Architecture），無須安裝 `npm` 包管理器或建置工具：

1. **複製專案：**
   ```bash
   git clone [https://github.com/kuochili-ops/Big-message.git](https://github.com/kuochili-ops/Big-message.git)
