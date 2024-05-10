
Todo computador precisa lidar com informações, porem apenas organizar de qualquer maneira irá gerar listas confusas que dificultam a procura por dados específicos e tornam o computador lento. Algumas técnicas básicas podem aumentar a eficiência por rodada de execução de um algoritmo e no mundo da TI alguns milissegundos podem ser a diferença entre estar em uma empresa de sucesso ou em um navio afundando.

# Básico estrutura de dados
A memória do computador é uma fita enorme de binários que contem dados de todas as aplicações que estão rodando nele. pense que para manter estes dados organizados é necessário manter uma lista atualizada que especifica em qual posição um dado esta guardado nesta fita, qual seu tamanho,o seu valor, a qual aplicação pertence entre outros detalhes.

Uma das maneiras que desenvolvedores utilizam para manter os dados organizados em linguagens de baixo nível como C/C++ é com um conjunto de dados chamado de ponteiro, o ponteiro indica para o computador qual pedaço de memória estamos nos referindo ao usar uma variável e qual o seu valor, muitas vezes em uma sintaxe similar a uma lista/array.

Não há necessidades de se perder o sono com questões de seguranças com ponteiros, porem é importante lembrar como eles funcionam pois dados complexos como classes e listas muitas vezes para evitar a duplicação de dados na memória é apenas repassado o endereço do ponteiro para essa classe em memória quando criamos uma nova variável.

> Normalmente o sistema operacional do computador lidar com o gerenciamento de memória, com o programa apenas pedindo acesso para um pedaço na fita para o computador com um tamanho especifico para o dado que precisa ser guardado.
>
> Em situações especiais o computador pode acidentalmente indicar um espaço maior que o tamanho real de uma variável ou armazenando um valor que acaba sendo interpretado como um ponteiro, permitindo acessar dados de outras aplicações.
>
> Este tipo de ataque se chama estouro de fita, ou para aqueles que utilizam nomenclaturas inglesas: a fita de dados se chama um buffer, portanto buffer overflow.
> 
> Neste link será mostrado um exemplo deste tipo de ataque, recomendado entendimento dos conceitos básicos. A ideia é ensinar conceitos básicos de segurança, mas para iniciantes é melhor manter estes conceitos no fundo da cabeça.
> https://www.youtube.com/watch?v=qpyRz5lkRjE

## Listas, Vetores e Matrizes.

No computador é comum possuirmos variáveis na memória, muitas vezes para se criar um programa a ideia de ter uma unica variável para guardar valores importantes é uma ótima solução, porem em certas situações é necessários guardar mais de um desses valores e criar uma variável para cada é custoso para o desenvolvedor.

A solução deste problema é a invenção de listas, vou utilizar uma linguagem de baixo nivel pois linguagens como JavaSript abstraem certas operações e as vezes ocultam os tipos de dados que estão sendo usados.

Normalmente para criar uma lista fazer
```cpp
int listaNumeros[5]; // cria uma lista de numeros vazia com 5 espaços.
// equivalente a: [X,X,X,X,X]
// importante lembrar que os endereços de uma lista são acessados começando pelo 0:
// listaNumeros[0] - primeira posição
// listaNumeros[4] - ultima posição
```

**Matrizes** são duas listas de dados para representar um mapa de dados, muitas vezes um gráfico cartesiano. uma lista para a posição X e a outra para Y.

```cpp
float matriz[2][3]; // cria uma matriz de 2 por 3.
// equivalente a: 
// [ 
//   [ [X], [X], [X] ],
//   [ [X], [X], [X] ]
// ]
// onde a primeira entrada indica uma lista e a segunda uma célula com dado.
```

## Registros.

Registros são coleções de variáveis que permite guardar informações de diferentes tipos incluindo dados de tipagem customizada ou criada pelo desenvolvedor. 

Na linguagem C/C++ a declaração de um registro é dada pela palavra reservada **struct**, Veja em seguida um exemplo de um registro que abstrai o conceito de uma fração e a representa em termos computacionais:

```cpp
// aqui temos uma fração comum.
struct fracao {
int numerador;
int denominador;
float valorReal;
}
```

## Ponteiros

Ponteiros são um tipo de dado diferente dos outros: ele permite utilizarmos vários tipos de dados em uma mesma lista alem de aumentar a eficiência do uso da memória no computador.

A maneira como funcionam é que todo dado na fita de memória para ser atribuído a outra variável este dado precisa ser duplicado: um dado, uma variável.

Ponteiros são essencialmente atalhos para certos pontos na memória do computador, ao invés de duplicar os dados apenas duplicamos o endereço que aponta para onde o dado real está localizado na fita, normalmente um ponteiro é representado por uma lista com dois componentes: 
- Endereço na memória
- Valor guardado
porem lembre-se que este ponteiro está abstraindo o ponteiro verdadeiro que é apenas um numero.

Ponteiros são uteis com grandes endereços de memórias como listas,objetos de classes, registros e até mesmo números.

Em linguagens como C/C++ normalmente um ponteiro é extraído usando ``*`` ao lado da variável para indicar ser um ponteiro e ``&`` do lado da variável que queremos o ponteiro:
```cpp
int numeroInteiro = 10;               // declaramos uma variavel e seu valor.
int *ponteiroNumero = &numeroInteiro; // pegamos o ponteiro da variavel original 
```

> 
> Números inteiros dedicam uma quantidade enorme de memória para si, por padrão em linguagens de alto nível é comum toda vez que for criado um numero inteiro a linguagem apenas assumir que esta criando um numero de 32 bits.
> 
> ![[Pasted image 20240430165802.png]]
>
>É sempre possível especificar um tipo de numero menor e isso auxilia no uso de memória de uma aplicação, mas muitas vezes isso acaba sendo um detalhe minimo e que deve ser levado a sério apenas em uma futura etapa de melhoria.
>



# Pilhas e Filas

Uma das maneiras comuns de utilizar dados é guardando eles em filas ou pilhas, permitindo um conjunto ordenado de dados, sim existem diferenças entre os dois.

## Pilhas

A pilha é uma estrutura simples, se trata de uma fila onde itens entram e saem porem apenas o item mais recente se torna acessível.

Imagine uma casa sendo construída: cada tijolo colocado irá receber outro tijolo em cima, caso queiramos retirar o tijolo da base teremos que retirar todos os que estão em cima. a mesma ideia se aplica para a pilha de onde os tijolos estão sendo retirados.

Na computação a pilha é uma estrutura em que dados são inseridos e removidos no seu topo formando uma estrutura do tipo **Last In, First Out** (LIFO).

Nesse exemplo visual temos uma pequena pilha de tamanho 10 com 4 itens na lista.
![[Pasted image 20240430192036.png]]

Caso queiramos adicionar dois novos números nesta lista temos apenas uma posição: o fim.
![[Pasted image 20240430192227.png]]

Agora imagine que precisamos remover um valor desta pilha, podemos apenas remover inicialmente o valor 2 e precisaremos remover todos os outros números caso queiramos remover o valor 1.

### Estrutura de uma pilha

Para construir uma pilha dentro do computador precisamos apenas de 3 tipos de dados básicos: 
- Uma lista -> para armazenar os dados
- dois números inteiros 
	- Um para armazenar o tamanho da lista.
	- Um para armazenar quantidade de itens na lista.

O livro entra em detalhes específicos de como a pilha funciona, similar a explicar detalhadamente que um valor booleano falso equivale a não verdadeiro. Porem por ser o primeiro tipo de dado abstrato (diferente dos dados primitivos como listas,inteiros e strings) o código a seguir é de uma pilha em C++, utilizando um compilador deixo á curiosidade do leitor testar esta classe.

caso não queira compilar na mão, utilize um compilador online como OnlineGDB : https://www.onlinegdb.com/online_c++_compiler

Nesta atividade usei uma classe, classes são estruturas que permitem a criação de um tipo de dado composto, similar a um registro, porem classes permitem restringir o acesso á variáveis internas.

```cpp
// W.I.P
```


## Filas

As filas são estruturas de dados com um funcionamento mais complexo que uma pilha, porem devido a isso podem atuar de maneiras mais precisas.

> As duas estruturas possuem diferenças em uma linguagem de baixo nível como C++, porem para linguagens de alto nível como Python ou PHP, que possuem tipagem fraca, uma fila e uma pilha se tornam a mesma estrutura: uma lista.
>
> Para uma linguagem de alto nível essas estruturas deixam de ser relevante e o que importa é a estratégia de seu funcionamento.

Imagine um banco com uma fila de clientes, para ser atendido um cidadão honesto se dirige para o final da fila esperando um dos caixas chama-lo. Quando um dos caixas ficar livre o primeiro cidadão na fila será atendido.

Filas funcionam com o conceito de First In, First Out (FIFO).

### Funcionamento de uma Fila

# Listas Dinâmicas