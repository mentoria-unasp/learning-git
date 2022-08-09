# Pull Request

Um processo importante no dia a dia profissional é o code review, que consiste que outro desenvolvedor avalie e sugira alterações no seu código.

Podemos iniciar esse processo através de uma pull request, que é basicamente uma solicitação para realizar o merge entre duas branchs distintas

## Iniciando

Para iniciarmos precisamos criar uma branch de desenvolvimento a partir de uma branch principal e iniciarmos o desenvolvimento dela

```sh
$ git branch
* develop
  main
```

```sh
$ git checkout -b docs/pr-topic
$ git commit -am "docs: writting about a lot of things"
```

Logo após precisamos subir a nossa nova branch em nossa plataforma de hospedagem

```sh
$ git push --set-upstream origin docs/pr-topic
```

## Abrindo a PR

Entre no repositório e clique na aba `Pull Requests` e em seguida clique no botão `New Pull Request`




## Links
[Comandos Básicos](/introducao/03_comandos_basicos.md)
[Github](/usando_git_github/03_adicionando_arquivos.md)
