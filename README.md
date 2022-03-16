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



