#Docker-Compose Example
Docker and Docker Compose Example.

2 Microservices (hello and bye) that publish 2 services (/hello and /bye) <hr>
Docker Files are created in order to generate images bye:<hr>
docker build -pXXXX/8080 helloserver:latest<hr>
docker build -pXXXX/8081 byeserver:latest.<hr>
<hr>
In order to execute docker-compose <hr>
docker-compose up -- build<hr>

In order to execute scale docker-compose :<hr>
docker-compose --file scale-docker-compose.yml up -d --build --scale byeserver=Y --scale helloserver=X<hr>
where X and Y are the number of instances of each service.<hr>
