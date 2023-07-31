 # Gerenciamendo do Dockerfile
    

## Comandos para criar (build) uma imagem a partir de um Dockerfile

No diretório que está o arquivo Dockerfile execute o sequinte conando:    
```docker build -t nome-da-imagem:1.0 .```   => Será criada (build) a imagem locamente    
```docker build -t seurepositorio/nome-da-imagem:1.0 .```   => Será criada (build) a imagem no repositório (HUB) do Docker   

--- 

## Instruções

```FROM Imagem``` => Imagem base do Dockerfile.    
Ex.: ```FROM ubuntu:20.04```

```WORKDIR Caminho``` => Define o diretório de trabalho do Dockerfile.    
Ex.: ```WORKDIR /app-node```

```ARG VAR=Valor``` => Variável usada na criação (build) da imagem. A variável criada com a instrução ARG é utilizada somente no Dockerfile, não é inserida "dentro" do container.   
Ex.: ```ARG PORT=3333```  => Cria a variável **PORT** de valor **3333**.   

```ENV VAR=Valor``` => Variável usada na criação da imagem. A variável criada com a instrução ENV é utilizada é inserida "dentro" do container.   
Ex.: ```ENV USUARIO=teste```  => Cria a variável **USUARIO** de valor **teste**.   

```COPY Origem Destino``` => Copia arquivos do host local para a imagem.    
Ex.: ```COPY . .``` => Copiará os do diretório atual do host local para o diretório ```/app-node``` que foi definido em ```WORKDIR```.   

```RUN comando``` => Executa um comando.    
Ex.: ```RUN npm install``` 

```ENTRYPOINT comando``` => Comando que será executado quando o container iniciar.    
Ex.: ```ENTRYPOINT npm start``` 

```EXPOSE porta``` => Executa um comando.    
Ex.: ```EXPOSE 3000```   

