# Padronização de tags

Todas as Linguagens de Marcação possuem um **conjunto de convenções** utilizadas na definição de suas marcações, isto é, contêm diversas marcas, cada qual com um significado próprio, estipulado previamente. Como exemplo anterior, em HTML a _tag_ `<b>` como mostrado anteriormente, é usada para delimitar um texto que será apresentado em negrito.

Cada _tag_ possui uma função específica, seja simplesmente para marcar um texto, seja para definir uma estrutura mais complexa como, por exemplo, uma **tabela**, um **formulário**, etc. Ao se delimitar um texto por _tags_, é possível estabelecer um **conteúdo semântico** que pode ser tratado e manipulado por programas de computador. No nosso caso, navegadores como Firefox, Chrome, etc.

Desde 1994 existe um comitê internacional chamado World Wide Web Consortium \(W3C\), responsável por **desenvolver e manter padrões para a Web**. O W3C é dirigido por [Tim Berners-Lee](https://pt.wikipedia.org/wiki/Tim_Berners-Lee), o inventor da World Wide Web, a internet como conhecemos hoje em dia. Dentre esses padrões encontram-se dezenas de linguagens de marcação.

É necessária a existência da padronização para que as Linguagens de Marcação possam ser **compartilhadas e utilizadas mundialmente**. Para que um fabricante possa desenvolver um navegador, por exemplo, é necessário que ele reconheça que a _tag_ `<b>` indica **negrito**, e assim por diante. Todas devem ser capazes também de diferenciar as _tags_ \(que compõem a **estrutura do documento**\) do texto propriamente dito \(que constitui o **conteúdo do documento**\).

O exemplo abaixo mostra o código e o resultado final, evidenciando que a tag `<b>` não é exibida no resultado porque faz parte apenas de sua estrutura. O que importa no resultado final, que é o que será visto pelo usuário, é o **conteúdo**.

{% tabs %}
{% tab title="Código" %}
```text
<b>Mais um texto em negrito</b>
```
{% endtab %}

{% tab title="Resultado" %}
**Mais um texto em negrito**
{% endtab %}
{% endtabs %}

Assim, uma ferramenta como um browser, por exemplo, pode identificar as marcas contidas e apresentar ao usuário somente o **conteúdo de texto do documento**, sem as tags.

