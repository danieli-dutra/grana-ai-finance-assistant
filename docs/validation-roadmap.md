# 🎯 Grana.ai — Validation Roadmap

## Visão do produto

O Grana.ai nasceu a partir de um desafio técnico durante o Bootcamp Lupo na DIO, mas rapidamente evoluiu para um experimento de produto real.

A proposta é simples:

**ajudar pessoas a organizarem suas finanças através de conversas naturais, sem depender de planilhas complexas ou interfaces frias.**

A hipótese central do produto é:

> Pessoas querem entender melhor seu dinheiro, mas muitas abandonam apps financeiros porque o processo de registro e acompanhamento exige esforço demais.

O Grana.ai busca resolver isso através de:

- Conversas naturais
- Registro financeiro por linguagem humana
- Metas financeiras visuais
- Insights personalizados
- Acompanhamento comportamental

---

# 🔍 Hipóteses que queremos validar

## Hipótese 01 — Conversação

> Usuários se sentem mais confortáveis registrando gastos em formato de conversa do que em formulários tradicionais.

### Como validar:

Testes de uso com usuários reais.

### Sinais positivos:

- Usuário registra múltiplos lançamentos sem dificuldade
- Usuário entende rapidamente como usar o chat
- Poucas dúvidas durante onboarding

### Métrica inicial:

- Tempo até primeiro lançamento
- Número de lançamentos por sessão

---

## Hipótese 02 — Clareza financeira

> Usuários conseguem entender melhor para onde o dinheiro está indo usando dashboard + conversa.

### Como validar:

Testes observacionais + feedback qualitativo.

### Sinais positivos:

- Usuário identifica categoria com maior gasto
- Usuário comenta espontaneamente sobre padrões de consumo

### Métrica inicial:

- Percentual de usuários que entendem o dashboard sem explicação

---

## Hipótese 03 — Assistente gera confiança

> Um assistente contextual aumenta a sensação de suporte financeiro.

### Como validar:

Questionário pós uso.

### Sinais positivos:

- Usuário sente que o assistente realmente "acompanha"
- Usuário entende sugestões financeiras como úteis

### Métrica inicial:

- Nota de confiança no assistente (0 a 10)

---

## Hipótese 04 — Confiança baseada em correção

> Usuários tendem a confiar mais no assistente quando ele reconhece dúvidas, pede confirmação e permite correções naturais.

### Como validar:

Testes observacionais com lançamentos ambíguos.

### Sinais positivos:

- Usuário aceita responder perguntas de categorização;
- Usuário corrige lançamentos sem frustração;
- Redução de erros de classificação.

### Métrica inicial:

- Número de correções por sessão;
- Taxa de sucesso nas correções.

---


# 👥 Público inicial de validação

## Fase 1 — Testes controlados

Pessoas próximas:

- Familiares
- Amigos
- Colegas de estudo

Perfil desejado:

- Pessoas que têm dificuldade em controlar gastos
- Pessoas que já tentaram apps financeiros antes
- Usuários que não usam planilhas

Objetivo:

Identificar problemas de UX, entendimento e confiança.

---

## Fase 2 — Testes ampliados

Após estabilização:

- Comunidade LinkedIn
- Comunidade DIO
- Colegas da faculdade
- Comunidades tech / produto

Objetivo:

Buscar padrões de comportamento.

---

# 🧪 Roteiro de testes

Cada participante deverá realizar:

## Cenário 01

Registrar:

- salário
- mercado
- streaming
- transporte

## Cenário 02

Criar uma meta financeira.

## Cenário 03

Pedir uma dica financeira.

## Cenário 04

Corrigir:

- uma categoria incorreta;
- um lançamento classificado como despesa em vez de meta;
- uma interpretação ambígua feita pelo assistente.

---

# 📋 Coleta de feedback

Após o teste, aplicar Google Forms com:

## Facilidade de uso

> Foi fácil registrar seus gastos?

Escala: 1 a 5

---

## Clareza

> Você entendeu para onde seu dinheiro estava indo?

Escala: 1 a 5

---

## Confiança

> Você confiaria em usar esse assistente por mais tempo?

Escala: 1 a 5

---

## Valor percebido

> O que mais te chamou atenção?

Resposta aberta

---

## Fricções

> Em algum momento você ficou confuso?

Resposta aberta

---

# 🚀 Próximas iterações

Após os testes, priorizar:

## UX

- Melhorar onboarding
- Reduzir dúvidas de categorização
- Melhorar clareza do dashboard

## IA

- Melhorar memória contextual
- Melhorar interpretação de intenções
- Reduzir respostas genéricas

## Produto

- Score de saúde financeira
- Gastos recorrentes automáticos
- Recomendações personalizadas

---

# 📅 Status atual

## Versão atual

MVP funcional em evolução contínua com:

- Lovable + Vibe Coding
- Iterações diárias orientadas por testes reais
- Correções baseadas em comportamento do agente
- Parser financeiro com regras determinísticas
- Sistema de categorização com fallback por confiança

Nesta fase, o produto já demonstra:

- reconhecimento de merchants e serviços recorrentes;
- metas separadas de despesas;
- correções contextuais;
- insights financeiros mais humanos e personalizados.

## Próximo marco

Primeiros testes externos com usuários reais.