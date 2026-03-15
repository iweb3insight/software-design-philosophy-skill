# Software Design Philosophy Skill

A multi-language design skill that turns software design thinking into structured outputs: outlines, actionable steps, review checklists, and diagrams. The guiding ideas are inspired by the book *A Philosophy of Software Design*.

## Quick Start (Vibe Coding Friendly)
1. Ask for a design outline
2. Ask for actionable methodology steps
3. Ask for a review checklist

Example prompts:
- "Give a structured design outline for a chat app."
- "Turn layering, modularity, and interface contracts into actionable steps."
- "Give me a review checklist with action + tip."

## Supported Languages
- English (default)
- Simplified Chinese
- Traditional Chinese
- French
- German
- Portuguese

## Supported Vibe Coding IDE/Agents
- Claude Code
- OpenCode
- Gemini CLI
- Codex

## Installation

### Claude / Claude Code (ZIP upload)
```bash
cd skills/public
zip -r software-design-philosophy.zip software-design-philosophy
```
Then upload the ZIP in Claude: Customize > Skills.

### OpenCode (project-local)
```bash
mkdir -p .opencode/skills
cp -R skills/public/software-design-philosophy .opencode/skills/
```

---

<div align="center">
  <img src="./assets/software-design-philosophy.png" width="480" />
</div>

### OpenCode (global)
```bash
mkdir -p ~/.config/opencode/skills
cp -R skills/public/software-design-philosophy ~/.config/opencode/skills/
```

### Gemini CLI (user scope)
```bash
gemini skills link /path/to/skills/public
```

### Gemini CLI (workspace scope)
```bash
gemini skills link /path/to/skills/public --scope workspace
```

### Codex (generic fallback)
```bash
cp -R skills/public/software-design-philosophy /path/to/your/codex/skills/
```

## Example: Chat System (Full)

### 1) Structured Outline
User:
```
We are building an internal chat system. Provide a structured design outline for review.
```

Skill route:
`references/outline.en.md`

Output:
```
Part 1: System goals and boundaries
- Use cases and roles
- Scope and non-goals

Part 2: Architecture and layering
- UI layer
- Application layer
- Message and conversation services
- Storage and infrastructure

Part 3: Core modules
- Users and organizations
- Conversations and messages
- Presence and notifications
- Permissions and audit

Part 4: Reliability and scalability
- Message reliability
- Storage scaling
- Monitoring and alerting
```

### 2) Actionable Methodology
User:
```
Turn layering, modularity, and interface contracts into actionable steps.
```

Skill route:
`references/methodology.en.md`

Output:
```
Layering
Principle: separate responsibilities and reduce coupling.
Method: UI only renders; application orchestrates use cases; domain enforces rules; infrastructure handles storage/queues.
Example: sending a message is orchestrated in the application layer; domain validates state changes.

Modularity
Principle: split by business capability.
Method: users, conversations, messages, presence, permissions as modules; modules interact only via interfaces.
Example: conversation module does not write to message storage directly.

Interface contracts
Principle: stable contracts over implementations.
Method: define inputs/outputs/errors/idempotency; version contracts for evolution.
Example: SendMessage supports idempotency key and status receipt.
```

### 3) Architecture Review Checklist
User:
```
Give a chat-system architecture review checklist. Each item must include an action and a tip.
```

Skill route:
`references/checklist.en.md`

Output:
```
1. Verify layer boundaries
Action: check UI, app, and message services responsibilities.
Tip: UI must not access storage or queues directly.

2. Verify module dependency direction
Action: review dependencies between conversation, message, and user modules.
Tip: avoid cross-layer writes and circular dependencies.

3. Define message interface contracts
Action: specify inputs, outputs, errors, and idempotency rules.
Tip: document idempotency key creation and validation.
```

### 4) Combined Request
User:
```
Prepare review materials: give a methodology summary first, then a checklist.
```

Skill route:
`references/methodology.en.md` then `references/checklist.en.md`

Output:
```
Methodology summary
- Clear layering with responsibility isolation
- Modularity by capability with one-way dependencies
- Stable interface contracts for evolution

Checklist
1. Draw system landscape
Action: produce component and dependency diagrams.
Tip: mark module boundaries and contracts.
2. Define module boundaries
Action: assign responsibilities and dependencies.
Tip: avoid circular dependencies.
```

### 5) Constraint Request
User:
```
Only give layering guidance. Do not include a checklist.
```

Skill route:
`references/methodology.en.md`

Output:
```
Layering
Principle: separate responsibilities and reduce coupling.
Method: UI renders; application orchestrates; domain enforces rules; infrastructure handles storage/queues.
Example: message sending is orchestrated in the application layer.
```
