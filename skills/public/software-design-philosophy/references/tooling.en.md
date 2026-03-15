# Multi-Tool Compatibility (Claude Code / OpenCode / Gemini CLI / Codex)

Goal: keep outputs consistent across CLI/IDE agents.

## Common Rules
- Output plain Markdown only.
- Diagrams:
  - Class diagram: PlantUML
  - Sequence diagram: Mermaid
- Structure: headings + flat bullet lists, no nested lists.

## Claude Code
- Preference: concise, task-first.
- Provide a short conclusion before details.
- Recommended: summary + diagrams + checklist.

## OpenCode
- Preference: engineering steps and file guidance.
- Include next steps and deliverables.
- Recommended: output checklist of artifacts.

## Gemini CLI
- Preference: clear, actionable steps.
- Avoid long background; emphasize steps and constraints.
- Recommended: sections as Goal / Steps / Output.

## Codex
- Preference: executable, grounded guidance.
- Mention the reference file used.
- Keep format consistent.
