# Introdução a CSS

**CSS** é a sigla para o termo em inglês _Cascading Style Sheets_ que, traduzido para o português, significa **Folha de Estilo em Cascatas**. É usado para **estilizar elementos escritos em uma linguagem de marcação** como [HTML](../html/introducao-html.md).

O CSS **separa o conteúdo da representação visual do site**. Utilizando o CSS é possível alterar a cor do texto e do fundo, fonte e espaçamento entre parágrafos. Também pode criar e usar variações de layouts, ajustar imagens para suas respectivas telas e assim por diante.

{% hint style="info" %}
"**Mas por que eu tenho que usar CSS?**"

Porque HTML não é feito para **formatar páginas da web**\
HTML é usado para **descrever conteúdo**
{% endhint %}

Quando estamos construindo nossas definições de estilo feito em CSS, elas **DEVEM** estar em um arquivo separado do documento HTML, com a extensão `.css`. Para que o browser possa interpretar os dois em conjunto, é necessário **criar um link por meio de um** [**metadado**](../html/metadados.md) (como visto anteriormente).

![](<../.gitbook/assets/Screen Shot 2020-10-13 at 09.35.43.png>)

```markup
<link rel="stylesheet" type="text/css" href="estilo.css" />
```

Aqui, consideramos que o arquivo `estilo.css` é a nossa folha de estilos e que ela está contida no mesmo nível que o arquivo index.html, os valores a serem utilizados no atributo `href` seguem os padrões de [URLs](../html/urls.md) vistos anteriormente.

Um mesmo arquivo css pode ser usado por várias páginas, uma vez que todas elas usem o mesmo metadado, apontando para o mesmo arquivo.

### Regras CSS e Sintaxe

Uma regra CSS segue uma sintaxe própria que define como será aplicado estilo a um ou mais elementos da marcação HTML de uma página. Um conjunto de regras CSS formam uma folha de estilos (um arquivo com extensão `.css`).

Uma **regra CSS**, na sua forma mais elementar, compõe-se de três partes: um seletor, uma propriedade e um **valor**. O código abaixo deve ser escrito no seu arquivo `.css`.

```css
seletor {
    propriedade: valor;
}
```

O significado das partes da regra CSS é:

* **seletor**: são usados para "achar" (ou selecionar) elementos HTML pelo seu nome (por exemplo: \<p>, \<h1>...), pelo nome de uma classe aplicada ao elemento da marcação HTML, pelo nome de um identificador ID aplicado ao elemento da marcação HTML
* **propriedade**: é a propriedade do elemento HTML ao qual será aplicada a estilização definida no valor (por exemplo: tamanho da fonte, cor do texto, altura do elemento).
* **valor**: é a característica específica a ser assumida pela propriedade (por exemplo: cor azul, fundo verde, altura igual a 300px)

Um exemplo dessas partes aplicadas é demonstrado abaixo, onde usamos um **seletor** que busca todos os elementos `<h1>`, e define a propriedade `color` (cor da fonte) para o valor `green` (verde).

```css
h1 {
    color: green;
}
```

A grande parte desse módulo vai se focar em explorar os **seletores** e demonstrar ocasionalmente novas propriedades e valores possíveis para cada uma delas, mas desde já, saiba que não vamos explorar todas as propriedades e valores, principalmente por não ser necessário. Cada um irá, naturalmente, identificar o que deseja fazer nos layouts de seus sites ou no projeto e irá buscar as propriedades necessárias pra isso.

{% hint style="warning" %}
Nesse ponto, é interessante que você revisite a seção [Atributos e valores](../html/atributos-e-valores.md) para revisar, pois iremos usar esse conceito com mais frequência a partir de agora.
{% endhint %}
