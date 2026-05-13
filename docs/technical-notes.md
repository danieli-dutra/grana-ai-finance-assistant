# Technical Notes — Grana.ai

## Bugs técnicos identificados

---

## Bug 01 — "99" sendo interpretado como transporte

### Cenário

paguei internet 99,90

### Problema

O parser associava o número "99" ao aplicativo de mobilidade.

### Correção

Foi removida a associação automática do número "99".

Agora o parser prioriza merchants e contexto.

---

## Bug 02 — Correções falsas

### Cenário

internet não é transporte

### Problema

O sistema respondia:

Atualizei de Transporte para Transporte.

### Correção

Foi criada validação obrigatória antes de confirmar alterações.

---

## Bug 03 — Savings sendo registradas como despesas

### Cenário

salvei 50 para placa de vídeo

### Problema

O lançamento impactava o gráfico de despesas.

### Correção

Foi criada prioridade máxima para intenções de meta e reserva.

---

## Bug 04 — Ambiguidade em lançamentos curtos

### Cenário

comprei 50

### Correção

Foi implementado sistema de confiança.

Agora o agente pergunta antes de registrar.