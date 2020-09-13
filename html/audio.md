# Áudio

O HTML dá suporte a embutir arquivos de áudio por meio do elemento `<audio>`, oferecendo a possibilidade de incorporar facilmente esse tipo de mídia em documentos HTML.

Um exemplo de áudio incorporado em um documento HTML

```markup
<audio src="musica.mp3">
    <p>Seu nevegador não suporta o elemento audio.</p>
</audio>
```

O atributo `src` pode ser a URL do arquivo de áudio ou o caminho do arquivo no sistema local. O elemento `<p>` dentro de `<audio>` serve como uma exceção, para ser exibido caso o navegador não dê suporte a esse elemento, em casos de computadores ou celulares mais antigos.

{% hint style="info" %}
Outros formatos além do .mp3 também são suportados, como o .ogg. Realize testes em vários navegadores antes de publicar um site para saber se ao menos a maioria dá suporte ao arquivo de áudio que você está usando.
{% endhint %}

Agora veja o exemplo abaixo:

```markup
<audio src="musica.mp3" controls autoplay loop>
    <p>Seu navegador não suporta o elemento audio </p>
</audio>
```

Esse exemplo de código usa atributos do elemento `<audio>`:

* `controls` : Mostra os controles padrão para o áudio na página.
* `autoplay` : Faz com que o áudio reproduza automaticamente ao carregar a página. Não funciona em alguns navegadores por questões de **permissão**.
* `loop` : Faz com que o áudio repita automaticamente.

Um exemplo de uso de áudio em HTML no Codesandbox pode ser encontrado [aqui](https://codesandbox.io/s/04-audio-28xmr?file=/index.html). Faça experiências com os atributos e com áudios diferentes. Um bom site pra buscar músicas sem restrições quanto a direitos autorais é o [Free Music Archive](https://www.freemusicarchive.org/).

