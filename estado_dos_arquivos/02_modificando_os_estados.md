# Modificando os Estados
O Git disponibiliza diversos comandos para manipularmos os estados, com eles podemos transitar arquivos através de todo o fluxo e desfazer possiveis erros.

## Unmodified / Modified 
As modificações de um arquivo trackeado podem ser desfeitas com o comando

Unmodified &larr; Modified
```sh
  git checkout nome_do_arquivos.ext
```

## Modified / Staged
Os seguintes comandos podem ser usados para mover um arquivo entre os estados de `modified` e `staged`

Modified &rarr; Staged
```sh
  git add nome_do_arquivo.ext
```

Caso o algum arquivo tenha sido enviado para a área de preparação acidentalmente, o processo pode ser revertido com o comando

Modified &larr; Staged
```sh
  git reset nome_do_arquivo.ext
```

## Staged / Commited
Uma vez que o arquivo esteja na área de preparação ele poderá ser commitado

Modified &rarr; Staged
```sh
  git commit -m "docs: creating states section"
```

## Links
[Estados Git](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F#_the_three_states)


