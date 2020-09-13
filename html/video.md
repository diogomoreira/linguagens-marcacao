# Vídeo

Assim como para arquivos de áudio, o HTML também dá suporte a embutir arquivos de vídeo por meio do elemento `<video>`. Um exemplo de áudio incorporado em um documento HTML é mostrado abaixo

```markup
<video src="videos/arcticmonkeys.mp4" controls autoplay loop>
    <p>Seu browser não dá suporte a vídeos em HTML</p>
</video>
```

O atributo `src` pode ser a URL do arquivo de vídeo ou o caminho do arquivo no sistema local. O elemento `<p>` dentro de `<video>` serve como uma exceção, para ser exibido caso o navegador não dê suporte a esse elemento, em casos de computadores ou celulares mais antigos.

O exemplo de código usa atributos do elemento `<video>`:

* `controls` : Mostra os controles padrão para o vídeo na página.
* `autoplay` : Faz com que o vídeo reproduza automaticamente ao carregar a página. Não funciona em alguns navegadores por questões de **permissão**.
* `loop` : Faz com que o vídeo repita automaticamente.

Outro atributo interessante é o **poster**

[https://codesandbox.io/s/05-videos-chs6l?file=/index.html](https://codesandbox.io/s/05-videos-chs6l?file=/index.html)

