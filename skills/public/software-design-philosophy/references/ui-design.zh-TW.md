# 聊天 UI 設計（網頁端）

## 頁面結構
1. 登入頁
- 帳號輸入、密碼/驗證碼、登入按鈕
- 工作區選擇

2. 會話列表頁（主畫面）
- 左側：會話列表（分組、未讀數）
- 中間：訊息列表（MessageList）
- 底部：輸入區（Composer）
- 右側：會話詳情（成員、檔案、設定）

3. 會話詳情頁
- 成員管理（角色/禁言/移除）
- 檔案與連結歸檔
- 通知與免打擾

## 元件層級（Web）
- AppShell
- Sidebar
- ConversationList
- ConversationItem
- MessagePanel
- MessageList
- MessageItem
- Composer
- AttachmentPanel
- PresenceIndicator
- MemberDrawer

## 互動要點
- 會話切換：更新 MessageList 與 MemberDrawer
- 送出訊息：Composer → 暫存訊息 → ACK 更新狀態
- 未讀數：推送更新 ConversationList
- 線上狀態：PresenceIndicator 訂閱狀態流
