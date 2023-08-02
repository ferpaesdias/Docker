# Docker - Comandos

## Principais comandos do Docker

#### Instalação do Docker independente da distribuição Linux
```
curl -fsSL https://get.docker.com/ | bash
```

#### Listar containers
```
docker container ls
docker ps
```

#### Instalar e executar o container Hello-World
```
docker container run -ti hello-world
```

#### Remover um container
```
docker container rm CONTAINER_ID
docker container rm -f CONTAINER_ID
```

#### Remover um container
```
docker container rm CONTAINER_ID
```

#### Instalar e executa o container NGINX com limite de 128 MB de memória RAM e 0,5 core CPU
```
docker container run -d -m 128M --cpu 0.5 nginx
```

#### Atualizar CPU e memória de um  container durante a sua execução
```
docker container update --cpus 0.8 -m 64M CONTAINER_ID
```

#### Acessar um container que está rodando como daemon (pode ser o bash ou sh)
```
docker container exec -ti CONTAINER_ID /bin/bash
docker container exec -ti CONTAINER_ID /bin/sh
```

#### Iniciar um container
```
docker container start CONTAINER_ID 
```

#### Reiniciar um container
```
docker container restart CONTAINER_ID 
```

#### "Pausar" um container
```
docker container pause CONTAINER_ID 
```

#### "Despausar" um container
```
docker container unpause CONTAINER_ID 
```

#### Mostrar detalhes de um container
```
docker container inspect CONTAINER_ID 
```

#### Mostra o consumo de recursos de um container
```
docker container stats CONTAINER_ID
```

#### Criar um container com um volume do tipo Bind

```bash
docker container run -ti --mount type=bind,src=/opt/giropops,dst=/giropops debian
```

#### Criar um container com um volume do tipo Bind somente leitura
```bash
docker container run -ti --mount type=bind,src=/opt/giropops,dst=/giropops,ro debian
```

#### Remove todos os container que não estão em uso
```
docker container prune
```
