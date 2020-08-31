# Exemplo de Linguagem de marcação

Um exemplo que podemos observar de linguagens de marcação são os chamados **feeds RSS**, para assinatura de **notícias**, **podcasts** e etc. Observe o trecho abaixo, que foi retirado do **RSS de notícias do G1 Paraíba.** Você não precisa entender ele por completo agora, mas veja que temos algumas indicações de que isso é uma **notícia**. O conteúdo dentro de `<title>`, por exemplo, nos diz qual o título da notícia.

```markup
<item>
    <title>Alerta de baixa umidade é emitido pelo Inmet para 100 municípios na PB</title>
    <link>https://g1.globo.com/pb/paraiba/noticia/2020/08/31/alerta-de-baixa-umidade-e-emitido-pelo-inmet-para-100-municipios-na-pb.ghtml</link>
    <description>
        <img src="https://s2.glbimg.com/xA6DG_xEJ94emHnCfOTs49ZGID4=/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2020/q/2/BNLtmNRcAHYAeiCMGj1g/inmet.jpg" />
        <br />Instituto recomenda que a população desses municípios beba bastante líquido e evite desgaste físico nas horas mais secas. Inmet emite alerta de baixa umidade para 100 municípios
        da Paraíba Reprodução/Inmet Um alerta amarelo de baixa umidade para 100 municípios da Paraíba foi emitido pelo Instituto Nacional de Meteorologia (Inmet). O aviso começou às 12h desta
        segunda-feira (31) até as 18h de terça-feira (1°). Moradores de municípios em alerta devem evitar desgaste físico nas horas mais secas, e exposição ao sol nas horas mais quentes do dia,
        segundo o Inmet. É recomendado que se beba bastante líquido. A umidade relativa do ar varia entre 30% e 20%. Existe baixo risco de incêndios florestais e à saúde.
    </description>
    <pubDate>Mon, 31 Aug 2020 16:48:06 -0000</pubDate>
</item>
```

A maneira como os vários interpretadores veem esse tipo de conteúdo é diferente, um navegador da web vai mostrar de uma maneira, um [**leitor de RSS**](https://www.oficinadanet.com.br/post/11004-alternativas-google-reader) ****de uma outra maneira e assim por diante. Abaixo, a notícia evidenciada no código sendo exibida pelo leitor de rss **Feedly**.

![Not&#xED;cias do G1 Para&#xED;ba na interface do leitor de RSS Feedly](../.gitbook/assets/screen-shot-2020-08-31-at-14.38.16.png)

O importante é que o **conteúdo** é o mesmo. As diferentes formas de **exibir informação** só são possíveis graças as linguagens de marcação. ****Durante o nosso curso iremos aprender a utilizar linguagens de marcação, mais especificamente **HTML**, **CSS** e **XML**. Porém, entendendo os conceitos que iremos ver na disciplina, será fácil entender outras linguagens caso você precise na sua vida profissional.

