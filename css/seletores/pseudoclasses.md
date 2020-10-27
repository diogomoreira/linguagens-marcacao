# Pseudoclasses

Uma **pseudo-classe CSS** é uma **palavra-chave** adicionada a qualquer um dos seletores que especifica um **estado** especial do elemento selecionado. Um estado de um elemento acontece quando for clicado, quando o mouse estiver acima do elemento, entre outras ações que são possíveis a partir da interação com os elementos utilizando mouse, telas de toque, etc.

Podemos separá-las em dois grandes grupos: **Estruturais** e **Dinâmicas**.

As **pseudo-classes dinâmicas** controlam os estados dos elementos. Abaixo, vão alguns deles:

* **`:hover`** – quando passamos o mouse em cima do elemento.
* **`:active`** – quando ativamos o elemento. Por exemplo, quando clicamos em um link e não soltamos o botão do mouse. Nesse momento, estamos ativando a ação do elemento. Esse estado é ativado também quando navegamos pelos links pelo teclado utilizando a tecla `tab`. Este estado não há em todos os elementos.
* **`:visited`** – quando o link é visitado.
* **`:focus`** – quando um elemento recebe foco. Muito utilizado em campos de texto. Quando clicamos em cima um campo de texto para escrever, o elemento está ganhando foco.

Veja o exemplo abaixo:

{% tabs %}
{% tab title="HTML" %}
```markup
<ul>
  <li>Início</li>
  <li>
    Bandas
    <ul>
      <li>Arctic Monkeys</li>
      <li>The Strokes</li>
      <li>The Libertines</li>
    </ul>
  </li>
  <li>Clipes</li>
  <li>Sobre o site</li>
</ul>
```
{% endtab %}

{% tab title="CSS" %}
```css
ul li ul {
  display: none;
}

ul li:hover ul {
  display: block;
}
```
{% endtab %}
{% endtabs %}

Nesse exemplo, temos \(linha 5\) uma lista \(vamos chamá-la de lista "filha"\) dentro de um dos elementos de uma outra lista. E queremos mostrar os elementos dessa lista filha apenas quando passarmos o mouse em cima do elemento `<li>` com o conteúdo **Bandas.**

No CSS, selecionamos primeiramente a lista filha \(usando seletores de [descendentes](filhos-e-descendentes.md)\) e falamos que ela não deve ser exibida \(`display: none;`\), já no segundo seletor, estamos declarando que, uma vez que o elemento `<li>` tiver com o estado `:hover`, ou seja, quando passarmos o mouse por cima, ele deve **mostrar** \(`display: block;`\) todos os elementos ul que sejam seus descendentes. Outros valores para display podem ser encontrados [aqui](https://developer.mozilla.org/pt-BR/docs/Web/CSS/display).

O exemplo de código no Codesandbox pode ser encontrado [aqui](https://codesandbox.io/s/05-pseudoclasses-u5kk9?file=/estilo.css:0-68).

Já as **pseudoclasses estruturais** tem uma sintaxe semelhante a pseudoclasse e servem para selecionarmos um elemento da estrutura do código, como por exemplo estilizar a primeira linha de um parágrafo, a primeira letra de um texto, etc. Alguns exemplos:

* **`:first-child`** – seleciona o elemento, apenas se ele for o primeiro.
* **`:first-of-type`** – seleciona o primeiro elemento daquele tipo.
* **`:last-child`**  –  seleciona o elemento, apenas se ele for o último.
* **`:last-of-type`**  –  seleciona o último elemento daquele tipo.
* **`:nth-child(argumento)`**  – admite um argumento que consiste em uma fórmula a ser inserida entre parênteses. A fórmula poderá ser um simples número inteiro, algo do tipo an+b ou as palavras chaves `odd` \(ímpar\) ou `even` \(par\).



