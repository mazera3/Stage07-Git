# Git

## Iniciar um novo repositório

- git init

## configurar o usuario e o email

- git config --global user.name "mazera3"
- git config --global user.email "mazera3@gmail.com"

## Verificar as configurações salvas

- git config --list

```
user.email=mazera3@gmail.com
user.name=Edio.Mazera
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```

## Commit

- git add .
- git commit -m 'criado o arquivo index.html'

## Log (historico de commits)

- git log

```
commit ec004a50a95b7859c9343ddcf4b4db4a19ce5981 (HEAD -> master)
Author: Edio.Mazera <mazera3@gmail.com>
Date:   Sun May 15 22:40:07 2022 -0300

    criado o arquivo index.html
```

- git log --oneline
  `ec004a5 (HEAD -> master) criado o arquivo index.html`
- git log -n 3 (mosstra os ultimos 3 commits)

# Estagio de um arquivo

<img src="./img/estagios.jpg" width="50%"/>

## Etapas
- iniciar o repositorio (git init) - diretorio de trabalho
- mover para area de staged - (git add) - preparar para repositorio
- registrar no repositorio (git commit)

- git status
```
No ramo master
nothing to commit, working tree clean
```
- Apos midific as o index.htm `git status`
```
No ramo master
Changes not staged for commit:
  (utilize "git add <arquivo>..." para atualizar o que será submetido)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

nenhuma modificação adicionada à submissão (utilize "git add" e/ou "git commit -a")
```
- git add .
```
No ramo master
Mudanças a serem submetidas:
(use "git restore --staged <file>..." to unstage)
  modified:   index.html
```
- git status

<img src="./img/commit.jpg" width="50%"/>

- git commit -m "criado html base"
- git status

<img src="./img/commit2.jpg" width="50%"/>

## Head (branch), (master), (main)
```
349dae1 (HEAD -> master) criado html base
88c55b9 criado o arquivo readme.md
ec004a5 criado o arquivo index.html
```
<img src="./img/head.jpg" width="50%"/>

- `git diff` (apresenta a diferença das modificações realizadas)
- `git restore .` (para restaurar o estado anterior com todos os arquivos)
- `git restore --staged .` (reverte git add .)
- `git commit --amend -m` "alterado title page" (altera o ultimo commit)
- `git reset --soft HEAD~1` (desfazer um commit inteiro)

---