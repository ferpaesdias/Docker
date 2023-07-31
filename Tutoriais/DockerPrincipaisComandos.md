# Lista dos principais comandos utilizados em Docker


## Push e Pull de uma imagem 

É necessário tem uma conta em [Docker](https://hub.docker.com/signup).

Fazer login na sua conta com o comando abaixo e logo depois será solicitada a senha
```docker login -u nomedousuario```  

```docker push nomedorepositorui/nomedaimagem:1.0```    

---  

## Criando um container com um volume do tipo Bind

```docker run -v /CaminhoHost:/CaminhoContainer imagem:1.0```   

ou    

```docker run --mout type=bind,source=/CaminhoHost,target=/CaminhoContainer imagem:1.0```    
