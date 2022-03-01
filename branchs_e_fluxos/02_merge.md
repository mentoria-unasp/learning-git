# Merge
Caso uma nova funcionalidade ou correção tenha sido feita em um branch específica, podemos mesclar ela com outra branch, de forma que essa branch herde as alterações da primeira

Por exemplo, em nosso projeto temos três branchs a `master`, `corrigindo-a-faq` e a `botao-whatsapp`, a correção da branch `corrigindo-a-faq` já foi feita e deve ir para produção. Para isso devemos colocar essas alterações em nossa branch principal, a `master`.

Como já vimos o ideal é não alterar a branch `master` diretamente, então para enviarmos as alterações da `corrigindo-a-faq` para a `master` precisamos realizar os seguintes passos

Devemos ficar na branch que herdará as alterações da outra, podemos visualizar a branch atual com o comando
```sh
  git branch
  * botao-whatsapp
    corrigindo-a-faq
    master
```

Estamos na branch `botao-whatsapp` e devemos ir para a `master`, então devemos executar o comando
```sh
  git checkout master
```

Feito isso podemos mesclar o conteúdo da branch `corrigindo-a-faq` com a `master`
```sh
  git merge corrindo-a-faq
```

A partir desse momento a nossa branch principal tem todas as alterações realizadas na `corrigindo-a-faq`, portanto ela não e mais necessária e ela já pode ser deletada de maneira segura

```
  git branch -D corrigindo-a-faq
```
```
  git branch
    botao-whatsapp
  * master
```

## Links
[Branch](https://git-scm.com/docs/git-branch)
[Merge](https://git-scm.com/book/pt-br/v2/Branches-no-Git-O-b%C3%A1sico-de-Ramifica%C3%A7%C3%A3o-Branch-e-Mesclagem-Merge)


