# Projeto integrador: Agenda Cidadã

**Unidade Curricular:** Modelos, métodos e técnicas da engenharia de software
(`0021638`) — UNIFG 2026/2
**Professor:** Petros Barreto
**Peso:** 65% da média final (50% nos marcos, 15% na apresentação)
**Formato:** equipes de 3 a 5 pessoas, formadas na aula 03

---

## O produto

O **Agenda Cidadã** é um sistema de agendamento de serviços públicos municipais.
Em vez de enfrentar fila para tirar a segunda via de um documento, marcar
atendimento no CRAS, agendar vacinação ou pedir a poda de uma árvore, o morador
agenda dia e hora.

A meta máxima do plano de ensino é aplicar as técnicas da engenharia de software a
um produto, do levantamento de requisitos até a entrega, usando desenvolvimento
ágil. O Agenda Cidadã é esse produto, e ele atravessa os oito blocos da UC.

```
BLOCO                          O QUE O PROJETO PRODUZ            MARCO
─────────────────────────────  ────────────────────────────────  ─────
1  Fundamentos                 caracterização do problema         M1
2  Modelos de processo         escolha do processo, justificada   M2
3  Desenvolvimento ágil        backlog e primeira iteração        M3
4  Engenharia de requisitos    documento completo + viabilidade   M4
5  Prototipação e interface    protótipo testado com usuários     M5
6  Arquitetura                 documento com táticas              M6
7  Padrões de projeto          fatia implementada                 M7
8  DevOps e entrega contínua   pipeline funcionando               M8
```

---

## Por que este domínio

A escolha do domínio foi determinada pelo bloco 5, que ocupa cinco aulas e trata
de prototipação, usabilidade e aceitação pelo usuário. Esse bloco só produz
aprendizado real se o sistema tiver usuários **diversos e não técnicos**.

```
PERFIS DE USUARIO

┌────────────────────────────────────┬──────────────────────────────────┐
│ Dona Zilda, 68 anos                │ celular simples, letra pequena   │
│ moradora, agenda 2 vezes por ano   │ e passo extra sao barreira        │
├────────────────────────────────────┼──────────────────────────────────┤
│ Lucas, 22 anos                     │ compara com apps comerciais;     │
│ morador, agenda pelo celular       │ abandona se demorar               │
├────────────────────────────────────┼──────────────────────────────────┤
│ Marcia, servidora do balcao        │ usa 8 h/dia; quer teclado,       │
│ atende quem nao tem celular        │ atalho e nenhum clique extra      │
├────────────────────────────────────┼──────────────────────────────────┤
│ Secretario de administracao        │ olha o painel 1x por semana;     │
│                                    │ quer numero agregado              │
├────────────────────────────────────┼──────────────────────────────────┤
│ Seu Antonio, 74 anos               │ nao tem celular; e atendido por  │
│ agenda por telefone                │ Marcia, que opera o sistema       │
└────────────────────────────────────┴──────────────────────────────────┘
```

O mesmo agendamento precisa servir aos cinco. A interface que agrada Lucas
provavelmente exclui Dona Zilda. A que serve Dona Zilda pode ser lenta demais
para Márcia, que repete a operação sessenta vezes por dia. Não existe solução
ótima para todos, e priorizar exige evidência — que vem de teste de usabilidade,
não de opinião da equipe.

### O domínio também sustenta os outros blocos

| Bloco | O que o domínio oferece |
|---|---|
| 2 e 3 | serviço público tem prazo legal e restrição de contratação, o que torna a escolha do processo uma decisão real |
| 4 | há legislação a consultar, servidores a entrevistar e um processo em papel a observar em campo |
| 6 | picos previsíveis de demanda (início de ano letivo, campanha de vacinação) criam requisito de desempenho |
| 7 | tipos de serviço com regras diferentes pedem estrutura que evite condicional em cascata |
| 8 | é um sistema público: indisponibilidade tem consequência, e implantação precisa de rollback |

E há dado pessoal em volume, o que traz a LGPD para dentro do projeto em vez de
deixá-la como assunto teórico.

---

## Os oito marcos

Cada marco é entregue como pull request com o título
`[Agenda Cidadã MN] Nome da Equipe`.

### M1 — Caracterização do problema · aula 04 · 8%

| Artefato | Conteúdo |
|---|---|
| Descrição do problema | a situação atual, com dados; o que dói, para quem |
| Perfis de usuário | de 4 a 6 perfis, com contexto de uso, não apenas idade e profissão |
| Hipóteses | de 5 a 8 afirmações que a equipe assume e ainda não verificou |
| Escopo inicial | quais serviços entram na primeira versão, e por quê |

O artefato central é a lista de **hipóteses**. Toda equipe começa um projeto com
suposições, e a diferença entre projeto conduzido e projeto improvisado é
escrevê-las. Exemplo de hipótese verificável: "moradores acima de 60 anos
preferem agendar por telefone a agendar pelo celular". Ela pode ser testada; e o
M5 vai testar.

### M2 — Modelo de processo · aula 10 · 8%

A equipe escolhe o modelo de processo e compara **três** alternativas, sendo pelo
menos uma dirigida a plano e uma ágil.

| Artefato | Conteúdo |
|---|---|
| Comparação | três modelos, avaliados nos mesmos critérios |
| Escolha justificada | por que o escolhido, no contexto **deste** projeto |
| Riscos da escolha | o que o modelo escolhido trata mal, e como compensar |

A terceira seção é a que separa análise de propaganda. Todo modelo tem ponto
cego: cascata trata mal mudança de requisito; Scrum trata mal prazo fixo com
escopo fixo; prototipação evolutiva tende a acumular dívida técnica. Escolher sem
declarar o ponto cego indica que ele não foi percebido.

### M3 — Planejamento e primeira iteração · aula 16 · 12%

| Artefato | Conteúdo |
|---|---|
| Backlog | itens priorizados, com critério de priorização declarado |
| Primeira iteração | **executada**, não planejada: com resultado e retrospectiva |
| Métricas de fluxo | quais serão acompanhadas, e a medição da primeira iteração |
| Quadro de trabalho | GitHub Projects configurado e em uso |

A iteração precisa ter acontecido. Um plano de iteração sem execução não
demonstra nada sobre desenvolvimento ágil.

### M4 — Engenharia de requisitos · aula 24 · 20%

O marco de maior peso, junto com o M5.

| Artefato | Conteúdo |
|---|---|
| Registro de elicitação | **três técnicas diferentes**, aplicadas a pessoas reais |
| Requisitos funcionais | mínimo de 25, identificados, com fonte e prioridade |
| Requisitos não funcionais | mínimo de 8, todos mensuráveis |
| Especificação | histórias ou casos de uso para os 12 itens de maior prioridade |
| Validação | como foram validados, com quem, e o que mudou depois |
| Registro de negociação | onde houve conflito e como foi resolvido |
| Estudo de viabilidade | técnica, econômica, operacional e legal |
| Gestão de requisitos | rastreabilidade e o registro de mudanças até aqui |

Duas exigências merecem destaque.

**Elicitação com pessoas reais.** Entrevistar um colega de turma fingindo ser
servidor público não é elicitação; é ensaio. A equipe precisa conversar com
alguém de fora — servidor de uma prefeitura, atendente de um posto, ou, no
mínimo, pessoas com o perfil dos usuários finais. O registro traz data, duração,
quem foi e o roteiro usado.

**Estudo de viabilidade legal.** O sistema trata dado pessoal. A dimensão legal
não é preenchimento burocrático: exige identificar qual base legal da LGPD
sustenta o tratamento, quais dados são realmente necessários e por quanto tempo
serão retidos.

### M5 — Protótipo e usabilidade · aula 29 · 18%

| Artefato | Conteúdo |
|---|---|
| Protótipo de baixa fidelidade | as primeiras versões, em papel, fotografadas |
| Protótipo navegável | Figma ou Penpot, cobrindo os fluxos principais |
| Roteiro de teste | tarefas a executar, sem instruções de como executá-las |
| Teste com usuários | mínimo de **5 pessoas reais**, de pelo menos dois perfis diferentes |
| Relatório de usabilidade | achados classificados por severidade, com evidência |
| Segunda versão | o protótipo corrigido a partir dos achados, com o antes e o depois |

O teste com cinco pessoas não é número arbitrário: é a recomendação de Nielsen,
discutida na aula 29, e a equipe precisa saber explicar por que cinco.

A **segunda versão** é o que dá sentido ao marco. Testar e não corrigir
transforma o teste em relatório. O antes e o depois é a evidência de que o
protótipo serviu ao propósito de aprender antes de construir.

### M6 — Arquitetura · aula 34 · 14%

| Artefato | Conteúdo |
|---|---|
| Atributos de qualidade priorizados | derivados dos RNFs do M4, com cenários de qualidade |
| Estilo arquitetural escolhido | com comparação de alternativas |
| Táticas | qual tática atende qual atributo, e a que custo |
| Diagramas | contexto, contêineres e componentes |
| Registros de decisão (ADR) | mínimo de 5, com consequências negativas declaradas |

O elemento novo em relação a outras disciplinas é o **cenário de qualidade**: uma
forma estruturada de tornar um RNF verificável do ponto de vista arquitetural.

```
CENARIO DE QUALIDADE — formato

  fonte do estimulo    morador
  estimulo             solicita agendamento
  ambiente             pico de campanha de vacinacao, 400 req/min
  artefato             servico de agendamento
  resposta             confirma ou recusa por indisponibilidade
  medida da resposta   95% em menos de 2 s; nenhuma dupla marcacao
```

### M7 — Padrões de projeto · aula 37 · 12%

| Artefato | Conteúdo |
|---|---|
| Fatia implementada | um fluxo completo, das camadas de entrada à persistência |
| Padrões aplicados | mínimo de 3, com a justificativa de cada um |
| Antes e depois | o trecho antes do padrão e depois, com o problema que ele resolveu |
| Testes | cobrindo as regras de negócio da fatia |

O critério não é usar muitos padrões. É usar padrão onde havia um problema. Um
`Factory` introduzido onde uma função simples resolvia é dívida, não projeto — e a
seção "antes e depois" torna isso visível.

O domínio favorece três padrões de forma natural: tipos de serviço com regras
diferentes pedem *Strategy*; a criação desses tipos pede *Factory*; e notificar o
morador por canais distintos pede *Observer*. A equipe não é obrigada a usar
esses, mas precisa justificar os que usar.

### M8 — Entrega contínua e apresentação · aula 40 · 8% + 15%

| Artefato | Conteúdo |
|---|---|
| Pipeline de CI/CD | em funcionamento, com estágios e quality gates |
| Estratégia de implantação | como publicar e como reverter |
| Métricas DORA | as quatro medidas, calculadas para o próprio projeto |
| Apresentação | 20 minutos |

As quatro métricas DORA — frequência de implantação, tempo de espera para
mudança, taxa de falha em mudança e tempo de restauração — são discutidas na
aula 38. Calcular para o próprio projeto, mesmo com números pequenos, é o que
transforma a leitura em compreensão.

Estrutura sugerida da apresentação: 3 minutos sobre o problema e os usuários; 4
sobre o que a elicitação revelou e contrariou as hipóteses do M1; 4 sobre os
achados do teste de usabilidade e o que mudou no protótipo; 4 sobre arquitetura e
padrões, com uma decisão difícil detalhada; 3 de demonstração do pipeline; 2 de
perguntas.

---

## Níveis de escopo

A equipe escolhe no M2 e declara no `README.md`.

| Nível | Escopo | Nota máxima |
|---|---|---|
| **1 — Essencial** | os oito marcos com o conteúdo mínimo; um tipo de serviço implementado | 8,5 |
| **2 — Completo** | + dois tipos de serviço com regras distintas; teste de usabilidade em duas rodadas; pipeline com implantação automatizada | 10,0 |
| **3 — Avançado** | + acessibilidade verificada (contraste, leitor de tela, navegação por teclado); teste de carga no cenário de pico; infraestrutura como código | 10,0 + bônus |

Bônus, até 1,5 ponto:

- Teste de usabilidade com pessoa acima de 60 anos, registrado em vídeo com consentimento
- Entrevista com servidor público de uma prefeitura real
- Análise comparativa do mesmo fluxo em dois estilos arquiteturais, com medição
- Protótipo testado também em celular de tela pequena e conexão lenta

---

## Critérios de avaliação

| Critério | Pontos |
|---|---|
| Corretude técnica | 35 |
| Justificativa das decisões técnicas | 30 |
| Qualidade dos artefatos | 25 |
| Clareza da comunicação | 10 |

### O que reduz a nota de forma significativa

Elicitação simulada entre colegas apresentada como elicitação de campo. Teste de
usabilidade com menos de cinco pessoas, ou com pessoas da própria equipe.
Requisito não funcional sem número. Padrão de projeto aplicado sem problema que o
justifique. ADR sem consequência negativa. Iteração planejada e não executada.
Pipeline que existe no repositório e nunca rodou.

### Sobre uso de assistentes de IA

Permitido, com declaração no `README.md` indicando em quais artefatos e de que
forma. O critério é o de qualquer fonte: a equipe precisa entender e defender cada
decisão. Há um limite natural — nenhum assistente entrevista o servidor da
prefeitura nem observa Dona Zilda usando o protótipo, e esses são exatamente os
artefatos de maior peso.

---

## Estrutura do repositório

```
agenda-cidada/
├── README.md                  visão geral, nível, declaração de uso de IA
├── docs/
│   ├── 01-problema.md · 02-perfis.md · 03-hipoteses.md
│   ├── 04-processo.md
│   ├── 05-requisitos.md · 06-viabilidade.md · 07-rastreabilidade.md
│   ├── 08-elicitacao/            registros por sessão
│   ├── 09-usabilidade.md
│   ├── 10-arquitetura.md
│   ├── adr/
│   └── diagramas/               .puml
├── prototipo/
│   ├── baixa-fidelidade/        fotos do papel
│   └── link-figma.md
├── src/  ·  tests/
├── .github/workflows/
└── metricas/
```

---

Dúvidas sobre o projeto podem ser registradas como *issue* no repositório de
exercícios.
