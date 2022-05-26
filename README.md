# Git

## O que é
---
Sistema de controle de versão distribuido

## Quais problemas ele resolve
---

## Como funciona
---
### gitignore
Um arquivo como nome de `.gitignore` pode ser criado na pasta do projeto. Escrevendo o nome de um arquivo ou pasta neste documento faz com que o git não adicione o mesmo ao versionamento.
```
.env
```


## Usos no dia a dia
---
### gitbash

### init
Inicia um repositório `git` na pasta atual
```sh
git init
```

### clone
Cria uma cópia de um repositório remoto na pasta atual. Caso um nome não seja informado criará uma pasta com o nome do projeto.
```sh
git clone endereço-do-repositório
```

### remote
Visualiza a origem do repositório atual.
```sh
git remote -v
```

### fetch
Busca atualizações existentes no repositório remoto
```sh
git fetch --all
```

### rebase
Atualiza repositório local com as mudanças existentes no repositório remoto
```sh
git rebase origin/master
```

### checkout
Navega entre `branchs` no repositório
```sh
git checkout nome-da-branch
```
Criar branch
```sh
git checkout -b nome-da-branch
```

### log
Exibe os `commits` na `branch` atual.
```sh
git log
```
Para sair aperte `q`.

### branch
Visualiza as branchs existentes no repositório.
```sh
git branch
```
Também é usado para deletar branch
```sh
git branch -d the_local_branch
```
Use `D` para deletar mesmo que não tendo feito `merge` da branch.
```sh
git branch -D the_local_branch
```
Deletar branch no repositório remoto
```sh
git push --delete <remote name> <branch name>
```
### status
Visualiza os arquivos que sofreram mudanças e se já está "comitados".
```sh
git status
```

### diff
Mostra o que foi alterado nos arquivos.
```sh
git diff
```

### stash
Salva alterações e retorna ao estado anterior
```sh
git stash
```
Mostra o que está salvo
```sh
git stash show
```
Recupera o que foi salvo
```sh
git stash apply
```

### add
Adiciona os arquivo ao versionamento.
```sh
git add .
```

### commit
Grava os arquivos adicionados pelo comando `add` e cria um ponto de controle que chamamos de `commit`
```sh
git commit -m "descrição do commit"
```

### push
Envia o `commit` com as mudanças para o repositório remoto.
```sh
git push origin HEAD
```


## Github
---
### Conta

#### Configuração
[Documentação](https://help.github.com/articles/setting-your-email-in-git/)

Ver configuração
```sh
git config -l

git config --global user.name “Paulo Sorrentino”
git config --global user.email “email@gmail.com”
git config --global color.ui true
```


- [Criar chave ssh](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Creates a new ssh key, using the provided email as a label
```sh
$ ssh-keygen -t rsa -b 4096 -C "email@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Paulo/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Paulo/.ssh/id_rsa
Your public key has been saved in /c/Users/Paulo/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:R9/qapFqoW+cj3dtxcodf/5+fqT1If2OwYiYrCoG51Q email@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|                 |
|                 |
|          .      |
|    E    . . .   |
|   .    S ... o. |
|. o    ..+o. = +=|
| =     o++..oo+B*|
|  +   ..*.o.. *oO|
| . ....+o+oo...=@|
+----[SHA256]-----+

```
Copies the contents of the id_rsa.pub file to your clipboard
```sh
$ clip < ~/.ssh/id_rsa.pub
````
Inicializar o ssh-agent
```sh
# start the ssh-agent in the background
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```
Adicionar chave SSH ao ssh-agent
```sh
$ ssh-add ~/.ssh/id_rsa
```


- [Guia básico Markdown](https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown#open)

### Criar repositório

### Criar PR (pull request)

### Code Review

### Merge

### Conflitos

### Release

