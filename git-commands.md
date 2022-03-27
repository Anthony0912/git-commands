# GUIA DE COMANDOS PARA USAR EN GIT

- ## ARCHIVOS DE GIT PARA SUBIR CARPETAS VACIAS
    - .gitkeep

- ## GIT INIT PROJECT
    ```
    git init
    git remote add origin <url-repositorio>
    git remote set-url origin <url-repositorio>
    git add .
    git commit -m "Initial commit"
    git push -u origin master
    ```

- ## GIT CONFIGURACION GLOBAL

    #### 1. GLOBAL
    ```
    git config --global alias.s status -sb -> Agregar alias
    git config --global -e -> Ver configuracion global de git
    git config --global user.name "FIRST_NAME LAST_NAME"
    git config --global user.email "MY_NAME@example.com"
    git config --list
    git config --global user.name
    git config --global user.email
    git config --global init.defaultBranch main -> Cambiar nombre de la rama principal 
    ```
    #### 2. CONFIGURACION POR PROYECTO
    ```
    git config user.name "FIRST_NAME LAST_NAME"
    git config  user.email "MY_NAME@example.com"
    git config user.name
    git config user.email
    ```

- ## GIT STASH
    ```
    git stash -> Crea un nuevo stash
    git stash save "detalle" -> Crea un nuevo stash con nombre personalizado
    git stash list
    git stash list --stat -> Muesta informacion de todos los stash
    git stash pop -> Toma los ultimos cambios
    git stash clear -> Borra todos los stash
    git stash drop <ident stash> -> Elimina el stash por su identificador
    git stash apply <ident stash> -> Obtiene cualquier almacenado stash
    git stash show <ident stash> -> Vista previa de las modificaciones del stash
    ```

- ## GIT TAGS
    ```
    git tag -d 
    git tag v0.0.1 -m "Esta es la versión inicial"
    git tag
    git show v0.0.2
    git push origin/master --tag
    git tag -a v4.2 -m "version" -> agregar tag un commit
    git tag -a v28 hascommit -m "<descripcion>"
    git push origin :refs/tags/v<verision> -> Elimina tag remoto
    ```

- ## GIT ELIMINAR RAMAS
    ```
    git branch -d ACM-F06
    git push origin :ACM-F06
    git fetch -p (es para actualizar y ver qué ramas ya se borraron)
    ```

- ## GIT COMMIT
    ```
    git pull origin development->baja cambios de la misma rama o otra rama
    git commit --amend -m "" -> Actualiza el mensaje del ultimo commit 
    git reset --soft (HEAD^) (HASH) (numero commit)-> Vuelve al utilmo commit o cualquiera
    git commit -am "commit" -> solo cuando se da seguimiento a los archivos
    git reflog -> Muestra de forma cronologica los commits realizados
    git reset --hard <hash commit> -> Desace los cambios forzadamente
    git commit -m "Title" -m "Description"
    ```

- ## GIT COMANDOS GENARALES

    ```
    git diff  o git diff --staged ->ver modificaciones
    git checkout -- . -> Recostruya el proyecto a como estaba el ultimo commit
    git reset <nombre-archivo> -> Remueve el archivo que no queremos subir al repositorio
    git branch -> rama en la que te encuentras
    git branch experimental-> crear rama
    git show-branch -> descripcion detallada de las ramas
    git checkout experimental-> pasar de una rama a otra
    git checkout -b otrarama -> crear una rama nueva y moverte a ella en un único paso.
    git merge experimental -> permite fusionarla con la rama
    git merge experimental -m 'Esto es un merge con mensaje'
    git branch -d rama_a_borrar -> Borrado de la rama en local
    git branch -D rama_a_borrar ->forzar el borrado de la rama
    git push origin --delete rama_a_borrar -> Eliminar un branch en remoto
    git mv <nombre archivo original> <ruta (se puede cambiar el nombre)> -> Funciona para mover archivos a otra ruta
    git rm <nombre del archivo> -> remueve el archivo
    ```