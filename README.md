# 猜猜我是誰 · 11/19 相調

翻牌猜人遊戲：先看描述，猜猜是誰，點一下卡片揭曉全名。打開網址就能玩，不用登入。

## 資料夾裡有什麼
| 檔案 | 用途 |
|---|---|
| `index.html` | 遊戲網頁本身（外觀、翻牌、投影模式） |
| `people.json` | 題庫名單：描述、姓氏、名字。改名單只要改這個檔案 |
| `CLAUDE.md` | 給 Claude Code 看的說明 |
| `.nojekyll` | 讓 GitHub 直接照原樣顯示網頁（不用動它） |

## 第一次架站（只要做一次）
1. 在 GitHub 建立新的儲存庫，名稱例如 `guess-who`，選 **Public（公開）**。
2. 把這個資料夾裡的所有檔案上傳進去（`.nojekyll` 也要）。
3. 進入儲存庫的 **Settings → Pages**，Source 選 **Deploy from a branch**，Branch 選 **main**、資料夾選 **/ (root)**，按 Save。
4. 等 1～2 分鐘，網址會出現在同一頁，格式是 `https://你的帳號.github.io/guess-who/`。

## 之後想修改
在 Claude Code 打開這個儲存庫，用中文直接說，例如：
- 「新增一位：愛唱詩歌的工程師，王小明」
- 「把謝宜彤的描述改成……」
- 「刪掉陳明輝」

Claude Code 改好、推上 GitHub 後，大約 1 分鐘網站就會更新。
