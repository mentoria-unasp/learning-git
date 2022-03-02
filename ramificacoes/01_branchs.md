# Branchs
As `branchs` são ramificações do nosso código fonte, ou seja, são versões isoladas uma das outras

Por exemplo, podemos ter em nosso projeto uma branch principal chamada `master`, que representa a versão mais atual e estável da aplicação e outra branch chamada `develop` onde novas funcionalidades estão sendo adicionadas e testadas.

As branchs permitem que o implementações e correções sejam iniciadas e pausadas sem atrapalhar outras atividades, a criação de fluxos e o code review.

## Criando branchs
Ao criar um repositório uma branch principal é gerada automaticamente, o nome dela costuma ser `master`, mas também pode aparecer como `main`, é uma má prática desenvolver diretamente nessa branch, pois ela representa a versão que está sendo usada em produção (a versão que está no ar) e alterações nessa branch afetam todos os desenvolvedores do projeto

Para contornar essa situação podemos criar uma nova branch, essa será uma ramificação da branch atual, então se nós estivermos utilizando a `master`, a nova branch será uma cópia dela.

Podemos criar uma nova branch com o seguinte comando
```sh
  git branch nome-da-branch
```
com a branch criada podemos visualizar todas as branchs com
```sh
  git branch
```
e então começar a usar a nossa nova branch com o comando
```sh
  git checkout nome-da-branch
``` 

Uma alternativa é utilizar o comando
```sh
  git checkout -b nome-da-branch
```
que é um atalho para 
```
  git branch nome-da-branch
  git checkout nome-da-branch
```


## Links
[Branch](https://git-scm.com/docs/git-branch)


