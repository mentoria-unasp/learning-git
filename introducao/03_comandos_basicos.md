## Comandos Básicos


<h3>Para criar um novo repositório</h3>

```
git init
```
<h3>Veficando estado dos arquivo3/diretório</h5>

```
git status
```
<ul>
    <li>Quando um arquivo for removido ou modificado, o mesmo aparecerá como untracked file ( na cor vermelha). Indicando que deverá adicionar o arquivo/diretório (Staged Area)
    </li>
</ul>

<h3>Adicionar arquivo/diretório (Stage3 Area) </h5>

<strong style="font-size:12px; color:gray;"> Adicionar um aquivo específico</strong>
```
git add nome_arquivo.txt
```
<strong style="font-size:12px; color:gray;"> Adicionar todos arquivos/diretórios</strong>
```
git add .
```

<h3>Remover arquivo/diretório</h3>

<strong style="font-size:12px; color:gray;"> Remover um aquivo específico</strong>
```
git rm nome_arquivo.txt
```
<strong style="font-size:12px; color:gray;"> Remover diretório</strong>
```
git rm -r diretorio
```
<h3>Comitando arquivos/diretórios</h3>

<strong style="font-size:12px; color:gray;"> Comitar um arquivo</strong>

```
git commit meu_arquivo.txt
```
<strong style="font-size:12px; color:gray;"> Comitar um vários arquivo</strong>

```
git commit meu_arquivo.txt outro_arquivo.txt
```
<strong style="font-size:12px; color:gray;"> Comitar informando uma mensagem</strong>

```
git commit meu_arquivo.txt -m "mensagem de commit"
```

<h3>Criando Branch (Ramificação)</h3>

```
git checkout -b nome_da_branch
```
<strong style="font-size:12px; color:gray;"> Trocando de branch</strong>

```
git checkout nome_da_branch
```

<h3>Enviar arquivos/diretórios par3 repositório remoto</h5>

<strong style="font-size:12px; color:gray;">  Primeiro push de um repositório deve conter o nome do repositório remoto e o branch.</strong>

```
git push origin master
```

<strong style="font-size:12px; color:gray;">Os próximos push não precisa informar o repositório remoto e nem a branch</strong>

```
git push
```

<h3>Clonar um repositório existente</h3>

```
git clone git@github.com:mentoria-unasp/learning-git.git
```