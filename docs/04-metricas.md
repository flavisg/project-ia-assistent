# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** Você define perguntas e respostas esperadas;
2. **Feedback real:** Pessoas testam o agente e dão notas.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente compreendeu corretamente a situação financeira do usuário e respondeu de forma adequada? | Usuário informa renda e despesas e o agente calcula corretamente a capacidade de economia |
| **Segurança** | O agente evita inventar informações ou dados financeiros? | Usuário pergunta algo sem dados suficientes e o agente solicita mais informações |
| **Coerência** | As recomendações fazem sentido para o objetivo do usuário? |Usuário quer sair do vermelho e o agente sugere priorização de dívidas |
| **Clareza das Recomendações** | As orientações fornecidas são compreensíveis e acionáveis? | Agente sugere ações práticas como redução de despesas específicas |
| **Consistência** | O agente mantém coerência entre respostas ao longo da conversa? | O agente não altera o diagnóstico financeiro sem novos dados |

---

## Exemplos de Cenários de Teste

> Testes práticos ajudam a validar se o agente está executando corretamente suas funções.

### Teste 1: Identificação de objetivo financeiro
- **Pergunta:** "Quero melhorar minha vida financeira."
- **Resposta esperada:** O agente solicita que o usuário defina um objetivo financeiro (ex.: sair do vermelho, juntar dinheiro, viajar).
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 2: Diagnóstico financeiro básico
- **Pergunta:** "Minha renda é 5000 e meus gastos são 4200. Estou conseguindo economizar bem?"
- **Resposta esperada:** O agente identifica a capacidade de economia aproximada e explica o impacto no objetivo financeiro.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 3: Análise de padrão de gastos
- **Pergunta:** "Estou gastando muito com lazer?"
- **Resposta esperada:** O agente analisa os dados do ' transacoes.csv ' e avalia a proporção da categoria lazer no orçamento.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 4: ### Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo amanhã?"
- **Resposta esperada:** O agente informa que sua especialidade é planejamento financeiro.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 5: Falta de dados suficientes
- **Pergunta:** "Como está minha situação financeira?"
- **Resposta esperada:** O agente solicita mais informações antes de realizar uma análise.
- **Resultado:** [ ] Correto  [ ] Incorreto

---

## Resultados

> Após os testes realizados, as conclusões podem ser registradas abaixo.

**O que funcionou bem:**

- O agente conseguiu identificar corretamente objetivos financeiros dos usuários.
- As recomendações apresentaram linguagem clara e orientada à ação.
- O fluxo de diagnóstico financeiro funcionou de forma consistente.

**O que pode melhorar:**

- Melhorar a precisão da análise de categorias de despesas.
- Refinar perguntas iniciais para obter mais contexto financeiro do usuário.
- Expandir a base de estratégias financeiras para diferentes objetivos.

---

## Métricas Avançadas

Além das avaliações qualitativas, também podem ser monitoradas métricas técnicas relacionadas ao desempenho do agente:

- latência e tempo médio de resposta
- consumo de tokens
- custo por interação
- registro de logs de conversação
- taxa de erros ou respostas incompletas

Ferramentas especializadas em observabilidade para LLMs podem auxiliar nesse monitoramento, como:

[LangWatch](https://langwatch.ai/)

[LangFuse](https://langfuse.com/)

Essas plataformas permitem acompanhar o comportamento do agente, identificar falhas e melhorar continuamente a qualidade das respostas.
