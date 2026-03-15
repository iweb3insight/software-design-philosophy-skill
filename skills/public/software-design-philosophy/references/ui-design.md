# 聊天软件 UI 设计（网页端）

## 页面结构
1. 登录页
- 账号输入、验证码/密码、登录按钮
- 组织或工作区选择

2. 会话列表页（主界面）
- 左侧：会话列表（支持分组、未读数）
- 中间：消息列表（MessageList）
- 底部：输入区（Composer）
- 右侧：会话详情（成员、文件、设置）

3. 会话详情页
- 成员管理（角色/禁言/移除）
- 文件与链接归档
- 通知与免打扰

## 组件层级（Web）
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

## 交互要点
- 会话切换：更新 MessageList 与 MemberDrawer
- 发送消息：Composer -> 临时消息 -> ACK 更新状态
- 未读计数：后台推送 -> ConversationList 更新
- 在线状态：PresenceIndicator 订阅状态流
