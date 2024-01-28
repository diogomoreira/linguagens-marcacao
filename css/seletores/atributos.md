# Atributos

O **seletor de atributos** seleciona elementos baseado no valor de um dado atributo.

Repare no exemplo de HTML a seguir, onde iremos incluir alguns links e iremos estilizar cada um de uma maneira diferente usando **seletores de atributos**. Antes de continuar, leia sobre [Atributos e valores](../../html/atributos-e-valores.md), especificamente em [Atributos data-\*](../../html/atributos-e-valores.md#atributos-data) antes de começar com os exemplos mostrados aqui.

```markup
<h1>Recomendações de música - outubro/2020</h1>
<ul>
  <li data-genero="indie dream-pop indie-pop twee-pop">Alvvays</li>
  <li data-genero="dream-pop indie indie-pop">Bombay Bicycle Club</li>
  <li data-genero="indie indie-rock shoegaze">Silversun Pickups</li>
  <li data-genero="indie indie-rock">Yo La Tengo</li>
  <li data-genero="indie lo-fi">Pavement</li>
  <li data-genero="synthpop">CHVRCHES</li>
</ul>
```

Perceba os atributos `data-genero` que trazem informações a mais para os itens de uma lista. Cada um deles tem **1 ou mais** valores, que são separados por espaço em branco.

Embora essas informações não fiquem visíveis para o usuário final, podemos usar isso para estilizar essa lista. Para selecionar um elemento a partir de seu atributo, usaremos a seguinte sintaxe:

* `[attr]` Representa um elemento que tenha um atributo de nome **attr**.
* `[attr=valor]` Representa um elemento que tenha um atributo de nome **attr**, o qual o valor é exatamente igual a **valor** que está declarado após o sinal de `=`.
* `[attr=~valor]` Representa um elemento com um atributo de nome **attr**, o qual value é uma lista de palavras separadas por espaços (como no caso das classes), e uma dessas é exatamente **valor**.
* `[attrˆ=valor]` Representa um elemento com um atributo com nome **attr** que tem um valor com prefixo igual a **valor**.
* `[attr$=valor]` Representa um elemento com um atributo com nome **attr** que tem um valor com sufixo igual a **valor**.
* `[attr*=valor]` Representa um elemento com um atributo de nome **attr** o qual valor contém ao menos uma ocorrência de **valor** contido na string.

Agora veja o exemplo abaixo, estilizando o HTML mostrado anteriormente.

```css
[data-genero] {
  font-weight: bold; /* Deixando a fonte em negrito */
}

[data-genero="indie lo-fi"] {
  background: linear-gradient(
    180deg,
    rgba(55, 55, 55, 1) 0%,
    rgba(0, 0, 0, 1) 100%
  ); /* Definindo o plano de fundo como um gradiente de uma cor A para uma B */
  color: white;
}

[data-genero~="shoegaze"] {
  color: crimson;
}

[data-genero^="dream-pop"] {
  color: grey;
}

[data-genero$="twee-pop"] {
  color: green;
}

[data-genero*="indie"] {
  font-size: 25px; /* Deixando a fonte em tamanho 25px */
}

```

Cada um dos itens da lista vai ser estilizado de uma maneira diferente. Perceba também que o **primeiro seletor** `[data-genero]` seleciona **todos** de uma vez, já que todos os itens da lista tem esse atributo.

Veja o exemplo completo [aqui](https://codesandbox.io/s/04-seletores-de-atributo-2ptwn).
