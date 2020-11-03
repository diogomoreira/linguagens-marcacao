# Elementos de bloco e linha

Todos os elementos HTML podem ser separados em dois grupos, em termos de comportamento visual CSS: elementos bloco \(`block`\) e elementos em linha \(`inline`\). Ser bloco ou em linha muda o **comportamento visual do elemento**, além de outras características.

**Elementos bloco** ocupam **todo o espaço horizontal** disponível e iniciam uma nova linha no documento. Novos elementos irão começar na próxima linha livre. Exemplos de elementos bloco são:

* `div` \(bloco genérico\)
* `h1` até `h6` \(títulos\)
* `p` \(parágrafo\)
* `blockquote` \(citação em bloco\)
* `ul` \(lista não ordenada\)
* `ol` \(lista ordenada\)

Já os **elementos em linha** ocupam apenas o espaço necessário e não iniciam uma nova linha. São chamados elementos em linha justamente por aparecer na mesma linha que outros elementos, caso seja possível. Exemplos de elementos em linha são:

* `span` \(tag em linha genérica\)
* `strong` \(destaca importância\)
* `em` \(ênfase\)
* `a` \(âncora, usada para links\)
* `img` \(imagem\)

Uma página HTML é feita de **blocos empilhados**. Dito isso, muitas vezes iremos **inserir um elemento dentro de outro para conseguirmos construir um layout adequado** e com a hierarquia de informações que desejamos. E agora que entendemos sobre elementos de bloco e de linha, algumas regras principais devem serem notadas:

* **Elementos bloco** podem conter qualquer elemento em linha;
* **Elementos bloco podem conter outros elementos bloco**, observadas algumas restrições, como colocar uma `<div>` dentro de um parágrafo, embora o contrário seja possível.
* **Elementos em linha nunca poderão conter elementos bloco**, observada algumas exceções, como o caso de `<a>` que pode englobar elementos de bloco.
* Elementos em linha podem conter outros elementos em linha

Além das diferenças já apresentadas, elementos bloco ou em linha também **diferem nas propriedades CSS que podem ser aplicadas**. **Elementos em linha** podem ter os seguintes tipos de propriedades modificadas: cores de texto e de fundo; propriedades de texto, como `font-family`, `font-size` e outras, como `text-decoration`; e bordas. **Elementos bloco**, além de todas as propriedades dos elementos em linha, também podem ter modificadas: Largura \(`width`\) e altura \(`height`\); Margens internas \(`padding`\) e externas \(`margin`\). Essas últimas serão importantes para entender [Box Model](box-model.md).

