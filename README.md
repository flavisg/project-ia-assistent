# 🤖 GUARDÃO FINANCEIRO

## Assistente Inteligente para Planejamento e Monitoramento Financeiro

O Guardião Financeiro é um agente inteligente projetado para auxiliar usuários na organização da vida financeira, definição de objetivos e acompanhamento de comportamento de gastos.

O agente atua como um mentor financeiro digital, analisando informações fornecidas pelo usuário e oferecendo orientações estratégicas para melhorar a saúde financeira e alcançar metas financeiras pessoais.

> [!TIP]
> Este projeto demonstra a aplicação prática de LLMs (Large Language Models) na criação de agentes inteligentes voltados para educação financeira, análise de dados e suporte à tomada de decisão.

---

## Problema

Muitas pessoas desejam melhorar sua vida financeira, porém enfrentam dificuldades como:

- falta de clareza sobre seus objetivos financeiros;
- ausência de acompanhamento de gastos;
- dificuldade em interpretar sua situação financeira atual;
- falta de orientação para atingir metas financeiras.

> Sem um sistema de acompanhamento consistente, decisões financeiras acabam sendo tomadas de forma reativa e pouco estratégica.

---

### Solução

O Guardião Financeiro funciona como um assistente que:

1. Identifica o objetivo financeiro do usuário
2. Avalia sua situação financeira atual
3.Analisa padrões de comportamento financeiro
4. Sugere estratégias práticas para melhorar sua saúde financeira
5. Acompanha o progresso ao longo do tempo

Entre os objetivos financeiros que podem ser definidos estão:
- sair do endividamento
- juntar dinheiro
- realizar uma viagem internacional
- construir patrimônio
- organizar a vida financeira
- internacionalizar investimentos

> O agente fornece orientações estruturadas, sempre baseadas nas informações fornecidas pelo usuário.

---

### Funcionalidades do Agente

- Identificação de objetivos financeiros
- Diagnóstico financeiro inicial
- Análise de renda e despesas
- Identificação de padrões de gastos
- Sugestão de estratégias financeiras
- Monitoramento de progresso financeiro
- Notificações de acompanhamento
- Orientações para melhoria do comportamento financeiro

---

### Arquitetura do Projeto

>flowchart TD
    A[Usuário] --> B[Interface do Agente]
    B --> C[LLM - Modelo de Linguagem]
    C --> D[Base de Conhecimento]
    C --> E[Motor de Diagnóstico Financeiro]
    D --> C
    E --> C
    C --> F[Resposta ao Usuário]
---

### Estrutura do Repositório

```
📁 projeto-guardiao-financeiro/
│
├── 📄 README.md
│
├── 📁 data/                          # Dados mockados para o agente
│   ├── historico_atendimento.csv     # Histórico de atendimentos (CSV)
│   ├── perfil_investidor.json        # Perfil do cliente (JSON)
│   ├── produtos_financeiros.json     # Produtos disponíveis (JSON)
│   └── transacoes.csv                # Histórico de transações (CSV)
│
├── 📁 docs/                          # Documentação do projeto
│   ├── 01-documentacao-agente.md     # Caso de uso e arquitetura
│   ├── 02-base-conhecimento.md       # Estratégia de dados
│   ├── 03-prompts.md                 # Engenharia de prompts
│   ├── 04-metricas.md                # Avaliação e métricas

```

---

## Autor

Projeto desenvolvido como estudo prático de agentes inteligentes aplicados a finanças pessoais, explorando conceitos de IA generativa, engenharia de prompts e modelagem de sistemas baseados em LLM.


