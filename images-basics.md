## Images

### Rodando uma imagem

``` docker pull [NOME DA IMAGEM] ```

### Listando as imagens

``` docker images ```

### Criando um Dockerfile

No dockerfile existem alguns coringas, estes são:
- FROM - nome da imagem que será iniciada por este dockerfile;
- RUN - os comando que serão executados. Como se rodasse estes mesmo comandos no terminal;
- CMD - Informa o camando final que será executado depois do ambiente configurado;

### Build de uma imagem
O parâmetro -t é o nome da imagem (vem de tag).

Ps.: Não esquecer do ponto no final.

``` docker build -t [NOME DO CONTAINER] .```

O comando lê o arquivo Dockerfile da pasta e faz um build para uma imagem lendo os comandos contidos no docker file.

### Push imagem para o docker hub

- Selecionar o id da imagem na lista de imagens locais;
- Digitar o comando: ``` docker tag [ID DA IMAGEM] [USUARIO DO DOCKER HUB]/[NOME DA IMAGEM]:[LABEL OU TAG DA IMAGEM]```

Explicação:

![Explicação](https://docs.docker.com/engine/getstarted/tutimg/tagger.png)

- Fazer login no docker hub pelo terminal: ``` docker login```
- Fazer o push da imagem: ``` docker push [NOME DA IMAGEM]```

### Removendo imagens

``` docker rmi -f [ID OU NOME DA IMAGEM]```
