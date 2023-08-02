# Docker - Comandos

## Principais comandos do Docker

#### Principais Argumentos
```
-d => detached   # Inicia o container com se estivesse em segundo plano
-r => 
-m => 
-t => 
-i => 
```

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

#### Cria um container de nome NomeContainer na rede minha-bridge e expõe a porta 3000
```
docker run -d --network minha-bridge --name NomeContainer -p 3000:3000 imagem:1.0
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
```
docker container run -ti --mount type=bind,src=/CaminhoHost,dst=/CaminhoContainer debian
```

#### Criar um container com um volume do tipo Bind somente leitura
```
docker container run -ti --mount type=bind,src=/CaminhoHost,dst=/CaminhoContainer,ro debian
```

#### Remove todos os container que não estão em uso
```
docker container prune
```
