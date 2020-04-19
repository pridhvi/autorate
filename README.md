# Autorate

A Java Web Application which is a forum for car enthusiasts.

# Build Maven project

Change directory to the respective directories (frontend or backend)

Run the following command

`mvn clean install`

A .war or ,jar file will be generated inside the target directory for frontend and backend respectively

# Run the docker container

## Front End

`docker container run -d -p 8080:8080 --name autorate-frontend pridhvi/autorate-frontend:latest`

## Back End

`docker container run -d -p 8081:8081 --name autorate-backend pridhvi/autorate-backend:latest`