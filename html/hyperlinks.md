# Hyperlinks

**Hyperlinks** são a base da _web_, é a partir dos hyperlinks, por exemplo, que você chegou a essa página. Os hyperlinks conectam um endereço da web a outro, ou páginas de uma mesmo site. Pra ser ainda mais abrangente, é isso que nos permite vincular nossos documentos `.html` a qualquer outro documento \(ou outro recurso, como imagens, instaladores de jogos, vídeos...\) que queremos. Também podemos vincular para **partes específicas de documentos**. Literalmente qualquer conteúdo da web pode ser convertido em um link, para que, quando clicado \(ou ativado de outra forma\) fará com que o navegador vá para outro **endereço**, que a partir de agora chamaremos [URL](urls.md).

Veja o exemplo da página inicial do IFPB, Campus Cajazeiras.

![P&#xE1;gina inicial do IFPB - Campus Cajazeiras. Screenshot tirada no dia 07/09/2020](../.gitbook/assets/image.png)

Aos que já estão familiarizados com a web, seja no computador ou no celular, sabem que em vários locais dessa página podemos "clicar" ou "tocar", dependendo do dispositivo usado, para que possamos acessar uma nova informação ou página. São os hyperlinks que possibilitam isso.

### Criando um hyperlink

Um link básico é criado envolvendo o texto \(ou outro conteúdo, como veremos mais adiante\) que você quer transformar em um link dentro de um elemento `<a>`, e dando-lhe um atributo `href`, \(também conhecido como **Hypertext Reference**\) que conterá o endereço da web para o qual você deseja que o link aponte.

{% tabs %}
{% tab title="Código" %}
```markup
<p>Estou criando um link para
<a href="https://www.ifpb.edu.br">a página inicial do IFPB</a>.
</p>
```
{% endtab %}

{% tab title="Resultado" %}
Estou criando um link para [a página inicial do IFPB](https://ifpb.edu.br).
{% endtab %}
{% endtabs %}

Outro atributo que podemos adicionar aos hyperlink é o `title`. É recomendado que ele contenha informações úteis sobre o link, como, quais tipos de informação a página contém ou outras informações importantes. Por exemplo:

```markup
<p>Estou criando um link para
<a href="https://www.ifpb.edu.br"
   title="Página do IFPB, com informações sobre a 
   oferta de cursos e outros documentos importantes">a página inicial do IFPB</a>.
</p>
```

### 

