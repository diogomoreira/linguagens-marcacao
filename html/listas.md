# Listas

As listas são muito importantes quando precisamos **listar itens no site** e também para a criação de menu de navegação, mas isso veremos apenas no módulo de CSS. As listas em HTML se assemelham aos "**Marcadores e Numeração**" em programas de edição de texto. Iremos explorar os variados tipos de lista a seguir. Os exemplos de código podem ser encontrados [aqui](https://codesandbox.io/s/02-listas-ebkdo).

### Listas não-ordenadas

Uma lista não-ordenada deve sempre começar com a tag `<ul>` (de **unordered list**). Dentro dessa lista, iremos adicionar **itens de lista**, com a tag `<li>`. É importante notar que todos os itens de uma determinada lista devem estar dentro do `<ul>` específico dela. Cada item aparece com um pequeno círculo preto antes do texto digitado entre as tags `<li></li>`. Veja o código de exemplo abaixo e o resultado.

{% tabs %}
{% tab title="Código" %}
```markup
<h2>Lista de bandas de Indie Rock</h2>
<ul>
    <li>Arctic Monkeys</li>
    <li>Bleachers</li>
    <li>Cage the Elephant</li>
</ul>
```
{% endtab %}

{% tab title="Resultado" %}
### Lista de bandas de Indie Rock

* Arctic Monkeys
* Bleachers
* Cage the Elephant
{% endtab %}
{% endtabs %}

A ordem dos itens dentro da lista é a mesma ordem que será mostrada na tela, então a **organização do código vai fazer a diferença** nesse caso.

Como falado anteriormente, itens que pertecem a mesma lista devem estar dentro do mesmo `<ul>`. Caso estejam em listas separadas, o resultado visual ficará diferente. Execute o código de exemplo abaixo, onde criamos duas listas e veja a diferença.

{% tabs %}
{% tab title="Código" %}
```markup
<h2>Lista de bandas de Indie Rock</h2>
<ul>
    <li>Arctic Monkeys</li>
    <li>Bleachers</li>
</ul>
<ul>
    <li>Cage the Elephant</li>
</ul>
```
{% endtab %}
{% endtabs %}

### Listas ordenadas

Já uma lista ordenada serve pra itens que fazem sentido serem colocados em uma ordem específica. Sempre começam com a tag `<ol>`(de **ordered list**). Os itens dessa lista continuam usando a mesma tag da lista não-ordenada: `<li>`. Cada item aparece com um número em sequência antes do texto digitado entre as tags `<li></li>`.

Exemplos variam desde uma sequência lógica de filmes a serem assistidos (**O Senhor dos Anéis: A Sociedade do Anel** deve ser assistido antes de **Senhor dos Anéis: As duas torres**, por exemplo) até um **ranking de suas bandas favoritas**. Veja os exemplos abaixo

{% tabs %}
{% tab title="Código" %}
```markup
<h2>Lista de bandas que mais escutei em 2019</h2>
<ol>
    <li>Vampire Weekend</li>
    <li>MGMT</li>
    <li>Bleachers</li>
</ol>
```
{% endtab %}

{% tab title="Resultado" %}
### Lista de bandas que mais escutei em 2019

1. Vampire Weekend
2. MGMT
3. Bleachers
{% endtab %}
{% endtabs %}

### Listas de definição

Uma lista de descrição/definição é uma lista com **termos** e suas descrições. Algo como um **glossário**. Deve começar com a tag `<dl>`, e dentro dela cada tag `<dt>` define o **termo**, enquanto a tag `<dd>` descreve esse termo anteriormente definido. Veja o exemplo abaixo e o resultado ao final da página

```markup
<h2>Gêneros musicais e suas definições</h2>
<dl>
    <dt>Indie rock</dt>
    <dd>
        Gênero musical surgido no Reino Unido e Estados Unidos durante a década
        de 1980. É enraizado em gêneros mais antigos, como o rock alternativo, o
        pós-punk e a new wave.
    </dd>
    <dt>Rock alternativo</dt>
    <dd>
        Gênero de rock surgido na década de 1980 que se tornou bastante popular
        na década de 1990.[1] Consiste de vários subgêneros oriundos da cena
        musical independente como grunge e britpop
    </dd>
</dl>
```

As listas de definição aparecem como um glossário, como falado anteriormente. Mostrando o **termo** sem indentação, enquanto sua **definição** aparece com uma indentação leve, para dar a resposta visual de que é a definição do termo mostrado acima. Veja que a ordem aqui importa, uma vez que os termos e suas respectivas definições devem estar em linhas sequenciais.

![Exemplo de lista de definição](<../.gitbook/assets/Screen Shot 2020-09-07 at 18.04.25.png>)

