# Grid Layout

O **Grid Layout** é uma tecnologia do CSS que está presente na maioria dos principais navegadores modernos. Ela nos permite criar _layouts_ baseados em _grids_ \(um conjunto de **linhas** e **colunas**, como na figura abaixo\) de uma forma extremamente rápida, fácil e padronizada.

![](../.gitbook/assets/image%20%2814%29.png)

O CSS Grid é bem poderoso e completo, permitindo que certas coisas sejam feitas de mais de uma maneira.

Primeiro de tudo temos que saber que teremos propriedades CSS para trabalhar com o **elemento que possui nossos itens** \(**grid container** ou elemento pai\) e propriedades para os nossos **itens da grid** \(**grid itens** ou ****elementos filhos\). Um exemplo pra facilitar o entendimento está na figura abaixo

![](../.gitbook/assets/image%20%2813%29.png)

### Grid container

Veremos as propriedades que ficam no elemento pai dos nossos itens, o grid container. Teremos basicamente **1 \(um\) container** com alguns itens dentro. Dependendo do exemplo a quantidade de itens poderá ser alterada, mas aqui usaremos 6. Aqui usaremos [classes](seletores/classe.md) para evidenciar o que é **container** e o que é **item**.

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

Primeiro precisamos definir que o nosso container é do tipo “`grid`”; Fazemos isso com a propriedade “`display`”.

```css
.container{
    display: grid;
}
```

Como estamos trabalhando com um grid de linhas e colunas, precisamos indicar quantas linhas e quantas colunas nosso grid vai ter. Para colunas usamos a propriedade `grid-template-columns` e para linhas usamos o `grid-template-rows`.

Se queremos 3 colunas, não indicamos com o número três. O que fazemos na verdade é **indicar qual o tamanho de cada coluna que queremos**. A medida pode ser em qualquer unidade \(px, em, %, etc\) ou em **frações** \(`fr`\). Cada valor deve ser separado por um espaço.

```css
grid-template-columns: 1fr 1fr 1fr;
```

No exemplo acima, dizemos que nosso grid vai ter 3 colunas, cada uma delas ocupando 1 fração \(`1fr`\) do espaço disponível.

Exatamente da mesma maneira nós declaramos as linhas utilizando a propriedade grid-template-rows. No exemplo abaixo, dizemos que nosso grid tem 2 linhas, cada uma delas ocupando `200px`.

```css
grid-template-rows: 200px 200px;
```

Dessa maneira, uma vez que temos 6 itens dentro de nosso container \(exemplo em HTML mostrado anteriormente\) com 3 colunas e 2 linhas, teremos a seguinte apresentação da nossa página:

![](../.gitbook/assets/image%20%2815%29.png)

Veja esse exemplo em código [aqui](https://codesandbox.io/s/grid-layout-columns-e-rows-xeqp8).

{% hint style="info" %}
O exemplo acima, logicamente, tem outras propriedades envolvidas, como `background-color: black;` e `gap: 10px;` para criar o espaço entre os itens. Iremos explorar mais propriedades dessas ao longo dos exemplos.
{% endhint %}

### Template areas

Até agora só declaramos o **tamanho das nossas colunas e linhas**. Você deve ter notado que nossos itens vão se organizando no grid de acordo com a **ordem em que estão no HTML**.

Porém, o CSS Grid nos permite ir além disso: podemos dar **nomes para cada área da nossa grade e depois indicar onde cada elemento deve ir**. Dessa maneira fica bem simples de entender a estrutura da nossa grid. Fazemos isso com a propriedade `grid-template-areas`.

Vamos alterar um pouquinho o nosso HTML. Deixamos apenas **4 \(quatro\) itens** e iremos colocar as classes `cabecalho`, `menu-lateral`, `conteudo` e `rodape` nos itens da grid para podermos indicar a posição de cada um deles depois.

```markup
<div class="container">
    <div class="item cabecalho"></div>
    <div class="item menu-lateral"></div>
    <div class="item conteudo"></div>
    <div class="item rodape"></div>
</div>
```

Para cada item, vamos declarar a propriedade `grid-area`, que serve para indicar o nome da área em que cada elemento deverá ocupar no grid. Para facilitar, daremos os mesmos nome das classes, mas você pode dar o nome que quiser.

```css
.cabecalho {
  grid-area: cabecalho;
}

.menu-lateral {
  grid-area: menu-lateral;
}

.conteudo {
  grid-area: conteudo;
}

.rodape {
  grid-area: rodape;
}
```

Agora vamos ao que interessa: **indicar o nome das áreas da nossa grid**. Para dar nomes às áreas de uma mesma linha, escrevemos dentro de aspas `""`. Ao abrir novas aspas estaremos indicando que estamos indo para a linha seguinte.

```css
.container{
    grid-template-areas: "cabecalho cabecalho" 
                         "menu-lateral conteudo" 
                         "rodape rodape";
}
```

Repetimos `cabecalho` e `rodape` duas vezes porque declaramos **duas colunas** e queremos que eles ocupem as duas. Experimente mudar os nomes das áreas de lugar e veja que nossos elementos irão mudar de posição também.

Veja esse exemplo em ação [aqui](https://codesandbox.io/s/grid-layout-template-areas-uzfrb).

