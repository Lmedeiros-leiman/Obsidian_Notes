https://livrodigital.uniasselvi.com.br/ADS07_introducao_ao_desenvolvimento_de_sistemas_web/unidade2.html?topico=1
# Tópico 1 : Fundamentos do HTML

HTML é uma linguagem de formatação e estuturação de documentos web, ela auxilia desenvolvedores a criarem componentes visuais atrativos, mesmo que o desenvolvedor não tenha conhecimento profundo em desenvolvimento.

Existem várias versões do HTML visto que sua criação vem junto com a expansão da internet.

| Versão    | Ano  |
| --------- | ---- |
| HTML      | 1991 |
| HTML+     | 1993 |
| HTML 2.0  | 1995 |
| HTML 3.2  | 1997 |
| HTML 4.01 | 1999 |
| XHTML     | 2000 |
| HTML5     | 2012 |

## Instalando um editor de texto.

Esse tópico já havia sido mencionado nos arquivos anteriores, mas com a perca de dados irei mencionar novamente: para trabalhar com desenvolvimento é necessário ferramentas de edição de código ou texto, alguns editores se dedicam para o desenvolvimento em uma linguagem: as IDEs.

### Listinha de editores notaveis

- Visual Studio Code -> leve, rápido e com plugins.
- Notepad++ -> leve e simples, bloco de notas do windows melhorado.
- Sublime -> similar ao Notepad++ porem para multiplas plataformas
- Emacs -> carro editavel, versão inicial é diferente e precisa de tempo até o usuário se adaptar mas com o tempo pode ser transformado num editor supremo que suporta desde o desenvolvimento de código até recebimento de emails e gerenciamento de calendário.

## Utilizando HTML

Primeiramente precisamos compreender o que são _tags_ para depois aprender a utilizá-las. As _tags_ são comandos de formatação de hipertextos específicos e distintos, colocados em um documento html para que o browser possa interpretá-lo.

São representadas pelo sinal menor que <, em sequência o nome da tag, finalizando com o sinal de maior que >.

```html 
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>Titulo do documento que aparecera na aba do navegador</title>
	</head>
	<body>
		<h1>Titulo que aparecera no documento</h1>
	</body>
</html>
```

Neste exemplo a tag ```<!DOCTYPE html>``` esta gindo para informar o leitor do arquivo que o código a seguir é um documento html e que deve ser passado por um interpretador html, normalmente o tipo de arquivo entrega essa informação, mas para evitar problemas é melhor indicar explicitamente, similar ao SHIBANG dos arquivos .sh ou .bash.


## Sites Uteis

A internet foi criada graças a um conjunto de pessoas que uniram forças para manterem a tecnologia acessível a todos, essas pessoas tambem se reuniram em um grupo chamado W3C (World Wide Web Consortium) para definir algumas normas técnicas, equivalente ao IEEE para engenheiros elétricos.

A fundação W3 tambem possui um site dispinibilizando informações sobre como funcionam tecnologias comuns na web em seu site W3School.

Ao mesmo tempo a fundação Mozzila tambem possui um histórico similar e tambem tendo seu website.


W3School -> https://www.w3schools.com/
- Exemplos práticos
- Direto ao assunto
- Tutoriais Rasos
- Sem muito suporte para o aluno que busca complexidade dos elementos.

Mozzila -> https://developer.mozilla.org/pt-BR/
- Exemplos mais complexos
- Explicações longas e técnicas
- Tutoriais Profundos
- Explica detalhadamente como funciona cada elemento dentro de uma página web.

## Elementos Comuns de uma página HTML

Toda página HTML pode ser escrita apenas com uma mesma tag por todo o documento, porem essa não é uma pratica boa e pode tornar o documento dificil de ser entendido dificultando o trabalho em equipe.


| Tags Primárias | Função                                                                                |
| -------------- | ------------------------------------------------------------------------------------- |
| HTML           | Descreve o inicio e fim do documento                                                  |
| Body           | Descreve a área com a parte visivel do documento                                      |
| Script         | Descreve um código em javascript que será executado após o carregamento do documento. |
| Style          | Descreve uma área ditando os estilos em CSS dos elementos html                        |

| Tags Dados | Função                                                                                                                                                                                                |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Head       | Define o cabeçario com dados sobre o documento.                                                                                                                                                       |
| Meta       | Atribui um valor a um atributo da página, como descrição, autor, viewport, lista de caracteres que a página usa e até mesmo que texto colocar em um post de rede social quando compartilhar a página. |
| Link       | Conecta a página com um outro documento, normalmente CSS porem tambem aceita scripts Javascript.                                                                                                      |
| Title      | Define o Titulo que aparecera na aba da janela do navegador. não visível no documento em si.                                                                                                          |
| !Doctype   | Especifica para o leitor do arquivo não apenas o tipo de arquivo, mas tambem qual versão do html foi utilizada.                                                                                       |

| Tags Comuns | Função                                                                 |
| ----------- | ---------------------------------------------------------------------- |
| a           |                                                                        |
| abbr        | Define uma abreviação                                                  |
| area        | Define uma área dentro de uma imagem/mapa                              |
| article     | define um artigo                                                       |
| b           | define um texto em negrito                                             |
| br          | define uma quebra de linha                                             |
| button      | define um botão                                                        |
| col         | especifica as propriedades de uma coluna de um elemento colgroup       |
| colgroup    | especifica um grupo de uma ou mais colunas de uma tabela para formatar |
| datalist    | especifica opções pre-definidas para uma entrada                       |
| dialog      | caixa de dialogo ou janela                                             |
| div         | seção de um documento                                                  |
| dl          | define uma descrição                                                   |
| dt          | nome da lista de inscrição                                             |
| footer      | rodapé                                                                 |
| h1 -> h6    | titulo/cabeçalho                                                       |
| header      | seção de cabeçalho                                                     |
| hgroup      | Define um grupo de cabeçalhos.                                         |
| ins         | texto que foi inserido em um documento                                 |
| li          | lista ordenada                                                         |
| main        | parte principal do documento                                           |
| mark        | texto marcado/realçado                                                 |
| menu        | lista/menu de comandos                                                 |
| menu item   | item da lista de menu                                                  |
| nav         | define uma área de links/navegação                                     |
| ol          | define uma lista ordenada                                              |
| output      | resultado/ saida de dado                                               |
| p           | paragrafo                                                              |
| param       | parametro de um objeto                                                 |
| pre         | texto pré-formatado                                                    |
| progress    | progresso                                                              |
| q           | curta  citação                                                         |
| section     | seção de um documento                                                  |
| small       | texto pequeno                                                          |
| sub         | texto subescrito                                                       |
| table       | inicio de uma tabela                                                   |
| tbody       | corpo de uma tabela                                                    |
| td          | dado da tabela                                                         |
| textarea    | área de entrada de texto                                               |
| tfoot       | rodapé de uma tabela                                                   |
| th          | cabeçário de uma tabela                                                |
| thead       | cabeçário de uma tabela                                                |
| time        | define uma data/horario                                                |
| tr          | linha de uma tabela                                                    |
| u           | texto estilizado diferente do texto normal                             |
| ul          | lista desordenada                                                      |
| var         | variavel                                                               |
| wbr         | possivel quebra de linha                                               |

| Tag Especial | Função                                                                             |
| ------------ | ---------------------------------------------------------------------------------- |
| img          | mostra uma imagem na página                                                        |
| audio        | traz um arquivo de audio para a página                                             |
| video        | mostra um video na página                                                          |
| form         | define um formulario para entrada de dados                                         |
| input        | define um campo para a entrada de dados                                            |
| label        | define texto para melhor descrever outra tag, normalmente uma de entrada de dados. |

Todo elemento/Tag HTML possui certos atributos que podem ser atribuidos durante sua criação, modificando algum dado: visivel ou não. Tambem inclui atributos Arial que auxiliam com a acessibilidade da página.

| Atributos Globais | Função                                                                    |
| ----------------- | ------------------------------------------------------------------------- |
| Alt               | especifica um texto alternativo para uma tag visual como imagem           |
| Disabled          | desativa a entrada de um campo                                            |
| Href              | especifica para qual URL um link enviara o usuario                        |
| Id                | especifica o ID de uma tag, util para javascript e tags.                  |
| style             | permite modificar o estilo de uma tag em linha                            |
| src               | a URL para a fonte de uma tag, normalmente scrip, video, audio ou imagem. |
| title             | texto que aparecera como dica de ferramenta (mouse parado em cima da tag) |
| value             | qual valor o conteúdo de entrada tem por padrão.                          |
> Nas linguagens de programação é normal querer utilizar um caractere extra para indicar um comentário. o HTML não é diferente com a tag <!- e -> > 
>    ``` html
 <!- Comentário HTML ou macarção visual no documento de texto. -> 

### Entendo links

No html é comum querer interligar páginas entre si. normalmente para isso utilizamos a tag ```<a>```.

essa é a tag chamada Anchor e ela possui atributos especiais, podendo receber um link pelo atributo ```href``` podendo selecionar até mesmo componentes DENTRO da página:

```html

<a href=#ListaProdutos> Esta ancora irá procurar um elemento com a tag ListaProdutos neste documento </a>

<a href="www.google.com">esta tag irá enviar a página para o site do google.</a>

<a href="www.google.com" target="_blank">essa tag irá abrir uma nova página e direcionar ela para o site do google.</a>
```

