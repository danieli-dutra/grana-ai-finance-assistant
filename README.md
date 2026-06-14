# 💰 Grana.ai — Assistente Financeiro com IA

![Status](https://img.shields.io/badge/status-active%20development-7C5CFF)
![Projeto](https://img.shields.io/badge/DIO-Lab%20Vibe%20Coding-blue)
![Feito com](https://img.shields.io/badge/feito%20com-Lovable-purple)

🇧🇷 Português | 🇺🇸 English (coming soon)

![Grana.ai Preview](./assets/preview.png)

🔗 **Acesse o projeto:** https://grana-ai-assistente.lovable.app

---

## 🧭 Por que esse projeto existe?

Eu sempre tive a sensação de que organizar a vida financeira não deveria ser tão complicado.

Mesmo com tantos apps disponíveis, a maioria exige esforço demais, organização manual e, no fim, não ajuda a entender o que realmente está acontecendo com o dinheiro.

O Grana.ai nasce dessa inquietação: tornar o controle financeiro algo simples, natural e presente no dia a dia.

---

## 💡 O que é o Grana.ai?

O Grana.ai é um aplicativo de finanças pessoais que combina duas formas de interação:

- 💬 uma conversa simples, quase como falar com alguém  
- 📊 uma visão clara da sua “carteira”  

A ideia é permitir que você registre, entenda e tome decisões financeiras sem precisar lidar com planilhas ou sistemas complexos.

---

## ⚙️ Como funciona na prática

Você pode usar o app de forma natural, como faria em uma conversa:

- "Gastei 30 no almoço"  
- "Assinei Netflix por 39,90"  
- "Guardei 100 para viagem"  

A partir disso, o sistema organiza tudo automaticamente.

Ele entende o tipo de transação, classifica a categoria e atualiza o que for necessário, incluindo metas.

---

## 🧠 Como o agente toma decisões

O comportamento do assistente combina:

### 1. Parser financeiro determinístico
Interpreta mensagens em linguagem natural.

Exemplos:

- "gastei 30 no almoço"
- "recebi bônus de 200"
- "guardei 50 para viagem"

O sistema extrai automaticamente:

- tipo da transação (receita, despesa ou meta);
- valor monetário;
- categoria financeira;
- intenção do usuário;
- contexto da conversa.

### 2. Regras de categorização
Algumas categorias utilizam mapeamento contextual para reduzir erros.

Exemplos:

| Entrada | Categoria |
|---------|------------|
| Netflix | Streaming |
| Amazon Prime | Streaming |
| Farmácia | Saúde |
| Mercado | Alimentação |
| Internet | Moradia |

Quando não há confiança suficiente, o sistema pergunta antes de registrar.

Exemplo:

Entrada:

```txt
comprei 50
```

Resposta:

```txt
Em qual categoria esse gasto entra?
```

### 3. Contexto conversacional
O agente mantém contexto do último lançamento para permitir correções naturais.

Exemplo:

```txt
isso era meta
```

O sistema entende o contexto e corrige automaticamente.

### 4. Memória contextual e recorrência

O assistente mantém memória do contexto recente para permitir:

- correções naturais;
- continuidade da conversa;
- identificação de padrões recorrentes.

Exemplos:

```txt
isso era meta
era mercado
```

---

## 🎯 O que esse projeto resolve

Mais do que registrar gastos, o Grana.ai busca resolver problemas reais:

- dificuldade em manter consistência no controle financeiro  
- falta de clareza sobre para onde o dinheiro está indo  
- subestimação de pequenos gastos recorrentes  
- ausência de orientação prática no momento certo  

A proposta aqui é reduzir fricção e aumentar consciência.

---

## ✨ Principais funcionalidades

- 🧾 registro de gastos usando linguagem natural  
- 🏷️ categorização automática com contexto e merchants
- 🤔 confirmação inteligente para entradas ambíguas
- 🔄 correções contextuais por conversa ("isso era mercado", "era meta")
- 🎯 metas financeiras com acompanhamento de progresso  
- 💰 contribuição para metas direto pelo chat
- 🔁 memória de gastos e receitas recorrentes (MVP sem automação) 
- 📈 sugestão contextual de poupança baseada no comportamento do mês
- 📊 dashboard financeiro integrado
- ❤️ score de saúde financeira contextual 
- 🧠 insights fianceiros baseados em comportamento
- 🔔 notificações leves para confirmação de ações
- 🧩 arquitetura determinística para tomada de decisão do agente


---

## 🎯 Próximos passos do produto

### Fase atual

- ✅ Desenvolvimento com Vibe Coding + Lovable  
- ✅ Testes internos diários  
- ✅ Correções contínuas de UX e IA  
- ✅ Evolução da arquitetura conversacional  
- ✅ Transição gradual para desenvolvimento local (VS Code + GitHub)  

### Próxima fase

- 🔜 Estabilização do core financeiro (Financial Health + memória contextual)  
- 🔜 Refinamento da arquitetura de decisão do agente  
- 🔜 Testes com familiares e amigos  
- 🔜 Coleta de feedback com Google Forms  
- 🔜 Identificação de padrões reais de uso  
- 🔜 Iterações orientadas por comportamento do usuário  


---

## 🧪 Validação com usuários

O Grana.ai está evoluindo com base em testes reais e iterações contínuas.

📄 Veja o plano de validação:
[Validation Roadmap](./docs/validation-roadmap.md)

---

## 🧩 Estrutura da experiência

A experiência foi reorganizada como uma carteira financeira unificada.

### 🏠 Carteira principal
- receitas, despesas e saldo
- conversa com o assistente
- metas financeiras
- dashboard por categoria
- saúde financeira

Tudo acontece em uma única interface, reduzindo fricção e tornando o uso mais natural.

---

## 🎨 Design

- 🌙 tema escuro  
- 🟣 cores em roxo e azul  
- 🧼 interface limpa  
- 🎯 foco na clareza  

A intenção nunca foi impressionar pelo excesso, mas pela simplicidade.

---

## 🔄 Evolução Visual do Produto

### Protótipo
![Prototype](./assets/testing/prototipo-grana-ai.png)

### Layout Evolution
![Layout Evolution](./assets/screenshots/before-after-layout.png)

---

## 🚀 Evolução do Produto

### Fase 1 — Protótipo
Foco em registrar gastos via conversa.

Problemas encontrados:
- dependência excessiva do chat;
- pouca clareza visual;
- respostas repetitivas.

### Fase 2 — Carteira Financeira
Centralização da experiência em uma única tela.

Melhorias:
- dashboard integrado;
- metas visíveis;
- saldo e despesas em destaque.

### Fase 3 — Inteligência Contextual
Refinamento do comportamento do agente.

Melhorias:
- categorização determinística;
- metas financeiras;
- correções contextuais;
- insights financeiros.

---

## 🛠️ Tecnologias e stack

### Produto & Desenvolvimento
- Lovable (Vibe Coding)
- React + Frontend gerado
- TypeScript
- Supabase (persistência e autenticação)
- GitHub

### IA & Lógica Conversacional
- Engenharia de prompts
- Pipeline determinístico de decisão
- Parser financeiro contextual
- Merchant normalization
- Context memory
- Recurring memory (MVP)
- Financial Health Score
- Interpretação de linguagem natural

### Produto & UX
- UX/UI Design
- Product Thinking
- Testes iterativos
  
---

## 🧩 Evolução do desenvolvimento

O Grana.ai começou como um experimento de Vibe Coding utilizando Lovable para acelerar prototipação, validação de ideias e testes rápidos de UX conversacional.

À medida que a lógica financeira e a arquitetura do agente se tornaram mais sofisticadas, o projeto passou a evoluir para um fluxo híbrido de desenvolvimento.

Hoje, o produto combina:

* prototipação rápida com IA;
* refinamento de comportamento via engenharia de prompts;
* edição direta do código localmente com VS Code;
* versionamento contínuo com GitHub;
* evolução gradual da arquitetura para maior controle técnico e escalabilidade.

A proposta não é abandonar o Vibe Coding, mas evoluir do protótipo acelerado para um produto progressivamente mais robusto e sustentável.

---

## 🔄 Reflexão sobre o processo

### ✅ O que funcionou bem

A combinação entre conversa e visualização trouxe equilíbrio.

O app deixou de ser apenas um registrador de gastos e passou a ajudar na leitura da própria vida financeira.

A criação da “carteira” como tela principal melhorou muito a experiência.

Separar confirmações (notificações) e insights (chat) deixou tudo mais fluido.

---

### ⚠️ O que não saiu como esperado no início

A primeira versão ficou muito dependente do chat.

As respostas eram repetitivas, a categorização inconsistente e faltava integração entre funcionalidades como metas e contribuições.

Isso mostrou que só descrever funcionalidades não era suficiente.

Foi necessário definir regras claras de comportamento.

---

### 🧠 O que aprendi nesse processo

A qualidade do resultado depende diretamente da clareza das decisões e regras do produto.

Ao longo do desenvolvimento, percebi que construir com IA não reduz a necessidade de pensamento técnico, apenas muda a forma de trabalhar.

Aprendi que:

- regras específicas melhoram significativamente a qualidade do comportamento do agente;
- pequenos detalhes de UX impactam diretamente a confiança e retenção;
- linguagem natural exige arquitetura de decisão, não apenas prompts; 
- iterar continuamente é parte essencial do desenvolvimento;
- prototipação rápida acelera o aprendizado, mas escalabilidade exige maior controle técnico. 

O projeto deixou de ser apenas um experimento de interface e passou a se tornar um laboratório prático de produto, IA conversacional e engenharia de comportamento.

---

## 📄 PRD — Product Requirements Document

### 🧭 Contexto
O Grana.ai combina conversa e visualização para simplificar o controle financeiro.

---

### 🎯 Problema
- dificuldade em manter controle financeiro  
- falta de clareza sobre gastos  
- insights pouco úteis  

---

### 👥 Público-alvo
- iniciantes em finanças  
- usuários que buscam simplicidade  
- pessoas sem conhecimento técnico  

---

### 💡 Proposta de valor
- registrar gastos facilmente  
- organizar automaticamente  
- gerar insights relevantes  
- integrar metas ao dia a dia  

---

### 🧩 Estrutura
- onboarding  
- carteira (home)  
- chat  
- metas  

---

### 🏷️ Categorias
- Alimentação  
- Transporte  
- Moradia  
- Lazer  
- Saúde  
- Educação  
- Assinaturas  
- Streaming  
- Compras Online  
- Outros  

---

### 💰 Regra de poupança

- margem: 10%  
- sugestão: 30% da sobra  

---

## 👩‍💻 Sobre mim

Projeto desenvolvido por Danieli Dutra como laboratório prático de UX, produto, IA conversacional e desenvolvimento full stack, explorando como experiências financeiras podem se tornar mais simples, contextuais e humanas.

## 📄 License

This project is licensed under the MIT License.

Grana.ai is an experimental product built for learning, portfolio development, and iterative validation of conversational AI applied to personal finance.
