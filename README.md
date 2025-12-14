# 葉宥汝的個人作品集網站 (Personal Portfolio)

這是一個展示個人簡歷、技能與作品集的靜態網頁專案。網站設計採用粉色系風格，包含個人介紹、趣味技能展示、成長經歷時間軸以及攝影作品集。

## ✨ 網站特色

- **響應式設計 (Responsive Design)**：適配桌面與行動裝置瀏覽。
- **動態視覺效果**：包含頭像浮動動畫、淡入視差捲動效果 (Intersection Observer)。
- **個人經歷時間軸**：記錄從深圳到台灣求學的成長歷程。
- **趣味技能表**：以進度條展示「睡覺時長」、「花錢能力」等個人特色技能。
- **作品集展示**：展示演唱會攝影與旅遊紀錄（aespa 演唱會、日韓旅遊）。

## 🛠️ 使用技術

- **HTML5**: 語意化標籤結構。
- **CSS3**: 
  - Flexbox & Grid 佈局。
  - CSS 動畫 (Keyframes)。
  - 漸層背景與玻璃擬態 (Glassmorphism) 效果。
- **JavaScript**: 
  - 滾動監聽 (Scroll Event)。
  - 元素顯現動畫 (Intersection Observer API)。

## 🚀 如何瀏覽

此專案為純靜態網頁，無需複雜的安裝步驟：

1. 下載此專案代碼 (Clone or Download ZIP)。
2. 直接使用瀏覽器 (Chrome, Edge, Safari 等) 開啟資料夾中的 `index.html` 檔案即可瀏覽。

---

# 📝 Git / GitHub 作業要求執行報告

本段落為記錄課堂作業之 Git 操作流程與決策說明。

## 1. 專案初始化與 Commit 記錄
本專案已完成多次具意義的提交，詳細記錄可見 Repository History。主要包含：
- `feat`: 新增作品集與時間軸區塊。
- `style`: 調整卡片佈局與 CSS 動畫效果。
- `docs`: 更新 README 文件說明。

## 2. 分支開發與 Pull Request (PR)
- 已建立功能分支 `feature/skills-bars` 進行技能區塊開發。
- 透過 Pull Request 機制將新功能合併回 `main` 分支。
- PR 過程中已包含修改內容的詳細描述。

## 3. 版本回復 (Version Revert)
**操作說明：**
我在這次作業中使用 `git revert` 回復了 Commit `71da1a6` ("update layout")。

**原因：**
該次提交在調整版面配置時，意外導致移動端顯示跑版（Layout Shift），且影響了導航列的固定定位。為了確保主分支 (`main`) 的穩定性，選擇使用 `revert` 指令產生一個新的 Commit 來抵銷該次變更，而非使用 `reset` 刪除紀錄，以保留完整的版本歷史軌跡。

## 4. A/B 版本實驗 (A/B Test)
針對「技能展示 (Skills)」區塊，我實作了兩種視覺呈現版本進行比較：

- **A 版本 (分支 `feature/skills-bars`)**：使用動態進度條 (Progress Bars) 展示。
- **B 版本 (分支 `feature/skills-tags`)**：使用標籤雲 (Tag Cloud) 方式排列。

**實驗結果與決策：**
- **最終採用**：A 版本 (進度條版)。
- **原因**：
  1. **視覺量化**：進度條能更直觀地呈現「趣味數據」（如：花錢能力 90%），比單純的標籤更具幽默感與視覺衝擊力。
  2. **排版整潔**：進度條的垂直排列與下方的時間軸 (Timeline) 設計語言較為一致，整體頁面閱讀動線更流暢。
  3. B 版本的標籤雲在手機版面上顯得過於擁擠，故決定合併 A 版本，並關閉 B 版本的 PR。

## 5. GitHub Pages 部署
本專案已啟用 GitHub Pages 進行靜態部署。

- **公開網址**： https://kkxcyy.github.io/yyy/
- **部署分支**： `main`

---

## 👤 作者
**葉宥汝**
- GitHub: [kkxcyy](https://github.com/kkxcyy)
- 
