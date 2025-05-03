# Git - Github

// Sort es una funcion que tiene efecto, para comparar restamos los precios y segun si es positivo o negativo significa q es > o <


## Git Flow

-> El proyecto lo podemos dividir en distintas ramas:
    - Main: Nuestra rama principal en la que esta la version mas estable
    - Hotfix: Arreglos urgentes directamente sobre la rama main
    - Release: Una rama mas estable, en la que los testers estan probando constantemnete las nuevas features
    - Develop
    - Features

## GitHub Flow

-> Todos los cambios hacia la rama main, haciendo pull request

### Merge

-> Merge sirve para fusionar los cambios de dos ramas

> Como se hace?

    - git merge <rama>          (Un nuevo commit con todos los cambios de la rama en paralelo, quedan en el historial los commits)
    - git merge --squash <rama> (Combina todos los commits en uno)
    - git rebase <rama>         (Todos los cambios se aplican en la rama principal)

# Versionado Semantico

## MAJOR.MINOR.PATCH

-> Dividir cada version del codigo 

    - Major : Incrementos incompatibles con la intefaz que esta ahora
        => Comienza con 0.x.x para desarrollo interno
        => Pasa a 1.x.x a partir que se define la api publica
    - Minor : Incrementos que agregan funcionalidades a versiones anteriores
    - Patch : Arreglos retrocompatibles, comienzan en 0 por cada Minor 

# Changelog

-> Archivo cronologicamente ordenado que muestra los cambios notables en la version de un software, por ejemplo: 
    -Added
    -Fixed
    -Security
    -Changed
    - Deprecated
    - Removed