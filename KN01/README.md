#### 1. Überprüfen der Docker-Version
- Befehl:
  ```bash
  docker version
 
 ![Mein Bild](/KN01/2.png)
 ![Mein Bild](/KN01/1.png)

#### 2. Suche nach offiziellen Docker-Images auf Docker Hub
- Befehl:
  ```bash
  docker search ubuntu
  docker search nginx
![Mein Bild](/KN01/3.png)
![Mein Bild](/KN01/4.png)
![Mein Bild](/KN01/5.png)
 
#### 3. Erklärung des Befehls docker run -d -p 80:80 docker/getting-started
- Befehl:
  ```bash
  docker run -d -p 80:80 docker/getting-started

![Mein Bild](/KN01/6.png) 
###### Erklärung:
- docker run: Startet einen neuen Container.
 
- d: Startet den Container im Hintergrund (detached mode).
 
- p 80:80: Leitet den Port 80 des Hosts auf den Port 80 im Container um.
 
- docker/getting-started: Spezifiziert das Docker-Image, das gestartet wird.

#### 4.Mit dem nginx Image verfahren Sie wie folgt. Wir zeigen, dass der Befehl docker run , das gleiche ist wie die drei Befehle docker pull , docker create und docker start hintereinander ausgeführt.

1. docker pull nginx
docker create --name mein-nginx -p 8081:80 nginx
docker start mein-nginx

#### 5.Mit dem ubuntu Image verfahren Sie wie folgt. Wir zeigen, dass nicht jedes Image im Hintergrund ausgeführt werden kann.

docker run -d ubuntu: Startet einen Container mit dem Ubuntu-Image im Hintergrund. Da Ubuntu keine dauerhafte Hintergrundaufgabe ausführt, wird der Container nach dem Start sofort wieder beendet, falls keine spezifische Aufgabe angegeben ist.
docker run -it ubuntu: Startet den Ubuntu-Container interaktiv mit einer Shell. Sie können Befehle innerhalb des Containers ausführen, und der Container bleibt aktiv, solange die interaktive Shell offen ist.

#### 6.Stellen Sie sicher, dass Ihr nginx-Container bereits läuft. Öffnen Sie nun nachträglich eine interaktive Shell. Der Unterschied zu vorher ist, dass Sie nicht den Container mit interactiver Shell starten, sondern eine Shell eines laufenden Containers öffnen. Der Befehl ist docker exec -it <name-ihres-container> /bin/bash

 docker rmi nginx ubuntu

 ![Mein Bild](/KN01/7.png)