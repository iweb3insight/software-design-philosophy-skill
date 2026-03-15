---
name: software-design-philosophy
description: Generate software design philosophy outlines, actionable methodology steps, and design review checklists. Use when users ask for software design principles, structured design outlines, design methodologies, architecture review preparation, or best-practice checklists.
---

# Software Design Philosophy

## Overview
Use this skill to turn software design philosophy into structured outputs: outlines, actionable methodology steps, and review checklists.

## Routing Rules
Decide which reference to load based on intent:
- Outline requests ("大纲/章节/结构/目录") -> `references/outline.md`
- Outline requests (English: "outline/structure/chapters") -> `references/outline.en.md`
- Outline requests (Traditional Chinese: "大綱/章節/結構/目錄") -> `references/outline.zh-TW.md`
- Outline requests (French: "plan/structure/chapitres") -> `references/outline.fr.md`
- Outline requests (German: "Gliederung/Struktur/Kapitel") -> `references/outline.de.md`
- Outline requests (Portuguese: "esboço/estrutura/capítulos") -> `references/outline.pt.md`
- Methodology and execution steps ("方法论/落地/步骤/实践/理念+方法+案例") -> `references/methodology.md`
- Methodology (English: "methodology/steps/actionable") -> `references/methodology.en.md`
- Methodology (Traditional Chinese: "方法論/落地/步驟/實作") -> `references/methodology.zh-TW.md`
- Methodology (French: "méthodologie/étapes") -> `references/methodology.fr.md`
- Methodology (German: "Methodik/Schritte") -> `references/methodology.de.md`
- Methodology (Portuguese: "metodologia/passos") -> `references/methodology.pt.md`
- Checklists and review items ("清单/检查/评审/核对") -> `references/checklist.md`
- Checklists (English: "checklist/review items") -> `references/checklist.en.md`
- Checklists (Traditional Chinese: "清單/檢查/評審") -> `references/checklist.zh-TW.md`
- Checklists (French: "checklist/revue") -> `references/checklist.fr.md`
- Checklists (German: "Checkliste/Review") -> `references/checklist.de.md`
- Checklists (Portuguese: "checklist/revisão") -> `references/checklist.pt.md`
- Class diagrams / domain models ("类图/UML/领域模型/实体关系") -> `references/class-diagram.md`
- Class diagrams (English: "class diagram/domain model") -> `references/class-diagram.en.md`
- Class diagrams (Traditional Chinese: "類圖/UML/領域模型") -> `references/class-diagram.zh-TW.md`
- Class diagrams (French: "diagramme de classes") -> `references/class-diagram.fr.md`
- Class diagrams (German: "Klassendiagramm") -> `references/class-diagram.de.md`
- Class diagrams (Portuguese: "diagrama de classes") -> `references/class-diagram.pt.md`
- Sequence diagrams ("时序图/流程图/交互流程") -> `references/sequence-diagram.md`
- Sequence diagrams (English: "sequence diagram/flow") -> `references/sequence-diagram.en.md`
- Sequence diagrams (Traditional Chinese: "時序圖/流程圖") -> `references/sequence-diagram.zh-TW.md`
- Sequence diagrams (French: "diagramme de séquence") -> `references/sequence-diagram.fr.md`
- Sequence diagrams (German: "Sequenzdiagramm") -> `references/sequence-diagram.de.md`
- Sequence diagrams (Portuguese: "diagrama de sequência") -> `references/sequence-diagram.pt.md`
- UI design for web ("UI 设计/页面结构/交互流程/原型/网页端") -> `references/ui-design.md`
- UI design for web (English: "UI design/page structure/web") -> `references/ui-design.en.md`
- UI design for web (Traditional Chinese: "UI 設計/頁面結構/網頁") -> `references/ui-design.zh-TW.md`
- UI design for web (French: "design UI/structure de page") -> `references/ui-design.fr.md`
- UI design for web (German: "UI-Design/Seitenstruktur") -> `references/ui-design.de.md`
- UI design for web (Portuguese: "design de UI/estrutura de página") -> `references/ui-design.pt.md`
- Multi-agent/CLI compatibility ("Claude Code/Opencode/Gemini CLI/Codex/多工具适配") -> `references/tooling.md`
- Multi-tool compatibility (English: "Claude Code/OpenCode/Gemini CLI/Codex") -> `references/tooling.en.md`
- Multi-tool compatibility (Traditional Chinese) -> `references/tooling.zh-TW.md`
- Multi-tool compatibility (French) -> `references/tooling.fr.md`
- Multi-tool compatibility (German) -> `references/tooling.de.md`
- Multi-tool compatibility (Portuguese) -> `references/tooling.pt.md`
- Combined requests -> produce sections in order (methodology summary first, checklist second).

## Output Constraints
- Output in English by default. If the user explicitly asks for Chinese, output in Chinese.
- If the user requests Chinese (Simplified), Traditional Chinese, French, German, or Portuguese, output in that language.

## Language Detection and Conflict Rules
- Explicit user request wins (e.g., "answer in French" overrides other cues).
- If the user message is primarily in a supported language, use that language.
- If multiple languages are mixed, follow this priority:
1. Explicit request in the message
2. Most recent explicit request in the conversation
3. Dominant language of the current user message
4. Default to English
- If uncertain, ask a short clarification question before responding.
- Use structured headings and flat bullet lists.
- Emphasize action items and decision points; avoid empty theory.
- Follow the user-specified format if provided.

## Context Adaptation
- If team or system size is given, scale the recommendations (merge non-critical modules for small teams, keep contracts clear).
- If no context is provided, provide a concise default and offer expansion by section.

## Usage Examples
Use condensed examples from `references/examples.md` for consistent phrasing and structure.

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

Ensure the skill folder name remains `software-design-philosophy`, then restart or reload the agent so it can index the new skill.

## Resources
### references/
- `outline.md`: design philosophy outline
- `outline.en.md`: design philosophy outline (English)
- `outline.zh-TW.md`: design philosophy outline (Traditional Chinese)
- `outline.fr.md`: design philosophy outline (French)
- `outline.de.md`: design philosophy outline (German)
- `outline.pt.md`: design philosophy outline (Portuguese)
- `methodology.md`: actionable methodology
- `methodology.en.md`: actionable methodology (English)
- `methodology.zh-TW.md`: actionable methodology (Traditional Chinese)
- `methodology.fr.md`: actionable methodology (French)
- `methodology.de.md`: actionable methodology (German)
- `methodology.pt.md`: actionable methodology (Portuguese)
- `checklist.md`: best-practice checklist
- `checklist.en.md`: best-practice checklist (English)
- `checklist.zh-TW.md`: best-practice checklist (Traditional Chinese)
- `checklist.fr.md`: best-practice checklist (French)
- `checklist.de.md`: best-practice checklist (German)
- `checklist.pt.md`: best-practice checklist (Portuguese)
- `examples.md`: full use cases (chat system, tetris, NFT)
- `examples.en.md`: full use cases (English)
- `examples.zh-TW.md`: full use cases (Traditional Chinese)
- `examples.fr.md`: full use cases (French)
- `examples.de.md`: full use cases (German)
- `examples.pt.md`: full use cases (Portuguese)
- `class-diagram.md`: chat system class diagram (PlantUML)
- `class-diagram.en.md`: chat system class diagram (PlantUML, English)
- `class-diagram.zh-TW.md`: chat system class diagram (PlantUML, Traditional Chinese)
- `class-diagram.fr.md`: chat system class diagram (PlantUML, French)
- `class-diagram.de.md`: chat system class diagram (PlantUML, German)
- `class-diagram.pt.md`: chat system class diagram (PlantUML, Portuguese)
- `sequence-diagram.md`: chat system sequence diagram (Mermaid)
- `sequence-diagram.en.md`: chat system sequence diagram (Mermaid, English)
- `sequence-diagram.zh-TW.md`: chat system sequence diagram (Mermaid, Traditional Chinese)
- `sequence-diagram.fr.md`: chat system sequence diagram (Mermaid, French)
- `sequence-diagram.de.md`: chat system sequence diagram (Mermaid, German)
- `sequence-diagram.pt.md`: chat system sequence diagram (Mermaid, Portuguese)
- `ui-design.md`: web UI structure and components
- `ui-design.en.md`: web UI structure and components (English)
- `ui-design.zh-TW.md`: web UI structure and components (Traditional Chinese)
- `ui-design.fr.md`: web UI structure and components (French)
- `ui-design.de.md`: web UI structure and components (German)
- `ui-design.pt.md`: web UI structure and components (Portuguese)
- `tooling.md`: compatibility guidance for Claude Code, OpenCode, Gemini CLI, Codex
- `tooling.en.md`: compatibility guidance (English)
- `tooling.zh-TW.md`: compatibility guidance (Traditional Chinese)
- `tooling.fr.md`: compatibility guidance (French)
- `tooling.de.md`: compatibility guidance (German)
- `tooling.pt.md`: compatibility guidance (Portuguese)
