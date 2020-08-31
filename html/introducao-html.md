# Introdução a HTML

HTML significa em inglês: **H**yper**T**ext **M**arkup **L**anguage. Em português: **Linguagem de Marcação de Hipertexto**. Tem como objetivo descrever a estrutura de uma página web por meio de uma linguagem de marcação e é a **linguagem base da internet**. Foi criada para ser de fácil entendimento por seres humanos e também por máquinas, como por exemplo o Google ou outros sistemas que percorrem a internet capturando informação.

* Todos os documentos HTML são **documentos de texto simples**, geralmente com a extensão .html.
* Podem ser criados e editados a partir de **qualquer editor de texto**.
* É interpretado por navegadores, sejam eles em um computador, _smartphone_, TV, videogames, etc.

O documento HTML sempre inicia com o que chamamos de **estrutura básica**, que é mostrada no exemplo de código abaixo. Esta estrutura é quase que imutável.

```markup
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="utf-8" />
        <title>Diogo Moreira - Meu site pessoal sobre música</title>
    </head>
    <body>
    
    </body>
</html>
```

É possível compreender o documento em HTML de uma maneira muito simples, através de uma divisão de blocos das tags essenciais, conforme a a seguinte estrutura:

* Definição do documento \(`doctype`\)
* Documento HTML \(`html`\)
* Cabeçalho \(`head`\)
* Corpo \(`body`\)

### Definição de documento

A definição de documento **sempre** deve existir, que é este código `<!DOCTYPE html>`. Essa definição não é uma _tag_ HTML, mas uma instrução para o navegador e outros programas que podem ler seu site, informando que o código que será encontrado ali é um código HTML. Assim, eles vão saber o que fazer para mostrar seu site da melhor forma possível.

### Documento HTML

A tag `<html>` representa a raiz/o início de um documento **HTML**. Ele **deve** conter o **atributo** `lang` indicando em qual idioma o documento está escrito. No caso acima, estamos indicando que ele está escrito em **Português do Brasil** \(pt-br\)**.** Uma lista com os códigos dos idiomas pode ser encontrado [aqui](https://www.w3schools.com/tags/ref_language_codes.asp).

As tags `<head>` e `<body>` obrigatoriamente devem estar dentro de `<html>`.

### Cabeçalho

O cabeçalho \(tag `<head>`\) contém informações que **não são transpostas visivelmente para o usuário/leitor do documento**. São dados implícitos, de uso e controle do documento: vinculação com outros arquivos, aplicação de lógica de programação e [metadados](https://pt.wikipedia.org/wiki/Metadados). Na prática, todo o conteúdo do cabeçalho fica delimitado entre a abertura e fechamento tag head.

Retomando o exemplo mostrado anteriormente, preste atenção nas seguintes linhas abaixo. Elas serão suficientes por enquanto.

```markup
<meta charset="utf-8" />
<title>Diogo Moreira - Meu site pessoal sobre música</title>
```

Na primeira linha, a tag `<meta>` representa um metadado. Nesse caso em específico ele está informando ao navegador qual o conjunto de caracteres que iremos usar. Por padrão, usamos **UTF-8**, que nos permite exibir qualquer caractere de qualquer língua, incluindo japonês, chinês, coreano.

Só é possível mostrar "こんにちは", ou seja, **Konnichiwa** \(ou "Olá" em japonês\), porque esse documento está sendo mostrado com o conjunto de caracteres **"UTF-8"**.

Já na segunda linha, temos a tag `<title>` que informa qual o título do nosso site. Porém, esse título nem sempre é exibido para o usuário, por isso ele está dentro de `<head>`. Vamos ao exemplo, usando [meu website](https://diogodmoreira.com) como caso de uso:

![Exemplo de aba no navegador Firefox](../.gitbook/assets/screen-shot-2020-08-31-at-17.55.08.png)

Ao abrir um website qualquer no seu navegador, ele provavelmente será exibido em formato de aba no canto superior, informando o que está dentro da tag `<title>`. Já nos navegadores de celular, esse comportamento de abas não é padronizado. Na imagem abaixo é possível ver que o conteúdo de `<title>` foi ignorado. Embora ele seja um **elemento obrigatório**, a sua exibição fica a cargo dos navegadores/interpretadores.

![Exemplo de website no navegador Safari](../.gitbook/assets/img_daa93655c329-1.jpeg)

### Corpo

Trata-se do documento em si, ou seja, a **informação legível para o usuário/leitor do documento**. É todo e qualquer texto que se deseja apresentar, assim como toda e qualquer forma de mídia de saída \(**imagens**, **sons**, **vídeos**, etc\). Tudo que estiver no corpo do documento HTML **deve** ser exibido.

Além disso, toda a apresentação de entrada de dados \(**formulários**\) também se aplica nesta seção do documento. Na prática, o **corpo do documento** é delimitado pelo par de tags `<body>` e `</body>`.

### Considerações finais

Este é o preceito básico que deve estar bem claro para você antes de sair desse módulo: **onde as tags se aplicam**, e **quais são os resultados**. Por exemplo: se vocês deseja informar **conteúdo textual para saída legível ao usuário** do seu website, esse texto com a sua respectiva marcação deverá obrigatoriamente estar no bloco do corpo da página \(`body`\). Ainda: para definir qual o tipo de codificação da página, devemos obrigatoriamente marcar isso no cabeçalho do mesmo documento \(como vimos em `<meta charset="utf-8">`, que é uma meta informação do documento\).



