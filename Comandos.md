# Comandos docker

#### Obter a versão do docker:

```bash
docker version
```

#### Criar container hello world

```bash
docker run hello-world
```

#### Baixar imagem

hub.docker.com/)

```bash
# Essas imagens podem ser baixadas do Docker hub
docker pull <image>
```

#### Listar containers

Lista containers em execução

```bash
docker ps
```

Lista todos os containers, mesmo os parados

```bash
docker ps -a
```

## Integrar terminal com terminal do container

```bash
docker run -it <container>
```

## Iniciar container

```bash
docker start <container-id>
```

## Parar execução de container

```bash
docker stop <container-id>
```

## Apagar container

```bash
docker rm <container-id>
```

```bash
# Apaga todos os containers inativos
docker container prune
```

# Listar imagens

```bash
docker images
```

# Apagar imagens

```bash
docker rmi <image-id>
```
