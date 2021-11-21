<!-- Caracterização da Linguagem L1 - Java - Álvaro Souza Oliveira -->


# Linguagem 1 - Java
## Caracterização

### Aspectos Gerais
Java é uma linguagem de programação que segue principalmente o paradigma de Orientação a Objetos, criada na década de 90, criada pela **Sun Microsystens**, em um projeto chamado **Green Project**, chefiado por **James Gosling**. Em 2008, a Sun é vendida e o Java passa a ser posse da **Oracle Corporation**. Surge como uma ferramenta que seguia a ideia de ser executada em todo e qualquer eletrônico possível, e para isso houve um árduo projeto para a criação dessa possibilidade, já que nesta época existia o problema de incompatibilidade envolvendo a execução de código em diferentes tipos de máquina por conta da arquitetura usada nos computadores, sistema operacional e vários outros problemas técnicos que faziam com que um mesmo código escrito em uma linguagem com compilação tradicional não funcionasse para todos os tipos de computadores da época. Então Java é criada usando o conceito de execução de código por uma Virtual Machine, a famosa JVM, que faz a compilação do seu código para um bytecode e após isso é gerado um código de máquina compatível com as propriedades da máquina em uso, o que faz com que um mesmo código escrito seja executado em Windows ou Linux por exemplo.
### Atributos de Qualidade
A linguagem de programação é popular pelo uso do paradigmas de Orientação de Objetos e é bem madura neste aspecto. Permite que o programador tenha um código modularizado, simples, com ótima legibilidade e facilidade de reutilização de código, além de confiabilidade e segurança dos softwares.

Outro ponto bastante importante é que a linguagem é relativamente fácil no que se refere a aprendizagem de sua sintaxe, sendo bastante parecida com outras linguagens, como C++. Também existem uma infinidade de materiais de ensino para a Linguagem, sendo livros, blogs, sites da internet, além de ser bastante difundida academicamente nas Universidades e demais cursos.

Sua comunidade é gigante, sendo uma das linguagens de programação mais usadas no mundo, segundo Stack Overflow. Com isso, pode-se ter uma visão de que vários problemas que um desenvolvedor pode ter com a linguagem na medida que este esteja aprendendo ou mesmo sendo experiente, a probabilidade de alguém ter passado por este erro e feito algum tópico na internet para ser ajudado é imensa, portanto, é muito fácil resolver problemas a partir destes sites que são voltados para essa dinâmica, como o próprio Stack Overflow.
#### Legibilidade

##### Simplicidade

Java é com certeza uma Linguagem Simples e relativamente fácil de aprender, sendo semelhante à diversas outras linguagens do mercado. Por conta disso ainda possui vários materiais para o iniciante da linguagem se adaptar ao seu estilo.

É baseado no Paradigma de Programação Orientação a Objetos, que nesta linguagem é bastante forte. No Java, com exceção de poucos detalhes, tudo é baseado em objetos. Os programas são compostos por classes, que por sua vez definem categorias de objetos que podem herdar atributos e até mesmo métodos de outras classes, facilitando várias implementações além de permitir o reuso de código, o que promete entregar ao desenvolvedor uma boa legibilidade de código.

Outra simplicidade que Java entrega é em favor do seu ambiente de desenvolvimento, sendo possível programar em quase todos os Sistemas Operacionais, seguindo o princípio "write once, run anywhere", que quer dizer,  escreva uma vez e execute-o em qualquer lugar, ou seja, não é preciso redefinir ou reescrever código, apenas precisa ser recompilado para executar novamente, o que garante uma flexibilidade incrível.

##### Ortogonalidade

Ortogonalidade está ligado diretamente à simplicidade da linguagem, e quer dizer basicamente, a facilidade que uma linguagem de programação tem para combinar recursos para construir estruturas de controle e de dados. Em Java podemos ver isso principalmente em:

- Classes podem conter variáveis;
- Funções podem conter variáveis e classes.

Um exemplo muito forte para ver isso é o uso das keywords public e static a um método, eles não interferem um com o outro, portanto, são ortogonais entre si.

##### Estruturas de controle

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
            Declarações do tipo <code>if/else if/else</code>.
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

O Java fornece uma facilidade imensa para a criação de estruturas de dados complexas a partir das suas vinculações e composições de classes. Além disso fornece uma gama de estruturas já prontas para uso, facilitando bastante a vida do programador. Estas são:

- String que pode ser usado para "tipar" uma variável.
- Collection que é um conjunto de interface e classes que funciona para representar e tratar um grupo de dados como uma única unidade. Com ele se pode usar coisas como um ArrayList que basicamente é um tipo de array para listar objetos ou até mesmo até outros arrays. Dentro desta ramificação temos ainda Set, Queue, Map, LinkedList, PriorityQueues e outros.

##### Aspectos sintáricos

Fatores:
- Simplicidade
- Ortogonalidade
- Estruturas de controle
- Estruturas e tipos de dados
- Aspectos sintáticos
- Boa definição
- Convenção de escrita de código

#### Redigibilidade

Fatores:
+ Suporte a abstração
+ Poder de expressão

#### Confiabilidade

Fatores:
+ Sistema de tipos
+ Tratamento de exceções

#### Custo

Fatores:
+ Treinamento
+ Ferramentas

#### Reutilização de Código
+ Reusabilidade

#### Produtividade
+ Principais Frameworks e Bibliotecas
+ Principais Ferramentas utilizadas para produção

