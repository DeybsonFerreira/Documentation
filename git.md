---
description: Tips for GitHub
---

# Git

## Git Flow, Git Workflow

Trabalhando com Master/Main / Feature/ Bugs/ Releases/ Hotfix: ::  **Link abaixo**:::

{% embed url="https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow" %}

## Remover commit / limpar branch

```aspnet
git clean -f (limpar alterações git, exclui comits, deixa branch original)
```

```aspnet
git reset --soft HEAD~
//este comando remove o último comit ( do histórico git)
// trazendo os comits para a máquina, sem excluír os arquivos do remoto/máquina
```



## Git Comandos iniciais

```aspnet
//New Repository

echo "# angular9-crud" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/DeybsonFerreira/angular9-crud.git
git push -u origin main
                
// Existent Repository
git remote add origin https://github.com/DeybsonFerreira/angular9-crud.git
git branch -M main
git push -u origin main
```

## Add Origin

```aspnet
git init  
git remote add origin your_repo.git  
git remote -v  
git status  
```

## Delete Commit 

> git reset HEAD~1

## Delete last Commit

* [x]  GIT RESET --HARD HEAD~1
* [x] PUSH ORIGIN HEAD --FORCE
* [x] GIT PUSH

## Unir commits

Para transformar todos os commits em um, existe o "Squash"  


![](.gitbook/assets/image%20%285%29.png)

