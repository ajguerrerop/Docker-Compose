#Docker-Compose Example
Docker and Docker Compose Example.

2 Microservices (hello and bye) that publish 2 services (/hello and /bye)

Docker Files are created in order to generate images bye:
docker build -pXXXX/8080 helloserver:latest
docker build -pXXXX/8081 byeserver:latest.

In order to execute docker-compose 
docker-compose up -- build

In order to execute scale docker-compose :
docker-compose --file scale-docker-compose.yml up -d --build --scale byeserver=Y --scale helloserver=X
where X and Y are the number of instances of each service.
