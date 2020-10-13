# Classe

Classe \(ou `class`\) é um **atributo global** e é reutilizável: pode se repetir em vários elementos na página e também combinar-se com outras \(podemos pôr mais de uma classe em um elemento\).

A diferença de identificador e classe é que, no primeiro caso, um único elemento é associado, já na classe vários elementos são associados e cada elemento também pode fazer parte de várias classes. 

Observe a figura abaixo. Todos os botões tem a mesma aparência em relação a altura, tamanho da fonte e espaçamento entre eles, o que evidencia a possibilidade de usarmos uma **classe**. Já o primeiro elemento tem uma cor de fundo diferente, o que poderia indicar um uso de **identificador**.

![](../../.gitbook/assets/image%20%2810%29.png)

É perfeitamente possível fazer um site apenas com ids, apenas com classes, com uma combinação das duas, ou sem nenhuma das duas. Tudo irá depender do seu estilo de fazer o código das páginas. O importante é **definir um padrão e segui-lo**.

Observe o exemplo abaixo, onde temos uma lista \(ver [Listas](../../html/listas.md)\) que vai representar um **menu** na nossa aplicação. Veja que todos os itens de lista tem a mesma classe `item-menu`.

```markup
<ul id="menu">
  <li class="item-menu">Início</li>
  <li class="item-menu">Recomendações de bandas</li>
  <li class="item-menu">Minha playlist</li>
</ul>
```

Sendo assim, podemos usar apenas **um seletor** para estilizar todos esses elementos de uma vez.

```css
.item-menu {
  font-weight: bold;
  font-size: 20px;
  color: navy;
}
```

No exemplo acima, definimos que o texto terá fonte em **negrito** \(bold\), tamanho de **20 pixels** e cor **azul-marinho** \(navy\). O exemplo pode ser [encontrado aqui](https://codesandbox.io/s/03-seletor-classes-6d51u?file=/estilo.css).

