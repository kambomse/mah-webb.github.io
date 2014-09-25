---
layout: instructions
code: me105a
title: Självstudier 4
---

<style>
table {border-collapse: collapse;font-size:smaller}
th, td {border: 1px solid #BBBBBB}
th, td {text-align:left}
th, td {padding: 6px;}
</style>

#Självstudier 4

##Uppgift 1 

Skapa tabellerna *classroom* och *building* utifrån E/R-diagrammen från självstudie 3 med lämplig SQL (CREATE TABLE classroom etc). Använd MySQL Query Browser. **OBS** Om du redan har en tabell *classroom* från självstudie 1 måste du börja med att ta bort den. Det gör du med

{% highlight sql %}
DROP TABLE classroom
{% endhighlight %} 

##Uppgift 2

Gör html och php-sidor med formulär för att mata in byggnader i tabellen *building*.

##Uppgift 3

Mata in minst två byggnader, tex Kranen och Ubåtshallen.

##Uppgift 4

Gör formulär för att mata in sal i tabellen *classroom*. Man ska med en dropdownmeny kunna välja vilken byggnad en sal ligger i. 

##Uppgift 5

Mata in några salar i de olika byggnaderna. 

