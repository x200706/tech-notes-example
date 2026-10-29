# 技術筆記

一個模擬部落格的靜態網站，用來呈現技術文件，並展示主題切換功能。內容是我過去整理的 Docker、Linux、SQL 學習筆記，重新校正後放上來。

線上展示：https://x200706.github.io/tech-notes-example/

## 內容

| 筆記 | 重點 |
| --- | --- |
| Docker 踩坑筆記 | Dockerfile 快取、Compose 健康檢查、掛載與權限、Nginx 反向代理、排程、上版策略 |
| Linux 小抄 | 系統服務、排程、磁碟與記憶體、檔案搜尋、網路埠查詢、Vim |
| SQL 小抄 | NULL 與引號、日期區間、索引與最左前綴、子查詢、分頁排序、備份還原 |

## 功能

- **12 套編輯器配色**：VS Code、GitHub、Catppuccin、Dracula、Nord 等，淺色與深色都有。整頁顏色由 CSS 變數控制，切換主題只替換一組設計 token。
- **記住選擇**：主題存在 localStorage；瀏覽器封鎖儲存時（例如無痕模式），頁面照常運作，只是不記住。沒選過時，依系統的深淺色模式挑預設值。
- **三篇筆記與目錄**：以網址 hash 切換筆記（`#docker`、`#linux`、`#sql`），側欄目錄可直接跳到段落。
- **程式碼**：語法上色（highlight.js）與一鍵複製。
- **無障礙**：主題選單支援方向鍵、Home／End、Esc 關閉並把焦點還給按鈕；尊重「減少動態效果」設定。
- **響應式**：手機到桌機都不會出現橫向卷軸，窄螢幕時側欄移到上方，目錄可收合。

## 技術

- HTML、CSS（CSS Variables、Grid）、原生 JavaScript，不需要建置步驟
- highlight.js 11.9.0（cdnjs）
- GitHub Pages 部署

## 本機預覽

```bash
git clone https://github.com/x200706/tech-notes-example.git
cd tech-notes-example
python3 -m http.server 8000
# 打開 http://localhost:8000
```

## 開發方式

這個網站以 AI 協作開發（Claude）。我負責需求定義、內容整理與技術校正、介面審查與驗收；頁面程式碼由 AI 依需求產出，再由我逐項確認。

## 配色出處

配色參考 VS Code Dark+、GitHub Primer、Catppuccin、Dracula、One Dark、Monokai、Tokyo Night、Nord、Gruvbox、Solarized 等公開主題，版權屬原作者。
