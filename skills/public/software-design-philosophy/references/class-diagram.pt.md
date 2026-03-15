# Diagrama de classes (PlantUML)

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

Notas:
- Conversation é a raiz do agregado.
- Membership modela a relação muitos-para-muitos e papéis.
- Receipt registra estados de entrega/leitura.
