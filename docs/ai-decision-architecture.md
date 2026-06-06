# AI Decision Architecture & Technical Notes — Grana.ai

## Bugs técnicos identificados

---

## Bug 01 — "99" sendo interpretado como transporte

### Cenário

*paguei internet 99,90*

### Problema

O parser associava o número 99 ao aplicativo de mobilidade, ignorando o contexto do merchant.

### Resultado:

Internet → Transporte

### Impacto

Esse comportamento reduzia a confiança do usuário, pois alterava o dashboard financeiro incorretamente.

### Correção

Foi removida a associação automática do número 99.

#### Agora o parser prioriza:

merchant detectado;
categoria contextual;
fallback por confiança.

### Resultado esperado:

Internet → Moradia
99 Food → Alimentação
Uber → Transporte

---

## Bug 02 — Correções falsas

### Cenário

*internet não é transporte*

### Problema

O sistema respondia:

Atualizei de Transporte para Transporte.

### Correção

Foi criada validação obrigatória antes de confirmar alterações.

---

## Bug 03 — Savings sendo registradas como despesas

### Cenário

*salvei 50 para placa de vídeo*

### Problema

O lançamento impactava o gráfico de despesas.

### Correção

Foi criada prioridade máxima para intenções de meta e reserva.

---

## Bug 04 — Ambiguidade em lançamentos curtos

### Cenário

*comprei 50*

### Correção

Foi implementado sistema de confiança.

Agora o agente pergunta antes de registrar.

---

# 🧠 Evolução da arquitetura de decisão

O **Grana.ai** evoluiu de respostas puramente baseadas em prompt para uma arquitetura mais determinística, reduzindo inconsistências conversacionais e melhorando a previsibilidade do comportamento do assistente.

---

## 🔄 Pipeline atual
**intent → parse → confidence → execute → response**

### Fluxo da decisão
- **Intent detection** → identifica a intenção do usuário  
- **Parse** → extrai valores, merchants, categorias e contexto  
- **Confidence layer** → avalia nível de confiança da interpretação  
- **Execute** → registra, corrige ou atualiza dados  
- **Response** → gera resposta contextual ao usuário  

---

## 🧩 Componentes atuais

### Intent detection
O sistema identifica automaticamente a intenção do usuário.

**Tipos atualmente suportados:**
- despesa  
- receita  
- meta  
- correção  
- saúde financeira  
- recorrência  

**Exemplos:**
- *gastei 30 no almoço* → despesa  
- *recebi salário 2500* → receita  
- *salvei 50 para viagem* → meta  
- *isso era meta* → correção  
- *como está minha saúde financeira?* → financial_health  

---

### Confidence layer
Entradas ambíguas exigem confirmação antes do registro.

**Exemplo:**
- Entrada: *comprei 50*  
- Resposta: *Em qual categoria esse gasto entra?*

O sistema evita assumir categorias quando não há confiança suficiente.

**Objetivos:**
- reduzir erros de classificação  
- aumentar confiança do usuário  
- evitar distorções no dashboard financeiro  

---

### Context memory
O assistente mantém contexto do último lançamento para permitir correções naturais.

**Exemplo:**
- *isso era meta*  
- *era mercado*  
- *corrigir categoria*  

Isso reduz fricção conversacional e aproxima a experiência de uma conversa natural.

---

### Merchant normalization
Reconhecimento contextual de merchants para reduzir erros de categorização.

**Exemplos:**

| Merchant | Categoria     |
|----------|---------------|
| Netflix  | Streaming     |
| Farmácia | Saúde         |
| Mercado  | Alimentação   |
| Internet | Moradia       |
| 99 Food  | Alimentação   |
| Uber     | Transporte    |

O sistema prioriza:
1. merchant detectado  
2. contexto textual  
3. fallback por confiança  

---

### Recurring Memory (MVP)
O assistente identifica padrões recorrentes e sugere lembretes sem automação.

**Exemplo:**
- *Internet parece um gasto recorrente.*  
- *Deseja lembrar desse lançamento nos próximos meses?*

**Características do MVP:**
- detecta padrões recorrentes  
- sugere apenas após recorrência percebida  
- nunca registra automaticamente  
- sempre aguarda confirmação explícita do usuário  

**Objetivo:**
Reduzir esforço de lançamento sem perder controle financeiro.


