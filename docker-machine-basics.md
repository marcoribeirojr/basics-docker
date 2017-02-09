## Docker Machine

### Listando as máquinas disponíveis
```
docker-machine ls
```

### Criando uma nova máquina
```
docker-machine create --driver virtualbox [NOME DA NOVA MÁQUINA]
```
Importante: esses comandos levam em consideração estar usando virtualbox para virtualização. No caso do windows a flag é marcada como ```--driver hyperv``` no caso de uma possível utilização do Microsoft Hyper-V para virtualização.

### Obtendo os comandos de ambiente da máquina virtual

```
docker-machine env [NOME DA MÁQUINA]
```

### Conectando o shell à nova máquina
```
eval "$(docker-machine env [NOME DA MÁQUINA])"
```
Importante: Usando fish ou windows shell este comando não funciona. Neste caso é necessário consultar a [documentação oficial dos comandos de ambiente](https://docs.docker.com/machine/reference/env/) para o devido caso.

### Iniciando máquinas
```
docker-machine start [NOME DA MÁQUINA]
```
### Parando máquinas
```
docker-machine stop [NOME DA MÁQUINA]
```

### Outros comandos de operação das máquinas
- `docker-machine config`
- `docker-machine env`
- `docker-machine inspect`
- `docker-machine ip`
- `docker-machine kill`
- `docker-machine provision`
- `docker-machine regenerate-certs`
- `docker-machine restart`
- `docker-machine ssh`
- `docker-machine start`
- `docker-machine status`
- `docker-machine stop`
- `docker-machine upgrade`
- `docker-machine url`

Importante: todos precedidos do [NOME DA MÁQUINA].

Exemplo: `docker-machine ip default`
