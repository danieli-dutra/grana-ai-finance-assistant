# Sprint 05 — Stabilization & Conversational State

## 🎯 Objetivo da sprint

Refinar a arquitetura de decisão do assistente financeiro para reduzir inconsistências conversacionais, melhorar confiança do usuário e preparar o produto para validação com usuários reais.

Após as evoluções da Sprint 04, o foco deixou de ser apenas implementar funcionalidades.

Nesta fase, o objetivo passou a ser:

**tornar o comportamento do agente mais previsível, contextual e confiável.**

---

## 🧠 Problema identificado

Durante testes internos, foram observadas falhas recorrentes no comportamento do assistente:

- categorização inconsistente;
- perda de contexto conversacional;
- respostas repetitivas;
- análise financeira pouco contextual;
- correções naturais não reconhecidas.

Exemplo observado:

```txt
comprei 50
```

Assistente:

```txt
Em qual categoria esse gasto entra?
```

Usuário:

```txt
alimentação
```

Resultado anterior:

O agente perdia contexto e interpretava a mensagem como uma nova conversa.

---

## ✅ Implementações realizadas

### 1. Arquitetura determinística do assistente

O agente passou a operar por um pipeline de decisão estruturado.

Nova ordem de processamento:

1. Detecção de intenção  
2. Parser determinístico  
3. Verificação de confiança  
4. Resolução de contexto  
5. Execução da ação  
6. Resposta conversacional

Objetivo:

Reduzir ambiguidade e comportamento imprevisível.

---

### 2. Sistema de categorização com confiança

Foi implementada lógica híbrida:

#### Alta confiança
O sistema categoriza automaticamente.

Exemplos:

| Entrada | Categoria |
|----------|------------|
| Internet | Moradia |
| Farmácia | Saúde |
| Netflix | Streaming |
| Amazon Prime | Streaming |
| Mercado | Alimentação |
| Uber | Transporte |
| 99 Food | Alimentação |

#### Baixa confiança
O agente pergunta antes de registrar.

Exemplo:

Entrada:

```txt
comprei 50
```

Resposta:

```txt
Em qual categoria esse gasto entra?
```

---

### 3. Clarification flow por texto

O sistema passou a aceitar respostas textuais após pedidos de confirmação.

Exemplo:

Entrada:

```txt
comprei 50
```

Assistente:

```txt
Em qual categoria esse gasto entra?
```

Usuário:

```txt
alimentação
```

Resultado esperado:

```txt
Registrei R$50 como despesa em Alimentação.
```

Antes desta melhoria, apenas botões funcionavam corretamente.

---

### 4. Sistema de Financial Health

Foi criado um novo intent dedicado:

```txt
financial_health
```

Agora o assistente consegue responder perguntas como:

- como está minha saúde financeira?
- estou gastando muito?
- como estão minhas finanças?
- como estou financeiramente?

A análise considera:

- renda x despesas;
- score financeiro;
- metas ativas;
- apostas recorrentes;
- concentração de gastos;
- padrão de consumo.

---

### 5. Health Card dinâmico

O card de saúde financeira passou a responder ao comportamento do usuário.

Exemplos de mensagens:

#### Saúde positiva

```txt
Despesas sob controle. Continue fortalecendo suas metas.
```

#### Moradia alta

```txt
Moradia representa uma grande parte dos gastos deste mês.
```

#### Gastos acima da renda

```txt
Você gastou mais do que recebeu neste período.
```

#### Apostas frequentes

```txt
Percebi recorrência em apostas. Vale acompanhar esse padrão.
```

---

## ⚠️ Problemas identificados nesta sprint

### 1. Correction flow ainda inconsistente

Correções contextuais ainda podem perder memória.

Exemplo:

```txt
era mercado
```

O agente ainda não associa corretamente ao último lançamento.

Necessário:

- persistência do estado de correção;
- memória contextual entre mensagens;
- interpretação natural de correções.

---

### 2. Dashboard temporal

Foi observado comportamento global nos cálculos financeiros.

Problema:

Após novo recebimento de salário, insights continuavam congelados.

Necessário:

- recalcular score mensal;
- atualizar dashboard por período;
- sincronizar Financial Health com novos lançamentos.

---

### 3. Repetição de respostas

Em alguns casos, o agente ainda responde com mensagens muito parecidas.

Exemplo:

```txt
como está minha saúde financeira?
```

```txt
estou gastando muito?
```

Retornam análises quase idênticas.

Necessário:

- respostas mais contextuais;
- nuance conforme intenção da pergunta;
- redução de repetição.

---

## 🧪 Testes realizados

Foram realizados testes internos envolvendo:

- metas financeiras;
- streaming;
- farmácia;
- internet;
- Uber;
- 99 Food;
- salário;
- reembolso;
- apostas;
- categorização ambígua;
- correções de categoria;
- perguntas sobre saúde financeira.

---

## 📌 Aprendizados da sprint

Esta sprint mostrou que construir um agente financeiro funcional vai além de interpretar linguagem natural.

Foi necessário trabalhar:

- arquitetura de decisão;
- regras de confiança;
- memória contextual;
- UX conversacional;
- consistência do comportamento.

O principal aprendizado foi:

> um bom agente não é apenas inteligente — ele precisa ser previsível e confiável.

---

## 🚀 Próxima sprint

### Sprint 06 — Conversational Reliability & User Validation

Foco:

- correção state machine;
- memória contextual persistente;
- dashboard mensal;
- refinamento do Financial Health;
- redução de respostas repetitivas;
- início dos testes com familiares e amigos;
- coleta estruturada de feedback.
