## Containers

### Exibindo containers em execução
`docker ps`

### Rodando um container
`docker run -it [NOME DO CONTAINER] [ARGUMENTS]`

- -i é pra rodar de forma interativa
- -t é para linkar com o terminal do container

Exemplo:

`docker run -i -t ubuntu /bin/bash`

### Exibindo containers pausados ou inicializados
`docker ps -a`
