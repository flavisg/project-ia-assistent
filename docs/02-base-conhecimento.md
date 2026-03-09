# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |


---

## Adaptações nos Dados

> Os dados mockados foram estruturados para representar cenários comuns de finanças pessoais.

As principais adaptações realizadas incluem:

- criação de categorias padronizadas de despesas (moradia, alimentação, lazer, transporte, investimentos);
- definição de objetivos financeiros frequentes entre usuários;
- associação entre objetivos financeiros e estratégias recomendadas;
- criação de exemplos de movimentações financeiras para simular análise de comportamento financeiro.

Essas adaptações permitem que o agente realize análises básicas de fluxo de caixa e comportamento financeiro, mesmo em ambiente de teste.

---

## Estratégia de Integração

### Como os dados são carregados?
> Os arquivos JSON e CSV são carregados no início da sessão do agente.

O processo segue as seguintes etapas:

  1. leitura dos arquivos da pasta data;
  2. conversão dos dados para estruturas manipuláveis (ex.: dicionários ou dataframes);
  3. disponibilização dessas informações para o motor de análise financeira do agente.

Os dados de transações são utilizados para identificar padrões de gastos e evolução financeira do usuário.

---

## Como os dados são usados no prompt?
Os dados são utilizados de duas formas:

*1. Contexto estrutural (System Prompt)*

Informações gerais sobre objetivos financeiros, estratégias e categorias de despesas são incluídas no contexto inicial do agente.

*2. Consulta dinâmica (Runtime)*

Os dados de movimentações financeiras do usuário são analisados dinamicamente para gerar:
- diagnósticos financeiros;
- alertas de comportamento;
- sugestões de ajustes no orçamento;
- acompanhamento do progresso financeiro.

---

## Exemplo de Contexto Montado?
Exemplo simplificado de dados estruturados enviados ao agente para análise:

```
Objetivo do usuário:
"Juntar dinheiro para uma viagem internacional em 12 meses"

Perfil financeiro identificado:
Renda mensal: 5000
Despesas fixas: 3200
Despesas variáveis médias: 1200
Capacidade potencial de economia: 600

Movimentações recentes:
Alimentação: 850
Lazer: 420
Transporte: 300
Compras online: 520

Diagnóstico preliminar:
O usuário possui potencial de economia mensal, porém apresenta aumento de gastos variáveis em lazer e compras online.

Estratégia sugerida:
Reduzir gastos variáveis em 20% para aumentar a taxa de poupança mensal e acelerar o alcance da meta.
...
```
