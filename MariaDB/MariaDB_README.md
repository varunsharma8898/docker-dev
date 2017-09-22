# MariaDB Docker setup

## To pull MariaDB image
Pulling the latest image:
```
docker pull mariadb:latest
```
Or using a particular version:
```
docker pull mariadb:10.3
```

## To run a specific version directly
```
docker run --name vsharma-mariadb -e MYSQL_ROOT_PASSWORD=mypass -d mariadb:10.3
```

## To take data dump in SQL format
Data dump of all the databases:
```
docker exec vsharma-mariadb sh -c 'exec mysqldump --all-databases -uroot -p"$MYSQL_ROOT_PASSWORD"' > /Users/sharmava/mariadb/all-databases.sql
```
Or a particular database:
```
docker exec vsharma-mariadb sh -c 'exec mysqldump --databases varundb -uroot -p"$MYSQL_ROOT_PASSWORD"' > /Users/sharmava/mariadb/varundb.sql
```

## To import all the data from previously dumped sql file
```
docker exec -i vsharma-mariadb mysql -uroot -pmypass < /Users/sharmava/mariadb/all-databases.sql 
```

## To find out IPAddress
This can also be used to find out a lot more info like port number. Use this data in your app in other docker containers to connect to this MariaDB container.
```
docker inspect vsharma-mariadb
``` 

## To connect MariaDB from another docker container
Use the IPAddress found from the previous step. I've not setup any user, so using the root user and a simple password used in one of the earlier steps.
```
docker run -it --link=vsharma-mariadb -v /Users:/Users github/vsharma-dockerdev /bin/bash

mysql -h vsharma-mariadb -u root -p
```

## For more info:
Check out MariaDB's official [docker repository](https://hub.docker.com/_/mariadb/) or [knowledge base](https://mariadb.com/kb/en/library/).

