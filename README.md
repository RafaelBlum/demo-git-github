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

<sub>Como ver histórico de commits</sub>
```
git reflog
```

### Comando avançados Git

<sub>Como voltar para alguma alteração commitada `voltar na sua linha do tempo`</sub>

```
git reflog
git reset --hard id_commit
```

```

```


<br>

Contato [rafaelblum_digital@hotmail.com](rafaelblum_digital@hotmail.com)

[![Youtube Badge](https://img.shields.io/badge/-Youtube-FF0000?style=flat-square&labelColor=FF0000&logo=youtube&logoColor=white&link=https://www.youtube.com/channel/UCMvtn8HZ12Ud-sdkY5KzTog)](https://www.youtube.com/channel/UCMvtn8HZ12Ud-sdkY5KzTog)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/rafael-blum-237133114s/)](https://www.linkedin.com/in/rafael-blum-237133114s/)
[![Instagram Badge](https://img.shields.io/badge/-Instagram-violet?style=flat-square&logo=Instagram&logoColor=white&link=https://www.instagram.com/rafablum_/)](https://www.instagram.com/rafablum_/)
