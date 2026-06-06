# Pseudo Code

## Syntaxe globale

```text
VARIABLE
    nom_variable : TYPE
DEBUT
    ...
FIN
```

## Les types de variable

- Entier
- ...
- ...
- ...

## Les opérations

### L'affectation

On utilise ... pour affecter une valeur à une variable.

```text
VARIABLES
    a : ENTIER
    b : ENTIER
    somme : ENTIER

DEBUT
    a ... 5
    b ... 3
    somme ... a + b
FIN
```

### Utiliser les variables

- `... "texte"` : affiche une information à l'écran
- `... variable` : Attends une saisie utilisateur et la stocke dans la variable

## Les conditions

Une condition s'exécute ses instructions uniquement si sa condition est **vrai**.

```text
SI condition ALORS
    // si vrai
SINON SI condition ALORS
    // si vrai
...
    // si faux
FIN_SI
```

### Les opérateurs de comparaison

- `<` : ...
- `>` : ...
- `>=` : ...
- `<=` : ...
- `==` : ...
- `!=` : ...

### Les opérateurs logiques

- `&&` : ...
- `||` : ...
- `!` : ...

## La trace

La Trace : simuler l'exécution d'un algorithme à la main.

### Méthode

1. Numéroter les lignes entre `...`et `...`.
2. Faire un tableau avec une colonne pour la ligne, une colonne pour chaque variable et une colonne pour l'affichage
3. Lire le programme ligne par ligne, et reporter dans le tableau la valeur des variables quand elle change. (Elle devra être en vert uniquement sur cette ligne)
4. Faire de même pour toutes les lignes.

## L'itération

### TANT QUE

La condition est vérifiée avant chaque tour et les instructions ... tant que la condition est valide.

```text
TANT QUE condition FAIRE
    // instructions
FIN TANT QUE
```

> Attention aux boucles infinies !

### FAIRE...TANT QUE

La condition est vérifiée après chaque tour.

```text
FAIRE
    // instructions
... condition
```

> A utiliser quand on veut exécuter au moins 1 fois les instructions.

### POUR

Utilise un compteur pour ... une plage de valeurs.

```text
POUR variable ← debut à fin {PAR PAS DE pas}
    // instructions
FIN POUR
```

## Tableau

C'est une structure qui permet de stocker plusieurs valeurs de même type dans une seule variable.

### Syntaxe

```text
VARIABLES
    nomTableau : TYPE [...]
```

### Accès aux cases : indice

```text
VARIABLES
    tab : ENTIER [3]
DEBUT
    tab... ← 234
    AFFICHER tab...
FIN
```

> Attention, les indices commencent toujours à 0 !

### Parcourir un tableau

```text
VARIABLES
    tab : ENTIER [3]
    i : ENTIER

DEBUT
    tab[0] ← 234
    tab[1] ← 48
    tab[2] ← 20
    ... i ← 0 à 2
        AFFICHER tab[i]
    FIN ...
FIN
```
