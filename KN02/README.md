
KN02 Dockerfile

## A) Dockerfile I

```docker
FROM nginx # nimm die docker image from nginx
COPY static-html-directory /var/www/html # kopiere die html ordner vom host auf das html verzeichnis im docker image
EXPOSE 80 # veröffentliche das Port 80 vom image
```

`docker build -t name:tag .`

![](./Images/1.png)  

![](./Images/2.png)

![](./Images/3.png)

![](./Images/4.png)

![](./Images/5.png)

## B) Dockerfile II

Befehle:

`docker build -t sairamtbz/m347:kn02b-db -f db.dockerfile .`

`docker build -t sairamtbz/m347:kn02b-web -f web.dockerfile .`

`docker run -d -p 3306:3306 --name KN02-db sairamtbz/m347:kn02b-db`

`docker run -d -p 5600:80 --name KN02-web --link KN02-db sairamtbz/m347:kn02b-web`

`docker push sairamtbz/m347:kn02b-web`

![](./Images/6.png)

![](./Images/7.png)

![](./Images/8.png)

![](./Images/9.png)

![](./Images/10.png)