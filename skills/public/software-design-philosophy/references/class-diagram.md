# 聊天软件类图（PlantUML）

以下为网页端聊天软件的核心领域模型类图，使用 PlantUML 表达。

```plantuml
@startuml
skinparam classAttributeIconSize 0

class User {
  +id: String
  +name: String
  +avatarUrl: String
  +status: String
}

class Conversation {
  +id: String
  +type: String  // direct | group
  +title: String
  +createdAt: DateTime
}

class Membership {
  +id: String
  +role: String  // owner | admin | member
  +joinedAt: DateTime
}

class Message {
  +id: String
  +senderId: String
  +content: String
  +type: String  // text | image | file
  +sentAt: DateTime
  +status: String // sending | sent | delivered | read
}

class Attachment {
  +id: String
  +url: String
  +mimeType: String
  +size: Long
}

class Receipt {
  +id: String
  +messageId: String
  +userId: String
  +status: String // delivered | read
  +timestamp: DateTime
}

User "1" -- "0..*" Membership
Conversation "1" -- "0..*" Membership
Conversation "1" -- "0..*" Message
Message "0..*" -- "0..*" Attachment
Message "1" -- "0..*" Receipt
@enduml
```

说明：
- Conversation 是会话聚合根；Membership 体现用户与会话的多对多关系与角色。
- Message 归属 Conversation；Receipt 记录消息到达/已读状态。
- Attachment 与 Message 为多对多，便于一条消息携带多个附件。
