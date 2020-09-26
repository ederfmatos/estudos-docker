# Estudos sobre docker

Este repositório contém minhas anotações sobre docker.

#### Github Docker: [https://github.com/docker](https://github.com/docker)

## Sumário

- [1 - Containers](./Containers.md)
- [2 - Comandos](./Comandos.md)
- [3 - Volumes](./Volumes.md)
- [4 - Redes](./Redes.md)

## Cursos

### Em andamento

- [x] [Docker: Criando containers sem dor de cabeça - Alura](https://www.alura.com.br/curso-online-docker-e-docker-compose)

# Principais comandos

## Comandos relacionados às informações

### Exibe a versão do docker que está instalada.

```bash
docker version
```

### Retorna diversas informações sobre o container.

```bash
docker inspect ID_CONTAINER
```

### Exibe todos os containers em execução no momento.

```bash
docker ps

```

### Exibe todos os containers, independentemente de estarem em execução ou não.

```bash
docker ps -a
```

## Comandos relacionados à execução


### Cria um container com a respectiva imagem passada como parâmetro.

```bash
docker run NOME_DA_IMAGEM
```

### Conecta o terminal que estamos utilizando com o do container.

```bash
docker run -it NOME_DA_IMAGEM
```

### Ao executar, dá um nome ao container e define uma porta aleatória.

```bash
docker run -d -P --name NOME dockersamples/static-site
```

### Define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.

```bash
docker run -d -p 12345:80 dockersamples/static-site
```

### Cria um volume no respectivo caminho do container

```bash
docker run -v "CAMINHO_VOLUME" NOME_DA_IMAGEM
```

### Cria um container especificando seu nome e qual rede deverá ser usada.

```bash
docker run -it --name NOME_CONTAINER --network NOME_DA_REDE NOME_IMAGEM
```

## Comandos relacionados à inicialização/interrupção

### Inicia o container com id em questão.

```bash
docker start ID_CONTAINER
```

### Inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.

```bash
docker start -a -i ID_CONTAINER
```

### Interrompe o container com id em questão.

```bash
docker stop ID_CONTAINER
```

## Comandos relacionados à remoção

### Remove o container com id em questão.

```bash
docker rm ID_CONTAINER
```

### Remove todos os containers que estão parados.

```bash
docker container prune
```

### Remove a imagem passada como parâmetro.

```bash
docker rmi NOME_DA_IMAGEM
```

## Comandos relacionados à construção de Dockerfile

### Cria uma imagem a partir de um Dockerfile.

```bash
docker build -f Dockerfile
```

### Constrói e nomeia uma imagem não-oficial.

```bash
docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM
```

### Constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.

```bash
docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM CAMINHO_DOCKERFILE
```

## Comandos relacionados ao Docker Hub

### Inicia o processo de login no Docker Hub

```bash
docker login
```

### Envia a imagem criada para o Docker Hub

```bash
docker push NOME_USUARIO/NOME_IMAGEM
```

### Baixa a imagem desejada do Docker Hub

```bash
docker pull NOME_USUARIO/NOME_IMAGEM
```

## Comandos relacionados à rede

### Mostra o ip atribuído ao container pelo docker (funciona apenas dentro do container)

```bash
hostname -i
```

### Cria uma rede especificando o driver desejado.

```bash
docker network create --driver bridge NOME_DA_REDE
```

## Comandos relacionados ao docker-compose

### Realiza o build dos serviços relacionados ao arquivo docker-compose.yml, assim como verifica a sua sintaxe.

```bash
docker-compose build
```

### Sobe todos os containers relacionados ao docker-compose, desde que o build já tenha sido executado.

```bash
docker-compose up
```

### Para todos os serviços em execução que estejam relacionados ao arquivo docker-compose.yml

```bash
docker-compose down
```

### Lista os serviços que estão rodando.

```bash
docker-compose ps
```

### Executa o comando ping node2 dentro do container alura-books-1

```bash
docker exec -it alura-books-1 ping node2
```
