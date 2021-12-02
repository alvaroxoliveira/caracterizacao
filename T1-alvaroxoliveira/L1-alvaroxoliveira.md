<!--
Recomendações:
1. A
2. B

Contribuidores:
+ Kenia e Luiz
+ Mauricio Santiago, Gustavo Santos, Matheus Novais, Ivens Joris, Matheus Silva
+ Álvaro Souza Oliveira; Carlos Mosselman Cabral Neto; Thiago Vieira Souza Andrade; Caio Nery Matos Santos; Vanessa Machado Araújo
+ Daniel

Fontes:
+ Criação do TOC
  + [Table of contents generated with markdown-toc](http://ecotrust-canada.github.io/markdown-toc/)
---

--> 

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

![Histórico da linguagem java](https://github.com/alvaroxoliveira/caracterizacao/blob/main/T1-alvaroxoliveira/Java-LP.png)
  
Java é uma linguagem de programação que tem como paradigmas principal a Orientação a Objetos, criada na década de 90, criada pela **Sun Microsystens**, em um projeto chamado **Green Project**, chefiado por **James Gosling**. Em 2008, a Sun é vendida e o Java passa a ser posse da **Oracle Corporation**.

Surge como uma ferramenta que seguia a ideia de ser executada em todo e qualquer sistema possível, e para isso houve um árduo projeto para a criação dessa possibilidade, já que nesta época existia o problema de incompatibilidade envolvendo a execução de código em diferentes tipos de máquina por conta da arquitetura usada nos computadores, sistema operacional e vários outros problemas técnicos que faziam com que um mesmo código escrito em uma linguagem com compilação tradicional não funcionasse para todos os tipos de computadores da época. Então Java é criada usando o conceito de execução de código por uma Virtual Machine, a famosa JVM, que faz a compilação do seu código para um bytecode e após isso é gerado um código de máquina compatível com as propriedades da máquina em uso, o que faz com que um mesmo código escrito seja executado em Windows ou Linux por exemplo.
## Características da Linguagem

### Modelo de tradução

<body style="text-align: justify">
    <p>
    Java é uma linguagem multi-paradigma e também de multi-plataforma, que tem sua compilação em duas etapas, as quais envolvem primeiro por meio de um compilador idependente do Sistema Operacional e na segunda compilação, tudo ocorre por meio da usa tão poderosa Máquina Virtual Java ou Java Virtual Machine, ou, para os íntimos, JVM, que é preparada justamente para cada tipo de Sistema Operacional que suporta seu código, que, conhecidamente é uma lista muito vasta.
    </p>
    <p>
    Em Java, os programas não são compilados diretamente em arquivos executáveis, em vez disso, são compilados em <b>bytecode</b>, que a JVM (Java Virtual Machine) executa em tempo de execução. Cada vez que um programa for executado, o bytecode é convertido usando o compilador Just-In-Time (JIT). Isso resulta em um código de máquina que é alimentado na memória e assim, é executado.
    </p>
    </p>
    <p>
    Um código escrito na linguagem Java precisa ser compilado em duas etapas:
        <ol>
            <li>Primeiramente, precisam ser compilados para o bytecode</li>
            <li>Em segundo, quando o bytecode é executado, através do JIT ele é convertido para Machine-code (Código de Máquina)</li>
        </ol>
    </p>
    <p>
    Em intermédio entre a primeira e a segunda compilações, ao converter o código-fonte em bytecode, o compilador segue as seguintes etapas de forma cronológica:
        <ul>
            <li><b>Etapa de Análise</b>: Lê os arquivos de origem <code>.java</code> e faz o mapeamento da sequência de tokens resultante em nós de uma AST <b>Árvore Sintática Abstrata (Abstract Sintax Tree).</b></li>
            <li><b>Enter</b>: Insere elementos para as suas definições na tabela de símbolos.</li>
            <li><b>Anotações de Processos</b>: Processa as anotações encontradas nas unitdades de compilação especificadas.</li>
            <li><b>Atribuição</b>: Atribui as árvores de sintaxe. Esta etapa inclui resolução de nome, verificação de tipo e dobra constante</li>
            <li><b>Fluxo/Flow</b>: Executa a análise de fluxo da etapa anterior, incluindo as verificações de atribuições e também os acessos.</li>
            <li><b>Desugar</b> Reescreve as AST e traduz o que se chama de <i>Sintatic Sugar</i>.</li>
            <li><b>Geração</b>: Gera os arquivos do tipo <code>.Class</code></li>    
        </ul>
    </p>
</body>

### Execução
<body style="text-align: justify">
    <p>
        Os arquivos de clase gerados, como falados anteriormente independem do tipo de Máquina (Hardware) ou mesmo do tipo de Sistema Operacional, o que torna Java uma linguagem muito versátil permitindo que um código escrito na linguagem seja executado em praticamente qualquer sistema. 
    </p>
    <p>
        Para executar, é passado para a JVM o arquivo de classe principal, aquele que contém o método main do programa, e em seguida, se passa por três etapas principais, antes que seja executado o código de máquina final. A seguir, listamos estas etapas:
        <ul>
            <li><b>Class Loader</b>: A classe principal é carregada na memória passando o seu arquivo <code>.class</code> e chamando a JVM, e assim, todas as outras classes referencidas também são carregadas. Existem dois carregadores de classes principais que são os primordiais e os não primordiais. Os primordiais está integrado na JVM e é o padrão utilizado normalmente. O não-primordial é um carregador definido pelo programador, que tem a finalidade de fazer o mesmo processo mas de forma personalizada</li>
            <li><b>Verificador de Bytecode</b>: Após o bytecode ser carregado pelo carregador de classe, da etapa anterior, se deve ser inspecionado pelo verificador de bytecode para varredura e verificação das instruções e evitar que haja ações prejudiciais. </li>
            <li><b>Compilador Just-In-Time(JIT)</b>: Basicamente, seu trabalho é converter o bytecode que foi gerado e verificado em código de máquina. Assim o hardware pode executar código nativo e por conta do JIT, se ganha bastante performance em termos de velocidade de execução.</li>
        </ul>
    </p>
</body>

### Nomes, variáveis e vinculação

#### Nomes

<body style="text-align: justify">
    <p>
      Em questão de nomes, no Java temos uma certa convenção para escrita de código. Essas convenções são bastante importantes do ponto de vista de organização, para que o código se mantenha legível e de fácil e rápida manutenção, afinal, em um projeto grande, não só um, como vários programadores irão participar, como dezenas e até mesmo centenas. Assim, para que nenhum programador tenha que adivinhar o que é uma classe ou até mesmo uma constante, em linguagens de programação, por muita influência de suas comunidades e outros fatores, essas convenções são adotadas para manter o código em um padrão para que todos entendam o código e possam também colocar a mão na massa, e no Java não poderia ser diferente.
    </p>
    <p>
      Em java, algumas convenções importantes são adotadas. Elas são listadas a seguir:
      <li><b>Pacotes/Packages</b>: Os nomes dos pacotes devem estar em letra minúscula. Em projetos pequenos, normalmente têm nomes simples, mas em projetos de grandes empresas, normalmente têm nomes mais complexos e subdividos com "." de acordo com o domínio da empresa. Um exemplo pode ser visto a seguir.</li>
      <div align=center><code> package br.minha.empresa; </code></div>
      <li><b>Classes/Class</b>: Classes são nomeadas começando sempre com palavras (normalmente substantivos, pois normalgeralmente representam objetos do mundo real) iniciando com letras maiúsculas a primeira letra de cada palavra. Tentar manter sempre nomes inteiros das palavras e também com boa descrição.</li>
      <div align=center><code> Class Bola {} </code></div>
      <li><b>Interfaces</b>: São nomeadas da mesma forma que se nomeiam as classes</li>
      <div align=center><code> interface iBola </code></div>
      <li><b>Métodos</b>: Devem ser verbos, com a primeira palavra iniciada e mantida com letras minúsculas e com as palavras internas iniciadas com letras maiúsculas.</li>
      <div align=center><code> public void chutarBola(); </code></div>
      <li><b>Variáveis</b>: Como os métodos, devem ser escritas em letras minúsculas e com exceção da primeira palavra, as internas devem começar com letras maiúsculas</li>
      <div align=center><code> int tamanhoDaBola</code></div>
      <li><b>Constantes</b>: As constantes devem ser palavras em upper case, ou seja, toda em maiúsculas, com divisão de palavra com o caractere underline "_"</li>
      <div align=center><code> final static int MAX_TAMANHO_BOLA = 4; </code></div>
    </p>
</body>

#### Variáveis

<body style="text-align: justify">
    <p>
      Na linguagem Java, usamos três tipos de variáveis:
    </p>
    <p>
      <ol>
        <li><b>Variáveis de Classe</b>: São variáveis que pertencem a classe, assim todos os objetos tem acesso a elas, contendo o mesmo valor. São declaradas com o uso da palavra reservada <code>static</code>.</li>
        <li><b>Variáveis de instância</b>: São normalmente às mais usadas, pois estão declaradas dentro das classes, normalmente encapsuladas, tendo seus valores acessados por meio de getters e setters.</li>
        <li><b>Variáveis Locais</b>: São variáveis que estão presente dentro de blocos ou subprogramas, normalmente dentro dos métodos e não visíveis para escopos mais gerais, apenas para o escopo do próbrio subprograma em que foram declaradas.</li>
      </ol>
    </p>
</body>

#### Vinculação (Binding)

<body style="text-align: justify">
    <p>
      Temos dois tipos de vinculação na linguagem Java:
      <div align=center>Vinculação Estática x Vinculação Dinâmica</div>
    </p>
    <p>
      <ul>
        <li><b>Vinculação Estática</b>: Temos esse tipo de vinculação quando a variável é determinada pelo compilador antes do programa ser executado, ou seja, em tempo de compilação. Temos este tipo de vinculação quando há algum método <code>private</code>, <code>static</code> ou <code>final</code>.</li>
        <li><b>Vinculação Dinâmica</b>: Temos esse tipo de vinculação quando a variável é determinada em tempo de execução. Ocorre em situações de código mais livre de encapsulamento, tornando o código mais versátil.</li>
      </ul>
    </p>
</body>

### Escopo, tempo de vida e ambientes de referência.

#### Escopo e tempo de vida

<body style="text-align: justify">
    <p>
      Cada tipo de variável tem seu tipo de escopo e tempo de vida específico:
    </p>
    <p>
      <ol>
        <li><b>Variáveis de Classe</b>: Declarada dentro de uma classe, fora de todos os blocos, conhecida também como variável estática. Seu tempo de vida vai do inicio do programa até o final da sua execução.</li>
        <li><b>Variáveis de instância</b>: Seu escopo é definido dentro de uma classe, mas declarada fora de todos os blocos e subprogramas, conhecida como instância. Seu tempo de vida vai desde quando foi declarada até que o objeto instanciado seja removido da memória.</li>
        <li><b>Variáveis Locais</b>: Seu escopo é definido dentro de um bloco ou subprograma. Seu tempo de vida finaliza quando o bloco ou subprograma seja finalizado. Exemplo é quando um método execute todas as suas instruções.</li>
      </ol>
    </p>
</body>

#### Ambientes de Referência

<body style="text-align: justify">
    <p>
      A linguagem Java é dita de escopo estático e apesar de ter recursos os quais podemos fazer vinculações dinâmicas, suas variáveis são referenciadas dentro de um ambiente estático.
    </p>
</body>

### Paradigmas
Java é uma linguagem multi-paradigma, ou seja, suporta muitos paradigmas. Dentre estes estão a Programação Orientada a objetos, Programação Funcional, Imperativo, Genérico, Reflexivo e concorrente.
O paradigma principal e mais famoso para o desenvolvimento com Java é o paradigma de Programação Orientado a Objetos. Foi com ele que a linguagem ganhou adeptos e fez ser a linguagem tão famosa que é atualmente.

### Propósito

O propósito da Linguagem é ser de escrita simples, de forma legível e com bastante produtividade, seguindo a Orientação a Objetos como principal paradigma de desenvolvimento de software. Durante os anos foi sendo usada em todos os ambientes de software por conta do seu princípio de escrever apenas uma vez o código e executá-lo em praticamente qualquer sistema, o que chamou atenção de vários programadores pelo mundo todo. 

É uma linguagem que tem o foco na construção de softwares de médio a grande porte, em que um time normalmente tem várias pessoas e sempre pode crescer. Além disso, segue a Orientação a Objetos com o intuito de simular o mundo real como abstração para facilitar as resoluções dos problemas.

### Atributos de Qualidade
A linguagem de programação é popular pelo uso do paradigmas de Orientação de Objetos e é bem madura neste aspecto. Permite que o programador tenha um código modularizado, simples, com ótima legibilidade e facilidade de reutilização de código, além de confiabilidade e segurança dos softwares.

Outro ponto bastante importante é que a linguagem é relativamente fácil no que se refere a aprendizagem de sua sintaxe, sendo bastante parecida com outras linguagens, como C++. Também existem uma infinidade de materiais de ensino para a Linguagem, sendo livros, blogs, sites da internet, além de ser bastante difundida academicamente nas Universidades e demais cursos.

Sua comunidade é gigante, sendo uma das linguagens de programação mais usadas no mundo, segundo Stack Overflow. Com isso, pode-se ter uma visão de que vários problemas que um desenvolvedor pode ter com a linguagem na medida que este esteja aprendendo ou mesmo sendo experiente, a probabilidade de alguém ter passado por este erro e feito algum tópico na internet para ser ajudado é imensa, portanto, é muito fácil resolver problemas a partir destes sites que são voltados para essa dinâmica, como o próprio Stack Overflow.

### Ortogonalidade

Ortogonalidade está ligado diretamente à simplicidade da linguagem, e quer dizer basicamente, a facilidade que uma linguagem de programação tem para combinar recursos para construir estruturas de controle e de dados. Em Java podemos ver isso principalmente em:

- Classes podem conter variáveis;
- Funções podem conter variáveis e classes.

Um exemplo muito forte para ver isso é o uso das keywords public e static a um método, eles não interferem um com o outro, portanto, são ortogonais entre si.



### Simplicidade

Java é com certeza uma Linguagem Simples e relativamente fácil de aprender, sendo semelhante à diversas outras linguagens do mercado. Por conta disso ainda possui vários materiais para o iniciante da linguagem se adaptar ao seu estilo.

É baseado no Paradigma de Programação Orientação a Objetos, que nesta linguagem é bastante forte. No Java, com exceção de poucos detalhes, tudo é baseado em objetos. Os programas são compostos por classes, que por sua vez definem categorias de objetos que podem herdar atributos e até mesmo métodos de outras classes, facilitando várias implementações além de permitir o reuso de código, o que promete entregar ao desenvolvedor uma boa legibilidade de código.

Outra simplicidade que Java entrega é em favor do seu ambiente de desenvolvimento, sendo possível programar em quase todos os Sistemas Operacionais, seguindo o princípio "write once, run anywhere", que quer dizer,  escreva uma vez e execute-o em qualquer lugar, ou seja, não é preciso redefinir ou reescrever código, apenas precisa ser recompilado para executar novamente, o que garante uma flexibilidade incrível.

### Sistema de tipagem

Sua tipagem ocorre por duas formas: por referência e por valor.

A passagem por valor vêm dos tipos primitivos da linguagem. Estes são:

+ boolean;
+ byte;
+ char;
+ short;
+ int;
+ long;
+ float;
+ e double.

Essas variáveis podem armazenar apenas um valor de seu tipo declarado por vez, assim, quando outro valor for atribuído a essa variável, seu valor iniciar será substituído.

A tipagem por referência é usada por classes que especificam os tipos de objeto. Podem ser dos tipos: String, Arrays Primitivos e Objetos. Esses Objetos que são referenciados podem ter várias variáveis de instância e métodos dentro desses objetos apontados.

Para ter acesso a um objeto e seus métodos, é preciso ter uma referência do mesmo, dada convencionalmente por uma variável de instância. Todas essas variáveis de referência são inicializadas com o valor nulo "null" que também é uma keyword do Java.



### Ambiente de execução

É importante saber sobre os ambientes de execução das linguagens de programação com o objetivo de resolver alguns problemas que podem ser rotineiros e também, além de tudo, se a linguagem consegue entregar aquilo que se deseja a um projeto que está se iniciando. Nesta parte que estarão definidas as informações sobre o sistema, controle de memória, rede, etc.

No Java, as informações sobre os recursos de Hardware são bem limitadas, pois a linguagem usa como seu alicerce para o funcionamento dos recursos da linguagem a JVM, além de ser uma linguagem de alto nível e multiplataforma, o que dificulta o acesso às bibliotecas do sistema operacional. Apesar de tudo isso, alguns elementos importantes estão disponíveis para serem acessados na sua API, como as propriedades e algumas informações sobre o sistema, controle de memória e também informações de rede.

As propriedades de sistema são pares de nome/valor que fornecem informações sobre o ambiente de execução e dsponibilizam informações diretas do sistema, as quais dizem sobre o Sistema Operacional da máquina, nome de usuário, caminho para as classes de carregamento da linguagem, versão da JVM, etc. Outras informações do sistema também são importantes e entre elas se destacam as informações específicas de operação do sistema e entre estas pode ser conferido se algum gerenciador de segurança está instalado, qual ```class loader``` foi utilizado para carregar a classe, quantas CPUs estão disponíveis, entre outras informações.

Uma das funções mais importantes e de mais destaques da JVM está no gerenciamento de memória. Em linguagens como C/C++ o controle de alocação e desalocação de memória é feito de forma manual pelo próprio programador, o que pode ser uma vantagem por conta da flexibilidade que existe nesse processo, mas em muitos outros cenários, se tornou um problema muito grande, pois não é um trabalho tão "trivial" até para programador experientes, e memória que é alocada e não é desalocada é um problema sério que pode complicar bastante um software. Por conta disso, na criação do Java e da sua JVM, foram criadas maneiras de gerenciar esse processo automaticamente, o que tirou essa flexibilidade, porém se ganhar uma produtividade ordens de grandeza maior pelo fato de não se preocupar mais com tantos detalhes sobre alocação/desalocação de memória. Uma das formas, a qual é mais conhecida, é o "garbage collection" ou coletor de lixo, que acontece quando a aplicação está precisando e solicitando de mais memória, então a JVM faz a verificação se pode atender usando a memória livre já alocada no processo, e caso não tenha essa possibilidade, a JVM realiza uma coleta de lixo, liberando memória utilizada por objetos referenciados como "null". Para fazer o monitoramento e gerenciamento da memória, afim de obter melhores desempenhos das aplicações Java, é interessante estar de olho no uso de memória da aplicação, o que pode ser feito via profiler, como o JProbe ou o OptimizeIt.

Já pra rede, como se necessitam de informações vindas de drivers de baixo nível vindo do Sistema Operacional, o Java, por ser de mais alto nível não tem accesso a tantas informações de rede, pois não é tão seguro o cenário contrário. As duas informações que estariam disponíveis e que realmente importam, são o hostname local e o endereço ip.

### Custos

Falando sobre custos, um software normalmente não tem um parâmetro comum para ser custeado. Tudo vai depender de como vai ser implementado, quantidade de programadores envolvidos no processo de criação, custos com infraestrutura, além do tempo que é o recurso mais precioso no desenvolvimento. Por isso é muito complicado definir um custo para desenvolver um software em Java ou em qualquer outra linguagem.

Mas para o uso da linguagem diretamente, não se paga nada, pois a linguagem é de uso liberado e gratuito, distribuido para qualquer pessoa ou empresa que deseja usar a linguagem para construir seus projetos. 

## Capacidades da Linguagem

### Metaprogramação

A metaprogramação é a capacidade de criar programas que podem representar ou manipular outros programas ou o próprio programa que está sendo executado, assim como o uso de seus dados. 

No Java, existem recursos para isso e o mais famoso é a API Java Reflection, que disponibiliza recursos para reflexão sobre classes e objetos que estão sendo usados na JVM, além de permitir inspecionar e manipular classes, interfaces, atributos, métodos e outros recursos em tempo de execução. Além disso é importante citar que a metaprogramação em Java é bastante importante para a criação de frameworks e que garantiu sucesso de alguns, como por exemplo o Spring, que é bastante usado para a criação de aplicações web.


### Gerenciamento de Ciclo de vida

Em Java o gerenciamento de Ciclo de Vida de Objetos para gerenciar dados de serviços pode reduzir consideravelmente os custos de armazenamento e o tempo que se passaria gerenciando dados manualmente. Este funciona realizando uma ação automatizada com base nas regras que o programador define.

Antes de um objeto ser criado, a classe Java que é responsável pelo instanciamento deste objeto deve ser carregada. Para isso, o Java em Tempo de Execução localiza essa classe e carrega-a em memória. Assim, quando é instanciado algum objeto ou acessado algum método da classe pela primeira vez, esta é carregada na memória também pela primeira vez.

Os objetos são criados a partir da keyword new que chama o construtor da classe do objeto especificado, criando uma referência para o mesmo. O construtor serve apenas para este propósito inclusive, que é criar um objeto e apontar para a variável de referência. Após o objeto ser inicializado e carregado no programa, este pode ter acesso e proporcionar o uso dos seus métodos públicos por outras classes, realizando seu propósito.

Quando não se utiliza-os mais, o próprio Java, mais precisamente, a JVM, se encarrega de maneira automática de removê-lo da memória, a partir do "garbage collection" ou coletor de lixo, "destruindo" os objetos que estão em desuso.

### Segurança

A segurança na linguagem de programação é uma das ênfases dp JDK. No próprio coração da linguagem Java, há um grande suporte de segurança para tipos, além do já citado coletor de lixo automático, que aumenta a robustez do código da aplicação. Outra coisa muito importante a ser citada é a existência de um mecanismo de verificação e carregamento de classes que garante que apenas o código legítimo é executado pela aplicação. Sua arquitetura ainda dispões de APIs, implementações de algoritmos, mecaniosmos e protocolos de segurança comumente usados.

As APIs de segurança são bastante gerais e cobrem uma ampla variedade de casos de uso para várias áreas, além de possuir interfaces de criptografia e de infraestrutura de chave pública que fornecem base para o desenvolvimento de aplicativos seguros. Isso faz com que haja um controle de acesso para a proteção contra acessos que não sejam autorizados.

Alguns dos processos de segurança ocorrem durante a compilação. Todo o bytecode é varrido e há uma verificação da JVM para verificar se esses códigos são legítimos para serem executados no Java Runtime. Assim é verificada a confirmidade do bytecode com as especificações da linguagem, para que não se viole coisas como regras da linguagem ou restrições de namespace. O verificador ainda varre o programa contra violações de gerenciamento de memória, estouro ou insuficiênte de pilha e previsões de tipos de dados ilegais. Depois que o bytecode é verificado, este passa para ser executado pelo runtime.

Além disso o Java permite o controle de acesso a atributos e métodos de classes através de seus modificadores de acesso que podem ser:

+ private: Acesso restrito à própria classe.
+ protected: Acesso restrito ao mesmo pacote.
+ padrão: Quando não é marcado explicitamente. Este só pode ser acessado ou definido dentro do mesmo pacote.
+ public: É o menos restritivo, todas as classes da aplicação tem visibilidade quando este é especificado.


Em termos de arquitetura, o JDK defiine um conjunto de APIs que abrangem as principais áreas de segurança, permitindo que os desenvolvedores integrem facilmente a seguraça do código em desenvolvimento. Essas APIs são projetadas em torno de três principios bastante importantes:

+ Independência de implementação: Neste, quer dizer que os aplicativos não precisam implementar a segurança por eles próprios e sim solicitar os serviços de segurança do próprio JDK.
+ Interoperabilidade de implementação: Quer dizer que um aplicativo não está ligado diretamente a um provedor específico se este não depender dos valores padrão do provedor.
+ Extensibilidade do algoritmo: O JDK inclui provedores integrado, permitindo que um conjunto básico de serviços de segurança sejam usados. Além disso o JDK suporta que outros provedores sejam instalados para que implementem outros serviços afim de customizações quando for preciso.

### Performance

Performance é um dos pontos considerados importantes ao se desenvolver uma aplicação. È bastante relevante pois nenhuma pessoa ou empresa quer desenvolver um software que não seja rápido, pois isso gera um impacto negativo muito forte para a experiência do usuário.

Java históricamente é uma linguagem de desenvolvimento de aplicações que são executadas via Máquina Virtual e não diretamente no processador, como ocorre com C/C++, e por isso as aplicações em Java sempre foram um pouco mais lentas se comparados à essas linguagens. Isso foi uma preocupação muito forte nos anos 90, mas que foi melhorando muito conforme a linguagem foi evoluindo e sendo adotada por uma gama de sistemas, como pode ser visto hoje.

Alguns recursos que ajudaram fortemente a melhoria dos fatores que se referem à desempenho e performance foi a adoção da compilação JIT (Just-in-Time) adotada pela Sun no em 1997, na versão 1.1. Outras coisas como a   adição de alguns recursos na linguagem como por exemplo o suporte á uma melhor análise de código e otimizações na JVM, a execução de bytecode em hardware também foram exploradas com o objetivo de melhoramento do desempenho.

### Escalabilidade

Escalabilidade tem a ver com a crescente do uso de um software, ou seja, do aumento de usuários e da frequência que passam a utilizar a aplicação. Geralmente pode ser feita aumentando o poder de processamento do hardware, adicionando mais recursos aos servidores, como mais RAM, Processadores com mais núcleos, disco, etc. que são úteis em certas ocasiões, mas não necessariamente pode ser barato, e também tem a forma de escalonamento via aumento de máquinas, ou horizontal, que são instância/nós de servidores adicionais, que também são chamados de clusters que trabalham juntos, normalmente feitos em ambientes baseados em nuvem, que geram efeitos positivos como barateamento de custos.

Normalmente Java tem suporte muito bom quanto às adaptações à esses dois tipos de infraestrutura, fornecendo suporte de armazenamento de componentes Java EE como EJBs. Não necessariamente a alta escalabilidade pode ser util ou mesmo um requisito para todos os aplicativos Java, mas é util levar em consideração na construção de um projeto, se este for designado para o público em geral, pois nunca se sabe o quanto de sucesso se obterá para uma dada solução.

Além disso ainda é importante falar que não necessariamente a escalabilidade vai resolver problemas de desempenho que venham ocorrer, e adicionando hardware de maneira infinita, chega um momento que isso se tornará caro e até pior, não irá funcionar, então por isso é sempre importante que haja um planejamento muito minuncioso e maneiras de otimizar o código e seu funcionamento, promovendo segurança nas setializações de dados e sincronizações, utilizando sempre código o mais otimizado e claro possível, mantendo o código sempre legível para manutenibilidade, sempre mantendo o equilíbrio. 

### Confiabilidade

Depois dos tópicos anteriores, é praticamente inegável que Java possui uma confiabilidade incrível, afinal é uma linguagem que alcançou um sucesso muito grande e depois de 30 anos, continua sendo uma linguagem muito utilizada ainda, estando atualmente na versão 17.

É certamente uma linguagem robusta, o que garante confiabilidade, oferecendo o tratamento de exceções que pode resistir aos problemas e condições de erro que venham ocorrer e tudo isso sem interromper o funcionamento da aplicação. Além dessa parte, é uma linguagem que permite a escrita de um código com segurança, portabilidade, com suporte a multithreading e muito mais.

### Concorrência e Threading 

A linguagem tem suporte a multithreading e foi projetada para a programação simultânea, que envolve o uso de multiplos canais do processador, promovendo melhores desempenhos para a aplicação. Contudo isso pode não ser seguro se não for feito de forma responsável, pois requer sincronização dessas instâncias, afinal elas estão gravando dados na mesma memória de maneira simultânea. A linguagem Java possui vários recursos para que haja possibilidade de programar com concorrência.

## Produtividade do Desenvolvedor

Java é uma linguagem que permite uma grande produtividade ao desenvolvedor. Depois de anos várias ferramentas, frameworks e vários outros recursos foram produzidos afim de aumentar a quantidade de desenvolvimento de aplicações em Java e isso foi bastante importante para a sua difusão, e além disso a linguagem ainda apresenta bons recursos que fazem com que isso se solifique ainda mais.
### Frameworks e Contâiners

Frameworks são agrupamentos de código organizados com o objetivo de entregar um esqueleto de uma aplicação para que um desenvolvedor não comece de um absoluto zero, entregando várias ferramentas conjuntas que façam com que a produtividade de uma aplicação cresça exponencialmente tornando muito mais rentável e mais rápido o desenvolvimento.

Frameworks em Java são incontáveis e muito usados para o desenvolvimento. Podemos citar:

+ Spring boot: É um ótimo framework que é muito utilizado para desenvolvimento de aplicações web, sendo o recordista de uso pelos desenvolvedores nos últimos anos.
+ Play: É uma alternativa para o desenvolvimento web, que permite a criação de aplições web modernas com foco em mobile a partir de uma arquitetura stateless.
+ Struts: Solução para aplicações web seguindo o padrão MVC, robusta e de código aberto.
+ Google Web Toolkit: Como o próprio nome sugere, é um framework criado pelo Google de integração de código Java ao lado do cliente com JavaScript, empregrando APIs do google.
+ Quarkus: É um framework que entrega uma facilidade muito grande de criação de APIs RestFull, compatível com infraestruturas nativas baseadas em nuvem, além de ser stack full.
+ Hibernate: Uma solução bastante conhecida, pois é um dos principais frameworks usados para a integração entre o Java e os Sistemas Gerenciadores de Bancos de Dados. Inclusive, vários frameworks incluem o Hibernate dentro deles com o intuito de facilitar o uso de bancos de dados nas aplicações.

O container mais utilizado em Java é o Apache Tomcat com JSP (Java Server Pages). Esse software foi desenvolvido pela Apache e permite a execução de aplicações web usando a linguagem Java.

### Ferramentas Disponíveis

Ferramentas que são importantes de serem citadas são suas IDEs que promovem produtividade para o desenvolvedor, sendo um ambiente que possui a maioria das ferramentas para uma melhor comodidade do desenvolvedor.

Dentre várias podemos citar:

+ Eclipse: Com certeza é a mais usada e famosa quando se fala em Java. Tem diversos recursos, além de ser de uso gratuito e relativamente fácil.
+ Intellij IDEA: IDE criada pela Jet Brains, é uma ótima opção para o uso profissional, oferecendo o melhor da tecnologia Jet Brains. Sua versão completa é paga, porém existe a versão Community que é totalmente gratuita.
+ Netbeans: É um IDE também bastante conhecida para desenvolvimento Java, sendo também gratuita, criado pela Apache.

Temos ferramentas para a criação de testes unitários, muito importantes para o desenvolvimento de software, dentre o qual o JUnit é o mais conhecido e mais utilizado. 

Outra ferramenta que também é bastante utilizada é o MAVEN, que é utilizada para automatizar a compilação de projetos Java. 

JBoss que é um servidor de aplicação de código aberto, uma ferramenta bastante incrível que faz aquilo que um servidor real deveria fazer, mas sem se preocupar com a maioria das coisas que em um cenário de produção viria a acontecer, entregando mais produtividade.

###  Sintaxe, Semântica e Operações Predefinidas

Como já citado antes, Java tem uma sintaxe bem parecida com linguagens como C/C++ e linguagens que derivam das mesmas. A semelhança é muito forte e para quem já teve uma experiência com essas linguagens é muito tranquilo para aprender a estrutura e funcionamento do Java.

Por exemplo, para declarar uma classe, basta apenas definir o modificador de visibilidade (public, private, default ou protected) que são importantes por conta do conceito de encapsulamento, a keyword class, o nome da classe e definir o bloco de código entre chaves. Antes de definir o bloco de código, ainda é possível declarar uma possível herança para alguma superclasse desejada (extends) e implementar interfaces (implements). Ex:

```
public class NomeDaClasse extends SuperClasse implements InterfaceDesejada, UmaSegundaInterfaceDesejada {
  // Código da classe
}
```

Um atributo é definido bem parecidamente. Basta adicionar o modificador, seu tipo e seu nome, com a opção de inicialização com um valor através do sinal de atribuição. Ex:

**Importante citar que todas as instruções devem finalizar com um ponto e vírgula**

```
public class NomeDaClasse {
  // Atributos de uma classe
  public int a;
  public int a = 10;
}
```

Um método também é super parecido. Deve ter um modificador, o tipo retornado, seu nome e entre parênteses deve apresentar seus parâmetros, sendo estes separados por virgula, tendo seus tipos declarados seguidos do seu nome e posteriormente definido o seu bloco de código correspondente.

```
public class NomeDaClasse {
  // Método em uma classe
  public float somaValor(float valor1, float valor2) {
    // Código do método
  }
}
```

Para instanciar uma classe e criar um objeto, temos que declarar o tipo da classe que queremos instanciar, seguido do nome da variável, uma atribuição seguido do operador **new** chamando o construtor da classe que é o nome da classe seguido de parênteses com os valores dos atributos desejados e compatíveis com aquele construtor.

Se temos uma classe produto que contem dois atributos, nome e preco, podemos ter um construtor envolvendo esses dois atributos, por exemplo:

```
public class Produto {
  private String nome;
  private float preco;

  public Produto(String nome, float preco) {
    this.nome = nome;
    this.preco = preco;
  }
}
```

Assim podemos instanciar um objeto desta forma:

```
public class Main {
    public static void main(String[] args) throws IOException {
        Produto produto1 = new Produto("Produto 1", "")
    }
}
```

Falando em objetos e classes, temos por convenção que cada classe fiquem em arquivos separados, assim temos que entender o conceito de pacotes e importações do Java. O conceito de pacote **package** está em dizer onde uma determinada classe está localizada, e o conceito de **imports** também quer dizer a mesma coisa, mas a diferença é que o último serve para localizar classes externas, sendo declarados nas primeiras linhas do arquivo. Assim, poderíamos ter algo da seguinte forma:

```
package src.Main;
import src.Produto;
public class Main {
    public static void main(String[] args) throws IOException {
        Produto produto1 = new Produto("Produto 1", "")
    }
}
```

#### Estruturas de controle

<body style="text-align: justify">
    <p>
      O compilador Java executa o código de cima para baixo. As instruções no código são executadas de acordo com a ordem em que aparecem. No entanto, o Java fornece instruções que podem ser usadas para fazer o controle o fluxo em códigos escritos na linguagem. Essas são chamadas de instruções de fluxo de controle. É um dos recursos fundamentais do Java e também de outras linguagens de programação, que fornece um bom fluxo de programa.
    </p>
    <p>
      O java Fornece três tipos de instruções de fluxo de controle, as quais são:
    </p>
    <ol>
      <li>
        Declarações de tomada de decisão.
        <ul>
          <li>
            Declarações do tipo <code>if/else if/else-if</code>.
          </li>
          <li>
            Declarações do tipo <code>switch/case</code>.
          </li>
        </ul>
      </li>
      <li>
        Instruções de repetição:
        <ul>
          <li>
            Repetições do tipo <code>for</code>. 
          </li>
          <li>
            Repetições do tipo <code>for-each</code>. 
          </li>
          <li>
            Repetições do tipo <code>while</code>. 
          </li>
          <li>
            Repetições do tipo <code>do-while</code>. 
          </li>
        </ul>
      </li>
      <li>
        Declarações de salto (jump).
        <ul>
          <li>
            Declarações do tipo <code>break</code>;
          </li>
          <li>
            Declarações do tipo <code>continue</code>.
          </li>
        </ul>
      </li>
    </ol>
    <p>
      Em Java uma instrução do tipo if é chamada de condicional, ou seja, seu uso é para avaliar expressões lógicas. Essa expressão lógica retorna verdadeiro ou falso e com isso há o desvio de fluxo dependendo do resultado da expressão. Existem quatro tipos dessas expressões:
      <ol>
        <li>
          Declaração <code>if</code> simples, na qual o <code>if</code> recebe uma expressão entre parenteses e caso a expressão seja verdadeira ele executa um bloco de código que é declarado logo após os parênteses.
        </li>
        <li>
          Declaração <code>if/else</code>, na qual existe um <code>else</code> logo após o <code>if</code> que executará um bloco de código caso a expressão que o <code>if</code> testou seja falsa.
        </li>
        <li>
          Declaração <code>if/else-if</code>, na qual existem várias condições aninhadas, as quais existe primeiramente um <code>if</code> e logo após condições <code>else if</code> também recebendo outras expressões entre parênteses e executando blocos de código para cada uma dessas outras expressões booleanas e podendo serem terminadas com <code>else</code> caso todas as outras expressões anteriores forem falsas.
        </li>
        <li>
          Declaração <code>if</code> aninhada é basicamente um conjunto de expressões <code>if</code>, na qual existe um <code>if</code> que contem dentro do seu bloco de código outros <code>if</code> ou <code>if-else</code> aninhados.
        </li>
      </ol>
    </p>
    <p>
      Em Java as instruções do tipo switch são super parecidas com às instruções do tipo if-else-if. Essas instruções contém vários blocos de código chamados cases, e um único case é executado com base na variável que está sendo alternada. A instrução switch tem uma certa vantagem em ser usada ao invés dos if's aninhados por conta da legibilidade que entrega.
    </p>
    <p>
      Pontos que devem ser levados em consideração ao usar switch:
    </p>
    <ul>
      <li>
        As condições de case podem ser de tipos primitivos ou enumaration e também, a partir do Java 7 podem ser usadas as Strings.
      </li>
      <li>
        Cases não podem ser duplicados.
      </li>
      <li>
        A instrução default é chamada quando nenhum dos casos corresponde à condição, semelhanto ao else e também é opcional.
      </li>
      <li>
        A instrução break finaliza um bloco de código quando a condição é satisfeita. Também é opcional e o próximo caso é executado.
      </li>
      <li>
        Obviamente ao usar esse tipo de estrutura, a condição case deve ser do mesmo tipo que a váriável usada na expressão switch.
      </li>
    </ul>
    <p>
      Falando agora sobre loop, no Java precisamos também considerar casos onde precisamos executar certos blocos de código mais de uma vez, então usamos estruturas de controle que chamamos de estruturas de repetição. Para executar esses loops, precisamos também de certas condições, para que haja uma entrada nessas repetições e também para que haja uma parada, pois um loop infinito nunca é um caso desejado para os programadores.
    </p>
    <p>
      Em java temos três tipos de loops que são executados de forma bastante semelhante, apesar da sintaxe de cada um se diferenciar um do outro. Essas formas são:
    </p>
    <ul>
      <li>
        O loop for.
      </li>
      <li>
        O loop for-each.
      </li>
      <li>
        O loop while.
      </li>
      <li>
        O loop do-while.
      </li>
    </ul>
    <p>
      O loop for é utilizado quando se há um loop controlado de certa forma que conhecemos o ponto de entrada no loop e o ponto de parada, ou seja, conhecemos quando vamos entrar e quando vamos sair do código. Este loop tem a sintaxe do tipo:
      <code>for(condicaoDeInicio; condicaoDeParada; controleIncrementoOuDecremento) {// bloco de código associado.}</code>
    </p>
    <p>
      O loop for-each é utilizado quando se deeja um loop iterável para atravessar estruturas de dados mais complexas como arrays ou collections. Neste tipo de loop não há necessidade de haver uma variável iteirável para ser um contador de loop para ser atualizada. O for-each então chega na estrura e executa seu bloco de código para cada um dos elementos dessas estruturas e fornece com isso uma segurança de que não irá dar erro por conta de alguma variável tentando ser acessada mas que na verdade não existe.
      <code>for(TipoDaEsrutura elemento: nomeDaEsrutura){// bloco de código associado.}</code>
    </p>
    <p>
      No loop While, as instruções são repetidas várias vezes, sem haver um controle tão rigoroso com nos loops anteriores. Esses loops são ideais quando não se sabe exatamente quantas iterações deverão ter para satisfazer as condições. Este loop ele carrega também uma expressão booleana que quando não satisfeita o loop para. Então também caso não seja tão rigorosamente controlado poderá gerar erros. A sintaxe é a seguinte:
      <code>while(condicao){// bloco de código associado.}</code>
    </p>
    <p>
      No loop do-While, é semelhante filosoficamente com o anterior, porem o bloco de código é executado pelo menos uma vez para depois verificar a condição. Ou seja, é para ser executado quando a quantidade de execuções não é definida e precisamos executar o bloco de código pelo menos uma vez. A sintaxe é a seguinte:
      <code>do{// bloco de código associado.} while(condicao);</code>
    </p>
    <p>
      Por fim, temos as declarações de Jump (saltos) que são usadas para transferir controle do programa para instruções específicas. Essas instruções basicamente transferem o controle e fluxo para outras partes do programa e existem duas delas bem conhecidas na linguagem Java que são:
    </p>
    <ul>
      <li>
        O salto break.
      </li>
      <li>
        O salto continue.
      </li>
    </ul>
    <p>
      O break basicamente serve para parar a execução de um fluxo atual e transferir o controle para uma próxima instrução que está fora daquele contexto ou bloco que está inserido, sempre dentro de uma estrutura switch ou mesmo dentro de uma das estruturas de repetição.
    </p>
    <p>
      O salto continue ao contrário do break, não desvia a instrução para fora da estrutura de repetição ou switch, ele apenas interrompe aquela parte específica e pula para a próxima iteração de forma imediata.
    </p>

</body>

##### Estruturas e tipos de dados

Em Java, temos duas divisões principais envolvendo os tipos de dados. Temos os tipos primitivos e os tipos complexos.

Os tipos primitivos são aqueles que normalmente vêm em todas as linguagens. Estes são int, float, double, boolean, char, byte, short e long. Existem alguns outros tipos que também são bastante usados para a definição de variáveis, que são os arrays primitivos das linguagens, ou seja, definidos a partir de uma das keywords que foram apresentadas para os tipos primitivos e ainda o tipo String, que não é um tipo primitivo necessariamente, mas vem com a linguagem, com intuito de facilitar a vida do programador, sendo uma estrutura de dados completa para o tratamento do tipo string, que é uma cadeia de caracteres.

Temos também os tipos complexos, ou tipos por referência, que são aqueles que através de variáveis de tipos por referência, armazenam as localizações de objetos na memória. Esses objetos referênciados podem ter várias variáveis de intância e métodos dentro do objeto apontado. Para conseguir acessá-los, é preciso ter uma referência a algum deles, e suas referências inicialmente são inicializadas como null.

O Java fornece uma facilidade imensa para a criação de estruturas de dados complexas a partir das suas vinculações e composições de classes. Além disso fornece uma gama de estruturas já prontas para uso, facilitando bastante a vida do programador. Algumas delas são:

- String que pode ser usado para "tipar" uma variável.
- Collection que é um conjunto de interface e classes que funciona para representar e tratar um grupo de dados como uma única unidade. Com ele se pode usar coisas como um ArrayList que basicamente é um tipo de array para listar objetos ou até mesmo até outros arrays. Dentro desta ramificação temos ainda Set, Queue, Map, LinkedList, PriorityQueues e outros.

## Ecossistema

### Maturidade

Como ja falado, é uma linguagem bastante antiga e que possui uma maturidade excelente, que ao longo dos anos foi sendo sempre atualizada afim de corrigir erros e também não ficar para trás perante às linguagens que foram surgindo.

### Comunidade

Como o tópico anterior, podemos brevemente falar que com todas as qualidades que Java mostrou durante o tempo, foi adotada por milhões de desenvolvedores o que por consequência formou uma comunidade muito grande e uma quantidade incrível de materiais de aprendizagem que estão disponibilizados pela internet, além de fóruns, github, etc. Além disso é uma linguagem que é bastante empregada na academia.

### Governança

Java é uma linguagem que atualmente é mantida pela Oracle Corporation, atualmente na versão 17 (estável).

## Informações Adicionais
## Referências 

1. https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html
2. https://www.learningjournal.guru/article/programming-in-java/scope-and-lifetime-of-a-variable/
3. https://www.geeksforgeeks.org/compilation-execution-java-program/
4. https://www.javatpoint.com/static-binding-and-dynamic-binding
5. https://elixir-lang.readthedocs.io/en/latest/technical/scoping.html
6. https://www.javatpoint.com/control-flow-in-java
7.  https://computerworld.com.br/plataformas/java-completa-20-anos-e-conquista-adeptos-pela-simplicidade/
8.  https://www.daniweb.com/programming/software-development/threads/301991/orthogonality-in-java
9.  https://www.alura.com.br/conteudo/estrutura-de-dados
10. https://www.researchgate.net/publication/220378102_The_Java_5_Generics_Compromise_Orthogonality_to_Keep_Compatibility
11. https://www.devmedia.com.br/java-collections-como-utilizar-collections/18450
12. https://docs.oracle.com/javase/9/security/java-security-overview1.htm#JSSEC-GUID-2EF91196-D468-4D0F-8FDC-DA2BEA165D10
13. https://www.infoq.com/br/news/2009/05/8-Best-Practices-Scalability/
14. https://www.dynatrace.com/resources/ebooks/javabook/performance-and-scalability/
15. http://highscalability.com/
16. https://www.techopedia.com/2/28705/development/programming-languages/why-is-java-preferred-to-other-languages-in-building-technological-blocks#:~:text=Unlike%20them%2C%20Java%20is%20not,with%20other%20frameworks%20and%20technologies.
17. https://www.vogella.com/tutorials/JavaConcurrency/article.html
18. http://tutorials.jenkov.com/java-concurrency/index.html
19. http://tutorials.jenkov.com/java-concurrency/index.html#what-is-multithreading
20. https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-a-Java-framework
24. https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-quarkus
25. https://www.codigofonte.com.br/artigos/os-dez-melhores-frameworks-java-do-mercado
26. https://www.devmedia.com.br/introducao-a-servlets-em-java/25285
27. https://www.devmedia.com.br/conheca-o-apache-tomcat/4546
28. https://www.guj.com.br/t/o-que-e-ciclo-de-vida/46122
29. https://faqcartx.info/programa%C3%A7%C3%A3o/41126-qual-%C3%A9-o-ciclo-de-vida-de-um-objeto-em-java.html
30. https://javaee.github.io/tutorial/overview005.html
31. http://www.dsc.ufcg.edu.br/~jacques/cursos/j2ee/html/servlets/intro.htm
32. https://www.guj.com.br/t/diferenca-entre-jboss-e-tomcat/88525
33. https://medium.com/@michellibrito/entendendo-o-que-%C3%A9-um-servidor-de-aplica%C3%A7%C3%A3o-e-um-servlet-container-na-programa%C3%A7%C3%A3o-java-para-web-d2146a4958ea
34. https://www.devmedia.com.br/principais-ferramentas-de-apoio-ao-desenvolvimento-java/34126
35. https://4linux.com.br/o-que-e-jboss/
36. https://www.devmedia.com.br/jboss-instalacao-arquitetura-configuracao-tuning-e-administracao/10118
37. https://www.jetbrains.com/pt-br/idea/
38. https://netbeans.apache.org/download/index.html
