# DICAS GIT

## BRANCH

```bash
git checkout -b <NOMEDABRANCH> --> Criar uma nova branch
git checkout <NOMEDABRANCH> --> Acessar uma branch
git branch -d <localBranchName> --> Deleta a branch local
git push origin --delete remoteBranchName --> Deleta a Branch remoto
git merge NOMEDABRANCH
git push origin <Branch> --> move para branch e solicita o merge
```

## LOGs

```bash
git log --> Mostra os commits
git log --oneline --> Mostra os commits simplificados
git log --graph --all
```

## Remoção 

```bash
git reset HEAD --> Retira o arquivo adicionado do git add
git reset --hard <COMMITS> --> Remove os commits
git fetch --> Equivale ao git pull, mas ele não faz o merge dos projetos
```


## Exemplo em resolver conflito de repo: 

```bash
git fetch
git remote
git checkout origin
git checkout master
git pull
git add .
git commit
```

## Move arquivo de um determinado commit

```bash
git cherry-pick <hash do commit>
```

## Configurar editor padrão

```bash
git config --global core.editor (code|vim|etc)
```

## Busca por perfil

Explore = language:java location:Brazil,SP,São Paulo  
 

## GIT-FLOW

### Install git-flow

https://github.com/nvie/gitflow/wiki/Installation

Main/Master --> Repo principal
Develop --> Desenvolvimento
Feature --> Novas ideias
Release --> Pré produção e correção de bug e depois pronto volta para Main/Master 
HotFix --> Correção de problema

```bash
git flow init --> Setar a branch q vai ser produção 
git flow <feature|release|hotfix> start <nome/feature> Iniciar uma branch a parte para desenvolvimento
git flow <feature|release|hotfix> publish <nome/feature> --> Compartilhar a branch com outros colaboradores
git flow <feature|release|hotfix> finish <nome/feature> Encerrar a branch e fazer o merge para dev ou prd
git push origin <Branch> --> move para branch e solicita o merge
git push origin --all --> Empurrar tudo para o repo.
```
