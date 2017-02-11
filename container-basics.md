## Containers

### Exibindo containers em execução
`docker ps`

### Criando um container
`docker run -it [NOME DO CONTAINER] [ARGUMENTS]`

- -i é pra rodar de forma interativa
- -t é para linkar com o terminal do container

Exemplo:

`docker run -it ubuntu /bin/bash`

### Exibindo containers pausados ou inicializados
`docker ps -a`

### Exibindo apenas id dos containers
`docker ps -qa`

### Criando um container com com um name
`docker run -it --name [NAME DO CONTAINER] [IMAGEM BASE]`

Exemplo:

`docker run -it --name nginx ubuntu`

### Acompanhando o uso de recursos do host pelo container
`docker stats [ID DO CONTAINER]`

### Commitando alterações
`docker commit [ID DO CONTAINER] [NOME DA NOVA IMAGEM OU TEXTO QUALQUER ESCOLHIDO]`

Exemplos:
- `docker commit 85e8a2ae1166 ubuntu/nginx`
- `docker commit 85e8a2ae1166 v.1.3`

### Criando um container autodestrutivo

Este tipo de container será excluído de forma autmoática ao fim de sua execução.

`docker run -it --rm [NOME DA IMAGEM]`

A flag `--rm` indica esta autodestruição

### Mapeando portas
`docker run -it [NOME DA IMAGEM] -p [PORTA EXTERNA]:[PORTA DO SERVIÇO DO CONTAINER]`

### Rodando um container em background

`docker run -d -p [MAPEAMENTO DE PORTAS] [NOME DA IMAGEM] [POSSÍVEIS ARGUMENTOS]`

A flag `-d` informa que o container ficará rodando em background.

Mesmo em background o container para iniciar seu funcionamento precisa ser inicializado.

### Manipulando o funcionamento dos containers
- Iniciando

`docker start [ID DO CONTAINER]`

- Parando

`docker stop [ID DO CONTAINER]`
