# git-course

Course of git follow Fernando Herrera´s course in DevTalles

## Commands Git
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
git checkout <branch-name>                           # Cambiar de rama
git switch <branch-name>                             # Cambiar de rama
git branch -d <branch-name>                          # Eliminar rama
git branch -d <branch-name> -f                       # Eliminar rama forzadamente
git checkout -b <branch-name> -f                     # Crar rama y cambiar a rama inmediatamente
git tag <tag-name>                                   # Crear una etiqueta
git tag                                              # Listar las etiquetas
git tag -d <tag-name>                                # Eliminar una etiqueta
git tag -a <tag-name> -m "message"                   # Crear una etiqueta con annotate(-a)
git tag -a <tag-name> HASH -m "message"              # Crear una etiqueta a un commit con el HASH
git show <tag-name>                                  # Ver la informacion de un tag
git stash                                            # Guardar cambios momentaneos
git stash list                                       # Listar los cambios momentaneos
git stash pop                                        # Recupera el ultimo stash y lo aplica
git stash apply stash@{0}                            # Recupera el stash con el id y NO lo borra
git stash drop stash@{0}                             # Elimina la posision 0 del stash
git stash show stash@{0}                             # Muestra la info del stash 0
git stash save "message"                             # Crear un stash con un nombre
git stash list --stat                                # Lista los stash con mas información
git stash clear                                      # Limpia todos los stash
git rebase <branch-name>                             # Hacer rebase
git rebase -i HEAD~4                                 # Hacer rebase itereactivo 4 commits anteriores
git checkout -- <file-name>                          # Reconstruir el archivo como estaba antes
git rebase --continue                                # Continuar con el rebase interactivo
```

## Commands GitHub
````
git remote add origin https://...... (git rao)       # Conectar con repositorio github
git push -u origin main              (git puom)      # Hacer push a github


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
rb = checkout -- .
ss = status --short
rbf = git checkout --
```

## Change name of principal branch
```
git branch -M master
```

## Config default branch to main
```
git config --global init.defaultBranch main
```