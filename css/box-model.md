# Box Model

Todos os elementos dentro de um documento HTML estão estruturados como uma caixa retangular. Essa idéia é composta por **quatro partes,** que podem ser visualizadas na imagem abaixo

* conteúdo
* espaçamento
* bordas
* margens

![Box Model](https://lh5.googleusercontent.com/EwEr2gBZJZf\_Mr5RoxCmjaWTQsHVsjlUHPX8V1U8Wb5zUaYJnvGa-ZpHxhEydrpBE1QxudY2Goulg6eTsqabP\_IkyCy1UQA3H8dXobfOZaGi777u3\_nodS5B66gTbZLxYyC1SiMCDOU)

Nesse exemplo, o **Conteúdo** é o que inserimos de informação dentro de uma tag como `<p>` por exemplo, o texto que irá aparecer para o usuário ao acessar o site. As demais partes são explicadas abaixo:

### Border / Borda

Estas propriedades são usadas para definir o **estilo**, **cor** e **espessura** da borda do elemento.

* **Propriedades**:
  * `border-style` (Estilo)
  * `border-width` (Espessura em pixels)
  * `border-color` (Cor)
  * `border` (Abreviação para definir todos)

Exemplos de border podem ser encontrados [aqui](https://codesandbox.io/s/07-border-u7q17?file=/index.html).

### Padding / Espaçamento

A propriedade padding se destina a criar um espaçamento interno em um um box entre seus 4 lados e a área de conteúdo. Os valores devem ser colocados em **porcentagem** (%) ou um **valor fixo** (em pixels).

* **Propriedades**:
  * `padding-top` (Superior)
  * `padding-right` (Direita)
  * `padding-bottom` (Inferior)
  * `padding-left` (Esquerda)
  * `padding` (Abreviação para definir todos)

Exemplos de padding podem ser encontrados [aqui](https://codesandbox.io/s/06-padding-96lcc).

### Margin / Margem

A propriedade margin se destina a criar uma **margem externa** de um elemento HTML, podendo ser para outros elementos ou para os cantos da tela. Os valores devem ser colocados em **porcentagem** (%) ou um **valor fixo** (em pixels)

* **Propriedades**:
  * `margin-top` (Superior)
  * `margin-right` (Direita)
  * `margin-bottom` (Inferior)
  * `margin-left` (Esquerda)
  * `margin` (Abreviação para definir todos)

Exemplos de margin podem ser encontrados [aqui](https://codesandbox.io/s/08-margin-1t3gy?file=/index.html).

### Usando o inspetor de elementos para visualizar um Box Model

Uma boa maneira de visualizar o Box model de qualquer elemento é usando o "Inspetor de Elementos", uma ferramenta que acompanha a maioria dos browsers modernos, como Chrome e Firefox. Ao clicar com o botão direito em um elemento de selecionar a opção "**Inspecionar Elemento**", seremos apresentados a uma tela semelhante a tela abaixo:

![](<../.gitbook/assets/Screen Shot 2020-11-03 at 15.03.12.png>)

Essa ferramenta mostra o código HTML (canto superior direito) e demais informações como CSS e Box Model (canto inferior direito, aba "**Layout**"). Veja que a figura da ferramenta é semelhante a que vimos aqui, evidenciando os valores para cada uma das propriedades, tornando mais fácil o trabalho de estilizar nossos componentes.

O inspetor de elementos é uma ferramenta poderosa para auxiliar no desenvolvimento de um website, e você pode encontrar mais sobre ele no vídeo abaixo ou [aqui](https://goomore.com/blog/inspecionar-elemento/).

{% embed url="https://www.youtube.com/watch?v=lb8T8CLebDA" %}



