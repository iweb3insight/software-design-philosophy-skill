# Checklist de boas práticas de design

## 1. Pensamento sistêmico
1. Desenhar a visão do sistema
- Ação: criar diagramas de componentes, fluxo de dados e dependências.
- Dica: marcar fronteiras e contratos.
2. Verificar consistência global
- Ação: revisar nomes, estilo e tratamento de erros.
- Dica: usar revisão ou análise estática.
3. Definir fronteiras primeiro
- Ação: definir responsabilidades, interfaces e dependências.
- Dica: complexidade interna não deve vazar.

## 2. Modularidade e camadas
4. Separar por função
- Ação: separar apresentação, negócio e dados.
- Dica: cada camada com uma responsabilidade.
5. Alta coesão, baixo acoplamento
- Ação: minimizar dependências externas.
- Dica: esconder implementações via interfaces.
6. Separar bibliotecas comuns e de negócio
- Ação: isolar utilitários comuns.
- Dica: evitar dependências circulares.

## 3. Design progressivo
7. Seguir YAGNI
- Ação: implementar apenas o necessário.
- Dica: evoluir quando os requisitos mudarem.
8. Refatorar módulos-chave
- Ação: simplificar módulos complexos.
- Dica: manter manutenibilidade.
9. Revisão e feedback
- Ação: revisar arquitetura por iteração.
- Dica: definir marcos regulares.

## 4. Compreensibilidade e manutenibilidade
10. Nomes claros
- Ação: nomes explícitos para classes/funções.
- Dica: convenções de equipe.
11. Interfaces simples
- Ação: expor apenas o necessário.
- Dica: documentar parâmetros, retornos, erros.
12. Padrões e templates
- Ação: usar padrões comprovados.
- Dica: reduzir design repetitivo.

## 5. Experiência e feedback
13. Extrair padrões de sucesso
- Ação: analisar projetos open-source ou internos.
- Dica: foco em práticas reutilizáveis e escaláveis.
14. Analisar falhas
- Ação: documentar causas raiz.
- Dica: criar biblioteca de lições aprendidas.
15. Estabelecer revisões
- Ação: registrar decisões e monitorar performance.
- Dica: fazer revisões pós-lançamento.
