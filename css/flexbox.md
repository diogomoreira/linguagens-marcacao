# Flexbox

O **Flexbox** \(Flexible Box\) nos permite organizar, alinhar e distribuir itens dentro de um container. Com ele fica mais simples definir o tamanho e o alinhamento vertical e horizontal de itens.

Primeiro de tudo temos que saber que teremos propriedades CSS para trabalhar com o **elemento que possui nossos itens** \(**container** ou elemento pai\) e propriedades para os nossos **itens** \(elementos filhos\). Bem semelhante ao [Grid Layout](grid-layout.md).

![](https://lh5.googleusercontent.com/pes2z_67UU4UU_eWyJB3LC89tGyCAHzMT2u0OCcXgJQPClrd3nhSMHLvGQsfKkuyigM8m4JV5TUpKFfrMU2GjciIRLBF5xMX1WngFR6VTKqBI0BIZQfZwNqzUldC9fZUFdvR8hTR0eA)

![](https://lh3.googleusercontent.com/7F1BVU3afP1MfQEUB0efFEy463FFbEHixZ7k9TyRJ0RHngshEBhar6gXLRRkW4Z1TAjwE8xlGecmf5R_DbXBfg8NGt1dJEbt8_25ztiITOrzrM8OFlrpcJiHdvio9L0GtPxjX7aYRk8)

### Flexbox Container

Veremos as propriedades que ficam no elemento pai dos nossos itens, o flexbox container. Teremos basicamente **1 \(um\) container** com alguns itens dentro. Dependendo do exemplo a quantidade de itens poderá ser alterada, mas aqui usaremos 6. Aqui usaremos [classes](seletores/classe.md) para evidenciar o que é **container** e o que é **item**.

```markup
<div class="container" >
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
</div>
```

Primeiro precisamos definir que o nosso container é do tipo “`flex`”; Fazemos isso com a propriedade “`display`”.

```css
.container{
    display: flex;
}
```

#### Eixos

Ao se utilizar o _flexbox_, é preciso ter em mente que todas as operações realizadas relacionam-se a dois eixos: o eixo principal e o eixo transversal. O **eixo principal** é definido através da propriedade `flex-direction` \(que veremos abaixo\) e o **eixo transversal** encontra-se na direção perpendicular a ele. Como esses eixos são as engrenagens fundamentais do flexbox é necessário compreender minuciosamente o seu funcionamento.

#### flex-direction

Indica a direção dos itens, definindo o que vamos chamar de `eixo principal` \(_main-axis_\).

* **row** \(padrão\): da esquerda para direita
* **row-reverse:** inverso de `row`
* **column:** de cima para baixo
* **column-reverse:** inverso de `column`

Se o valor escolhido for `row` \(linha\) ou `row-reverse` \(linha reversa\), seu **eixo principal** se moverá ao longo da linha — na **direção inline**.

![](https://mdn.mozillademos.org/files/15614/Basics1.png)

O **eixo transversal** é perpendicular ao eixo principal, logo, se a propriedade `flex-direction` estiver definida nas linhas, como `row` ou `row-reverse`, o eixo transversal estará na direção das colunas, como `column` ou `column-reverse`.

![If flex-direction is set to row then the cross axis runs in the block direction.](https://mdn.mozillademos.org/files/15616/Basics3.png)

Se o valor escolhido for `column` \(coluna\) ou `column-reverse` \(coluna reversa\) e o **eixo principal** se moverá do topo até o fim da página — na **direção block**.

![](https://mdn.mozillademos.org/files/15615/Basics2.png)

Se o eixo principal for definido nas colunas, como `column` ou `column-reverse`, então o **eixo transversal** estará na direção das linhas, como `row` ou `row-reverse`.

![](https://mdn.mozillademos.org/files/15617/Basics4.png)

#### flex-wrap

O comportamento padrão dos itens de um elemento flex é ficar em uma única linha. Se a largura total de todos os itens for maior do que o espaço disponível, os itens continuarão na mesma linha.

Esta propriedade permite que os itens sejam jogados em outra linha caso não haja mais espaço na linha.

* **nowrap** \(padrão\): todos os itens ficam em uma única linha
* **wrap:** os itens que não cabem na linha são jogados para baixo
* **wrap-reverse:** os itens que não cabem na linha são jogados para cima

#### justify-content

Define o alinhamento dos itens ao longo do `eixo principal`.

* **flex-start** \(padrão\): os itens ficam junto no começo da eixo
* **flex-end:** os itens ficam juntos no final do eixo
* **center:** os itens ficam centralizados no eixo
* **space-between:** os itens são distribuídos igualmente no espaço disponível. O primeiro item fica no começo do eixo e o último fica no final.
* **space-around:** os itens são distribuídos igualmente no espaço disponível ao redor deles.
* **space-evenly:** os itens são distribuídos igualmente no espaço disponível.

#### align-items

Define o alinhamento dos itens perpendicularmente em relação ao `eixo principal`.  
 Pense nele como um `justify-content`, mas que alinhará os itens no outro eixo.

* **stretch** \(padrão\): estica os elementos para preencherem o container.
* **flex-start:** os itens ficam junto no começo do eixo perpendicular
* **flex-end:** os itens ficam juntos no final do eixo perpendicular
* **center:** os itens ficam centralizados no eixo perpendicular
* **baseline:** parecido com o `center`, mas usando a base da linha como referência. No exemplo abaixo, note como os textos dos itens ficam alinhados.

#### align-content

Alinha as linhas do container. Por alinhar as linhas, esta propriedade só tem efeito quando há mais de uma linha.

* **stretch** \(padrão\): estica as linhas para preencherem o espaço restante.
* **flex-start:** as linhas ficam juntas no começo do container
* **flex-end:** as linhas ficam juntas no final do container
* **center:** as linhas ficam centralizadas no container
* **space-between:** as linhas são distribuídas igualmente. A primeira linha fica no começo do container e a última fica no final.
* **space-around:** as linhas são distribuídas igualmente no espaço disponível ao redor delas.

### Flexbox Itens

As propriedades vistas até agora são aplicadas ao **Container**, veremos agora as propriedades que serão aplicadas aos itens de um container flexbox. Para começar, vamos adicionar uma classe em um dos itens para vermos a diferença de propriedades aplicada em um único item.

```markup
<div class="container">
    <div class="item"></div>
    <div class="item selected"></div>
    <div class="item"></div>
</div>
```

#### order

Por padrão, os itens de um Flex Container são **exibidos na ordem presente no HTML**. Com a propriedade `order` nós podemos alterar a ordem dos elementos. O valor deve ser um número inteiro, negativo ou positivo. o seguinte código deixa o elemento com a classe `selected` aparecendo como o primeiro item.

```css
.selected {
    order: 1;
}
```

#### flex-grow

Indica o quanto **um item pode crescer caso seja necessário**. Deve ser um número inteiro positivo.

Isso significa que se todos os itens tiverem o valor `1`, o espaço disponível será distribuído igualmente a todos eles. Caso um dos itens tenha o valor `2`, este item poderá ter duas vezes mais espaço do que os outros.

#### flex-basis

Define o tamanho padrão de um elemento antes do espaço disponível ser distribuído. O valor pode ser em `px`, `%`, `em`, etc. Se o valor for `auto`, ele irá olhar para o valor de `width` e `height` do item.

Se o valor for `content`, ele irá olhar para o tamanho do conteúdo do item.

#### flex-shrink

Indica o quanto **um item pode encolher caso seja necessário**. Deve ser um número inteiro positivo.

Isso significa que se todos os itens tiverem o valor `1`, o espaço disponível será distribuído igualmente a todos eles. Caso um dos itens tenha o valor `2`, este item poderá ter metade do espaço do que os outros.

#### align-self

Assim como a propriedade `align-items`, a propriedade `align-self` nos permite **sobrescrever o valor desta propriedade para um único item**. Assim podemos, por exemplo, colocar um único item no final de uma linha enquanto todos os outros estão no começo.



