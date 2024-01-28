# Metadados

Como já vimos anteriormente, em [Introdução a HTML](introducao-html.md), o **cabeçalho** (tag `<head>`) contém informações que **não são transpostas visivelmente para o usuário/leitor do documento**. Tratam-se de dados implícitos, de uso e controle do documento: **vinculação com outros arquivos**, **aplicação de lógica de programação** e [**metadados**](https://pt.wikipedia.org/wiki/Metadados). É todo o conteúdo do cabeçalho fica delimitado entre a abertura e fechamento tag head. Vamos ver mais sobre os metadados nesse conteúdo.

Metadados são **dados que descrevem dados**. Com eles é possível compreender os dados através do tempo. E são as **meta tags** que são responsáveis por marcar esses dados no documento HTML.

Você com certeza já presenciou o resultado de uma aplicação que utilizou de informações inseridas em meta tags, como por exemplo, **o texto que descreve sobre uma página em um resultado de busca no Google**, como no exemplo abaixo.

![](<../.gitbook/assets/image (13).png>)

Meta tags são etiquetas para **marcam e descrevem informações relacionadas ao website** para que determinadas aplicações possam utilizadas. São responsáveis, por exemplo, por informar sobre dados como uma descrição do conteúdo da página, seu autor, data de criação, entre outras informações.

Começamos com o cabeçalho padrão que usamos até agora.

```markup
    <head>
        <meta charset="utf-8" />
        <title>Meu site pessoal sobre música</title>
    </head>
```

### \<title>

Nós já vimos o elemento `<title>` em ação — ele pode ser usado para adicionar um **título ao documento**, mas pode ser confundido com o elemento `<h1>`, que é usado para adicionar um título de nível superior ao conteúdo do body — as vezes também é associado como o título da página. **Mas são coisas diferentes**!

* O elemento `<h1>` **aparece na página quando é carregado no navegador** — geralmente isso deve ser usado uma vez por página, para marcar o título do conteúdo da sua página, (o título da história, ou da notícia, ou o que quer que seja apropriado para o uso).
* O elemento `<title>` é um **metadado que representa o título** de todo o documento HTML (não o conteúdo do documento).

### \<meta>

O `<meta>` é a tag que podemos chamar de maneira "oficial" de declarar metadados em HTML. Claro, as outras coisas (como `<title>`) que estamos falando também podem ser pensadas como metadados. Existem muitos tipos diferentes de elementos `<meta>` que podem ser incluídos no cabeçalho da sua página, mas aqui estarão apenas os mais comuns.

Já vimos o funcionamento da tag `<meta>` para definir o **charset** do nosso documento, o que nos permitiu exibir caracteres de outros idiomas. Caso não lembre, veja em [Introdução a HTML](introducao-html.md).

Agora, vamos definir informações sobre autor e descrição do nosso site.

```markup
    <head>
        <meta charset="utf-8" />
        <title>Meu site pessoal sobre música</title>
        <meta name="author" content="Diogo Moreira">
        <meta name="description" content="Um site sobre música, principalmente
        indie rock">
    </head>
```

Veja que os novos elementos `<meta>` que incluimos tem atributos de `name` e  `content`:

* O `name` especifica o **tipo de elemento meta** que é; **que tipo de informação contém**.
* O `content` especifica o **conteúdo real do meta**.

Especificar um autor é útil de muitas maneiras: é útil para poder descobrir quem escreveu a página, se quiser enviar perguntas sobre o conteúdo que você gostaria de contacta-la. Alguns sistemas de gerenciamento de conteúdo possuem ferramentas para extrair automaticamente as informações do autor da página e disponibilizá-las para seus propósitos.

Além de autor e descrição da página, também podemos adicionar as palavras-chave do nosso site.

```markup
<meta name="keywords" content="Música, Rock, Indie Rock">
```

Lembre-se que adicionar todo tipo de palavras-chave na expectativa que seu site seja encontrado por meio de mais palavras não é eficiente. Os mecanismos de busca como o google conseguem identificar se as palavras-chave realmente estão relacionadas ao conteúdo de seu site.

### \<link>

A tag `<link>` especifica as **relações entre o documento atual e um recurso externo** (arquivos .css, ícones e outros recursos). Este elemento é mais usado para vincular as folhas de estilo (CSS), que será nosso próximo módulo da disciplina.

#### Adicionando um ícone para a seção de favoritos

Para enriquecer ainda mais o design do seu site, você pode adicionar referências a **ícones personalizados em seus metadados**, e estes serão exibidos em determinados contextos. O mais usado é o **favicon** (abreviação de "favorites icon", referindo-se ao seu uso nas listas "favoritos" nos navegadores). Esse ícone também aparece nas abas dos navegadores, com mostrado abaixo.

![](<../.gitbook/assets/Screen Shot 2020-10-05 at 11.12.58.png>)

Um **favicon** pode ser adicionado à sua página:

1. Salvando-o no mesmo diretório que a página de índice do site, salvo no formato `.png`, de preferência.
2. Adicionando a seguinte linha ao HTML `<head>` para fazer referência a ele:

```markup
<link rel="shortcut icon" href="favicon.png" type="image/x-icon">
```

Os ícones de favoritos hoje vão muito além dos navegadores de computador, estando também nos celulares em tamanhos diferentes para dispositivos com resoluções maiores. Para gerar essas metatags de maneira rápida, você pode usar o [Favicon Generator](https://realfavicongenerator.net/).

### Outras metatags e redes sociais

Ao navegar pela web, você também encontrará outros tipos de metadados. Muitos dos recursos que você verá em sites são criações **proprietárias,** projetados para fornecer a determinados sites (como redes sociais) informações específicas que eles podem usar.

O [Open Graph Protocol](https://ogp.me/) do Facebook é um exemplo disso. É pelo uso das suas metatags que ele consegue identificar o que tem dentro de um link e criar uma pré-visualização de um produto, de um vídeo ou de uma imagem, como mostrado abaixo.

![](<../.gitbook/assets/image (12).png>)

Outras redes sociais como Twitter também dispõe desse tipo de metadados, ficando a cargo dos desenvolvedores adequarem seus sites para essas redes sociais. O site [`metatags.io`](https://metatags.io/) disponibiliza uma ferramenta para gerar metadados automaticamente para várias redes sociais e ajuda a visualizar como elas serão vistas pelo usuário em diferentes meios, inclusive no Google.
