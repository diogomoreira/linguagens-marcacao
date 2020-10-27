# Negação

A pseudo-classe CSS de **negação**, `:not(X)`, é uma notação funcional que recebe um seletor simples `X` como argumento. Ela seleciona um elemento que não é representado por seu argumento. `X` não pode conter outro seletor de negação.

Considere o seguinte código HTML:

```markup
<p>Um pouco de texto.</p>
<p class="classico">Um pouco mais de texto.</p>
<span>Mais um texto<span>
```

E então o código css abaixo

```css
p:not(.classico) { 
    color: red;
}

body *:not(p) {
    color: green;
}
```

Vai produzir um parágrafo com a cor vermelha \(o primeiro, que **não é** da classe "classico"\), e também vai produzir um texto em cor verde, com o elemento span, que é [filho](filhos-e-descendentes.md) de `body` e **não é** um elemento do tipo `p`.

