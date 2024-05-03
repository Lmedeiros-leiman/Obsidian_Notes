O obsidiam não deixa colocar # 😡
https://learn.microsoft.com/pt-br/dotnet/csharp/?WT.mc_id=dotnet-35129-website

O C afiado (C Sharp ou C#, também [Ce]Cerquilha) é uma linguagem de programação moderna, não por ser ter sido inventada em 2020+ mas por ainda estar sendo mantida e atualizada e possui múltiplos anos de horas de códigos colocadas na sua história: Desde livrarias escritas em C ou até mesmo Fortran dependendo da aplicação. 

C# se mantem relevante por meio de livrarias que expandem sua abstração: considere que C/C++ é a versão mais próxima da linguagem assembly enquanto C# está mais próxima de Python. Uma das livrarias mais utilizadas para C# é a .NET que permite a criação de aplicativos desktop E web enquanto mantem suporte para múltiplas plataformas.

O código-fonte escrito em C# é diferente de C++: ao invés de ser compilado diretamente em binário transformamos o código em uma linguagem intermediária (IL) junto com outros arquivos importantes em um arquivo .DLL.

> Alem de permitir rodar em maquinários com arquiteturas diferentes de onde o software foi produzido, contato que seja dentro do windows, a utilização da IL permite integrar códigos de diferentes linguagens dentro de um mesmo projeto, como f#, visual basic, C++ e qualquer outra linguagem suportada pelo .NET.

## Estilo da linguagem

C# é uma linguagem compilada de tipagem forte altamente abstraída orientada a objetos: Isso significa que muitas funcionalidades já existem e o desenvolvedor apenas precisa chamar a classe especifica para aquela função.
No exemplo abaixo temos um simples programa "Olá mundo.":

```cs
using System;

class Hello
{
    static void Main()
    {
        Console.WriteLine("Hello, World");
    }
}
```

Perceba que primeiros chamamos o namespace System que possui a classe Console que utiliza do método WriteLine para apresentar uma string no terminal: existe uma grande complexidade sendo simplificada e mostrada para o desenvolvedor e esse é o diferencial de C# para linguagens como Python.

Todo programa em C# possui uma estrutura especifica que auxilia com o desenvolvimento, para iniciantes todas estas regras podem tornar C uma linguagem complicada, mas para grandes projetos essas funcionalidades permitem a fácil expansão da base de código.

vamos começar pelo básico:

### Tipos e variáveis

Em C# uma variável é um rotulo que se refere a uma instancia de um tipo especifico de dado, seja por um tipo de referencia ou por um tipo de valor. Enquanto variáveis de valor possuem o seu valor variáveis de referencias possuem um ponteiro para um objeto, em alguns casos o mesmo objeto.

Toda variável é declarada primeiro constatando seu identificador e então seu nome, podendo ou não declarar o seu valor.

C# permite a criação de identificadores personalizados usando declarações especificas:
* **Class**: define uma estrutura de dados que contem membros de dados e funções (nomeados de propriedades,métodos e outros...) os tipos de classe dão suporte à herança e ao polimorfismo dessas funções, permitindo estender para outras classes.
* **Struct**: similar ao tipo de classe também representa uma declaração especifica que pode possuir tanto dados quanto funções, porem structs não precisam de alocação de heap e a estrutura não suporta herança. todos os tipos structs são herdados implicitamente do tipo `object`. 
* **Interface**: essa estrutura define uma interface para uma estrutura `class` ou `struct` permitindo facilitar o uso por parte de um desenvolvedor. Uma classe ou struct pode possuir multiplas interfaces porem uma interface pode herdar apenas uma classe ou struct.
* **Delegate**: Um tipo delegate representa referências aos métodos com uma lista de parâmetros e tipo de retorno específicos. Delegados possibilitam o tratamento de métodos como entidades que podem ser atribuídos a variáveis e passadas como parâmetros. Os delegados são análogos aos tipos de função fornecidos pelas linguagens funcionais. Eles também são semelhantes ao conceito de ponteiros de função encontrado em algumas outras linguagens. Ao contrário dos ponteiros de função, os delegados são orientados a objetos e fortemente tipados.

Os tipos `class`,`struct`,`interface` e `delegate` dão suporte a tipos genéricos e podem ser parametrizados com outros tipos.

C# dá suporte a matrizes unidimensionais e multidimensionais de qualquer tipo de dado não precisando declarar antes de utilizar mas utilizando `[]` após a declaração para indicar ser uma lista: 
```cs
int[]; // lista de inteiros
int[,] // lista de inteiros com duas coordenadas. 
int[][] // lista de listas de inteiros.
// Primeiro caso é uma lista unidimencional
// Segundo caso é uma matriz bidimensional
// terceiro caso é uma matriz unidimensional de matrizes unidimensionais.
```

Toda variavel pode ser anulavel utilizando `?` com seu tipo, porem uma estrutura pode especificar que seus membros não aceitam valores nulos:
```cs
int?; // um numero inteiro que pode ser nulo.
int;  // um numero inteiro que NÃO pode ser nulo.
```



### Estrutura do programa

Os principais conceitos para se organizar um programa em C# vão de: 
Programas -> namespaces -> tipos -> membros -> assemblies

Programas declaram tipos que contem membros e podem ser organizados em namespaces. classes, structs e interfaces são exemplos de  tipos com os campos, métodos, propriedades e eventos sendo exemplos de membros. Ao compilar um programa em C# eles são empacotados dentro de um arquivo assemblie que tem uma extensão ```.exe``` para executáveis ou aplicação enquanto ```.dll``` para livrarias/bibliotecas.

Considere a classe a seguir para melhor entender como a separação dos elementos em classificações menores funciona:

```cs
namespace Acme.Collections; 

public class Stack<T> { 
	Entry _top; 
		
		public void Push(T data) 
		{ 
		_top = new Entry(_top, data); 
		} 
		
		public T Pop() { 
		if (_top == null) { 
			throw new InvalidOperationException(); 
			} 
		T result = _top.Data; _top = _top.Next; return result; 
	} 
			
	class Entry { 
		
		public Entry Next { get; set; } 
		public T Data 
		{ 
			get; 
			set; 
		} 
		public Entry(Entry next, T data) 
		{ 
			Next = next; Data = data; 
		} 
	} 
}

```

Essa é uma classe Stack, ela define uma abstração para representar uma pilha de dados.
O nome completo para encontrar essa abstração dentro do programa é **Acme.Collections.Stack**. essa classe possui vários membros entre eles:
- Um campo _top
- Dois métodos
	- Push
	- Pop
* Uma classe aninhada chamada Entry que por si possui 3 membros:
	* um campo chamado Next
	* Um campo chamado Data
	* Um construtor.

Stack é uma classe genérica com um parametro de tipo `T` que é substituido por um tipo concreto quando aplicado.

Uma Stack é uma lista de elementos que seguem a ideia "Primeiro a entrar - Ultimo a sair" (FILO). Util para alguns exercicios que envolvem dados. para usar basta apenas declarar uma variavel como tipo Stack e usala:

```cs
class Example 
{
	Public static void Main() 
	{
		// perceba que para utilizar a classe, precisamos encontrala primeiro:
		var s = new Acme.Collections.Stack<int>(); // declara uma pilha de inteiros
		s.push(1);   // pilha tem 1
		s.push(10);  // pilha tem 1,10
		s.push(100); // pilha tem 1,10,100
		Console.WriteLine(s.Pop()); // pilha tem 1, 10
		Console.WriteLine(s.Pop()); // pilha tem 1
		Console.WriteLine(s.Pop()); // pilha ta vazia
	}
}

```


Os programas C# podem ser armazenados em vários arquivos de origem pois quando compilado todos os arquivos serão unificados em um só arquivo para então serem processados. C# tambem não limita a quantidade de tipos declarados por arquivo.

> Até aqui fiz 17 páginas do pdf... horay!
> Para interessados a partir da página 17 tem um pequeno roteiro para quem já conhece Java ou outras linguagens famosas.


# Introdução ao C++++
> Abaixo começamos na página 25

## Configurando o ambiente local

antes de desenvolvermos em C# precisamos configurar o ambiente de desenvolvimento, para isso precisamos de um editor de texto.

##### Windows
Para usuário windows existe a opção do Visual Studio: uma IDE exclusiva para C# e .NET que possui uma versão gratuita para comunidade e já inclui uma versão da livraria .NET instalada.

##### LInux
Para usuário linux (ou para usuário windows curiosos) a Microsoft disponibiliza o editor Visual Studio Code, que pode ser modificado por extensões para permitir criar uma área de desenvolvimento que nem o Visual Code. 

Existem alternativas criadas por outros grupos, alguns precisam ser configurados para ativar as funcionalidades outros vem pré-prontos:
* Kdevelop
* Kate
* Gnome Builder
* Jetbrains : Rider (PAGO) (provavelmente a versão mais completa aqui)
*  

Como a plataforma é para windows, será necessário fazer a instalação da versão de desenvolvimento do .NET (SDK). cheque seu gerenciador de pacotes ou faça a instalação manualmente.











