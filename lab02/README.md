## Tarefa sobre catálogo de componentes

![Notebook](https://github.com/jep84/inf331/blob/master/lab02/notebook/components-01-catalog.ipynb)

## Tarefa Web Components 1

```xml
<dcc-trigger label="Mundo"
             action="noticia/mundo/politica"
             value="Donald Trump derruba muro na fronteira com México e inaugura programa de incentivo à imigração para o país do Tio Sam!">
</dcc-trigger>

<dcc-trigger label="BrasilP"
             action="noticia/brasil/politica"
             value="Brasil libera vacina contra Covid-19">
</dcc-trigger>


<dcc-trigger label="BrasilE"
             action="noticia/brasil/esporte"
             value="Presidente do Corinthians e Palmeiras falam em unificação dos times">
</dcc-trigger>


<dcc-trigger label="Bahia"
             action="noticia/bahia/esporte"
             value="Estudo comprova que Acarajé pode atenuar efeitos da Covid-19">
</dcc-trigger>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Olá! ">
  <subscribe-dcc topic="noticia/#/politica"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="Olá! ">
  <subscribe-dcc topic="noticia/(brasil|bahia)/#"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="Olá! ">
  <subscribe-dcc topic="noticia/#"></subscribe-dcc>
</dcc-lively-talk>
```

## Tarefa Web Components 2

```xml
<dcc-trigger label="Next Item" action="next/rss">
</dcc-trigger>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="News ">
  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="News ">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="News ">
  <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
```
