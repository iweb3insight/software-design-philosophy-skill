# Compatibilité multi-outils (Claude Code / OpenCode / Gemini CLI / Codex)

Objectif : conserver des sorties cohérentes entre agents CLI/IDE.

## Règles communes
- Markdown texte brut uniquement.
- Diagrammes :
  - Diagramme de classes : PlantUML
  - Diagramme de séquence : Mermaid
- Structure : titres + listes à plat, pas de listes imbriquées.

## Claude Code
- Préfère concis et orienté tâche.
- Donner d'abord la conclusion.
- Recommandé : résumé + diagrammes + checklist.

## OpenCode
- Préfère les étapes d'ingénierie et les livrables.
- Inclure la prochaine étape et les artefacts.
- Recommandé : liste des livrables.

## Gemini CLI
- Préfère des étapes claires et actionnables.
- Éviter le background long.
- Recommandé : sections Objectif / Étapes / Sortie.

## Codex
- Préfère des indications exécutables.
- Mentionner le fichier reference utilisé.
- Format cohérent.
