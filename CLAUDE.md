# 猜猜我是誰（11/19 相調）— 給 Claude Code 的說明

使用者 Howard 沒有技術背景，請用台灣繁體中文、白話說明，並在動手前簡短確認要改什麼。

## 專案
- 純靜態網站，用 GitHub Pages 從 `main` 分支根目錄發佈。沒有建置步驟、沒有套件。
- `index.html`：所有 CSS 與 JS 都寫在裡面。
- `people.json`：題庫。格式為陣列，每筆 `{"描述": "...", "姓氏": "...", "名字": "..."}`。陣列順序不影響遊戲（每輪會隨機洗牌）。

## 常見需求的做法
- **新增 / 修改 / 刪除人**：只改 `people.json`。保持 UTF-8、2 格縮排、合法 JSON（改完用 `python3 -m json.tool people.json` 檢查）。
- **改外觀**：改 `index.html` 的 `<style>`。顏色都在 `:root` 的 CSS 變數；深色模式在 `@media (prefers-color-scheme: dark)` 區塊。
- 右上角圓形按鈕（`#themeBtn`）切換深淺色：預設跟著裝置，按過後用 `localStorage` 記住該裝置的選擇（寫在 `<html data-theme>`）。淺色時顯示月亮圖示、深色時顯示太陽圖示。
- 名字（`.name`）必須一行顯示：保留 `white-space:nowrap` 與 `24cqi` 自動縮放。
- 一律使用投影模式版面（`<body class="big">`，沒有切換按鈕）：卡片高度要能和按鈕一起放進一個畫面。

## 改完之後
1. 本機用 `python3 -m http.server` 開起來看一下（直接雙擊 index.html 會讀不到 people.json，這是正常的）。
2. `git add`、`git commit`（中文訊息，簡述改了什麼）、`git push`。
3. 告訴 Howard：約 1 分鐘後重新整理網站就會看到。

## 注意
- 儲存庫是公開的，名單任何人都看得到。新增個人資料時，若內容可能敏感（電話、地址、健康狀況等），先提醒 Howard。
