# Imagens

Para inserir uma imagem em uma página da web, usamos a tag `<img>`. Essa tag é um [elemento vazio](tags-elementos.md) \(quer dizer que **não possui conteúdo de texto ou tag de fechamento**\) que requer, no mínimo, um atributo para ser útil — `src` \(abreviação de _source_\). O atributo `src` contém um caminho apontando para a imagem que você deseja incorporar na página, que pode ser uma [URL](urls.md) relativa ou absoluta, da mesma maneira que o valores de atributo `href` no elemento `<a>`.

Por exemplo, se sua imagem for chamada `album.jpg`, e está no mesmo diretório de sua página HTML, você poderia inserir a imagem assim:

```markup
<img src="album.jpg">
```

Se a imagem estivesse em um subdiretório de `imagens`, que estivesse dentro do mesmo diretório da página HTML, então você a incorporaria da seguinte maneira:

```markup
<img src="imagens/album.jpg">
```

E assim por diante. Dúvidas sobre URL? Veja [aqui](urls.md).

### Atributo "alt"

Um dos atributos opcionais, mas que são de extrema importância para imagens, é o `alt`. Seu valor deve ser uma **descrição textual da imagem**, para uso em situações em que a imagem não pode ser vista/exibida ou leva muito tempo para carregar devido a uma conexão lenta à Internet. Por exemplo, nosso código acima pode ser modificado da seguinte maneira:

```markup
<img src="imagens/album.jpg"
     alt="A capa do primeiro álbum do Arctic Monkeys,
     mostrando uma fotografia em preto e branco com um homem fumando">
```

A maneira mais fácil de testar seu texto `alt` é **digitar incorretamente seu nome de arquivo**. Se, por exemplo, o nome da nossa imagem estivesse escrito `albunn.jpg`, o navegador não exibiria a imagem, mas exibiria o texto alternativo.

Veja [nesse exemplo](https://codesandbox.io/s/03-imagens-zjlr2) no Codesandbox como esse comportamento é apresentado no navegador.

O que **exatamente você deve escrever** dentro do seu atributo `alt`? Depende do _por que_ a imagem está lá em primeiro lugar. Em outras palavras, **o que você perde se sua imagem não aparecer**.



