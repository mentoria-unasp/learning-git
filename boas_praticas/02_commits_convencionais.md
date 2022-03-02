# Commits Convencionais
  Os commits sempre são acompanhados por uma mensagem que deve descrever as alterações realizadas, e podemos usar a especificação [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/) para torná-los mais descrítiveis.

## Tipos de Commit 
  * fix
    * Commits que solucionam um erro
  * feat
    * Commits que implementam novas funcionalidades ao nosso projeto
  * chore
    * Commits onde são feitas configurações no projeto, como alterações em scripts de build e desenvolvimento
  * docs
    * Commits relacionados a alteração em documentações
  * style
    * Commits onde a estilização do código é alterada, por exemplo indentação, espaços em branco, pontos e virgulas faltantes...
  * refactor
    * Commits onde o código é reescrito, mas não são adicionadas novas funccionalidades ou correções
  * test
    * Commits que implementam novos testes ou corrigem já existentes

## Estrutura
  A mensagem do commit deve seguir a seguinte estrutura _tipo(escopo): descrição_, o `tipo` são os citados anteriormente, é um elemento opcional e diz respeito ao que está sendo alterado, e a `descrição` é uma breve explicação do que foi alterado

  ### Exemplos
  * Alteração em alguma documentação
  ```sh
    git commit -m "docs: updating how to use explanation"
  ```

  * Correção de um bug na página de um produto
  ```sh
    git commit -m "fix(product): adjusting item value"
  ```

  * Criação de uma nova funcionalidade na página da conta do usuário
  ```sh
    git commit -m "feat(account): creating a recover password button"
  ```

## Links
[Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/) 

