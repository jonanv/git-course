# git-course

Course of git follow Fernando Herrera´s course in DevTalles

## Commands
```
git --version                                        # Ver la versión de git
git help                                             # Ver comandos ayuda
git commit                                           # Hacer commit
git --help config                                    # Ver comandos ayuda de config
git config --global user.name "John Doope"           # Asignar nombre de usuario global
git config --global user.email "johndoope@gmail.com" # Asignar email de usuario global
git config --global -e                               # Ver configuraciones globales
git config -e                                        # Ver configuraciones de proyecto
git init                                             # Inicializar un repositorio
git status                                           # Ver los archivos que tienen cambios
git add <name>                                       # Agregar un archivo al stage
git commit -m "Coment"                               # Crear un commit con mensaje
git checkout -- .                                    # Reconstruir el proyecto a como estaba antes
git brach                                            # Listar las ramas
git branch <name>                                    # Crear nombre de rama
git diff                                             # Ver los cambios entre archivos
git diff --staged                                    # Ver los cambios entre archivos en el stage
git commit -am "message"                             # Agregar un commit de forma abreviada (add message)
git commit --amend -m "message"                      # Reescribir el commit anterior o correguirlo
git reset --soft HEAD^                               # Revertir el cambio anterior (ejem. ^2)
git commit --amend                                   # Abre todo el editor para reescribir el commit
git reset --soft <65ed0b2>                           # Revertir el cambio anterior con HASH
git reset --mixed <769efb3>                          # Revertir el cambio anterior, no deja en el stage
git reset --hard <f710079>                           # Revertir el cambio anterior, destructivo
git reflog                                           # Muestra todo el historial de commits
git mv destruir-mundo.md salvar-mundo.md             # Renombrar archivo
git rm salvar-mundo.md                               # Eliminar archivo
```

## Create alias
```
git config --global alias.rebuild "checkout -- ."
```

## Alias
```
co = checkout
lodag = log --oneline --decorate --all --graph
unstage = reset HEAD --
s = status
sw = switch
bsc = branch --show-current
rank = shortlog -sn --no-merges
alias = config --get-regexp ^alias\\.
b = branch
rv = remote -v
fo = fetch origin
pso = push origin
plo = pull origin
rebuild = checkout -- .
ss = status --short
```

## Change name of principal branch
```
git branch -M master
```

## Config default branch to main
```
git config --global init.defaultBranch main
```