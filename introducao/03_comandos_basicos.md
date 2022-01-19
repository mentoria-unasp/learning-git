## Comandos Básicos


<h5>Para criar um novo repositório</h5>

```
git init
```
<h5>Veficando estado dos arquivos/diretório</h5>

```
git status
```
<ul>
    <li>Quando um arquivo for removido ou modificado, o mesmo aparecerá como untracked file ( na cor vermelha). Indicando que deverá adicionar o arquivo/diretório (Staged Area)
    </li>
</ul>

<h5>Adicionar arquivo/diretório (Staged Area) </h5>

<strong style="font-size:12px; color:gray;"> Adicionar um aquivo específico</strong>
```
git add nome_arquivo.txt
```
<strong style="font-size:12px; color:gray;"> Adicionar todos arquivos/diretórios</strong>
```
git add .
```

<h5>Remover arquivo/diretório</h5>

<strong style="font-size:12px; color:gray;"> Remover um aquivo específico</strong>
```
git rm nome_arquivo.txt
```
<strong style="font-size:12px; color:gray;"> Remover diretório</strong>
```
git rm -r diretorio
```
<h5>Comitando arquivos/diretórios</h5>

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

<h5>Criando Branch (Ramificação)</h5>

```
git checkout -b nome_da_branch
```
<strong style="font-size:12px; color:gray;"> Trocando de branch</strong>

```
git checkout nome_da_branch
```

<h5>Enviar arquivos/diretórios para repositório remoto</h5>

<strong style="font-size:12px; color:gray;">  Primeiro push de um repositório deve conter o nome do repositório remoto e o branch.</strong>

```
git push origin master
```

<strong style="font-size:12px; color:gray;">Os próximos push não precisa informar o repositório remoto e nem a branch</strong>

```
git push
```

<h5>Clonar um repositório existente</h5>

```
git clone git@github.com:mentoria-unasp/learning-git.git
```