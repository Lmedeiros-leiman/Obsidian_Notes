https://livrodigital.uniasselvi.com.br/ADS07_introducao_ao_desenvolvimento_de_sistemas_web/unidade3.html?topico=1

# Entendendo CSS

CSS: Cascading Style Sheets ou Folhas de Estilo em Cascata é uma linguagem de estilação para documentos web.

antes da invenção do CSS o HTML dependia de tags especiais que ditavam os estilos de um documento como a tag ```<font>``` que atribuía uma fonte especifica para aquela seção do documento, porem isso tornava o documento convolado e de difícil entendimento forçando a criação de uma linguagem dedicada ao estilamento.

Um comando CSS é composto por 3 partes: ![[Pasted image 20240428151352.png]]

- **Seletor:** Tag, classe ou ID utilizado no documento HTML que será alterada.
- **Declaração:**
	- **Propriedade:** o parâmetro que sera alterado
	- **Valor:** uma nova qualificação ou quantificação do parâmetro.
toda declaração é separada por ``;``.

Para uma lista de seletores o site Mozilla para desenvolvedores web possui uma lista de seletores atualizados para o css moderno: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_selectors

Para uma lista de propriedades e alguns de seus valores o site Mozilla para desenvolvedores tambem possui uma lista atualizada para o css moderno: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

### Inserindo CSS na página

A linguagem de estilo possui diversas maneiras de ser incluida na página:
- Em linha -> Utilizando o atributo ```<style>```dentro do elemento HTML
![[Pasted image 20240428152638.png]]
- Internamente -> Utilizando a tag ```<style>``` no documento. ![[Pasted image 20240428152617.png]]

- Externamente -> Importando um arquivo .css utilizando a tag ```<link>```
![[Pasted image 20240428152546.png]] 
![[Pasted image 20240428152557.png]]
### Múltiplas folhas de estilo:
Muitas vezes em grandes documentos a mesma tag será selecionada por multiplas tags, nesses casos a menos que seja utilizado a palavra chave ```!important``` para forçar o estilo, a tag mais especifica será utilizada herdando os atributos da tag pai.





# JavaScript

Javascript é uma linguagem interpretada que é executada dentro de um documento web, o interpretador normalmente é o navegador web do usuário, porem a ferramenta Node.js permite utilizar a linguagem a nivel de servidor.

Javascript é utilizada com a tag ```<script>```, podendo tambem chamar os comandos javascript de um arquivo .js utilizando ```<script src={URL ou caminho}]>```.

As regras, como uma língua é construída, são chamadas de sintaxe da linguagem. As sentenças em uma linguagem de programação são chamadas declarações de programa. Um programa de computador é uma sequência de "comandos executáveis" chamados declarações. As instruções JavaScript são separadas por ponto e vírgula.

Algumas sintaxes do javascript são universais, como a representação de um valor de texto com aspas, variáveis sendo textos sem as aspas e números podendo ser interpretados tanto quanto números, sem as aspas, ou texto: com as aspas.

Caso não saiba como funciona a estruturação básica de sintaxe de uma linguagem, recomendo assistir ao curso abaixo até ter em mente mais ou menso como funciona.
https://www.youtube.com/watch?v=Ptbk2af68e8

O importante é lembrar que no navegador a linguagem não atua sozinha, diferente de um projeto em branco de outras linguagens, JavaScript possui por padrão o conhecimento de algumas classes e objetos padrões dos navegadores:
```js
let DocumentBody = Document.body; // retonar o elemento <body>
DocumentBody.style.backgroundColor = "red"; // deixa o fundo do corpo avermelhado.
```

Quando tiver duvidas, a wiki da Mozilla possui uma lista de variaveis, objetos e classes utilizadas pela linguagem que é mantida atualizada conforme a fundação e a internet em si crescem: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects

