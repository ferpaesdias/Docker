# Gerenciamendo do Dockerfile

## Comandos para criar uma imagem a partir de um Dockerfile

No diretório que está o arquivo Dockerfile execute o sequinte conando:    
```docker build -t nome-da-imagem:1.0 .```   => Será criada a imagem locamente    
```docker build -t seurepositorio/nome-da-imagem:1.0 .```   => Será criada a imagem no repositório (HUB) do Docker   

--- 

## Instruções

```FROM``` => Imagem base do Dockerfile.    
Ex.: ```FROM: ubuntu:20.04```

```WORKDIR``` => Define o diretório de trabalho do Dockerfile.    
Ex.: ```WORKDIR: /app-node```

```COPY Origem destino``` => Copia arquivos do host local para a imagem.    
Ex.: ```COPY . .``` => Copiará os do diretório atual do host local para o diretório ```/app-node``` que foi definido em ```WORKDIR```.   

```RUN comando``` => Executa um comando.    
Ex.: ```RUN npm install``` 

```ENTRYPOINT comando``` => Comando que será executado quando o container iniciar.    
Ex.: ```ENTRYPOINT npm start``` 
