# git-course

Course of git follow Fernando Herrera´s course in DevTalles

## Commands Git
```
git --version                                        # Ver la versión de git
git help                                             # Ver comandos ayuda
git commit                                           # Hacer commit
git --help config                                    # Ver comandos ayuda de config
git config list                                      # Ver configuraciones
git config --local --list                            # Ver la configuración del proyecto actual (Local)
git config --local user.username "John Doope"  
git config --local user.name "johndoope"
git config --local user.email "johndoope@gmail.com"
git config --global --list                           # Ver la configuración de tu usuario (Global)
git config --global user.name "John Doope"           # Asignar nombre del usuario global
git config --global user.username "johndoope"        # Asignar nombre de usuario global
git config --global user.email "johndoope@gmail.com" # Asignar email de usuario global
git config --global -e                               # Ver configuraciones globales
git config -e                                        # Ver configuraciones de proyecto
git config --global --unset user.name                # Eliminar una configuracion global user.name
git init                                             # Inicializar un repositorio
git status                                           # Ver los archivos que tienen cambios
git status --short                                   # Ver los archivos que tienen cambios forma corta
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
git commit --amend --date="AAAA-MM-DD HH:MM:SS"      # Cambia la fecha de un commit
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
git rebase --abort                                   # La rama se volverá al estado anterior a la rebase interactiva
git revert -m 1 <hash_del_commit_merge>              # Hacer rollback en git con el hash del merge para revertir cambios. La bandera -m 1 es fundamental. Indica a Git que mantenga la línea principal (la rama en la que estabas cuando hiciste el merge).
```

## Commands for delete commit in server
```
Para eliminar parte del historial de commits en Git, puedes usar el comando git rebase -i con la opción --interactive para editar el historial de commits de manera interactiva. Luego, en el editor de texto que se abre, puedes marcar los commits que deseas eliminar con la opción drop, guardar y cerrar el editor. Finalmente, puedes forzar la actualización del historial con git push --force

git rebase -i HEAD~1                                 # Hacer rebase itereactivo 4 commits anteriores
git push --force                                     # Forzar la actualización del historial
```

## Commands GitHub
```
git remote add origin https://...... (git rao)       # Conectar con repositorio github
git push -u origin main              (git puom)      # Hacer push a github

git remote add upstream https://...... (git rau)     # Hacer referencia a otro repositorio Fork

git clone --depth=1 <repo>                           # Clonar un repositorio Git sin el historial de commits

git clone --branch <branchname> <remote-repo-url>    # Clonar una rama especifica

git push --tags                                      # Publicar todas las etiquetas
git fetch                                            # Actualizar las referencias con el servidor git
git checkout HASH <file-name>                        # Revertir el cambio con el HASH de un archivo
git status -sb                                       # Ver el estado de la rama
git status -short --branch                           # Ver el estado de la rama
git pull --all                                       # Traer todo del repositorio
git push --all                                       # Subir todo del repositorio
git branch --all                                     # Ver todas las ramas del repositorio
git branch --a                                       # Ver todas las ramas del repositorio
git push origin :<branch-name>                       # Eliminar la rama desde el origen
git remote prune origin                              # Revisa y actualiza las referencias de las ramas
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
ssb = status --short --branch
rbf = checkout --
ba = branch --all
rpo = remote prune origin
t = tag
ta = tag -a 
pt = push --tags
ce = config -e
```

[Gist about git alias](https://gist.github.com/jonanv/9c2419dbea9561e742473895e5d437e6)

## Change name of principal branch
```
git branch -M master
```

## Config default branch to main
```
git config --global init.defaultBranch main
```

# Signing commits with SSH key
```
git config --global user.signingkey <SSH_KEY_ID>
git config --global commit.gpgsign true
```

## Verify signed commit
```
git log --show-signature                           # Verify all commits
git log --show-signature -1                        # Verify last commit
```

# Steps to generate SSH key
🧩 PASO 1 — Ver si ya tienes llave SSH

En PowerShell o Git Bash:
```
ls ~/.ssh
```

Si ves algo como:
```
id_ed25519
id_ed25519.pub
```

👉 Ya tienes llave, salta al PASO 3

🧩 PASO 2 — Crear llave SSH (si no tienes)
```
ssh-keygen -t ed25519 -C "tu_email_de_github@correo.com"
```

Dale Enter a todo
(Opcional: ponle passphrase)

🧩 PASO 3 — Subir la llave a GitHub

Copia tu llave pública:
```
cat ~/.ssh/id_ed25519.pub
```

Ve a:
👉 https://github.com/settings/keys

Haz clic en:

- New SSH Key

Y MUY IMPORTANTE:

- Title: Mi PC trabajo
- Key type: 🔽 Signing key
- Pega la llave
- Save

🧩 PASO 4 — Decirle a Git que firme con SSH

Configura esto:
```
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

🧩 PASO 5 — Arreglar tu commit actual

Firma el commit que ya existe:
```
git commit --amend --no-edit -S
```

🧩 PASO 6 — Push
```
git push --force-with-lease
```

1️⃣ Verifica que Git quedó configurado para firmar con SSH

Corre esto:
```
git config --global --get gpg.format
git config --global --get user.signingkey
git config --global --get commit.gpgsign
```

Debe salir algo así:
```
ssh
C:/Users/TU_USUARIO/.ssh/id_ed25519.pub
true
```


# 🚑 Solución en Git Bash (Windows)
1️⃣ Arranca el ssh-agent

Ejecuta esto tal cual:

```
eval "$(ssh-agent -s)"
```

Deberías ver algo como:

```
Agent pid 1234
```

2️⃣ Agrega tu llave SSH
```
ssh-add ~/.ssh/id_ed25519
```

Si te pide passphrase → ponla
Si no da error → perfecto

3️⃣ Verifica que quedó cargada
```
ssh-add -l
```

Debe mostrar algo como:

```
256 SHA256:xxxxx id_ed25519 (ED25519)
```

# ✅ Solución definitiva (haz esto TAL CUAL)
1️⃣ Crea el archivo que Git necesita

En Git Bash:

```
mkdir -p ~/.config/git
touch ~/.config/git/allowed_signers
```

2️⃣ Mete tu llave pública ahí dentro

Primero copia tu llave:

```
cat ~/.ssh/id_ed25519.pub
```

Ahora edita el archivo:

```
nano ~/.config/git/allowed_signers
```

Pega esta línea en UNA sola línea:

```
<USER> <PEGA_AQUÍ_TU_LLAVE_COMPLETA>
```

Ejemplo real:

```
pruebauser ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIMabc123xyz... tucorreo@dominio.com
```

Guarda:

- CTRL + O → Enter
- CTRL + X

3️⃣ Dile a Git que use ese archivo
```
git config --global gpg.ssh.allowedSignersFile ~/.config/git/allowed_signers
```

4️⃣ Verifica que quedó bien

```
git config --global --list | grep ssh
```

Debe salir:

```
gpg.format=ssh
user.signingkey=~/.ssh/id_ed25519.pub
gpg.ssh.allowedSignersFile=~/.config/git/allowed_signers
commit.gpgsign=true
```


# Setup SSH for authentification
 
Setup SSH for signing commits
This guide sets up SSH commit signing globally using a dedicated signing key (separate from your auth key).
Official documentation → 

[SSH README](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key-for-a-hardware-security-key)

1. Create a Dedicated Signing Key
```
ssh-keygen -t ed25519 -C "your-email@example.com" -f ~/.ssh/id_ed25519_signing
```

2. Load the Key into the Agent (and Keychain)
```
eval "$(ssh-agent -s)"ssh-add --apple-use-keychain ~/.ssh/id_ed25519_signing
```

3. Add the Public Key to GitHub as a Signing Key
Copy your public key:
 ```
cat ~/.ssh/id_ed25519_signing.pub
```

Then on GitHub:
- Go to Settings → SSH and GPG keys → New SSH key
  - Set Key type to Signing key
  - Paste the public key
  - You should then have one Authentication Key and one Signing Key in Github.

4. Configure Git Globally to Sign Commits
```
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519_signing
git config --global commit.gpgsign true
```

5. Enable Local Verification (Optional but Recommended)
Create an allowed signers file:
```
mkdir -p ~/.config/gittouch ~/.config/git/allowed_signers
```
Add a line to `~/.config/git/allowed_signers` with your public (.pub) key as in:
 
```
echo "your-email@example.com $(cat ~/.ssh/id_ed25519_signing.pub)" >> ~/.config/git/allowed_signers
```
`~/.config/git/allowed_signers` shoudl look like

```
your-email@example.com ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAI...
```

Point Git to it:
 
```
git config --global gpg.ssh.allowedSignersFile ~/.config/git/allowed_signers
```

6. Verify Locally
After your next commit (the first one that should be signed now), run below
 
```
git log --show-signature -1
```

Expected output:
 
```
Good "git" signature for your-email@example.com with ED25519 key ...
```

7. Verify on GitHub
Push a commit and confirm it shows Verified.

Common Issues

| Issue | Cause |
| :--------: | :-----------------------: |
| "No signature" on GitHub | Key wasn't added as a Signing key (auth key isn't enough) |
| "No signature" in `git log --show-signature` | Missing allowedSignersFile or wrong contents |
| Wrong key used | Check `git config --global user.signingkey` |

 
