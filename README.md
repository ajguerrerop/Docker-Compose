<h3>Docker and Docker Compose Example.<h3>

2 Microservices (hello and bye) that publish 2 services (/hello and /bye) <br>
Docker Files are created in order to generate images bye:<br>
docker build -pXXXX/8080 helloserver:latest<br>
docker build -pXXXX/8081 byeserver:latest.<br>

In order to execute docker-compose <br>
docker-compose up -- build<br>

In order to execute scale docker-compose :<br>
docker-compose --file scale-docker-compose.yml up -d --build --scale byeserver=Y --scale helloserver=X <br>
where X and Y are the number of instances of each service.<br>
