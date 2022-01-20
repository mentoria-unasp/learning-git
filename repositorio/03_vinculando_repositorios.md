# Vinculando Repositórios
Já vimos a diferença entre repositórios `remotos` e `locais`, agora veremos como os vincular.

## Vinculando Repositórios
Para vincularmos os repositórios precisamos executar o seguinte comando em nosso repositorio local.

```sh
  git remote add {{remote}} {{url}}
```
e.g.
```sh
  git remote add origin https://github.com/mentoria-unasp/repositorio-teste
```

* `remote` - É o nome que será usado para identificar a conexão entre os repositórios, geralmente o nome da conexão principal é `origin`

* `url` - É a URL do repositório remoto da plataforma de hospedagem

Executando esse comando os repositórios estarão conectados e já é possível sincronizar os arquivos.


## Links
[Comandos Básicos](/introducao/03_comandos_basicos.md)
