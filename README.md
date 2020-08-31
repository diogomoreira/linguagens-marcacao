# Linguagens de Marcação

A linguagem de marcação possui “uma forma de descrever a estrutura lógica ou semântica de um documento e fornecer instruções a computadores sobre como apresentar o conteúdo de um arquivo”. \(Davies, 2004\). Uma visão que interessa diretamente aos estudos da Ciência da Informação: a **possibilidade de** _**descrever**_ ****_**o conteúdo semântico**_ **de um texto**.

Existem diversos tipos de linguagem de marcação, para usos e finalidades específicas. Editores de texto, como o **Microsoft Word** por exemplo, podem manter marcações internas para controlar diversos atributos de um texto, como **cor, tamanho, formatação**, etc.

Como o próprio nome sugere, as Linguagens de Marcação têm como característica principal criar **marcações** \(aqui vamos chamar de _tags_\) para delimitar um texto ou algum elemento de um documento. Uma marca é um tipo de código que **envolve uma palavra ou um trecho de um texto**.

Por exemplo, em HTML um trecho delimitado pelas marcas `<b>` e `</b>` aparecerá em negrito \(o b vem da palavra _bold_, negrito em inglês\), um trecho delimitado pelas marcas `<u>` e `</u>` aparecerá sublinhado \(_underline_\), e um trecho delimitado pelas marcas `<i>` e `</i>` será apresentado em itálico

Abaixo um exemplo de um **texto** envolvido pelas marcações `<b>` e `</b>`. Esse texto ao ser interpretado por um navegador como Firefox, Chrome ou Safari irá exibir o texto em negrito.

```markup
<b>Este texto aparecerá em negrito</b>
```

Num primeiro momento, essas marcas eram usadas apenas para definir a forma como um texto seria apresentado. Mais tarde, com a evolução das linguagens, tornou-se possível usar marcas para **fornecer significado ao texto**. Veja o exemplo abaixo:

```markup
<b>Este texto aparecerá em negrito</b>
<strong>Este texto também aparecerá em negrito</strong>
```

A diferença aqui é que:

* `<b>` define um estado **físico**
* `<strong>` define um estado **lógico**.

Pode ser que algum interpretador entenda `<strong>` de outra maneira que não seja negrito. Aqui, strong é usado para dizer que este texto deve ter **ênfase**. Por outro lado, `<b>` sempre será interpretado como negrito. É importante reforçar que existem diversos interpretadores para linguagens de marcação, incluindo tecnologias assistivas, como **Leitores de Tela** para pessoas com deficiência visual. Você pode se informar mais [nesse artigo](https://brasil.uxdesign.cc/acessibilidade-como-funcionam-os-leitores-de-tela-3d9b610216e1).

Todas as Linguagens de Marcação possuem um **conjunto de convenções** utilizadas na definição de suas marcações, isto é, contêm diversas marcas, cada qual com um significado próprio, estipulado previamente. Como exemplo anterior, em HTML a _tag_ `<b>` como mostrado anteriormente, é usada para delimitar um texto que será apresentado em negrito.

Cada _tag_ possui uma função específica, seja simplesmente para marcar um texto, seja para definir uma estrutura mais complexa como, por exemplo, uma **tabela**, um **formulário**, etc. Ao se delimitar um texto por _tags_, é possível estabelecer um **conteúdo semântico** que pode ser tratado e manipulado por programas de computador. No nosso caso, navegadores como Firefox, Chrome, etc.

### Padronização

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

### Exemplo de linguagens de marcação no dia-a-dia

Um exemplo que podemos observar de linguagens de marcação são os chamados **feeds RSS**, para assinatura de **notícias**, **podcasts** e etc. Observe o trecho abaixo, que foi retirado do **RSS de notícias do G1 Paraíba.** Você não precisa entender ele por completo agora, mas veja que temos algumas indicações de que isso é uma **notícia**. O conteúdo dentro de `<title>`, por exemplo, nos diz qual o título da notícia.

```markup
<item>
    <title>Alerta de baixa umidade é emitido pelo Inmet para 100 municípios na PB</title>
    <link>https://g1.globo.com/pb/paraiba/noticia/2020/08/31/alerta-de-baixa-umidade-e-emitido-pelo-inmet-para-100-municipios-na-pb.ghtml</link>
    <description>
        <img src="https://s2.glbimg.com/xA6DG_xEJ94emHnCfOTs49ZGID4=/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2020/q/2/BNLtmNRcAHYAeiCMGj1g/inmet.jpg" />
        <br />Instituto recomenda que a população desses municípios beba bastante líquido e evite desgaste físico nas horas mais secas. Inmet emite alerta de baixa umidade para 100 municípios
        da Paraíba Reprodução/Inmet Um alerta amarelo de baixa umidade para 100 municípios da Paraíba foi emitido pelo Instituto Nacional de Meteorologia (Inmet). O aviso começou às 12h desta
        segunda-feira (31) até as 18h de terça-feira (1°). Moradores de municípios em alerta devem evitar desgaste físico nas horas mais secas, e exposição ao sol nas horas mais quentes do dia,
        segundo o Inmet. É recomendado que se beba bastante líquido. A umidade relativa do ar varia entre 30% e 20%. Existe baixo risco de incêndios florestais e à saúde.
    </description>
    <pubDate>Mon, 31 Aug 2020 16:48:06 -0000</pubDate>
</item>
```

A maneira como os vários interpretadores veem esse tipo de conteúdo é diferente, um navegador da web vai mostrar de uma maneira, um [**leitor de RSS**](https://www.oficinadanet.com.br/post/11004-alternativas-google-reader) ****de uma outra maneira e assim por diante. Abaixo, a notícia evidenciada no código sendo exibida pelo leitor de rss **Feedly**.

![Not&#xED;cias do G1 Para&#xED;ba na interface do leitor de RSS Feedly](.gitbook/assets/screen-shot-2020-08-31-at-14.38.16.png)

O importante é que o **conteúdo** é o mesmo. As diferentes formas de **exibir informação** só são possíveis graças as linguagens de marcação. ****Durante o nosso curso iremos aprender a utilizar linguagens de marcação, mais especificamente **HTML**, **CSS** e **XML**. Porém, entendendo os conceitos que iremos ver na disciplina, será fácil entender outras linguagens caso você precise na sua vida profissional.



\*\*\*\*



