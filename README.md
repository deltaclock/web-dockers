# Dockers Setup

## Python

`sudo docker build -t "python:ecsc" -f python.docker .`

`sudo docker run --network host --name py --hostname py -v $PWD:/home/host -it --rm python:ecsc /bin/bash`

## PHP

`sudo docker run -p 80:80 --name php --hostname php -v $PWD:/var/www/html -it --rm php:7.2-apache /bin/bash`

## NodeJS

`sudo docker run -p 3000:3000 --name node --hostname node -v $PWD:/home/host node:12.11 -it --rm /bin/bash`

## For Databases

```bash
sudo docker run --network host --name mysql -e MYSQL_ROOT_PASSWORD=root -d mysql
sudo docker exec -it mysql mysql -uroot -p
sudo docker run --network host --name post -e POSTGRES_PASSWORD=root -d postgres
sudo docker exec -it post psql -U postgres
sudo docker run --network host --name mongo -d mongo
sudo docker exec -it mongo mongo
```
