# Configurando SSH Key

Para adicionar aquivos em seu repositório, primeiramennte é necessário associar uma <a href="https://en.wikipedia.org/wiki/Ssh-keygen" target="blank" title="O que é SSH Key?">SSH Key</a>. 

Siga os passos abaixos para configurar sua SSH key

Na barra de tarefas no campo de pesquisa, procure por Git GUI. Caso não tenha o Git instalado em sua máquina [clique aqui](/introducao/02_instalacao_e_configuracao.md).
<br><br>
<img src="../assets/gerando-ssh-key.png" alt="Git GUI" title="Git GUI">
<br>
<br>
Após abrir o programa aparecerá a tela abaixo:

<img src="../assets/git-gui.png" alt="Git GUI" title="Git GUI">
<br>
<br>

 1.Clique em `Help` <br><br>
<img src="../assets/git-gui-02.png" alt="Git GUI" title="Git GUI">
<br><br>

2.Clique em `Show SSH key`<br><br>
<img src="../assets/git-gui-03.png" alt="Git GUI" title="Git GUI">
<br><br>

3.Clique em `Generate Key`<br><br>
<img src="../assets/git-gui-04.png" alt="Git GUI" title="Git GUI">
<br><br>

Copie tudo que estiver dentro deste retangulo (como mostra a imagem acima com fundo azul). Agora vamos associar essa chave no GitHub.

<p style="text-align:center; font-size:25px; color:#28a745;">Parabéns você gerou sua SSH Key!!</p>


# Associando SSH Key no GitHub

Com seu GitHub aberto vá em `Settings`
<br><br>
<img src="../assets/associando-ssh-key.png" alt="Settings" title="Settings">
<br><br>
Depois procure `SSH and GPG keys`
<br><br>
<img src="../assets/associando-ssh-key-02.png" alt="SSH and GPG keys" title="SSH and GPG keys">
<br><br>
Estamos quase Finalizando a associação da SSH Key. Realizado o passo acima essa tela aparecerá para você:
<br><br>
<img src="../assets/associando-ssh-key-03.png" alt="SSH and GPG keys" title="SSH and GPG keys">
<br><br>

Clique em `New SSH Key`
<br><br>
<img src="../assets/associando-ssh-key-04.png" alt="SSH and GPG keys" title="SSH and GPG keys">
<br><br>

Coloque um título de sua escolha para sua SSH Key. E logo abaixo no campo `Key`, cole a chave gerada no Git Gui (passo 3).

<img src="../assets/associando-ssh-key-05.png" alt="SSH and GPG keys" title="SSH and GPG keys">
<br><br>

Feito isso, clique em `Add SSH key` abaixo do campo `Key`. E Pronto! sua SSH Key está associada ao seu GitHub.

# O que fazer Agora?

Agora sim estamos prontos para adicionar nossos arquivos no repositório que criamos.

[Adicionar Arquivos no repositório](/usando-git-github/03_adicionando_arquivos.md).  