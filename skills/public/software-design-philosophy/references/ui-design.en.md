# Chat UI Design (Web)

## Page Structure
1. Login
- account input, password/OTP, login button
- workspace selection

2. Main (conversation list)
- Left: conversation list (groups, unread count)
- Center: message list (MessageList)
- Bottom: composer (Composer)
- Right: conversation details (members, files, settings)

3. Conversation details
- member management (roles/mute/remove)
- files and links archive
- notifications and mute

## Component Hierarchy (Web)
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

## Interaction Notes
- Switching conversation updates MessageList and MemberDrawer
- Sending: Composer -> temp message -> ACK updates status
- Unread count: push updates ConversationList
- Presence: PresenceIndicator subscribes to status stream
