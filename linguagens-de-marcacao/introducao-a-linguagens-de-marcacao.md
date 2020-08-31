# Introdução a Linguagens de Marcação

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

### 

### Exemplo de linguagens de marcação no dia-a-dia





\*\*\*\*



