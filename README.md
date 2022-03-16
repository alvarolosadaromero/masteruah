alvar@DESKTOP-I2VC12C MINGW64 ~ (main)
$ cd desktop

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop (main)
$ cd Alvaro

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (main)
$ echo "#masteruah" >> README.md

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (main)
$ git init
Initialized empty Git repository in C:/Users/alvar/Desktop/Alvaro/.git/

## README
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (master)
$ git add README.md
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory

## Push inicial
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (main)
$ git push --tags

## Añadir fichero 1.txt
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (master)
$ echo "Fichero1" >> Fichero1.txt

## Crear el tag v0.1
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (master)
$ git tag v0.1

## Subir el tag v0.1
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git push --tags
Everything up-to-date


## Crear una rama v0.2
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (main)
$ git branch v0.2

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (main)
$ git checkout v0.2
Switched to branch 'v0.2'

## Añadir fichero 1.txt

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ touch 2.txt

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git add .
warning: LF will be replaced by CRLF in Fichero1.txt.
The file will have its original line endings in your working directory

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git commit -m "añadido 2.txt"
[v0.2 3ca5ebf] añadido 2.txt
 2 files changed, 1 insertion(+)
 create mode 100644 2.txt
 create mode 100644 Fichero1.txt
 

## Merge directo
 
 alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (main)
$ git merge v0.2 -m "merge v0.2 sin conflictos"
Updating 2bda955..3ca5ebf
Fast-forward (no commit created; -m option ignored)
 2.txt        | 0
 Fichero1.txt | 1 +
 2 files changed, 1 insertion(+)
 create mode 100644 2.txt
 create mode 100644 Fichero1.txt
 
 ## Merge con conflicto
 
 git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "adios en 1.txt"


## Listado de ramas

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git branch --merged
* v0.2

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git branch --no-merged
  main


## Arreglar conflicto
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ vim 1.txt

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git add .

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git commit -m "arreglado merge en 1.txt"
[v0.2 f0e26f4] arreglado merge en 1.txt
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 .1.txt.swo
 create mode 100644 .1.txt.swp

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$

## Borrar rama
alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git tag v0.2

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git branch -d v0.2
error: Cannot delete branch 'v0.2' checked out at 'C:/Users/alvar/Desktop/Alvaro'

## Listado de cambios

alvar@DESKTOP-I2VC12C MINGW64 ~/desktop/Alvaro (v0.2)
$ git config --global alias.list 'log --oneline --decorate --graph --all'
git list
* f0e26f4 (HEAD -> v0.2, tag: v0.2) arreglado merge en 1.txt
| * 2ee0308 (main) hola en 1.txt
|/
* 3ca5ebf (origin/v0.2) añadido 2.txt
* 2bda955 Commit inicial
* b9f69ac (tag: v0.1, origin/main) Commit inicial

![image](https://user-images.githubusercontent.com/99832565/158630666-607a14fa-a89e-4806-a416-5d24657ed7d5.png)


