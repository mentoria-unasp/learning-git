## Comandos Básicos
<hr>

<p>Para criar um novo repositório</p>
```
git init
```
<p>Veficando estado dos arquivos/diretório</p>
```
git status
```
<ul>
    <li>Quando um arquivo for removido ou modificado, o mesmo aparecerá como untracked file ( na cor vermelha). Indicando que deverá adicionar o arquivo/diretório (Staged Area)
    </li>
</ul>

<p>Adicionar arquivo/diretório (Staged Area) <p>

<strong style="font-size:12px"> Adicionar um aquivo específico</strong>
```
git add nome_arquivo.txt
```
<strong style="font-size:12px"> Adicionar todos arquivos/diretórios</strong>
```
git add .
```

<p>Remover arquivo/diretório<p>

<strong style="font-size:12px"> Remover um aquivo específico</strong>
```
git rm nome_arquivo.txt
```
<strong style="font-size:12px"> Remover diretório</strong>
```
git rm -r diretorio
```
<p>Comitando arquivos/diretórios</p>
<strong style="font-size:12px"> Comitar um arquivo</strong>
```
git commit meu_arquivo.txt
```
<strong style="font-size:12px"> Comitar um vários arquivo</strong>
```
git commit meu_arquivo.txt outro_arquivo.txt
```
<strong style="font-size:12px"> Comitar informando uma mensagem</strong>
```
git commit meu_arquivo.txt -m "mensagem de commit"
```

<p>Criando Branch (Ramificação)</p>
```
git checkout -b nome_da_branch
```
<strong style="font-size:12px"> Trocando de branch</strong>
```
git checkout nome_da_branch
```

<p>Enviar arquivos/diretórios para repositório remoto</p>

<strong style="font-size:12px">  Primeiro push de um repositório deve conter o nome do repositório remoto e o branch.</strong>

```
git push origin master
```

<strong style="font-size:12px">Os próximos push não precisa informar o repositório remoto e nem a branch</strong>

```
git push
```

<p>Clonar um repositório existente</p>

```
git clone git@github.com:mentoria-unasp/learning-git.git
```