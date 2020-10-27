# Filhos e descendentes

Para selecionar objetos que são filhos ou descendentes de algum outro elemento, utilizaremos seletores específicos, mas antes disso, vamos entender o que queremos dizer por **filho, ancestral** e **descendente**. Preste atenção no código abaixo

```markup
  <body>
    <h1>Menu de navegação</h1>
    <ul>
      <li>Início</li>
      <li>Sobre</li>
    </ul>
  </body>
```

Quando falamos que um elemento é **filho** de outro elemento, significa que ele está "dentro" ou "contido" em outro elemento. No exemplo acima, os elementos `<h1>` e `<ul>` são **filhos** do elemento `<body>`. Assim como os elementos `<li>` são **filhos** do elemento `<ul>`, que é o elemento **ancestral** dessa relaçao.

Já os elementos descendentes são aqueles que estão contidos em outros elementos mas não de uma maneira direta, **podendo estar em níveis mais profundos**. Um exemplo está nos elementos `<li>` do código acima, eles não são filhos de `<body>` mas estão contidos em um elemento que está dentro dele. Sendo assim, uma vez que eles não são filhos, mas estão dentro de `<body>` de alguma forma em algum nível, eles são **descendentes**.

Elementos **filhos também são descendentes**. Já elementos descendentes não necessariamente são filhos. Pense no seguinte auxiliar para lembrar disso:

* Minha filha é minha filha E minha descendente
* Minha neta não é minha filha, MAS é minha descendente.

Essa hierarquia e descendência é ferramenta muito poderosa para aplicarmos estilos com CSS a determinadas tags descendentes.

### Seletores de filhos

Utilizando `>` selecionamos elementos que são filhos diretos do elemento especificado anteriormente. No exemplo abaixo, usamos essa sintaxe para estilizar com **negrito** todos os itens de lista que sejam filhos diretos de um `ul` com id `lista1`

```css
ul#lista1 > li {
    font-weight: bold;
}
```

### Seletores de descendentes

Separando os elementos por espaço selecionamos os elementos que são descendentes do elemento especificado anteriormente \(não é necessário que seja um filho direto\). No exemplo abaixo, utilizamos esse seletor para estilizar com **negrito** todos os itens de lista que sejam descendentes de um ul com id lista1

```css
ul#lista1 li {
    font-weight: bold;
}
```



