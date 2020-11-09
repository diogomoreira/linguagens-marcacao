# Textos e fontes

Conteúdos textuais são inseridos em uma página com uso de elementos de marcação, tais como, `h1`, `p`, `div`, `span`, `body`, etc. Vamos explorar algumas propriedades que serão aplicados aos textos exibidos em uma página web e aprender sobre algumas recomendações sobre apresentação das fontes em dispositivos eletrônicos.

### Propriedades de texto

#### Propriedade `color`

A propriedade `color` é usada para **mudar a cor do texto**. Pode assumir os seguintes valores:

* **Nome** - como "red", "white", "blue"
* **Valor hexadecimal** - como "\#ff0000"
* **Valor RGB**, que é uma combinação de Red \(Vermelho\), Green \(Verde\) e Blue \(Azul\) - por exemplo "rgb\(255,0,0\)"

Um gerador de cores em hexadecimal pode ser encontrado [aqui](https://www.w3schools.com/colors/colors_picker.asp). É possível também usar funções pra gerar cores com opacidades diferentes. Veja sobre [`rgba`](https://www.maujor.com/tutorial/css3-modulo-para-cores.php).

#### Propriedade `text-align`

Propriedade usada para mudar o **alinhamento horizontal do texto**. Pode assumir os seguintes valores:

* **left** \(esquerda\)
* **right** \(direita\)
* **center** \(centralizado\)
* **justify** \(justificado\)

#### Propriedade `text-decoration`

Usado para definir ou remover decorações no texto, como sublinhado. Pode assumir os seguintes valores:

* **overline** \(acima\)
* **line-through** \(no meio do texto\)
* **underline** \(abaixo\)

#### Propriedade `text-transformation`

Usado para transformar o texto em **maiúsculas** e **minúsculas**. Pode assumir os seguintes valores:

* **uppercase** \(maiuscula\)
* **lowercase** \(minuscula\)
* **capitalize** \(primeira letra\)

#### Propriedade `text-indent`

Usada para alterar a **indentação da primeira linha de um parágrafo**. Pode assumir qualquer valor numérico \(em pixels e porcentagem, por exemplo\).

#### Propriedade `letter-spacing`

Usada para mudar o **espaçamento entre os caracteres de um texto**. Pode assumir qualquer valor numérico \(em pixels e porcentagem, por exemplo\).

#### Propriedade `word-spacing`

Semelhante a `letter-spacing`, porém para mudar o **espaçamento entre as palavras de um texto**. Pode assumir qualquer valor numérico \(em pixels e porcentagem, por exemplo\).

#### Propriedade `line-height`

Usada para mudar o **espaçamento entre as linhas de um texto**. Pode assumir qualquer valor numérico.

#### Propriedade `text-shadow`

Usada para adicionar **sombra ao texto**. Tem 3 valores a serem definidos: deslocamento horizontal \(numérico\) deslocamento vertical \(numérico\) cor \(igual a color\). Opcionalmente, pode ser definido valor de desfoque.

![](../.gitbook/assets/image%20%2812%29.png)

Um gerador de propriedade `text-shadow` pode ser encontrado [aqui](https://cssgenerator.org/text-shadow-css-generator.html).

### Fontes

As propriedades relativas às fontes alteram a aparência do texto, diferente das propriedades já vistas que alteram a disposição dele no documento. A primeira diferença a ser observada nas fontes é sobre serifas. A imagem abaixo mostra a diferença entre fontes **serifadas** e **não-serifadas**.

![](https://lh6.googleusercontent.com/kj6PIdDN5ZmiCAqVL_FzIHCdw71snXRPVlX6_furfXBVlcm5WK88vvAxNr1Fr01qg54Rz1Q3RN9CuoEnRHtqHMc4qrTnok0TApO3wREuHlCYub6m-R55qSNaunr_GTcC7I_BYXzX78Y)

![](https://lh4.googleusercontent.com/DsjL5lT2VCTlPpnYf4J9A-QyqUV3fvAvp53R5I-W7zisGWg1aP9gqy4wGEdTNQ9T3i1I2L8C8WB7-wVPXVbVBbxp74VXioN58N57cBvLoh-rKfEL9UI1zwwl_TPut3EqWiP4W8OiwaM)

![](https://lh6.googleusercontent.com/tVD7bE1czzymF5nioq8E6d9L9Q2x9hG5tP3i5QDbZjSS74LJUEJntIlxPDcRXJxAqY8sKQeH1JR2coGWJMax03X1VIAxyOCFoH_L9-80DH9ObxcAO22UQyNdjpTjuzX5mx9Yy-UHpig)

De maneira geral: **Fontes serifadas são melhores em textos impressos** enquanto **Fontes não-serifadas são melhores para leitura em tela**. Enquanto estivermos desenvolvendo páginas para a _web_, preze pelo uso de fontes não serifadas.

#### Propriedade `font-family`

Essa propriedade muda a **família de fontes** a ser usada para exibição. Aceita vários valores. Exemplo:

```css
font-family: "Times New Roman", Times;
```

Também pode ser usada para definir um tipo de fonte genérico \(**serifada** ou **não-serifada**\) para ser usada, caso a fonte definida não esteja disponível. Exemplo:

```css
font-family: "Times New Roman", Times, serif;
```

No exemplo acima, caso a fonte "**`Times New Roman`**" não esteja disponível \(uma vez que ela é do Windows\), a fonte serifada padrão do sistema será utilizada no lugar. Pode assumir os seguintes tipos de fonte: `serif` \(Com serifa\), `sans-serif` \(Sem serifa\) **e `monospace` \(Monoespaçada\).**

**A boa prática** aqui é definir suas fontes preferenciais e, por último, colocar o tipo de fonte, para que o sistema use caso não encontre as que você definiu.

```css
font-family: "Times New Roman", Times, serif;
font-family: Arial, Helvetica, sans-serif;
```

#### Propriedade `font-style`

Usada para definir se o texto estará em **itálico** ou não. Possíveis valores: 

* `normal` \(Sem itálico\)
* `italic` \(Itálico\)

#### Propriedade `font-size`

Usada para definir o **tamanho do texto**. Aceita valores númericos, em pixels e porcentagens.

```css
font-size: 16px;
font-size: 110%;
```

#### Propriedade `font-weight`

Usada para definir o **peso da fonte**, ou seja, se ela vai ser densa \(bold/**negrito**\) ou se vai ser mais fina \(**light**\). Possíveis valores:

* Valores numéricos de 100 a 900.
* `normal` \(Sem negrito\)
* `bold` \(Com negrito\)

### Fontes web

As fontes web \(ou _web fonts_\) proporcionaram uma nova maneira de trabalhar com tipografia na internet. Antigamente, era preciso se limitar às fontes mais comuns, pois se dependia completamente daquelas que o usuário tinha instaladas no computador. Com as web fonts, esta obrigatoriedade é eliminada, sendo possível **usar as fontes que o layout pedir sem precisar se preocupar com compatibilidade.**

Um ótimo site com um conjunto variado de fontes, e com gerador de código é o [**Google Web Fonts**](https://fonts.google.com/).

#### 

