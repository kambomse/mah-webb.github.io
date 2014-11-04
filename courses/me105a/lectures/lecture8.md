---
layout: instructions
code: me105a
title: Föreläsning 8
controls: false
date: 2014-11-03
theme: bopeterson/cleaver-lecture
---

<style>
table {border-collapse: collapse;font-size:smaller}
th, td {border: 1px solid #BBBBBB}
th, td {text-align:left}
th, td {padding: 6px;}
hr {display: none}
pre {font-size:large}
li {text-align:left}
.content {text-align:left}
</style>

# Databasbaserad publicering

## Föreläsning 8

### Dagens innehåll

- Normalisering - läs mer på <http://www.databasteknik.se/webbkursen/normalisering/index.html>
- Export av data

### Normalisering


**studentnamn** är funktionellt beroende av **studentid**. Det kan skrivas

	studentid -> studentnamn



    {studentid,labnr} -> labstatus. 

### Tredje normalform 3NF


Följande exempel uppfyller inte första normalformen. Förutsättningen är att en person kan ha endast en adress men flera telefonnummer.
| --- | --- 

Följande exempel uppfyller 1NF men innehåller redundanta data

Vi har följande funktionella beroenden:

{% highlight text %}
studentid -> studentnamn
studentid -> postnr
studentid -> stad
{% endhighlight %}


Vi har följande funktionella beroende:

{% highlight text %}
postnr -> stad



Utöver 1NF, 2NF och 3NF finns det ytterligare normalformer, tex Boyce-Codds normalform, *BCNF*. Den kan ni läsa om på 

<http://www.databasteknik.se/webbkursen/normalisering/index.html>

### Import av data

Hur importerar man data från en databas till InDesign eller annat layoutprogram?

Första steget är att exportera data på något av de sätt som beskrevs på förra föreläsningen, tex som xml, csv, tsv eller json

Andra steget är att antingen någon av InDesigns inbyggda importfunktioner, eller att använda en plugin. 

![](im8/xml.png)

Den funktionen är kraftfull och flexibel men svåranvänd. Ett enklare men mer begränsat sätt är att använda InDesigns Data Merge-funktion:

![](im8/datamerge.png)

Data Merge-funktionen kan importera tab-separerade filer (tsv) och skapa ett innehåll med konsistent layout. 

Det finns även olika plugins till InDesign, som ger ytterligare möjligheter till automatiserad layout. Några sådana exempel  är [InData](http://emsoftware.com/products/emdata/), [CatBase](https://www.catbase.com/) och [Easy Catalog](http://www.65bit.com/software/easycatalog/). 

Vi kommer att använda dels inbyggda Data Merge, dels InData i veckans laboration. 

![](im8/indata.png)

![](im8/word.png)