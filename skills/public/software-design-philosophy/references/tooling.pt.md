# Compatibilidade multi-ferramenta (Claude Code / OpenCode / Gemini CLI / Codex)

Objetivo: manter saídas consistentes entre agentes CLI/IDE.

## Regras comuns
- Apenas Markdown em texto puro.
- Diagramas:
  - Diagrama de classes: PlantUML
  - Diagrama de sequência: Mermaid
- Estrutura: títulos + listas planas, sem listas aninhadas.

## Claude Code
- Preferência: conciso, orientado a tarefas.
- Fornecer conclusão antes dos detalhes.
- Recomendado: resumo + diagramas + checklist.

## OpenCode
- Preferência: etapas de engenharia e entregáveis.
- Incluir próximos passos e artefatos.
- Recomendado: lista de entregáveis.

## Gemini CLI
- Preferência: passos claros e acionáveis.
- Evitar fundo longo.
- Recomendado: Objetivo / Passos / Saída.

## Codex
- Preferência: orientações executáveis.
- Mencionar o arquivo de referência usado.
- Manter formato consistente.
