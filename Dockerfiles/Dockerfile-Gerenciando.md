# Gerenciamendo do Dockerfile

```FROM``` => Imagem base do Dockerfile.    
Ex.: ```FROM: ubuntu:20.04```

```WORKDIR``` => Define o diretório de trabalho do Dockerfile.    
Ex.: ```WORKDIR: /app-node```

```COPY Origem destino``` => Copia arquivos do host local para a imagem.    
Ex.: ```COPY . .``` => Copiará os do diretório atual do host local para o diretório ```/app-node``` que foi definido em ```WORKDIR```.   

```RUN comando``` => Executa um comando.    
Ex.: ```RUN npm install``` 

```ENTRYPOINT comando``` => ????     
Ex.: ```ENTRYPOINT npm start``` 
