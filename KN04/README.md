# KN04 - Docker Compose

## A) Docker Compose: Lokal

### Teil A) Verwendung von Original Images

![](./Images/1.png)

![](./Images/2.png)

![](./Images/3.png)

![](./Images/4.png)

![](./Images/5.png)

Docker compose up baut / (neu)erstellt, startet und verbindet alle containers, die im docker compose datei definiert werden.

### Teil B) Verwendung Ihrer eigenen Images 

![](./Images/6.png)

![](./Images/7.png)

Der Fehler kommt vor, da wir die werte für db login hard codiert haben, können wir nicht einfach verbinden. Wir könnten im Docker Compose eine environment und im db.php die werte von systemvariable benutzten. da ist es viel einfacher, einstellungen setzen

## B) Docker Compose: Cloud

![](./Images/8.png)

![](./Images/9.png)

![](./Images/10.png)

![](./Images/11.png)

![](./Images/12.png)

