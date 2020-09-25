# Redes

### Criar uma rede

```shell
docker network create --driver bridge <network-name>
```

### Listar redes

```bash
docker network ls
```

### Criar container conectado à uma rede docker

```bash
docker run --name <container-name> --network <network-name> <image>
```
