<!-- Caracterização da Linguagem L2 - Elixir - Álvaro Souza Oliveira -->


# Linguagem 2 - Elixir

![Histórico da linguagem Elixir](https://github.com/alvaroxoliveira/caracterizacao/blob/main/T1-alvaroxoliveira/Elixir-LP.png)

# Guia para Caracterização de Linguagens de Programação

+ Linguagem de Programação: <nome>

  * [Apresentação e histórico](#apresentação-e-histórico)
  * [Características da Linguagem](#características-da-linguagem)
  * [Capacidades da Linguagem](#capacidades-da-linguagem)
  * [Produtividade do Desenvolvedor](#produtividade-do-desenvolvedor)
  * [Ecossistema](#ecossistema)
  * [Informações Adicionais](#informações-adicionais)
  * [Referências](#referências)

## Apresentação e histórico

Elixir é uma linguagem de programação dinâmica, funcional e concorrente, como o próprio site já diz. Foi lançado em 2012, através de um projeto da empresa brasileira Plataformatec chefiado por José Valim. É uma linguagem que aproveita da Erlang Virtual Machine (A Máquina Virtual Erlang), compilando em cima de Erlang para fornecer softwares distribuidos, em tempo real e tolerantes a falhas. A Máquina Virtual Erlang também é conhecida por executar sistemas de baixa latência pois foi criada principalmente com intuito de ser utilizada em redes de telefonia, pois é realmente importante que tudo ocorra em tempo real e com o mínimo de perda possível. 

José Valim e sua equipe trabalhavam para a melhoria da performance do framework Ruby on Rails, que é um framework utilizado também para desenvolvimento web, que aumenta a velocidade de produção e facilita o desenvolvimento de sites orientados a bancos de dados. Este trabalho de melhoria de performance depois de um tempo começou a ser repensado e a decisão foi de mudar o rumo das coisas e investir em uma nova linguagem e por consequência, Erlang foi escolhida por conta dos recursos e da maturidade que tinha para trabalhar com multiprocessamento, baixa latêncie e tolerância a falhas. Por conta disso, foi criado o Elixir, que como já falado, é executada em cima da Erlang VM.

O Elixir é uma linguagem amplamente usada para o desenvolvimento para web, além também de sistemas embarcados, ingestão de dados e sistemas de multimídia por uma quantidade cada vez mais crescente de empresas.

Seu código é executado através de processos isolados que permitem que sejam coletados de maneira independente, reduzindo pausas e fazendo o aproveitamento dos recursos da máquina de maneira muitíssimo eficiente, e esses processos ainda podem se comunicar entre outras máquinas diferentes dentro de uma mesma rede.

Ainda por conta do Elixir utilizar da Erlang VM, esta permite que a linguagem ainda utilize as bibliotecas do próprio Erlang.
## Características da Linguagem

### Paradigma

Elixir é uma linguagem multiparadigma, tendo como principal o paradigma Funcional, mas também sendo concorrente e distribuída. 

O paradigma funcional é uma característica de linguagens de programação que a construção de software é baseada na escrita de composição de funções puras, sem compartilhamento de estados, dados mutáveis e efeitos colaterais. É bastante semelhante com o pensamento de funções matemáticas, assim, para parãmetros iguais o resultado sempre será o mesmo, que é a definição de função na matemática que é o mesmo que dizer que a função é pura.

### Propósito

O propósito é bem geral, mas especificamente o Elixir foi criado para obter bastante performance para sistemas, buscando a concorrência, obtendo o máximo possível de velocidade, além de ter capacidade para criar aplicações utilizadas por milhões de pessoas ao mesmo tempo, sendo possível trabalhar com múltiplos usuários realizando requisições simultâneas. Além disso tem uma ótima escalabilidade, por conta da Erlang VM, tornando possível a aplicação ser executada em múltiplos nós e juntamente a tolerância a falhas no qual o Elixir tem uma vantagem muito grande a esse recurso de segurança, que permite que a aplicação continue sua execução mesmo quando alguma falha ocorre durante o seu uso.

### Sistema de tipagem

Elixir é uma linguagem dinamicamente tipada e isso quer dizer que não é preciso especificar os tipos para definir variáveis nem especificar tipos do parâmetros de funções ou retorno das mesmas. Os tipos são inferidos em tempo de execução.

Entre os tipos básicos em Elixir podem ser citados: 

+ Number;
+ Boolean;
+ Atom - Constantes cujo o valor é seu próprio nome;
+ String;
+ Anonymous Function - Funções anônimas;
+ List - Estruturas definidas através de colchetes, podendo conter diversos dados;
+ Tuples - Similar a listas e criadas com chaves;
+ Maps - Estruturas de chave-valor;

### Ambiente de execução

O ambiente de execução é via Erlang VM, que cria, escalona e gerencia os processos de forma extremamente rápida e independente do sistema operacinal executado. A comunicação entre estes processos ocorre através do envio e recebimento de mensagens, sendo os dados trocados dessa forma. Cada processo tem sua caixa de mensagens e estes por sua vez armazenam também as mensagens recebidas, acontecendo de maneira muito rápida, tendo o tempo de execução bastante reduzido comparado a outras linguagens.

Erlang ainda permite a atualização de codigo fonte com o sistema em execução e para isso o sistema contém uma tabela que registra o endereço de todos os módulos carregados e por sua vez, executa os módulos antigos até os mesmos terminarem de carregar e consequentemente os novos processos são criados com a versão do código fonte atualizada, possibilitando melhorias sem que o sistema precise de uma interrupção, o que é bem vantajoso do ponto de vista comercial. Erlang ainda possui um ambiente distribuído onde diferentes ambientes das aplicações podem ser executadas em diferentes máquinas e tudo isso é perfeitamente feito por conta da troca de mensagens.

### Custos

Elixir é uma linguagem ótima para desenvolvimento de aplicações, tendo como objetivo ser de ótima escalabilidade, concorrente e tolerãncia a falhas. É uma linguagem ótima para o mercado por conta de todos esses recursos que deriva da Erlang e isso traz um valor imenso para o mercado. É uma linguagem que não é tão trivial de aprender como outras linguagens, então depende de um certo grau de senioridade para desenvolver com a linguagem, mas isso pode ser vantajoso muito pelo fato de ter uma certa garantia de qualidade e desempenho do software.

## Capacidades da Linguagem
  + Metaprogramação
  + Gerenciamento de Ciclo de Vida
  + Segurança 
  + Performance
  + Escalabilidade
  + Confiabilidade
  + Concorrência e Threading 
  + Custos
  _Custos aqui ... _

## Produtividade do Desenvolvedor
  + Frameworks e Contâiners
  + Ferramentas Disponíveis
  + Sintaxe, Semântica e Operações Predefinidas
    + Legibilidade
    + Redigibilidade
  + Custos 

## Ecossistema
  + Maturidade
  + Comunidade
  + Governança
  + Fragmentação

---

## Informações Adicionais


## Referências 

1. https://www.gartner.com/en/documents/2071615/programming-languages 
framework for assessing and characterizing programming languages and assessing their applicability to specific projects

