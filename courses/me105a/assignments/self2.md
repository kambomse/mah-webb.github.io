---
layout: instructions
code: me105a
title: Självstudier 2
---
<style>
table {border-collapse: collapse;font-size:smaller}
th, td {border: 1px solid #BBBBBB}
th, td {text-align:left}
th, td {padding: 6px;}
</style>



#Självstudier 2

##Uppgift 1

Gör en sida *showrooms.php* som visar alla rum och antal platser i rummen som finns lagrade i tabellen *classroom* från föreläsning 1 och självstudieuppgift 1.

##Uppgift 2

Gör en sida *showrooms.php* som visar alla rum och antal platser i rummen som finns lagrade i tabellen *classroom* men nu ska de vara sorterade i stigande ordning med minst antal platser först och flest antal platser sist i listan.

Vi har inte gått igenom hur man sorterar ett sökresultat från en databas än. För att lösa denna uppgift kan du t. ex. googla "sort sql"

##Lösning uppgift 1

###showrooms.php:

{% highlight php %}
<?php
//ändra userid till ditt eget
include $_SERVER['DOCUMENT_ROOT'].'/userid/me105a/connect.php';

$sql="SELECT * FROM classroom";
$result=$pdo->query($sql);

foreach ($result as $row) {
	$roomnumber=$row['roomnumber'];
	$seats=$row['seats'];
	
	echo "$roomnumber har $seats platser";
	echo "<br>";
}
?>
{% endhighlight %}

##Lösning uppgift 2

Ändra SELECT-raden till

{% highlight php  startinline=True %}
$sql="SELECT * FROM classroom ORDER BY seats";
{% endhighlight %}





