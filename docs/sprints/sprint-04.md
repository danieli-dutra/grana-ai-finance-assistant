# Sprint 04 — Estabilização da IA Financeira

## Objetivo da sprint

Após múltiplas sessões de testes reais com o Grana.ai, foram identificadas inconsistências na interpretação das intenções do usuário.

O objetivo desta sprint foi estabilizar a lógica central do agente antes de iniciar testes externos com usuários reais.

---

# Principais problemas encontrados

## 1. Serviços recorrentes sendo categorizados incorretamente

### Exemplo testado

paguei amazon prime 16,90

### Problema

O sistema não reconhecia corretamente serviços de assinatura e, em alguns cenários, tratava esse tipo de lançamento como compras genéricas.

### Correção aplicada

Foi implementado um mapeamento fixo para serviços recorrentes.

### Serviços adicionados

- Netflix
- Amazon Prime
- Prime Video
- Spotify
- Disney+
- HBO

### Resultado esperado

Categoria: Streaming

---

## 2. Metas financeiras sendo registradas como despesas

### Exemplo testado

salvei 50 para placa de vídeo

### Problema

O sistema interpretava esse comando como gasto, impactando:

- histórico de despesas;
- gráfico de categorias;
- saldo mensal.

### Correção aplicada

Foi criada prioridade máxima para intenções de:

- guardar;
- salvar;
- reservar;
- separar valores.

### Resultado esperado

O sistema deve:

- reduzir saldo disponível;
- atualizar a meta correspondente;
- não registrar como despesa.

---

## 3. Correções contextuais não reconhecidas

### Exemplo testado

isso era meta

### Problema

O agente não conseguia associar a correção ao último lançamento.

### Correção aplicada

Foi implementada memória contextual da última transação.

### Resultado esperado

O agente deve:

- localizar o último lançamento;
- corrigir tipo ou categoria;
- atualizar saldo, metas e dashboard.

---

## 4. Respostas repetitivas

### Problema

O assistente repetia os mesmos insights independentemente do contexto.

### Correção aplicada

Os insights passaram a considerar:

- tipo da transação;
- comportamento recente;
- metas ativas;
- padrão de gastos.

---

# Melhorias implementadas

## Parser financeiro determinístico

Nova ordem de interpretação:

1. Meta / Reserva  
2. Receita  
3. Despesa  
4. Correções  
5. Dicas financeiras  

---

## Sistema de confiança para categorização

### Com contexto suficiente

O agente categoriza automaticamente.

Exemplos:

- Internet → Moradia
- Farmácia → Saúde
- Netflix → Streaming
- Supermercado → Alimentação

### Com baixa confiança

O agente pergunta antes de registrar.

Exemplo:

Entrada:

comprei 50

Resposta esperada:

Posso registrar 🙂 Em qual categoria esse gasto entra?

---

## Insights financeiros mais contextuais

Exemplo:

Entrada:

recebi bônus de 300

Resposta esperada:

Ótimo. Esse bônus pode acelerar sua meta sem mexer na sua rotina.

---

# Cenários testados

Nesta sprint foram testados:

- contas fixas;
- serviços de assinatura;
- farmácia e saúde;
- entradas via pix;
- bônus e reembolsos;
- metas financeiras;
- correções contextuais;
- respostas comportamentais.

---

# Status atual

O Grana.ai começa a apresentar sinais consistentes de estabilidade e se aproxima de um MVP funcional para testes externos.

---

## Refinamentos Pós-Sprint

### Ajustes realizados após testes reais

Após ciclos de testes manuais no ambiente Lovable, foram identificadas inconsistências no comportamento do agente financeiro. A sprint passou a incluir refinamentos incrementais focados em interpretação contextual, categorização e UX conversacional.

#### Melhorias implementadas

- Parser financeiro refinado;
- Melhorias na categorização determinística;
- Metas financeiras desacopladas de despesas;
- Correções contextuais ("isso era meta");
- Streaming reconhecido como categoria própria;
- Pix, bônus e reembolso diferenciados como receitas;
- Saudação dinâmica por período do dia;
- Health Score financeiro integrado ao dashboard;
- Insights financeiros mais contextuais.

#### Casos corrigidos

**Streaming**

Entrada:

`paguei amazon prime 16,90`

Resultado esperado:

Categoria: `Streaming`

---

**Meta financeira**

Entrada:

`salvei 50 para placa de vídeo`

Resultado esperado:

- Atualizar meta;
- Não registrar como despesa;
- Não impactar gráfico de gastos.

---

**Correção contextual**

Entrada:

`isso era meta`

Resultado esperado:

O agente deve localizar o último lançamento relacionado e corrigir o tipo da transação.

---

**Receitas diferenciadas**

Exemplos:

`recebi pix 55`  
`recebi bônus de 300`  
`recebi reembolso de 45`

Resultado esperado:

Classificação correta por tipo de receita.

#### Problemas ainda em refinamento

- Interpretação contextual de saúde financeira;
- Mensagens dinâmicas do card Health Score;
- Casos ambíguos ainda dependem de refinamento do parser;
- Ampliação do mapeamento determinístico de categorias.

# Próxima sprint

Sprint 05:

- testes com familiares e amigos;
- coleta de feedback com Google Forms;
- validação com usuários reais.
