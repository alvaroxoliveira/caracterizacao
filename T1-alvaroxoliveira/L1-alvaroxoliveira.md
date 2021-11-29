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

![Contribution guidelines for this project](T1-alvaroxoliveira/Linguagens.drawio.png)
  
Java é uma linguagem de programação que segue principalmente o paradigma de Orientação a Objetos, criada na década de 90, criada pela **Sun Microsystens**, em um projeto chamado **Green Project**, chefiado por **James Gosling**. Em 2008, a Sun é vendida e o Java passa a ser posse da **Oracle Corporation**.
Surge como uma ferramenta que seguia a ideia de ser executada em todo e qualquer sistema possível, e para isso houve um árduo projeto para a criação dessa possibilidade, já que nesta época existia o problema de incompatibilidade envolvendo a execução de código em diferentes tipos de máquina por conta da arquitetura usada nos computadores, sistema operacional e vários outros problemas técnicos que faziam com que um mesmo código escrito em uma linguagem com compilação tradicional não funcionasse para todos os tipos de computadores da época. Então Java é criada usando o conceito de execução de código por uma Virtual Machine, a famosa JVM, que faz a compilação do seu código para um bytecode e após isso é gerado um código de máquina compatível com as propriedades da máquina em uso, o que faz com que um mesmo código escrito seja executado em Windows ou Linux por exemplo.

_Breve texto de apresentação._
_Comentar sobre perspectivas / papéis._
_Colocar uma figura / árvore, com pais e filhos_.

## Características da Linguagem
### Paradigmas
Java é uma linguagem multi-paradigma, ou seja, suporta muitos paradigmas. Dentre estes estão a Programação Orientada a objetos, Programação Funcional, Imperativo, Genérico, Reflexivo e concorrente.
O paradigma principal e mais famoso para o desenvolvimento com Java é o paradigma de Programação Orientado a Objetos. Foi com ele que a linguagem ganhou adeptos e fez ser a linguagem tão famosa que é atualmente.

### Propósito

O propósito da Linguagem é ser de escrita simples, de forma legível e com bastante produtividade, seguindo a Orientação a Objetos como principal paradigma de desenvolvimento de software. Durante os anos foi sendo usada em todos os ambientes de software por conta do seu princípio de escrever apenas uma vez o código e executá-lo em praticamente qualquer sistema, o que chamou atenção de vários programadores pelo mundo todo. 

É uma linguagem que tem o foco na construção de softwares de médio a grande porte, em que um time normalmente tem várias pessoas e sempre pode crescer. Além disso, segue a Orientação a Objetos com o intuito de simular o mundo real como abstração para facilitar as resoluções dos problemas.

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


