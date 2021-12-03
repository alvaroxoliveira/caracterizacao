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

### Modelo de tradução

Elixir é uma linguagem que suporta multi-paradigma, mas tem centralizado o desenvolvimento primariamente no paradigma funcional.

Foi projetada para ser executada em cima da Máquina Virtual Erlang, conhecida por executar sistemas em baixa latência como exemplo principal, redes de telefone.

O Earlang VM por sua vez foi projetado para executar como um processo do Sistema Operacional. Por padrão ele executa um thread do SO por núcleo para atingir a utilização máxima da máquina. Esse número de threads é definido automaticamente ao ligar a máquina. Os processor do Erlang são totalmente implementados pela sua VM, assim eles não tem contato direto com os processor do Sistema Operacional. Em um sentido de que a execução do Erlang roda apenas uma thread por núcleo, mesmo com um milhão de processor, podemos chamar a VM Erlang de uma espécie de "Máquina Virtual de Processos".

### Nomes, variáveis e vinculação
#### Nomes

<body style="text-align: justify">
<ul>
    <li>Elixir utiliza <code>snake_case</code> ao definir variáveis, nomes de funções atributos de módulo e várias outras declarações.</li>
    <li>Aliases são comumente usados como nomes de módulos são exceção para a regra, pois devem ser escritos em forma <code>CamelCase</code>. Para aliases, as letras maiúsculas são mantidas em siglas.</li>
    <li> Átomos são escritos na forma <code>:snake_case</code> ou <code>:CamelCase</code>, embora a convenção seja na forma snake.</li>
    <li> Nomes de arquivos também devem seguir o padrão <code>:snake_case</code>.</li>
    <li>Valores que não devem ser usados, por exemplo, como parametros de funções, devem seguir o padrão adicionando como prefixo o caractere "_" underline.</li>
    <li>Os chamados <b>Trailing bang</b>, casos que significam que uma função ou macro podem gerar um caso de falha/exceção levam como sufixo o caractere "!" ponto de exclamação.</li>
    <li>As funções que retornam um booleano são nomeadas com um sufixo "?".</li>
    <li>As verificações do tipo booleanas, devem ser nomeadas com um <code>is_</code> como prefixo.</li>
</ul>
    
</body>

#### Variáveis

<body style="text-align: justify">
    <p>
        As variáveis no Elixir não funcionam como acontece normalmente em linguagens de paradigma imperativos. No Elixir, as variáveis são rótulos para seus valores, o que diferencia de uma variável apresentar um valor.
    </p>
    <p>
        Temos dois tipos de variáveis no Elixir, que são as variáveis globais, que são aquelas que são visíveis e tem acesso por toda a parte do programa e temos também às variáveis locais, que funcionam dentro de seus blocos ou subprograma.
    </p>
    
</body>

#### Vinculação (Binding)

<body style="text-align: justify">
    <p>
      Sua vinculação é do tipo dinâmica e forte, ou seja, não há como mudar o tipo das variáveis, mas a vinculação das variáveis é feita em tempo de execução.
    </p>
</body>

### Escopo, tempo de vida e ambientes de referência.

#### Escopo e tempo de vida

<body style="text-align: justify">
    <p>
      Para variáveis globais, seu escopo é inteiramente como seu nome sugere, ou seja, é visível por todo o programa e tem sua vida extendida por toda a execução do programa.
    </p>
    <p>
      Para variáveis locais, seu escopo é inteiramente como seu nome sugere, ou seja, é visível por todo o subprograma em que foi declarada, e tem sua vida até o fim da execução das instruções do bloco ou sobprograma em que foi declarada.
    </p>
</body>

#### Ambientes de Referência

<body style="text-align: justify">
    <p>
      A linguagem Elixir é dita de escopo dinâmico e suas variáveis são referenciadas dentro de um ambiente dinâmico.
    </p>
</body>

### Estruturas de controle a nível de Instrução

<body style="text-align: justify">
    <p>
        Elixir possui quatro tipos de desvios de controle principais:
    </p>
    <ol>
        <li>case</li>
        <li>cond</li>
        <li>if and unleess</li>
        <li>do end blocks</li>
    </ol>
</body>

#### Case

<body style="text-align: justify">
    <p>
        Case nos permite compara um valor com muitos padrões até encontrarmos um valor correspondente. Podemos ver o caso de uso que existe no site da linguagem:
    </p>
</body>

~~~~
    iex> case {1, 2, 3} do
    ...>   {4, 5, 6} ->
    ...>     "This clause won't match"
    ...>   {1, x, 3} ->
    ...>     "This clause will match and bind x to 2 in this clause"
    ...>   _ ->
    ...>     "This clause would match any value"
    ...> end
    "This clause will match and bind x to 2 in this clause"
~~~~ 

<body style="text-align: justify">
    <p>
        Para padronizar a correspondência com uma variável existente, é preciso usar o <code>^</code> operador.
    </p>
</body>
~~~~
    iex> case {1, 2, 3} do
    ...>   {1, x, 3} when x > 0 ->
    ...>     "Will match"
    ...>   _ ->
    ...>     "Would match, if guard condition were not satisfied"
    ...> end
    "Will match"
~~~~

#### Cond


<body style="text-align: justify">
    <p>
        Case é útil quando é preciso comparar valores diferentes. No entanto, em várias circunstancias, queremos verificar várias condições e obter o resultado daquela primeira que não for falsa. Para esse caso usamos o <code>cond</code>. Ele é equivalente ao if/else if em linguagens imperativas. Se todas as condições retornarem <code>nil</code> ou <code>false</code>, um erro <code>CondClauseError</code> será gerado. Então para que isso não ocorra, normalmente é adicionado uma condição no final igual a <code>true</code>, que servirá como um suporte para não cair no erro citado.
    </p>
</body>

~~~~
    iex> cond do
    ...>   2 + 2 == 5 ->
    ...>     "This is never true"
    ...>   2 * 2 == 3 ->
    ...>     "Nor this"
    ...>   true ->
    ...>     "This is always true (equivalent to else)"
    ...> end
    "This is always true (equivalent to else)"
~~~~ 

#### If e Unless

<body style="text-align: justify">
    <p>
        Além dessas citadas acima, temos também o if e o unless que tem sua utilidade quando se precisa verificar apenas uma condição. Se a expressão if for verdadeira o bloco entre seu <code>do-end</code> será executado, caso contrário, retorna <code>nil</code> ou <code>false</code>. Exatamente o oposto ocorre para <code>unless</code>. Outra coisa é que também suportam os blocos <code>else</code>.
    </p>
</body>

~~~~ 
    iex> if true do
    ...>   "This works!"
    ...> end
    "This works!"
    iex> unless true do
    ...>   "This will never be seen"
    ...> end
    nil  
~~~~
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

### Metaprogramação

Metaprogramação é o processo de usar o código para escrever código. Em Elixir isso é incrivelmente possível, dando a capacidade de levar a linguagem a um nível de adequação às necessidades do programador alterando o código dinamicamente.

O primeiro passo para a metaprogramação em elixir é a compreensão das representações das expressões. Ao ver mais a fundo a estrutura da linguagem, pode-se observar que a Árvore de Sintaxe Abstrata é composta de tuplas e essas tuplas por sua vez contém três partes: O nome da função, metadados e argumentos da função.

O Elixir tem algumas funções que proporcionam a visualização dessas estruturas internas, as quais são ```quote``` e ```unquote```.

Na primeira se passa a função e o retorno desta é uma tupla contendo a estrutura de como o elixir representa na árvore abstrata.

A segunda faz totalmente o contrário, então ao passar uma estrutura interna, esta função retorna o código elixir respectivo para aquela estrutura.

Outro recurso dentro desse mundo da metaprogramção são as macros. Na documentação oficial se aconselha ser moderado com os mesmos, mas ao entender as funções anteriores, o programador está pronto para entendê-lo.

Macros são funções especiais destinadas a retornar uma expressão entre aspas que será inserida no aplicativo. Com isto, têm-se o necessário para estender Elixir e adicionar código dinâmicamente nas aplicações.

### Segurança

Elixir é uma linguagem bastante segura. Começando pelo garbage collector e controle da memória usada, o Elixir é uma linguagem que faz o gerenciamento de memória automaticamente, semelhante ao que a linguagem Java faz, mas o que as outras linguagens que contém o GC fazem, o Elixir também faz para seguraça em concorrência.

A segurança em Threads é muito desafiadora e difícil de ser proporcionada em uma linguagem de programação. O Elixir não entrega Threads para uso diretamente, e o garbage collection juntamente com o gerenciamento de threads é feito em tempo de execução. O que se faz é aproveitar do Erlang para a criação de processos leves que são fornecidos.

Essa coisa toda de processos individualiza muito a aplicação, e o uso deles no desenvolvimento ajuda muito para a segurança da aplicação. Dois processos não compartilham memória, eles apenas se comunicam trocando mensagens. Assim, nas aplicações desenvolvidas em Elixir, as Threads não vazam estado, até porque isso é praticamente impossível, pois a linguagem torna isso extremamente difícil, o que fica improvável de acontecer.

### Performance

Elixir é uma linguagem que proporciona uma performance muito grande. Muito disso é por conta do grande poder que a Erlang VM proporciona. O fato de Elixir não compartilhar estados entre seus processos e estes se comunicarem através de trocas de mensagens, isso faz com que muita coisa seja simplificada. Essa estratégia certamente é uma das maiores vantagens do motivo do uso da Máquina Virtual Erlang, além do poder de que a concorrência da mesma proporciona, fazendo a linguagem ser bastante rápida e uma ótima opção para sistemas de grande escala, com milhões de usuários simultâneos.

### Escalabilidade Concorrência e Threading 

Em escalabilidade Elixir é um grande destaque. Não é uma surpresa o motivo: Erlang VM. O fato de poder usar múltiplos processos faz com que se usem todos os núcleos de um nó com uma grande facilidade. Isso faz com que seja possível utilizar também múltiplos nós, o que facilita a criação de infraestruturas bastante parrudas e isso contém um efeito colateral positivo: ótima performace da aplicação.

É muito comum a Erlang VM utilizar todas as CPUs da máquina, com milhares de processos que se comunicam através da troca de mensagens em uma aplicação Elixir.

A concorrência é um dos pontos fortes do Elixir que graças (mais uma vez) ao Erlang VM, há uma facilidade muito grande para adaptar o código para a concorrência. O modelo de comunicação segue o modelo de Atores, processos isolados que se comunicam através de mensagens.

### Confiabilidade
  
Elixir é uma linguagem super confiável. É derivada do Erlang, uma linguagem muito madura, presente no mercado há anos e bastante usada em telecomunicações por conta de vários recursos que tem por conta da sua máquina virtual.

Dentre esses recursos podem ser citados a tolerância a falhas, onde basicamente o Elixir se destaca bastante, pelo fato das aplicações continuarem funcionando mesmo quando há presença de falhas na execução, o que é bastante importante, pois mantém a aplicação no ar. Outra coisa bastante importante são os multiplos processos criados pela VM, o que faz com que Elixir use todos os CPUs e garante escalabilidade e concorrência, além do garbage collection e da boa gerência de memória.

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

1. https://elixir-lang.org/
2. https://www.hostgator.com.br/blog/elixir-linguagem-programacao-brasileira/
3. https://medium.com/@marcelomg21/microsservi%C3%A7os-com-elixir-erlang-otp-beam-b76a5fb3bef
4. https://latam.sinch.com/blog/elixir-brasil-o-funcional-encontra-se-aqui/
5. https://www.lambda3.com.br/2016/07/elixir-tipos-operadores-e-o-iex/
6. https://code.tutsplus.com/pt/tutorials/elixir-walkthrough-part-2-data-types--cms-27510
7. https://ateliware.com/blog/tudo-que-voce-precisa-para-escolher-elixir
8. https://deinfo.uepg.br/~alunoso/2020/SO/Erlang/erlang-site.html
9. http://www.each.usp.br/petsi/jornal/?p=2459
10. https://elixirschool.com/pt/lessons/advanced/metaprogramming/
11. https://www.pravaler.com.br/por-que-o-pravaler-escolheu-a-linguagem-elixir/
12. 
13. 
14. 
15. 
16. 
17. 
18. 
19. 
20. 
21. 
22. 
23. 
24. 

