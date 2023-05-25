# VOLUME

docker containers are ephemeral when you remove container by default it will delete the data.

# craete volume

docker volume create mysql-data

docker run -d -p 80:80 -v mysql-data:/var/lib/mysql mysql

# wih password

docker run -d -p 80:80 -v mysql-data:.var.lib.mysql -e MYSQL_ROOT_PASSWORD=... mysql

host path : /var/lib/docker/volumes/mysql-data/_data/

continer path : /var/lib/mysql

