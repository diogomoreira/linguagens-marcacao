# Títulos e Parágrafos

Vamos começar a construir o corpo do nosso documento a partir de dois tipos de elementos básicos: **títulos** e **parágrafos**.

### Títulos

Em HTML, o título é exatamente o que parece: um **título real** ou **subtítulo**, quando você coloca no texto a tag `<h1>`, por exemplo, o texto ficará maior e a dimensão das letras será de acordo com o número de cabeçalhos. Os títulos podem ter dimensões de **1** a **6**, onde **1** é a maior dimensão e **6** a menor.

* &lt;h1&gt;
* &lt;h2&gt;
* &lt;h3&gt;
* e assim até &lt;h6&gt;

As tags de títulos precisam de fechamento. No exemplo abaixo, todo o texto que está dentro de `<h1>` e `</h1>` sofrerá as alterações citadas anteriormente

```markup
<h1>Top 3 bandas de indie rock</h1>
```

### Parágrafos

A tag `<p>` representa um **parágrafo do texto**. Parágrafos são, geralmente representados, em mídia visual, como bloco de texto que são separados dos blocos adjacentes por espaços brancos verticais e/ou recuo de primeira-linha.

{% tabs %}
{% tab title="Código" %}
```markup
<p>Indie rock é um gênero musical surgido na década de 1980.</p>
<p>É enraizado em gêneros como o rock alternativo, o pós-punk e a new wave</p>
```
{% endtab %}

{% tab title="Resultado" %}
Indie rock é um gênero musical surgido na década de 1980.

É enraizado em gêneros como o rock alternativo, o pós-punk e a new wave
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Explore o uso de **parágrafos** e **quebras de linha**, como falado na seção [Tags e elementos](tags-elementos.md) e veja a diferença entre os dois.
{% endhint %}

Ao final desse exemplo, nosso código inteiro está exatamente como indicado abaixo e pode ser visualizado no [Codesandbox](https://codesandbox.io/s/01-titulos-e-paragrafos-fcwev?file=/index.html).

```markup
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="utf-8" />
    <title>Diogo Moreira - Meu site pessoal sobre música</title>
  </head>
  <body>
    <h1>Top 3 bandas de indie rock</h1>
    <p>Indie rock é um gênero musical surgido na década de 1980.</p>
    <p>
      É enraizado em gêneros como o rock alternativo, o pós-punk e a new wave
    </p>
  </body>
</html>
```







