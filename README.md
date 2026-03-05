# PopMagic Skills

這是一個 PopMagic Skills 的集合庫。

## 使用方式

在你的專案中，使用以下指令來加入 skills：

```bash
npx skills add wpsteak/popmagic-skills --skill emotion-bird
```

## Available Skills

### emotion-bird

情勒鳥 (Emotional Bird)

一個用來督促使用者完成任務的 skill，特色是有點像 Duolingo 的 Duo 風格，使用帶有黑色幽默和輕微威脅的語氣來提醒待辦事項。

主要功能：
- 檢查 Notion 中的 "Daily Task"。
- 找出當天未完成的待辦事項。
- 在 Notion 頁面上留下「情勒」風格的留言提醒。

### screen-logger

Screen Logger

一個自動化記錄 macOS 螢幕活動的 AI Skill（工作流程）。

主要功能：
- 自動執行 macOS `screencapture` 指令擷取當前螢幕畫面。
- 透過視覺能力讀取並分析畫面內容，判斷使用者當前進行的任務。
- 將包含時間戳記及輕量摘要的活動記錄附加至 `activity_log.txt` 中。
- 自動刪除暫存截圖，保持專案整潔。
