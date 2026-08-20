# Exercícios — Modelos, Métodos e Técnicas da Engenharia de Software

**UNIFG 2026/2** · UC `0021638` · Prof. Petros Barreto
**160 horas** · 40 aulas de 4h · sextas-feiras

Repositório público da unidade curricular. Contém as listas semanais e a
especificação do projeto integrador **Agenda Cidadã**.

Os slides ficam em repositório separado, cujo endereço é distribuído em sala e no
ambiente virtual.

---

## Preparação do ambiente

```bash
# 1. Faça fork deste repositório

# 2. Clone o seu fork
git clone https://github.com/SEU-USUARIO/modelos-metodos-es-2026-exercicios.git
cd modelos-metodos-es-2026-exercicios

# 3. Aponte para o original, para receber as listas novas
git remote add upstream https://github.com/petrosbarreto/modelos-metodos-es-2026-exercicios.git
```

Ferramentas necessárias ao longo do semestre, instaladas conforme o bloco:

| Bloco | Ferramenta | Quando |
|---|---|---|
| 4, 6 | PlantUML | aula 21 em diante |
| 5 | Figma ou Penpot (conta gratuita) | aula 25 |
| 5 | papel e caneta | aulas 25 e 27 |
| 7 | Python 3.13 ou Node 22 | aula 35 |
| 8 | Docker e Docker Compose | aula 38 |

Para PlantUML, a opção mais simples é a extensão do VS Code. Alternativas:
`brew install plantuml`, `sudo apt install plantuml`, ou o servidor público em
<http://www.plantuml.com/plantuml/uml/>, sem instalar nada.

---

## Entrega de uma lista

```bash
git switch main && git pull upstream main
git switch -c aula07
# resolva em exercicios/aula07/
git add exercicios/aula07
git commit -m "Aula 07: comparação entre incremental e iterativo"
git push -u origin aula07
```

Abrir pull request com o título `[Aula NN] Seu Nome Completo`. Para o projeto,
`[Agenda Cidadã MN] Nome da Equipe`.

Pull request com título fora do padrão não é corrigido.

### Verificação automática

| Verificação | Comportamento |
|---|---|
| Presença de `RESPOSTAS.md` | falha se ausente |
| Sintaxe dos `.puml` alterados | falha se algum diagrama não compila |
| Título do pull request | aviso |
| Testes, quando houver código | falha se algum quebrar |

A verificação dos diagramas existe por razão prática: um `.puml` que não compila
indica diagrama que nunca foi visualizado, e diagrama nunca visualizado costuma
estar errado.

---

## Formato de cada entrega

```
exercicios/aulaNN/
├── RESPOSTAS.md          respostas, análises e justificativas
├── diagramas/            .puml, quando a lista pedir
├── prototipo/            capturas ou link, no bloco 5
├── src/                  código, nos blocos 7 e 8
└── evidencias/           saídas de comando, fotos, registros
```

Três regras valem para todas as listas.

As seções do `RESPOSTAS.md` seguem a numeração do enunciado. Diagramas vão em
PlantUML, como texto — a imagem pode acompanhar, mas o `.puml` é obrigatório, pois
texto entra no controle de versão e aparece no *diff*. E **toda decisão técnica vem
acompanhada da justificativa**: escolher um padrão de projeto, um estilo
arquitetural ou um tipo de protótipo sem explicar por que não se escolheu outro
deixa o artefato incompleto.

---

## Critérios de correção

| Critério | Pontos | O que se avalia |
|---|---|---|
| Corretude técnica | 35 | as respostas e artefatos estão certos |
| Justificativa das decisões técnicas | 30 | as escolhas se sustentam a uma pergunta |
| Qualidade dos artefatos | 25 | completos, legíveis, coerentes entre si |
| Clareza da comunicação | 10 | organização e redação |

A justificativa pesa 30 pontos porque as decisões desta UC — qual modelo de
processo, qual estilo arquitetural, qual padrão, qual fidelidade de protótipo —
quase nunca têm resposta única. Resposta diferente da esperada, bem fundamentada,
vale mais que a esperada sem fundamento.

### Prazos

Entrega até a véspera da aula seguinte, 23h59. Atraso de até sete dias desconta 20
pontos; acima disso a lista não é corrigida e conta como uma das duas descartadas.

A nota de exercícios é a média das 40 listas, descartando as duas piores.

---

## Composição da nota final

| Instrumento | Peso |
|---|---|
| Marcos do projeto Agenda Cidadã (M1 a M8) | 50% |
| Listas de exercícios (40) | 25% |
| Participação em atividades entre equipes e revisões | 10% |
| Apresentação final | 15% |

---

## Projeto integrador: Agenda Cidadã

Equipes de 3 a 5 pessoas desenvolvem um sistema de agendamento de serviços
públicos municipais, do levantamento de requisitos à entrega contínua, aplicando
desenvolvimento ágil.

| Marco | Aula | Entrega | Peso |
|---|---|---|---|
| M1 | 04 | Caracterização do problema, perfis de usuário e hipóteses | 8% |
| M2 | 10 | Modelo de processo escolhido, com comparação de três alternativas | 8% |
| M3 | 16 | Backlog, primeira iteração **executada** e métricas de fluxo | 12% |
| M4 | 24 | Engenharia de requisitos completa, com elicitação de campo e viabilidade | 20% |
| M5 | 29 | Protótipo navegável testado com 5 usuários reais, e a segunda versão | 18% |
| M6 | 34 | Arquitetura, com táticas justificadas por atributo de qualidade | 14% |
| M7 | 37 | Fatia implementada, com padrões de projeto justificados | 12% |
| M8 | 40 | Pipeline de CI/CD funcionando e apresentação | 8% |

O M4 e o M5 somam 38% do projeto. É deliberado: elicitar requisitos de pessoas
reais e testar interface com usuários reais são as duas atividades desta UC que
não se aprendem lendo.

Duas exigências que reprovam entregas com frequência: **elicitação simulada entre
colegas** apresentada como elicitação de campo, e **teste de usabilidade** com
menos de cinco pessoas ou com integrantes da própria equipe.

Especificação completa em [`projeto/README.md`](projeto/README.md).

---

## Índice das listas

| Bloco | Aulas | Tema |
|---|---|---|
| **1** | [01](exercicios/aula01) · 02 · 03 · 04 | Fundamentos da engenharia de software |
| **2** | 05 · 06 · 07 · 08 · 09 · 10 | Modelos de processo |
| **3** | 11 · 12 · 13 · 14 · 15 · 16 | Desenvolvimento ágil |
| **4** | 17 · 18 · 19 · 20 · 21 · 22 · 23 · 24 | Engenharia de requisitos |
| **5** | 25 · 26 · 27 · 28 · 29 | Prototipação e interface |
| **6** | 30 · 31 · 32 · 33 · 34 | Arquitetura de software |
| **7** | 35 · 36 · 37 | Padrões de projeto |
| **8** | 38 · 39 · 40 | DevOps e entrega contínua |

As listas são publicadas na semana da aula correspondente.

---

## Bibliografia

**Básica**
- SOMMERVILLE, I. *Engenharia de Software*. 10ª ed. Pearson.
- PRESSMAN, R.; MAXIM, B. *Engenharia de Software: uma abordagem profissional*. 9ª ed.
- BASS, L.; CLEMENTS, P.; KAZMAN, R. *Software Architecture in Practice*. 4ª ed.

**Complementar**
- GAMMA, E. et al. *Padrões de Projeto*. Bookman.
- NIELSEN, J. As dez heurísticas de usabilidade — <https://www.nngroup.com/articles/ten-usability-heuristics/>
- BECK, K. *Programação Extrema Explicada*. Bookman.
- ANDERSON, D. *Kanban*. Blue Hole Press.
- FORSGREN, N.; HUMBLE, J.; KIM, G. *Accelerate*. IT Revolution.
- HUMBLE, J.; FARLEY, D. *Entrega Contínua*. Bookman.
- BROOKS, F. *O Mítico Homem-Mês* e *No Silver Bullet* (1986).
- SWEBOK v4, IEEE — gratuito em <https://www.computer.org/education/bodies-of-knowledge/software-engineering>
- *Guia do Scrum* — <https://scrumguides.org>

---

## Colaboração e integridade

É permitido discutir ideias com colegas, consultar livros e internet, e usar
assistentes de IA. O uso de IA deve ser declarado no `RESPOSTAS.md` ou no
`README.md` do projeto, indicando em quais partes e de que forma.

O critério é o de qualquer fonte: é preciso entender e defender cada decisão. Há
um limite natural nesta UC — nenhum assistente entrevista o servidor da
prefeitura nem observa uma pessoa de 68 anos usando o protótipo, e esses são
exatamente os artefatos de maior peso.

Não é permitido apresentar elicitação simulada como elicitação de campo, nem
teste de usabilidade fictício.

---

Dúvidas podem ser registradas como [issue](../../issues) neste repositório.
