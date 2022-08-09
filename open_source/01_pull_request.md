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

Nessa aba selecione as branchs que deverão ser mergeadas, a esquerda deve estar a branch que receberá as alterações e a direita a branch que foi utilizada durante o desenvolvimento

![Abrindo a PR](/assets/pull_request-01.png)

Em seguida preencha a descrição da PR e selecione os possíveis revisores

![Abrindo a PR](/assets/pull_request-02.png)

Após a abertura da PR, será necessário que um revisor faça o merge da Pull Request 

![Aceitando a PR](/assets/pull_request-03.png)
 
![Aceitando a PR](/assets/pull_request-04.png)
 
![Aceitando a PR](/assets/pull_request-05.png)

Caso a PR seja mergeada as alterações da branch de desenvolvimento serão enviadas para a branch de destino e o processo estara pronto

![Commits](/assets/pull_request-06.png)

## Links
[Comandos Básicos](/introducao/03_comandos_basicos.md)
[Github](/usando_git_github/)
