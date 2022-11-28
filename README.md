<p align="center">
	<a href="#" title="git-github">
		<img src="imges/git-github.png" alt="logo header" width="320">
	</a>
</p>

<p align="center">Demo trabalhando com versionamento em seus projetos</p>


# Introdução

Projeto com objetivo de mostrar o `funcionamento do sistemas de controle de versão Git`, com seus comandos `basicos` aos `avançado`, conecxão
com github via chave `SSH` e como `subir os projetos para github` e suas alteraões.
<br>

## Installation

Para trabalhar com controle de versão, você vai precisar:

> Instalar o [`Git`](https://git-scm.com/)
> Criar uma conta no [`GitHub`](https://github.com/)


<br>


## Versionando projeto e subir no github

<p>É importante nos identificarmos para o Git, informando nosso nome e e-mail. Em um terminal, execute os comandos a seguir</p>

- git config --global user.name "Fulano da Silva"
- git config --global user.email fulanodasilva.git@gmail.com
- Pode verificar todos dados com comando `git config –list`.

<p>Iniciando repositório local</p>

```
git init
git status
git log
git add .
git commit -m "first commit"
```

<p>Para subir o projeto no Github é importando criar um chave SSH na sua conta</p>

> Documentação do Github [`GitHUb`](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=windows)

<p>Com o Git Bash aberto</p>

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Quando você for solicitado a `Inserir um arquivo no qual salvar a chave`, pressione `Enter` para aceitar o local padrão 
do arquivo.Observe que, se você criou chaves SSH anteriormente, o ssh-keygen pode solicitar que você reescreva outra chave; 
nesse caso, recomendo a criação de uma chave SSH com nome personalizado. Para fazer isso, digite o local padrão 
do arquivo e substitua id_ssh_keyname pelo nome de sua chave personalizada.

Agora basta copiar a chave e depois ir na sua conta no github para criar a nova chave SSH.

```
clip < ~/.ssh/id_ed25519.pub
```

Depois de cria a chave, basta criar um repositório no github e seguir os comandos abaixo.

```
git remote add origin git@github.com:RafaelBlum/demo-git-github.git
git branch -M main
git push -u origin main
```

Como enviar as alterações realizadas no seu projeto.

```
git status
git add .
git commit -m "Alterações na feature x"
git push
```

<sub>Mensagens de pré e pós commits</sub>

- Untracked files `Arquivos não rastreados no controle de vesão`
- Changes to be committed `Arquivos rastreados no controle de versão`
- Changes not staged for committed `Arquivos rastreados, mas com alterações`

<sub>Como ver histórico de commits e alterações</sub>
```
git log
git reflog
git log --stat
git log --oneline
```


<sup>Mostra o conteúdo que foi alterado, mas antes do commit</sup>
```
gif diff
```

<sup>Mostra arquivo que foi alterado, mas antes do commit</sup>
```
gif diff --name-only
```

<sup>Remove alterações realizadas em algum arquivo especifico</sup>
```
git checkout HEAD -- style.css
```

<sub>Como voltar para alguma alteração commitada `voltar na sua linha do tempo`</sub>

```
git reflog
git reset --hard id_commit
```

### Comando avançados Git - Branchs
###### Trabalhando nas linhas do tempo

<p align="center">
	<a href="#" title="git-github">
		<img src="imges/machine-git.jpg" alt="time machine" width="350">
	</a>
</p>

Como podemos ver, trabalhar com git é como se estivessemos em uma `máquina do tempo`, onde `podemos voltar` na nossa linha do 
tempo, o que chamamos de `commits`, voltando no inicio do projeto ou em qulquer momento.

Agora vamos utilizar outro poder do tempo, o poder de criar uma `linha do tempo em paralelo`, o que chamamos de `branchs`.
Estas linhas, branchs, usamos quando vamos desenvolver uma feature nova ou quando vamos `trabalhar em equipe`, pois assim
todos podemos trabalhar em uma parte do projeto sem que haja problemas em nosso projeto que está funcionando corretamente.

> Desta forma, podemos ter um desenvolvedor trabalhando na branch 2, na página de produtos e outro desenvolvedor trabalhando na branch 1, com a Home.

<sup>Verificar qual branch esta ativo e quais existem</sup>

```
git branch
```

<sup>Como criar um branch `linha do tempo`</sup>

```
git branch new_feature
```

<sup>Como passar para uma branch `linha do tempo`</sup>

```
git checkout new_feature
git branch
```

<p align="center">
	<a href="#" title="git-github">
		<img src="imges/time-line.png" alt="time machine" width="450">
	</a>
</p>

Agora temos duas linhas do tempo `main` e `new_feature`.

Podemos subir mais uma Branch para github (remoto).
```
Git push origin branch-name
```

Remover uma branch remoto
```
Git push origin :branch-name
```


Remover branch local
```
Git branch –D branch-name
```

<sup>Como fazer Git Merge e pull</sup>

Antes de fazer o `merge` é importante fazer um `pull` no projeto `remoto Github`, puxando e atulizando para o projeto local, pois
pode acontecer de outro desenvolvedor tenha modificado algo, então na branch `main`.

```
git pull origin branch-name
git push --set-upstream origin branch-name
```

Agora sim, podemos fazer o merge

```
git branch
git merge branch_name
```

<p align="center">
	<a href="#" title="merge">
		<img src="imges/merger.png" alt="merge" width="350">
	</a>
</p>

<br>

Contato [rafaelblum_digital@hotmail.com](rafaelblum_digital@hotmail.com)

[![Youtube Badge](https://img.shields.io/badge/-Youtube-FF0000?style=flat-square&labelColor=FF0000&logo=youtube&logoColor=white&link=https://www.youtube.com/channel/UCMvtn8HZ12Ud-sdkY5KzTog)](https://www.youtube.com/channel/UCMvtn8HZ12Ud-sdkY5KzTog)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/rafael-blum-237133114s/)](https://www.linkedin.com/in/rafael-blum-237133114s/)
[![Instagram Badge](https://img.shields.io/badge/-Instagram-violet?style=flat-square&logo=Instagram&logoColor=white&link=https://www.instagram.com/rafablum_/)](https://www.instagram.com/rafablum_/)
