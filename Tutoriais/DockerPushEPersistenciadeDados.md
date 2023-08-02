# Lista dos principais comandos utilizados em Docker


## Push de uma imagem 

É necessário tem uma conta em [Docker](https://hub.docker.com/signup).

Fazer login na sua conta com o comando abaixo e logo depois será solicitada a senha   

```docker login -u nomedousuario```  

```docker push nomedorepositorui/nomedaimagem:1.0```    

---  

## Persistência de dados com Bind Mounts

```docker run -v /CaminhoHost:/CaminhoContainer imagem:1.0```   

ou    

```docker run --mount type=bind,source=/CaminhoHost,target=/CaminhoContainer imagem:1.0```    

---   

## Persistência de dados com Volume

```docker run -v volumehost:/CaminhoContainer imagem:1.0```   

ou    

```docker run --mount source=/CaminhoHost,target=/CaminhoContainer imagem:1.0```    

> **Obs**.: No host, os arquivos ficam em: `/var/lib/docker/volumes/`   

---   

## Persistência de dados com TMPFS

Armazena os dados na memória RAM. Só funciona em Hosts Linux.

```docker run --tmpfs=/CaminhoContainer imagem:1.0```   

ou    

```docker run --mount type=tmpfs,destination=/CaminhoContainer imagem:1.0```    

--- 
