# 🎯 Grana.ai — Validation Roadmap

## Visão do produto

O Grana.ai nasceu a partir de um desafio técnico durante o Bootcamp Lupo na DIO, mas rapidamente evoluiu para um experimento de produto real.

A proposta é simples:

**ajudar pessoas a organizarem suas finanças através de conversas naturais, sem depender de planilhas complexas ou interfaces frias.**

A hipótese central do produto é:

> Pessoas querem entender melhor seu dinheiro, mas muitas abandonam apps financeiros porque o processo de registro e acompanhamento exige esforço demais.

O Grana.ai busca resolver isso através de:

- Conversas naturais
- Registro financeiro por linguagem natural
- Metas financeiras integradas
- Dashboard contextual
- Score de saúde financeira
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

## Hipótese 05 — Perguntas aumentam confiança

> Usuários confiam mais no sistema quando ele reconhece ambiguidades, pede confirmação antes de registrar um lançamento e sugere padrões recorrentes sem agir automaticamente.

### Como validar:

Testes com entradas incompletas, ambíguas e recorrentes.

### Exemplos:

- "comprei 50"
- "pix de 30"
- "salvei 100"

Recorrência:

- salário
- internet
- streaming

### Sinais positivos:

- Usuário responde à pergunta do assistente sem frustração;
- Usuário percebe maior precisão no sistema;
- Usuário aceita sugestões de recorrência;
- Redução de lançamentos incorretos.

### Métrica inicial:

- taxa de confirmação aceita;
- número de correções após categorização;
- taxa de aceitação de recorrência.

---

## Hipótese 06 — Saúde financeira aumenta percepção de valor

> Usuários percebem mais valor no produto quando o assistente interpreta sua situação financeira e oferece contexto personalizado.

### Como validar:

Testes de uso + feedback qualitativo.

### Exemplos:

- "como está minha saúde financeira?"
- "estou gastando muito?"
- "como estou financeiramente?"

### Sinais positivos:

- Usuário considera a análise útil;
- Usuário sente que o sistema "entende" sua situação;
- Usuário retorna para acompanhar evolução.

### Métrica inicial:

- percepção de utilidade da análise (1 a 5);
- intenção de reutilização do assistente.

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

## Cenário 05

Testar entradas ambíguas.

Exemplos:

- "comprei 50"
- "pix de 30"
- "salvei 100"

Objetivo:

Verificar se o assistente pede confirmação antes de registrar.

---

## Cenário 06

Perguntar sobre saúde financeira.

Exemplos:

- "como está minha saúde financeira?"
- "estou gastando muito?"
- "como estou financeiramente?"

Objetivo:

- Verificar se o assistente interpreta contexto financeiro e oferece análise útil.
- evita respostas repetitivas;
- adapta a análise conforme a pergunta;
- atualiza a análise após novos lançamentos.

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

- Refinar parser determinístico
- Melhorar interpretação contextual
- Refinar memória de recorrência
- Melhorar detecção de padrões financeiros
- Melhorar análise da saúde financeira
- Reduzir ambiguidade em lançamentos
- Tornar insights mais personalizados

## Produto

- Saúde financeira contextual via assistente
- Gastos recorrentes automáticos
- Memória financeira persistente
- Recomendações mais personalizadas
- Histórico inteligente de padrões financeiros

---

# 📅 Status atual

## Versão atual

MVP funcional em evolução contínua com:

* Lovable + Vibe Coding
* Iterações diárias orientadas por testes reais
* Parser financeiro determinístico
* Sistema de categorização por merchants e contexto
* Correções contextuais do assistente
* Metas desacopladas de despesas
* Dashboard financeiro integrado
* Score de saúde financeira
* Insights comportamentais

Nesta fase, o produto já demonstra:

* reconhecimento de merchants recorrentes (Netflix, Amazon Prime, farmácia, internet etc.);
* diferenciação entre receitas, despesas e metas;
* correções contextuais com memória do último lançamento;
* sugestões de recorrência com confirmação manual;
* análise contextual da saúde financeira;
* fallback por confiança para entradas ambíguas;

* respostas mais humanas e contextualizadas;
* comportamento orientado a hábitos financeiros.

## Próximo marco

Estabilização do núcleo conversacional e início dos primeiros testes externos controlados.

Foco imediato:

- refinamento do correction flow;
- consistência do Financial Health;
- memória contextual persistente;
- dashboard mensal;
- redução de edge cases conversacionais.

Após estabilização:

Primeiros testes controlados com familiares, amigos e colegas, seguidos de coleta estruturada de feedback.
