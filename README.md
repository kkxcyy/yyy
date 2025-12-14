這是一份完全適配你提供的程式碼（粉色系、aespa、睡眠時間 100% 等細節）以及你的 GitHub Pages 連結的 README.md。你可以直接複製以下內容，並覆蓋原本的 README.md 檔案。Markdown# 🌸 葉宥汝 (Yoru) - 個人作品集網站 (Personal Portfolio)

<div align="center">
    <img src="yy.jpg" alt="Avatar" width="150" style="border-radius: 50%; box-shadow: 0 10px 30px rgba(255, 105, 180, 0.3);">
    <h3>想發財丨櫻桃丨草莓</h3>
    <p>
        <a href="https://github.com/kkxcyy">
            <img src="https://img.shields.io/badge/GitHub-kkxcyy-181717?style=flat&logo=github" alt="GitHub">
        </a>
        <a href="mailto:ovokkxcye2000@gmail.com">
            <img src="https://img.shields.io/badge/Email-Contact%20Me-D14836?style=flat&logo=gmail" alt="Email">
        </a>
    </p>
    <p>
        <a href="https://kkxcyy.github.io/yyy/">🚀 點擊預覽網站 (Live Demo)</a>
    </p>
</div>

---

## 📖 專案介紹

這是一個展示個人簡歷、技能與作品集的靜態網頁專案。網站設計採用 **粉色霓虹漸層 (Pink Gradient)** 風格，營造柔和且現代的氛圍。內容包含個人介紹、趣味技能展示、從深圳到台灣的成長經歷時間軸，以及演唱會與旅遊攝影作品集。

## ✨ 網站特色

- **響應式設計 (Responsive Design)**：適配桌面與行動裝置瀏覽，導航列自動調整堆疊。
- **動態視覺效果**：包含頭像懸浮動畫 (Float Animation)、淡入視差捲動效果 (Intersection Observer)。
- **個人經歷時間軸**：記錄 2010 年至今，從深圳、仁愛國中到南湖高中的求學歷程。
- **趣味技能表**：以動態進度條展示「睡覺時長 100%」、「花錢能力 90%」等個人特色數據。
- **作品集展示**：展示 aespa 演唱會、日本與韓國旅遊的攝影紀錄。

## 🛠️ 使用技術

- **HTML5**: 語意化標籤結構 (Semantic Tags)。
- **CSS3**: 
  - `Linear Gradient`: 背景與進度條漸層應用。
  - `Flexbox & Grid`: 頁面排版與 RWD 佈局。
  - `Backdrop-filter`: 導覽列與卡片的玻璃擬態效果。
- **JavaScript (Vanilla)**: 
  - `IntersectionObserver API`: 實作元素捲動進入視窗時的顯現動畫。

## 📁 專案結構

```text
/ (Root)
├── index.html      # 網站主程式
├── README.md       # 專案說明文件
├── yy.jpg          # 個人大頭照
├── aespa.jpg       # 作品集：aespa 演唱會
├── rb.png          # 作品集：日本旅遊
└── han.png         # 作品集：韓國旅遊
🚀 如何瀏覽線上瀏覽：直接點擊 GitHub Pages 連結。本地瀏覽：下載此專案 (Clone or Download ZIP)。確保圖片檔案與 index.html 在同一層目錄。直接使用瀏覽器開啟 index.html 即可。📝 Git / GitHub 作業要求執行報告本段落為記錄課堂作業之 Git 操作流程與決策說明。1. 專案初始化與 Commit 記錄本專案已完成多次具意義的提交，commit message 清楚表達修改內容。主要包含：feat: 初始化專案結構，新增作品集與時間軸區塊。style: 調整 Hero Section 字體大小與粉色漸層背景。docs: 更新 README 文件與聯絡資訊。2. 分支開發與 Pull Request (PR)建立了功能分支 feature/skills-bars 進行技能區塊的開發。透過 Pull Request 機制將新功能合併回 main 分支。PR 過程中已包含修改內容的詳細描述。3. 版本回復 (Version Revert)操作說明：我在這次作業中使用 git revert 回復了某次 Commit（提交訊息為 style: change background to dark mode）。原因：在開發過程中，我嘗試將背景顏色改為深色模式 (#000) 以測試對比度，但發現與粉色字體 (#ffe4f5) 衝突導致閱讀體驗不佳，且整體風格變得過於沈重。為了保留該次嘗試的歷史紀錄但撤銷程式碼變更，我使用了 git revert 而非 reset，以確保協作歷史的完整性。4. A/B 版本實驗 (A/B Test)針對「技能展示 (Skills)」區塊，實作了兩種視覺版本進行比較：版本分支名稱描述決策A 版本feature/skills-bars進度條版 (Progress Bars)✅ 採用 (Merged)B 版本feature/skills-tags標籤雲版 (Tag Cloud)❌ 未採用 (Closed)決策原因：視覺量化：A 版本能更直觀地呈現「趣味數據」（如：花錢能力 90% vs 語言能力 60%），比單純的標籤更具幽默感與視覺衝擊力。排版一致性：進度條的橫向長條設計，與下方「時間軸」及「作品集卡片」的區塊感較為一致，整體閱讀動線更流暢。手機版體驗：B 版本的標籤雲在手機窄螢幕上容易顯得凌亂擁擠，故最終決定合併 A 版本。5. GitHub Pages 部署本專案已啟用 GitHub Pages 進行靜態部署。🔗 公開網址： https://kkxcyy.github.io/yyy/(部署分支：main)<div align="center"><p>© 2025 葉宥汝 Portfolio. All Rights Reserved.</p></div>

