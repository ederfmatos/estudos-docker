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

# Detach terminal

```bash
# Roda um comando sem travar o terminal
docker run -d <container-id>
```

# Saber porta de container

```bash
docker port <container-id>
```

# Nomear container

```bash
--name <container-name>

# Exemplo:

docker run --name meu-linux ubuntu
```

# Mapear porta da propria maquina para o docker

```bash
docker run -p <porta-maquina>:<porta-docker>

# Exemplo
docker run -p 1234:80 dockersamples/static-site
```

# Listar id's de containers ativos

```bash
docker ps -q
```

# Parar todos os containers ativos

```bash
docker stop -t 0 $(docker ps -q)
```
