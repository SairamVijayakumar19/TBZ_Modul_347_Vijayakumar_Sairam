# KN03 - Netzwerk, Sicherheit

## A) Eigenes Netzwerk

```bash
docker network create -d bridge tbz 
```

```bash
docker run --network=tbz -d --name=busybox-1 busybox
```

`docker inspect busybox-n`

`docker inspect tbz`

`docker inspect bridge`

TBZ netzwerk:

-  "Subnet": "172.18.0.0/16"
-  "Gateway": "172.18.0.1"

Busybox-1: 172.17.0.5

Busybox-2: 172.17.0.6

Busybox-3: 172.18.0.2

Busybox-4: 172.18.0.3

Busybox-1 Default Gateway: 172.17.0.1

Busybox-4 Default Gateway: 172.18.0.1

![](1.png)

![](2.png)

![](3.png)

Der Unterschied ist, dass beim default bridge, dass sie teilweise verbunden sind, aber nur durch das Ip ist, das sich in der Zeit verändern kann. Wenn ich aber mein eigenes Netzwerk erstelle. kann ich auch dass container namen benutzen, dass sich nicht in der Zeit verändert.

In KN02 befanden sich die Container im gleichen Gateway, aber sie konnten nicht durch den container name kommunizieren. mit dem Link, verbinde ich den neme mit der Ip-Adresse uns so konnte der Container kommunizieren.