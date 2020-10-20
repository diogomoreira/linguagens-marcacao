# Atributos e valores

A **tag de início** de um elemento pode possuir **atributos** que fornecem mais informações sobre o elemento, como propriedades específicas ou formatação a ser aplicada sobre ele.

Um atributo consiste em um nome de atributo seguido de um valor entre aspas duplas, ligados por um sinal de igual \(`=`\), como no exemplo abaixo, que já vimos anteriormente.

```markup
<html lang="pt-br">
```

Neste exemplo a tag **&lt;html&gt;**, que define o início do nosso documento HTML, possui um atributo `lang` cujo valor é igual a “**pt-br**“, o que permite que o navegador e outros sistemas \(como o buscador do Google\) saibam que essa página está escrita em idioma **Português do Brasil**. 

O valor de um atributo deve, preferencialmente, ser declarado entre aspas, mesmo que alguns atributos não o exijam. Um elemento **pode ter mais de um atributo**, ou **pode simplesmente não usar atributo algum**. A medida que o curso for avançando, o uso dos atributos vai se tornar mais comuns, principalmente no módulo **CSS**.

### Atributos globais

Atributos globais se aplicam a todos os elementos HTML, pois eles fornecem informações adicionais que os navegadores usam para determinar a forma como os elementos são exibidos na página. É o caso dos atributos `id` ou `class`, que são usados comumente em [CSS](../css/introducao-a-css.md).

Uma lista completa com todos os atributos globais pode ser encontrado [aqui](https://www.w3schools.com/tags/ref_standardattributes.asp).

### Atributos data-\*

Atributos `data-*` \(onde o \* pode ser qualquer coisa\) nos permite armazenar **informações extras** em elementos HTML padrões. A sintaxe é simples, qualquer atributo de qualquer elemento no qual o nome do atributo inicia com `data-` é um atributo data. Digamos que você possui uma lista e quer armazenar informações extras que não possuem nenhuma representação visual, como no exemplo abaixo.

```markup
<ul>
    <li data-origem="reino-unido">Arctic Monkeys</li>
    <li data-origem="estados-unidos">The Strokes</li>
</ul>
```



