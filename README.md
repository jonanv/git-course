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
git branch <name>                                    # Crear nombre de rama
```

# Create alias
```
git config --global alias.rebuild "checkout -- ."
```

# Alias
```
co = checkout
lodag = log --oneline --decorate --all graph
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
```

# Cambiar de nombre de la rama master
```
git branch -M master
```