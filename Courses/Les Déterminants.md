# Les Déterminants

## Overview

Trouver le déterminant d'une matrice à 2 utilités:
1. Déterminer si la matrice est inversible
2. Déterminer si la transformation produit un agrandissement ou non

Le calcul des déterminants permet aussi de résoudre des SEL à l'aide de la méthode de Cramer, qui est une méthode utilisée pour résoudre des ODEs (Wronskian)

## Comment Calculer le déterminant avec les propriétés

On peut utiliser les propriétés lignes et colonnes pour obtenir une matrice triangulaire, et le déterminant n'est que le produit de la diagonale

Opérations:
- Addition
- Swap: x-1
- Multiplication

## Comment déterminer si la matrice est inversible

Si le déterminant z ``det(A)=0`` l'inverse n'existe pas.

Remarque: l'inverse d'une matrice est unique

## Interprétation géométrique du déterminant

Il faut se souvenir que le déterminant calcule l'aire d'un parallélogramme. Ce même parallélogramme mesure l'aire de notre système de coordonnées. Ainsi, si :

- 0 < |det(A)| < 1 : le vecteur rétrécit après transformation
- |det(A)|=1: la transformation préserve la longueur du vecteur
- |det(A)|>1: le vecteur s'agrandit après transformation

- det(A) positif: même sens
- det(A) négatif: miroir

## Propriétés du déterminants

Propriétés du produit de matrices: `` det(AB) = det(A) det(B)``

Propriétés de la transposée de matrice: ``det(A) = det(A^T)``

## Règle de Cramer

- [Règle de Cramer](Règle de Cramer)
