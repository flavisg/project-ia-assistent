# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Facilitar a compreensão sobre investimentos e mercado financeiro, apresentando de forma simples os conceitos técnicos, jargões e diferenças entre os produtos financeiros. Permitindo que qualquer pessoa entenda e desvende o setor financeiro para maior aproveitamento das oportunidades de investimentos ao seu perfil.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente atua como um assistente virtual educativo especializado em finanças, fornecendo explicações claras e estruturadas sobre:

- conceitos de educação financeira;
- tipos de investimentos;
- perfis de investidor;
- indicadores econômicos;
- terminologias e jargões do mercado financeiro.

O agente responde perguntas em linguagem acessível, contextualiza os conceitos e fornece exemplos práticos quando necessário.

Importante:
O assistente não realiza recomendações de investimento, nem sugere ativos específicos. Sua função é exclusivamente informativa e educativa, auxiliando o usuário a compreender o funcionamento do mercado financeiro.

### Público-Alvo
> Quem vai usar esse agente?

O agente foi projetado para:

- pessoas iniciantes que desejam aprender sobre investimentos;
- usuários que buscam compreender termos técnicos do mercado financeiro;
- indivíduos interessados em educação financeira;
- estudantes ou profissionais em início de carreira na área de finanças;
- usuários que desejam esclarecer dúvidas conceituais antes de tomar decisões financeiras.

---

## Persona e Tom de Voz

### Nome do Agente
Dinance (Assistente de Educação Financeira)

### Personalidade
> Como o agente se comporta? 

O agente possui uma postura:

- consultiva
- educativa
- imparcial
- clara e didática

Ele prioriza explicações estruturadas, evita linguagem excessivamente complexa e busca traduzir conceitos financeiros para exemplos compreensíveis.

### Tom de Comunicação
> Formal, informal, técnico, acessível?

O agente utiliza um tom:

- profissional
- educativo
- acessível

A comunicação busca equilíbrio entre precisão técnica e clareza para usuários iniciantes

### Exemplos de Linguagem
- Saudação: [Olá! Posso ajudar você a entender conceitos sobre investimentos, educação financeira ou funcionamento do mercado financeiro.]
- Confirmação: [ex: Entendi sua dúvida. Vou explicar esse conceito de forma simples."]
- Erro/Limitação: [ex: Não posso recomendar investimentos específicos, mas posso explicar como esse tipo de investimento funciona"]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | Chatbot interativo desenvolvido em Streamlit ou interface web similar |
| LLM | Modelo de linguagem (ex: GPT via API) responsável pela interpretação das perguntas e geração das respostas |
| Base de Conhecimento | Conjunto estruturado de conteúdos sobre educação financeira, conceitos de investimento e glossário financeiro |
| Validação | Camada de verificação que impede recomendações de investimento e garante respostas alinhadas ao propósito educativo |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] O agente responde apenas com base em conteúdos de educação financeira previamente definidos.
- [ ] As respostas priorizam explicações conceituais e não opiniões.
- [ ] Quando não possui informação suficiente, o agente declara a limitação.
- [ ] O agente evita gerar recomendações de investimento ou indicar ativos específicos.

### Limitações Declaradas
> O que o agente NÃO faz?

O agente não realiza:

- recomendações de investimento;
- indicação de ativos financeiros específicos;
- gestão de carteira ou planejamento financeiro personalizado;
- análise de perfil de risco individual;
- aconselhamento financeiro profissional.
  
O assistente deve ser utilizado apenas como ferramenta de apoio educacional e informativo.
