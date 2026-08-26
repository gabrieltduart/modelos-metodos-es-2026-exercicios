**PARTE A****

A1:

a. Programação.

b. Engenharia, cliente

c. Engenharia, cliente

d. Engenharia, equipe tecnica

e. Engenharia, cliente

f. Programação

g. Engenharia, equipe técnica

h. Engenharia, cliente

i. Engenharia, equipe técnica

j. Engenharia, equipe tecnica

A2:

Os itens d e j são de engenharia de software, pois tratam diretamente de como o sistema sera implementado e estruturado. O item d envolve a implementação da busca por horários disponíveis, enquanto o item j envolve a definição da estrutura dos dados de horários. Os itens tratam de regras e requisitos do sistema, como políticas de agendamento, armazenamento de dados, comunicação e capacidade.

**PARTE B**

B1:

### Sistema escolhido: <Discord>
Aplicativo social para comunicacao de texto e chamada, tambem conta com integracoes para desenvolvedores e a famosa opcao de compartilhamento de tela.

#### Complexidade
Creio que seja um aplicativo dificil de se acostumar para leigos, para pessoas que nao tem o costume de utilizar softwares. A navegacao nao e tao intuitiva, alem de haver funcoes mais especificas que alguem nao aprenderia sozinho tao facil.

#### Conformidade
O Discord precisa seguir diversas regras e padrões, principalmente relacionados à privacidade dos usuários, segurança e protecao de dados. Além disso, precisa estar de acordo com regras de lojas de aplicativos e sistemas operacionais, como Android, iOS, Windows e macOS. Também existem regras internas da propria plataforma, como os Termos de Serviço e as Diretrizes da Comunidade.

#### Mutabilidade
Sofre atualizacoes e mudanças com bastante frequência. Novas funções são adicionadas, enquanto outras podem ser modificadas ou removidas de acordo com as necessidades dos usuários e dos desenvolvedores. A interface também pode mudar ao longo do tempo, fazendo com que os usuários precisem se adaptar às novas versoes.

#### Invisibilidade
Grande parte do funcionamento do Discord acontece de forma invisivel para o usuario. O sistema precisa gerenciar servidores, canais, mensagens, chamadas de voz, transmissao de tela, notificações e conexões em tempo real sem que o usuario precise saber como essas operações funcionam internamente. Isso torna a parte tecnica do sistema bastante complexa, mesmo que seu funcionamento pareça simples para quem está utilizando.

B2:

Eu considero a conformidade a propriedade mais seria no Discord, pois o sistema precisa seguir diversas regras externas que não são controladas diretamente pelos desenvolvedores. Isso inclui leis de proteção de dados e privacidade, regras das lojas de aplicativos e exigencias relacionadas ao uso de servicos de terceiros.

**PARTE C**

C1:

Dificuldade	Classificação	Justificativa / Contramedida
a. Decidir quais serviços entram na primeira versão - Essencial	- É necessario entender as necessidades do sistema e tomar uma decisão de escopo. Nenhuma ferramenta consegue determinar sozinha quais serviços são realmente prioritários para os usuários e para o negócio.

b. O ambiente de desenvolvimento leva dois dias para configurar - Acidental.

c. Entender por que uma pessoa de 68 anos abandona a tela de agendamento - Essencial - É necessário compreender o comportamento e as necessidades reais do usuario. Ferramentas podem coletar dados sobre o abandono, mas nao eliminam a necessidade de investigar e interpretar o motivo.

d. O teste manual leva três horas a cada versão - Acidental.

e. Conciliar a regra do decreto municipal com o que o secretário pediu - Essencial - Existe uma necessidade de interpretação e negociação entre requisitos externos e decisões humanas. Nenhuma ferramenta consegue eliminar a necessidade de determinar qual regra deve prevalecer em caso de conflito.

f. O erro só aparece em produção, nunca no ambiente local - Acidental.

g. Descobrir que o morador frequentemente agenda para outra pessoa - Essencial - É uma descoberta sobre como o sistema é realmente utilizado. Ferramentas podem ajudar a coletar dados, mas não eliminam a necessidade de observar o comportamento dos usuarios e adaptar os requisitos.

h. O código repete a mesma validação em quatorze lugares - Acidental.

C2:
Exemplo: GitHub Copilot

O GitHub Copilot é uma ferramenta de IA para auxiliar no desenvolvimento de software.
Ele pode reduzir principalmente dificuldades acidentais, como a dificuldade de escrever codigo repetitivo.
Por exemplo, ele poderia ajudar diretamente na dificuldade h, em que uma validação aparece em quatorze lugares.
O Copilot pode sugerir uma função de validação centralizada e indicar pontos onde ela poderia ser reutilizada.
Isso reduz o esforço necessário para realizar uma tarefa que já sabemos como solucionar.
Também pode ajudar na dificuldade d, sugerindo testes automatizados para substituir parte dos testes manuais.
Porem, o Copilot não elimina as dificuldades essenciais do desenvolvimento.
Ele não consegue decidir quais serviços devem estar na primeira versão do sistema (a).
Também não consegue determinar por conta própria por que uma pessoa de 68 anos abandona o agendamento (c).
Da mesma forma, não pode decidir como resolver o conflito entre um decreto municipal e uma ordem do secretário (e).
Essas situações exigem conhecimento do contexto, comunicação e decisões humanas.
Portanto, o Copilot reduz algumas dificuldades acidentais, mas não elimina as essenciais.
Embora seja divulgado como uma forma de aumentar a produtividade dos programadores,
isso não significa que ele resolva os problemas fundamentais de entender requisitos e tomar decisões.
Assim, seu beneficio está principalmente em diminuir o trabalho mecânico e repetitivo do desenvolvimento.

**PARTE D**

D1:
Sistema de bagagens do Aeroporto Internacional de Denver

O sistema automatizado de bagagens do Aeroporto Internacional de Denver deveria transportar automaticamente as malas entre os balcões, areas de triagem e aeronaves.
A ideia era criar um sistema altamente automatizado, capaz de movimentar e direcionar as bagagens rapidamente por todo o aeroporto.
Durante os testes, porém, ocorreram falhas graves, incluindo malas sendo carregadas incorretamente, desviadas para destinos errados e causando congestionamentos no sistema.
Os problemas foram tão grandes que a inauguração do aeroporto precisou ser adiada várias vezes.
Em fevereiro de 1994, um grande teste revelou falhas importantes e indicou que o sistema não estaria pronto para a data planejada.
A cidade acabou construindo um sistema convencional de bagagens como alternativa para permitir a abertura do aeroporto.
Entre os problemas estavam falhas tanto no software quanto no hardware e dificuldades para realizar testes suficientes antes da inauguração.
Também houve mudanças no projeto e no escopo do aeroporto durante seu desenvolvimento, aumentando a complexidade do sistema.
A causa, portanto, não foi apenas um erro de programação, mas também problemas de planejamento, mudanças de requisitos e gerenciamento do projeto.
A propriedade de Brooks que aparece com mais força é a complexidade, pois o sistema tentava coordenar automaticamente uma enorme quantidade de bagagens, equipamentos e operações simultaneas.
A complexidade tornou dificil prever todos os comportamentos e testar adequadamente o sistema antes de colocá-lo em funcionamento.
O caso demonstra como aumentar o tamanho e a complexidade de um sistema pode tornar seu desenvolvimento e sua validação muito mais difíceis.

D2:
Lei de Brooks

A Lei de Brooks afirma que “acrescentar pessoas a um projeto atrasado o torna mais atrasado” porque novos integrantes não começam imediatamente produzindo trabalho util. Eles precisam aprender o sistema, o codigo, os requisitos e os processos utilizados pela equipe. Esse periodo de aprendizado consome tempo dos desenvolvedores que ja estavam no projeto.

Um primeiro mecanismo é o custo de comunicação. Conforme a equipe aumenta, cresce a quantidade de pessoas que precisam trocar informações e coordenar suas atividades. Isso pode gerar mais reuniões, duvidas, conflitos e necessidade de alinhamento.

Um segundo mecanismo é a divisao limitada do trabalho. Nem toda tarefa pode ser dividida entre varias pessoas. Algumas possuem dependencias ou precisam ser realizadas em sequencia. Colocar mais desenvolvedores nessas tarefas pode gerar interferencia e aumentar o trabalho de integração em vez de acelerar o projeto.

Porem, a lei não é absoluta. Acrescentar pessoas pode funcionar quando o trabalho restante é bem modularizado e independente, com tarefas que podem ser distribuidas sem muita comunicacao entre os participantes. Por exemplo, se um projeto atrasado possui varios testes independentes ainda nao executados, novos integrantes podem assumir conjuntos diferentes de testes com pouco treinamento e pouca interferência.

Nesse caso, a situacao é diferente porque o custo de comunicação e aprendizado é pequeno em relação ao trabalho que pode ser paralelizado. Assim, adicionar pessoas pode realmente aumentar a velocidade do projeto.

**PARTE E NO problema.md**

**PARTE F:**

### — Investigação: ferramentas CASE

As ferramentas **CASE (Computer-Aided Software Engineering)** ganharam destaque no final dos anos 1980 e início dos anos 1990.
A promessa era aumentar a produtividade e a qualidade do desenvolvimento, automatizando partes do ciclo de vida e permitindo criar sistemas a partir de modelos e especificações.
Na prática, elas entregaram recursos úteis de modelagem, documentação, integração e, em alguns casos, geração de código.
Porém, a integração completa entre as ferramentas e as diferentes etapas do desenvolvimento continuou sendo um problema.
Também havia limitações na geração de código e na tecnologia disponível nas primeiras ferramentas CASE.
O próprio SEI registrou que afirmações exageradas de fornecedores e expectativas irreais contribuíram para fracassos na adoção de CASE.
Assim, as ferramentas não conseguiram eliminar a parte difícil de compreender requisitos e decidir exatamente o que o software deveria fazer.
Modelar o sistema podia facilitar a representação do projeto, mas não garantia que o modelo estivesse correto ou que os requisitos fossem compreendidos.
Portanto, a promessa de tornar o desenvolvimento muito mais automático não correspondia totalmente ao que a tecnologia podia entregar.
A dificuldade que CASE realmente atacava era principalmente acidental, reduzindo trabalho repetitivo de documentação, modelagem e geração de partes do código.
Ela não eliminava a dificuldade essencial de entender o problema e transformá-lo em requisitos corretos.
O caso mostra que automatizar a produção do código não elimina a necessidade de tomar as decisões difíceis que vêm antes dela.