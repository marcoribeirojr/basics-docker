## Tópicos básicos sobre o Docker

### O que é Docker?
Docker é uma ferramenta para manter serviços virtualizados de forma isolada do sistema operacional. Seu símbolo já diz tudo, uma baleia em forma de cargueiro levando vários conteineres.

### O que é um container?
São os serviços virtualizados criados e mantidos isoladamente do host e dos demais containers pelo Docker.

### O que é uma imagem?
É um modelo para criação de containers.

### Qual a diferença entre uma imagem e um container?
Pensando em OO, uma imagem é como se fosse uma classe e um container é como se fosse uma instância desta classe. Uma imagem é um modelo, um template para a criação de novos containers. Logo de uma mesma imagem podem ser criados vários containers, todos encapsulados e funcionando de forma independente dos demais.

### O que são Cgroups?
É um recurso utilizado pelo Docker para administrar o uso de recursos como CPU, memória, disco disponíveis no host com os containers.

### O que são Namespaces?
É um espaço de trabalho criado para cada container quando ele é criado. Dessa forma cada container tem seus processos funcionando de forma independente e isolada dos demais containers.

Tipos de Namespaces:
- pid - processos
- net - interface de redes
- ipc - controle do IPC (intercomunicação entre processos)
- mnt - pontos de montagem
- uts - controle de recursos do Kernel

### Commits
Qualquer alteração realizada em um container é perdida assim que ele deixar de estar ativo. Para persistir alterações feitas em um container é necessário comiitar (assim como no git) as alterações feitas. Dessa forma o estado atual no momento do commit será registrado. Além de fazer esse registro é possível também retornar a estado anteriores através do versionamento.

Ao salvar um commit de um container uma nova imagem é gerada a partir do commit de alteração.
### Basics:

- [Images - Basics](../master/docker-basics.md)
- [Containers - Basics](../master/container-basics.md)
- [Docker Machine - Basics](../master/docker-machine-basics.md)
