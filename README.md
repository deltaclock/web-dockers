# Dockers Setup

`sudo docker build -t "node:ecsc" -f node.docker .`

`sudo docker run --network host --name nodejs --hostname nodejs -v $HOME/node:/home/host -itd node:ecsc`

## For dbs

```
sudo docker run --network host --name mysql -e MYSQL_ROOT_PASSWORD=root -d mysql
sudo docker exec -it mysql mysql -uroot -p
sudo docker run --network host --name post -e POSTGRES_PASSWORD=root -d postgres
sudo docker exec -it post psql -U postgres
sudo docker run --network host --name mongo -d mongo
sudo docker exec -it mono mongo
```
