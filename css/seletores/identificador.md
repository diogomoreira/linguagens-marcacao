# Identificador

Com este seletor, selecionamos **um único elemento da página**, por meio de seu identificador único.

O [atributo global](../../html/atributos-e-valores.md#atributos-globais) `id` é usado e deve ser definido no HTML para o elemento que desejamos selecionar, definindo um **identificador exclusivo** \(ID\) que deve ser **único em todo o documento**. Observe o exemplo abaixo

```markup
<p id="primeiro-paragrafo">Algum texto</p>
```

Por exemplo, se digitamos `#primeiro-paragrafo` estaremos selecionando **apenas 1 \(um\) elemento** que tem o atributo `id` com o valor `primeiro-paragrafo` da página e poderemos aplicar estilos a ele, como o código abaixo que acrescenta uma cor da fonte **azul** \(blue\) e centraliza o texto dentro do parágrafo.

```css
#primeiro-paragrafo {
    color: blue;
    text-align: center;
}
```

A demonstração do exemplo encontra-se [nesse link](https://codesandbox.io/s/02-seletor-id-u72nm).

