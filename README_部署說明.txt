AR 荷花觀察教室｜圖片辨識版
================================
檔案
- index.html：學生使用的 AR 互動教材
- lotus-card.png：圖片辨識圖卡（請使用原始檔）
- compile-target.html：官方編譯器操作指南
- README_部署說明.txt：本說明

為什麼舊版會顯示「MindAR Compiler 載入失敗」？
MindAR 1.2.x 的瀏覽器版本採用 ES modules，並非舊版 window.MINDAR.Compiler 全域物件。
因此舊版 compile-target.html 的程式呼叫方式不相容。新版已改成使用 MindAR 官方線上 Image Targets Compiler。

步驟 1：產生 targets.mind
1. 開啟 compile-target.html，或直接前往：
   https://hiukim.github.io/mind-ar-js-doc/tools/compile/
2. 上傳本資料夾中的 lotus-card.png。
3. 按 Start，等待圖片特徵分析完成。
4. 按 Download，下載 targets.mind。
5. 確認 targets.mind 與 index.html、lotus-card.png 放在同一層。

步驟 2：上傳 GitHub
1. Repository：https://github.com/oldtall99/-ar-lotus-classroom
2. 將 index.html、lotus-card.png、targets.mind 一起上傳到 Repository 根目錄。
   compile-target.html 和 README 也可一併上傳。
3. Settings > Pages > Deploy from a branch > main > /(root) > Save。
4. 等待 GitHub Pages 部署完成。

步驟 3：學生掃描
1. 列印 lotus-card.png，或在另一台螢幕以清晰原圖顯示。
2. 用手機開啟 GitHub Pages 網址並允許相機。
3. 將手機鏡頭對準這張完全相同的荷花圖片。
4. 辨識成功後，畫面會顯示 3D 荷花示意模型。

注意事項
- 必須用同一張 lotus-card.png 產生 targets.mind；辨識圖卡不可任意更換、裁切、旋轉或加字。
- 建議列印至少 12 x 12 公分，避免反光並保持平整。
- 相機功能必須在 HTTPS 網站或 localhost 執行。
- 官方編譯器若無法啟動，請改用桌面版 Chrome 或 Edge，並確認瀏覽器允許 WebGL。
- 網頁使用 MindAR、A-Frame CDN，首次載入需要網路。
- 目前 3D 模型是教學示意模型，非精密植物解剖模型。

官方參考
MindAR 圖片編譯工具：https://hiukim.github.io/mind-ar-js-doc/tools/compile/
MindAR 編譯說明：https://hiukim.github.io/mind-ar-js-doc/quick-start/compile/
MindAR 安裝說明：https://hiukim.github.io/mind-ar-js-doc/installation/
