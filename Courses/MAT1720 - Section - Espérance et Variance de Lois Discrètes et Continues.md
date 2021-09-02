# MAT1720 - Section - Espérance et Variance de Lois Discrètes et Continues

## Overview

1. Espérance et variance de variables aléatoires discrètes: l'espérance est la moyenne pondérée; la variance est E2(X(X-1))
2. Espérance et variance de variables aléatoires continues: l'espérance est la moyenne pondérée calculée à l'aide d'une intégrale; la variance est `` E(X) = E(X^2) - E(X)^2 ``

## Espérance et variance d'une variable aléatoire discrète

### Espérance d'une variable discrète

On peut interpréter l'espérance comme la moyenne pondérée des valeurs que peut prendre une variable aléatoire. Ainsi, il suffit de calculer

``` latex
\sum{p(x) x_i}
```
### Variance d'une variable discrète

La variance mesure la dispersion autour de l'espérance: `` V(X) = E[(X-u)^2]``

En distribuant, on se rend compte que `` V(X) = E(X^2) - E(X)^2 ``

Cepedant, les moments d'ordre 2 sont parfois plus difiiciles à évaluer que
`` E(X(X-1)) ``, qui est egal a `` E(X(X-1)) = E(X^2) - E(X)^2 ``

### Propriétés de l'espérance et de la variance

- Linéarité de l'espérance: `` E(aX+b) = aE(X) + b ``
- `` V(aX+b) = a^2 V(X)``

### Calcul Espérance et variance pour les variables aléatoires discrètes

- Espérance et variance d'une loi binomiale
- Espérance et variance d'une Poisson
- Espérance et variance d'une géométrique

## Espérance et variance d'une variable aléatoire continue

### Calcul de l'espérance et de la variance d'une variable aléatoire continue

Notons que les principes du calcul de l'espérance et de la variance pour une variable aléatoire continue restent les mêmes que celles discrètes. Cependant:
- l'espérance est calculée avec une intégrale, non pas une somme
- Les intégrales nous permettent d'évaluer E(X^2), on n'a pas besoin de calculer E(X(X-1)) pour calculer la variance, il suffit d'utiliser la formule  ``V(X) = E(X^2)-E(X)^2``

Calcul d'espérance et de variance pour:
- loi uniforme
- loi exponentielle
- loi normale

## Ressources
