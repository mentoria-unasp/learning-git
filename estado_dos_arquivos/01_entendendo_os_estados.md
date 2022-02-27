# Estado dos Arquivos
Os arquivos em um repositório Git possuem estados, e os principais deles são modificado (`modified`), preparado (`staged`) e consolidado (`commited`), esses estados são responsáveis por sinalizar em qual etapa do processo de versionamento o arquivo se encontra.

Podemos visualizar o estado dos arquivos através do comando

```sh
  git status
```

## Modified
Os arquivos que se encontram nesse estado já estão sendo versionados e tiveram seu conteúdo alterados de alguma forma recentemente.
```sh
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
```

## Staged
Esse estado sucede o `modified`, os arquivos que estão nesse estado são movidos para a área de preparação, ou seja, estão em uma área onde ficam os arquivos que serão salvos no `commit`

```sh
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
```

## Commited
Esse é o último estado do arquivo no fluxo, aqui o arquivo em questão teve seu conteúdo versionado de forma segura em seu repositório local, e já pode ser enviado para um remoto.
```sh
commit dd3b585518e014e87d4684f6c74cb8460e152db0
Author: RaphaelBRodrigues <raphaelbarbosa.rodrigues@gmail.com>
Date:   Sun Feb 27 15:41:49 2022 -0300

    docs: creating states section

 README.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

## Links
[Estados Git](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F#_the_three_states)


