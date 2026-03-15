# Metodologia de design (acionável)

## 1. Pensamento sistêmico
- Princípio: design é o sistema como um todo.
- Métodos:
1. Desenhar cedo a visão do sistema (componentes, fluxo de dados, dependências).
2. Priorizar fronteiras claras e contratos de interface.
3. Verificar consistência global (estilo, nomes, tratamento de erros).
- Exemplo: projetos open-source definem fronteiras e contratos cedo para escalar.

## 2. Modularidade e camadas
- Princípio: modularidade clara reduz acoplamento.
- Métodos:
1. Separar por função e dependência (apresentação, negócio, dados).
2. Alta coesão interna, baixo acoplamento externo.
3. Separar bibliotecas comuns de bibliotecas de negócio.
- Exemplo: separação entre acesso a dados e lógica de negócio.

## 3. Design progressivo
- Princípio: design evolui com requisitos e tecnologia.
- Métodos:
1. Evitar over-design (YAGNI).
2. Refatorar módulos-chave regularmente.
3. Ajustar via revisões e feedback.
- Exemplo: limites de microservices refinados por iterações.

## 4. Compreensibilidade e manutenibilidade
- Princípio: código e docs são ferramentas de comunicação.
- Métodos:
1. Nomes claros e sem ambiguidades.
2. Interfaces simples, complexidade escondida.
3. Usar padrões e templates.
- Exemplo: frameworks como Django são fáceis devido a APIs claras.

## 5. Experiência e ciclo de feedback
- Princípio: design melhora com prática.
- Métodos:
1. Extrair padrões de casos de sucesso.
2. Analisar falhas (causa raiz).
3. Estabelecer revisões e monitoramento.
- Exemplo: revisões regulares mantêm sistemas saudáveis.
