# Design UI Chat (Web)

## Structure des pages
1. Connexion
- compte, mot de passe/OTP, bouton connexion
- choix d'espace de travail

2. Écran principal (liste des conversations)
- Gauche : liste des conversations (groupes, non lus)
- Centre : liste des messages (MessageList)
- Bas : zone de saisie (Composer)
- Droite : détails (membres, fichiers, réglages)

3. Détails de la conversation
- gestion des membres (rôles/mute/suppression)
- archive des fichiers et liens
- notifications et mode silencieux

## Hiérarchie des composants (Web)
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

## Interactions clés
- Changer de conversation met à jour MessageList et MemberDrawer
- Envoi : Composer -> message temporaire -> ACK
- Non lus : push met à jour ConversationList
- Présence : PresenceIndicator souscrit au flux d'état
