
## Build Docker
docker build -t brunopassi/app-validador-cpf-java -f Dockerfile .

## Build Docker com tag
docker build -t brunopassi/app-validador-cpf-java:0.0.1 -f Dockerfile .

## Build Docker and run
sudo docker run -d -p 8080:8080 --name app-validador-cpf-java  brunopassi/app-validador-cpf-java

## Build watch Docker
docker run -it -p 80:3000 --name app-imersao-docker-nodejs didox/app-imersao-docker-nodejs

# Para parar o docker
docker stop app-validador-cpf-java

# Para startar o docker
docker start copiad id do docker

# para remover a imagem do docker
docker rm app-validador-cpf-java

# para depurar
docker attach app-imersao-docker-nodejs

# entra dentro do container
docker exec -it app-validador-cpf-java bash
docker exec -it app-validador-cpf-java /bin/sh
docker exec -it app-validador-cpf-java /bin/bash

# roda comando dentro do container
docker exec -it app-imersao-docker-nodejs ls -la

# para ver logs
docker logs app-imersao-docker-nodejs -f --tail 100

# Gerar a tag da imagem no docker hub, coloca como latest
docker tag brunopassi/app-validador-cpf-java hub.docker.com/r/brunopassi/app-validador-cpf-java

# Gerar a tag da imagem no docker hub, com tag 0.0.1
docker tag brunopassi/app-validador-cpf-java hub.docker.com/r/brunopassi/app-validador-cpf-java:0.0.1

# Publicar a imagem no docker hub, para o latest
docker push brunopassi/app-validador-cpf-java

# Publicar a imagem no docker hub, para o tag 
docker push brunopassi/app-validador-cpf-java:0.0.1



