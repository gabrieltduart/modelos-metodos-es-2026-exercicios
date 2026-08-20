# Lista 01 — Fundamentos: o que é engenharia de software

**UC:** Modelos, métodos e técnicas da engenharia de software — UNIFG 2026/2
**Bloco 1:** Fundamentos da Engenharia de Software
**Entrega:** até a véspera da aula 02 · pull request `[Aula 01] Seu Nome Completo`

A Parte E produz o rascunho do M1 do projeto integrador e é individual, mesmo
para quem já tem equipe. As versões individuais são comparadas na aula 04, e a
divergência entre elas costuma revelar onde o entendimento do problema difere sem
que ninguém tenha notado.

---

## Parte A — Programação e engenharia de software (15 pontos)

**A1 (10 pontos).** Classifique cada pergunta como de **programação** ou de
**engenharia de software**. Para as de engenharia, indique **quem** deveria
responder — a equipe técnica, o cliente, o usuário, ou alguém de fora do projeto.

| | Pergunta |
|---|---|
| a | Como validar o formato do CPF informado? |
| b | Precisamos armazenar o CPF do morador? |
| c | Com quantos dias de antecedência o agendamento pode ser feito? |
| d | Como implementar a busca por horários livres? |
| e | O morador pode remarcar? Quantas vezes? |
| f | Qual banco de dados usar? |
| g | O que acontece se o morador não comparecer? |
| h | Como enviar a confirmação: SMS, e-mail ou papel impresso? |
| i | Quantos agendamentos simultâneos o sistema precisa suportar? |
| j | Como estruturar as tabelas de horário? |

**A2 (5 pontos).** Dois itens parecem de programação e são de engenharia de
software. Identifique quais e explique por quê.

Uma dica sobre o critério: reformule a pergunta começando com "se", "quanto",
"para quem" ou "o que acontece quando". Se a reformulação faz sentido e muda a
resposta, a pergunta é de engenharia.

---

## Parte B — As quatro propriedades de Brooks (20 pontos)

**B1 (16 pontos).** Escolha **um** sistema que você conhece bem — pode ser um
aplicativo que usa, o sistema acadêmico da faculdade, ou um sistema onde você
trabalha ou trabalhou. **Não** use o Agenda Cidadã.

Para cada uma das quatro propriedades, escreva uma manifestação concreta nesse
sistema, com pelo menos três linhas de desenvolvimento.

```markdown
### Sistema escolhido: <nome>
Breve descrição do que ele faz e quem usa.

#### Complexidade
...

#### Conformidade
...

#### Mutabilidade
...

#### Invisibilidade
...
```

A propriedade **conformidade** é a mais difícil e a mais reveladora: exige
identificar restrições externas que o sistema não controla — legislação, formato
de dados de terceiros, regras institucionais, prazos legais. Uma resposta que
descreve apenas complexidade interna não caracterizou conformidade.

**B2 (4 pontos).** Das quatro propriedades, qual você considera a mais séria **no
sistema que escolheu**? Justifique comparando com pelo menos outra.

---

## Parte C — Essencial e acidental (20 pontos)

**C1 (12 pontos).** Classifique cada dificuldade como **essencial** ou
**acidental**. Para as acidentais, indique uma contramedida concreta. Para as
essenciais, explique por que nenhuma ferramenta a elimina.

| | Dificuldade |
|---|---|
| a | Decidir quais serviços entram na primeira versão |
| b | O ambiente de desenvolvimento leva dois dias para configurar |
| c | Entender por que uma pessoa de 68 anos abandona a tela de agendamento |
| d | O teste manual leva três horas a cada versão |
| e | Conciliar a regra do decreto municipal com o que o secretário pediu |
| f | O erro só aparece em produção, nunca no ambiente local |
| g | Descobrir que o morador frequentemente agenda para outra pessoa |
| h | O código repete a mesma validação em quatorze lugares |

**C2 (8 pontos).** Escolha **uma** ferramenta, framework ou tecnologia que ganhou
atenção nos últimos três anos e avalie, em 12 a 18 linhas: ela reduz dificuldade
acidental, essencial, ou promete reduzir essencial sem conseguir?

A resposta precisa ser específica sobre **qual** dificuldade, e não uma avaliação
geral da ferramenta. Uma ferramenta pode reduzir dificuldade acidental de forma
excelente e ser apresentada comercialmente como se resolvesse a essencial — e
essas duas afirmações não se contradizem.

---

## Parte D — A crise do software (15 pontos)

**D1 (9 pontos).** Pesquise **um** caso histórico de fracasso em projeto de
software, entre 1960 e 2000. Sugestões: OS/360 da IBM, Therac-25, o sistema de
bagagens do aeroporto de Denver, Ariane 5 Voo 501, o sistema de despacho de
ambulâncias de Londres em 1992.

Escreva de 10 a 15 linhas informando: o que o sistema devia fazer; o que
aconteceu; qual foi a causa técnica ou organizacional identificada; e qual das
quatro propriedades de Brooks aparece com mais força no caso. Cite a fonte com
link.

**D2 (6 pontos).** A Lei de Brooks afirma que acrescentar pessoas a um projeto
atrasado o torna mais atrasado.

Explique o raciocínio por trás dela, apresentando pelo menos **dois mecanismos
concretos** pelos quais o resultado pode ser pior que não contratar ninguém.
Depois indique **uma** situação em que acrescentar pessoas a um projeto atrasado
poderia funcionar, e o que essa situação precisa ter de diferente.

A segunda parte é a mais interessante. A lei não é absoluta; ela descreve um
mecanismo, e mecanismos têm condições de aplicação.

---

## Parte E — Caracterização do problema (30 pontos)

Individual. É o rascunho do M1.

**E1 (20 pontos).** Escreva a caracterização do problema do Agenda Cidadã, com
quatro seções.

| Seção | Conteúdo | Pontos |
|---|---|---|
| Situação atual | o que acontece hoje, com dados. Estimativas são aceitas se declaradas como tais, com o raciocínio | 6 |
| Quem sofre e como | pessoas com contexto, não "os cidadãos" | 5 |
| O que já foi tentado | se algo foi, e por que não resolveu. Se nada foi, dizer isso | 4 |
| O que muda se resolvido | com número, quando possível | 5 |

Um critério de reprovação, declarado antes: **a descrição do problema não pode
conter a solução**. "O problema é que a prefeitura não tem um sistema de
agendamento" é a solução escrita como se fosse problema. O problema é a fila às
seis e meia da manhã, e as consequências dela.

**E2 (10 pontos).** Escreva de **quatro a seis perfis de usuário**. Cada perfil
precisa de:

```markdown
### <nome>, <idade> — <papel>

**Contexto de uso:** onde, quando, com qual dispositivo, com quanto tempo
**Familiaridade digital:** e como isso afeta o uso
**O que quer:** em uma frase
**O que teme:** em uma frase
**Frequência de uso:** quantas vezes por mês ou por dia
```

Ao menos um dos perfis deve ser de alguém que **não usa** o sistema diretamente,
mas é afetado por ele.

---

## Parte F — Investigação (sem pontos, obrigatória)

A ausência desta parte reduz a nota da lista em 10 pontos.

Encontre um caso, atual ou histórico, de ferramenta ou metodologia que foi
apresentada como capaz de eliminar a parte difícil do desenvolvimento de
software. Exemplos de categorias, sem indicar resposta: ferramentas de
programação visual, CASE dos anos 1990, geradores de código a partir de modelo,
plataformas sem código.

Escreva de 8 a 12 linhas informando: qual era a promessa; o que efetivamente
entregou; onde a promessa não se cumpriu; e qual dificuldade — essencial ou
acidental — ela realmente atacava. Cite a fonte.

A pergunta que interessa não é se a ferramenta era boa. Várias eram, e são. É se
a promessa correspondia ao que a ferramenta podia entregar.

---

## Formato da entrega

```
exercicios/aula01/
├── RESPOSTAS.md          Partes A, B, C, D e F
└── problema.md           Parte E — caracterização e perfis
```

## Distribuição dos pontos

| Critério | Pontos |
|---|---|
| Corretude técnica | 35 |
| Justificativa das decisões técnicas | 30 |
| Qualidade dos artefatos | 25 |
| Clareza da comunicação | 10 |
| Ausência da Parte F | −10 |

---

## Observações sobre algumas questões

**Parte A.** Os itens **f** e **j** são os que mais dividem opinião. Escolher
banco de dados parece decisão puramente técnica, e é — até o momento em que a
prefeitura informa que só pode contratar licença de um fornecedor específico, ou
que a equipe de TI municipal mantém apenas um tipo de servidor. Aí a pergunta
muda de natureza.

**Parte B.** Escolher um sistema que você conhece bem, em vez do Agenda Cidadã, é
deliberado. Caracterizar as propriedades num sistema que existe e que você usa
produz exemplos concretos; fazê-lo num sistema hipotético produz exemplos
genéricos.

**Parte C2.** A tentação é escrever uma avaliação favorável ou desfavorável da
ferramenta. A questão não pede isso. Pede identificar **qual** dificuldade ela
ataca — o que exige nomear a dificuldade antes de avaliar a ferramenta.

**Parte E1.** A separação entre problema e solução é a habilidade central da
engenharia de requisitos, e é o assunto do bloco 4. Praticá-la agora, antes de
estudar as técnicas, torna visível o quanto ela é contraintuitiva: a tendência
natural é descrever o problema já pela ausência da solução que se imagina.

**Parte E2.** O perfil de alguém que não usa o sistema diretamente costuma ser
esquecido. No Agenda Cidadã, há pelo menos dois candidatos: quem não tem celular
e é atendido por um servidor que opera o sistema, e o gestor que só consome
relatório. O segundo é usuário; o primeiro é afetado sem ser usuário — e essa
distinção importa no bloco 5.
