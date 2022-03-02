# Git Flow
  O Git Flow é um modelo de fluxo muito famoso implementado em empresas, geralmente com algumas adaptações, a ideia é que sejam usadas duas branchs principais, e diversas outras secundárias onde as funcionalidades serão desenvolvidas.

## Branchs 
As branchs são recursos fundamentais em fluxos complexos no Git, no git flow elas são divididas e principais e secundárias, e cada uma delas possui uma função específica

### Branchs Principais
  * Master - É a branch que representa o ambiente de produção  
  * Develop - É a branch onde as novas funcionalidades serão validadas e então enviadas para a branch `master`

### Branchs Secundárias
  * Feature 
    * São branchs onde novas funcionalidades serão desenvolvidas e posteriomente mergeadas com a `develop`
    * Geradas a partir da `develop`
  * Hotfix 
    * São branchs utilizadas para corrigir erros críticos em produção, após a conclusão é mergeada diretamente na `master`
    * Geradas a partir da `master`
  * Bugfix 
    * São branchs criadas para a correção de bugs no sistema e são mergeadas com a `develop`
    * Gerada a partir da `develop`
  * Release 
    * A branch release é responsável por fazer o merge
    * Geradas a partir da `develop`

## Fluxos
  O Git flow pode ser adaptado conforme a necessidade do projeto, veremos dois modelos a seguir, um simplificado e o original

### Fluxo adaptado
  Nesse fluxo adaptado, muito comum em diversos projetos, não ocorre o merge entre as branchs principais, apenas entre as principais com as secundárias, ou entre as secundárias com elas mesmas.

  A ideia é que a branch `master` represente o ambiente de produção e a `develop` um ambiente de QA, então quando alguma alteração for feita em uma branch secundária ela será enviada paraa o ambiente de testes e validada, e só então enviada para a branch `master`.

  #### Branchs Utilizadas
  * Master
  * Develop
  * Bugfix
  * Feature
  * Hotfix

  #### Fluxo
  Todas as branchs secundárias serão criadas a partir da `master`, então devemos ir para ela
  ```sh
    git checkout master
  ```
  Já na branch master podemos criar uma ramificação 
  ```
    bugfix/adjusting-label-text
  ```
  Quando a correção for commitada na branch `bugfix/adjusting-label-text` as alterações devem ser enviadas para a branch `develop` onde a correção será testada
  ```sh
    git checkout develop
  ```
  ```sh
    git merge bugfix/adjusting-label-text
  ```
  Estando tudo validado no ambiente de QA a correção deve ser enviada para a master
  ```sh
    git checkout master
  ``` 
  ```sh
    git merge bugfix/adjusting-label-text
  ``` 
  ```sh
    git branch -D bugfix/adjusting-label-text
  ``` 

### Fluxo Original 
  No fluxo original continuamos desenvolvendo em nossas branchs secundárias e na maioria dos casos fazemos o merge delas com a `develop`, porém ao contrário do fluxo adaptado onde a `master` e a `develop` eram independentes, nesse fluxo as alterações que estão na develop são enviadas para a `master` através de uma branch secundária chamada `release`

  #### Branchs Utilizadas
  * Master
  * Develop
  * Bugfix
  * Feature
  * Hotfix
  * Release

  #### Fluxo
  Nesse modelo as branchs são geradas a partir da `develop`, com exceção da `hotfix`, o fluxo em geral é `Branch Secundária` &rarr; `Develop` &rarr; `Branch Release` &rarr; `Master`, veremos o fluxo com o comando `git flow` e sem ele.

  Antes de começarmos precisamos inicializar o git flow
  ```
    git flow init
  ```

  E então iniciar um fluxo para o tipo de desenvolvimento que estamos realizando, no nosso exemplo será uma feature
  ```
    git flow feature start novo-botao
  ```
  ou 
  ```
    git checkout develop
    git checkout -b feature/novo-botao
  ```
  Após finalizar e commitar a nova funcionalidade devemos enviar as alterações para a `develop`
  ```
    git flow feature finish
  ```
  ou 
  ```
    git checkout develop
    git merge feature/novo-botao
    git branch -D feature/novo-botao
  ```
  Com as alterações testadas na branch `develop` podemos criar uma `release` que irá mandar as correções para a `master`
  ```sh
    git flow release start 1.0.0
  ``` 
  ou 
  ```sh
    git checkout -b release/1.0.0
  ```
  Criada a branch `release` com todas as alterações que irão para produção podemos finalizar o fluxo
  ```sh
    git flow release finish 1.0.0
  ```
 ou
 ```sh
  git tag -a 1.0.0
  git checkout master
  git merge release/1.0.0
  git checkout develop
  git merge release/1.0.0
 ```

Nessa última etapa é criada uma tag com a versão atual do projeto na branch `release`, então todos os commits e a tag são enviadas para a branch `master` e então para a `develop`

#### Hotfix
  As branchs `hotfix` são as únicas que são mergeadas diretamente com a master
  ```sh
    git flow hotfix start valor-no-checkout
  ```
  ou 
  ```sh
    git checkout master
    git checkout -b hotfix/valor-no-checkout
  ```
  A nossa branch `hotfix` foi gerada a partir da `master` e quando concluída será enviada para ela e para a `develop`
  ```sh
    git flow hotfix finish valor-no-checkout
  ```
  ou 
  ```sh
    git checkout master
    git merge hotfix/valor-no-checkout
    git checkout develop
    git merge hotfix/valor-no-checkout
  ```
  
## Links
[Branch](ramificacoes/01_branchs.md)

[Merge](ramificacoes/02_Merge.md)

[Versionamento Semântico](https://semver.org/lang/pt-BR/)

