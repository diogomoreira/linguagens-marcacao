# Tabelas

Uma tabela é um **conjunto estruturado de dados constituído por linhas e colunas**. Uma tabela permite consultar, fácil e rapidamente, valores que indiquem alguma **relação entre diferentes tipos de dados**, por exemplo, uma pessoa e a sua idade, ou os dias da semana num horário de uma piscina.

As tabelas são definidas com a tag `<table>`. Uma tabela é dividida em linhas (com a tag `<tr>`), e cada linha é dividida em células de dados (com a tag `<td>`). Além dessas tags, `<th>` é usada ao invés de `<td>` quando a célula contém o cabeçalho da coluna.

Imagine a tabela abaixo, mostrando as **bandas de indie rock mais ouvidas do** [**Last.fm**](https://last.fm) juntamente com o país onde a banda surgiu. Em seguida, veja o código que usamos para construi-la.

![Exemplo de tabela](<../.gitbook/assets/Screen Shot 2020-09-19 at 20.47.53.png>)

```markup
<table>
  <tr>
    <th>Banda</th>
    <th>País</th>
    <th>Ouvintes</th>
  </tr>
  <tr>
    <td>The Killers</td>
    <td>Estados Unidos</td>
    <td>4.624.348</td>
  </tr>
  <tr>
    <td>Arctic Monkeys</td>
    <td>Reino Unido</td>
    <td>3.720.334</td>
  </tr>
  <tr>
    <td>The Strokes</td>
    <td>Estados Unidos</td>
    <td>3.438.082</td>
  </tr>
  <tr>
    <td>Franz Ferdinand</td>
    <td>Reino Unido</td>
    <td>3.301.074</td>
  </tr>
  <tr>
    <td>Death Cab for Cutie</td>
    <td>Reino Unido</td>
    <td>2.931.326</td>
  </tr>
  <tr>
    <td>Bloc Party</td>
    <td>Reino Unido</td>
    <td>2.582.592</td>
  </tr>
</table>
```

Perceba que usamos apenas um elemento `<table>` que contem todas as informações da tabela. Para cada linha, usamos um elemento `<tr>` que contem seus elementos. No caso da primeira linha, usamos `<th>` e nas demais, a tag `<td>`. Veja no exemplo do [Codesandbox](https://codesandbox.io/s/06-tabelas-c26oj?file=/index.html:287-1068) que a tabela não está visualmente igual a que mostramos aqui, isso acontece porque ainda não estilizamos ela com CSS, mas nós chegaremos lá durante nossa disciplina.

### Células em múltiplas linhas e colunas <a href="#permitir_que_as_celulas_sejam_distribuidas_por_multiplas_filas_e_colunas" id="permitir_que_as_celulas_sejam_distribuidas_por_multiplas_filas_e_colunas"></a>

Às vezes teremos a necessidade de que uma célula de uma tabela ocupe mais de uma coluna ou linha. É o que chamamos de células "mescladas" em programas como Excel ou até mesmo o Word. O exemplo anterior, reformulado para células em múltiplas linhas e colunas (coluna **país**) pode ser visto abaixo para um melhor entendimento.

![](<../.gitbook/assets/Screen Shot 2020-09-19 at 20.55.34.png>)

Para isso utilizaremos os atributos `colspan` e `rowspan` nas células da tabela. Elas servem para expandir as células fazendo com que uma única célula ocupe mais de uma linha (`rowspan`) ou mais de uma coluna (`colspan`).

```markup
<table>
  <tr>
    <th>País</th>
    <th colspan="2">Banda e número de ouvintes</th>
  </tr>
  <tr>
    <td rowspan="2">Estados Unidos</td>
    <td>The Killers</td>
    <td>4.624.348</td>
  </tr>
  <tr>
    <td>The Strokes</td>
    <td>3.438.082</td>
  </tr>
  <tr>
    <td rowspan="4">Reino Unido</td>
    <td>Franz Ferdinand</td>
    <td>3.301.074</td>
  </tr>
  <tr>
    <td>Death Cab for Cutie</td>
    <td>2.931.326</td>
  </tr>
  <tr>
    <td>Bloc Party</td>
    <td>2.582.592</td>
  </tr>
  <tr>
    <td>Arctic Monkeys</td>
    <td>3.720.334</td>
  </tr>
</table>
```

### Quando não usar tabelas?

Por muitos anos, o elemento `<table>` foi usado para criar layouts de páginas inteiras. Isso é **extremamente desencorajado** nos dias de hoje. Layouts com tabelas **reduzem acessibilidade de utilizadores com deficiências visuais**, uma vez que tabelas não são uma ferramenta adequada para o layout, e a marcação é mais complexa do que se recorresse a técnicas de layout de CSS, a informação dada pelos leitores de tela será confusa para os seus utilizadores.
