# autorate-mysql-server

# Steps to run the mysql server

## Run the container first

`docker container run -d -p 3306:3306 --name autorate-mysql-server mysql/mysql-server:latest`

## Copy the sql file into the container

`docker cp carstats.sql autorate-mysql-serve:/`

## Get the automatically generated password

`docker logs autorate-mysql-server 2>&1 | grep GENERATED`

## Go into the container using the above password

`docker container exec -it autorate-mysql-serve mysql -u root -p`

## Change the mysql root password

Replace **password** with your own password

`ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';`

## Run the sql file to create the database structure

`source carstats.sql`
