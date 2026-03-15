# Chat-UI-Design (Web)

## Seitenstruktur
1. Login
- Konto, Passwort/OTP, Login-Button
- Workspace-Auswahl

2. Hauptansicht (Konversationsliste)
- Links: Konversationsliste (Gruppen, ungelesen)
- Mitte: Nachrichtenliste (MessageList)
- Unten: Composer (Composer)
- Rechts: Details (Mitglieder, Dateien, Einstellungen)

3. Konversationsdetails
- Mitgliederverwaltung (Rollen/Mute/Entfernen)
- Datei- und Link-Archiv
- Benachrichtigungen und Stummschalten

## Komponenten-Hierarchie (Web)
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

## Interaktionen
- Wechsel der Konversation aktualisiert MessageList und MemberDrawer
- Senden: Composer -> temporäre Nachricht -> ACK aktualisiert Status
- Ungelesen: Push aktualisiert ConversationList
- Präsenz: PresenceIndicator abonniert Status-Stream
