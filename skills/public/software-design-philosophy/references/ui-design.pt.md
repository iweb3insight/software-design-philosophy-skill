# Design de UI do chat (Web)

## Estrutura de páginas
1. Login
- conta, senha/OTP, botão entrar
- seleção de workspace

2. Tela principal (lista de conversas)
- Esquerda: lista de conversas (grupos, não lidas)
- Centro: lista de mensagens (MessageList)
- Base: composer (Composer)
- Direita: detalhes (membros, arquivos, configurações)

3. Detalhes da conversa
- gestão de membros (papéis/mute/remover)
- arquivo de arquivos e links
- notificações e modo silencioso

## Hierarquia de componentes (Web)
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

## Interações
- Trocar conversa atualiza MessageList e MemberDrawer
- Envio: Composer -> mensagem temporária -> ACK atualiza status
- Não lidas: push atualiza ConversationList
- Presença: PresenceIndicator assina fluxo de status
