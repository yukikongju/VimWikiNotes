# MAT1600 - Section - Matrices Inversibles

## Overview

La matrice inverse de A, notée A^{-1}, est la matrice qui nous permet de revenir retrouver le vecteur avant la transformation.

## Définition d'une matrice inversible

Une matrice carrée est inversible ssi AB= BA = I

## Résolution du SEL Ax=b avec la matrice inverse

Si on veut trouver le vecteur x en sachant b, le vecteur après transformation, et A, la matrice de transformation, on peut utiliser son inverse SI ELLE EXISTE. En multipliant par l'inverse des 2 côtés, on obtient:
`` A^-1A x = A^-1b``

## Analogie: nombre réel -> Pourquoi les matrices ne sont pas toujours inversibles

On sait que les nombres réels forment un groupe abélien, ce qui veut dire que tous les nombres possèdent un inverse, sauf 0.

Par exemple: trouver la valeur de 4x = 6 -> x = 6/4, car inversible

Cependant, trouver la valeur de x dans 0x = 0 -> impossible, car il existe une infinité de valeurs.

## Comment déterminer si une matrice est inversible: déterminants

- [Les Déterminants](Les Déterminants)

## Comment trouver la matrice inverse avec la méthode de Gauss-Jordan (si elle existe)

[A|I] ~ [I|A^{-1}]

## Matrices élémentaires

Si A est une matrice inversible, alors on peut la représenter comme le produit de matrices élémentaires, qui ne sont que des matrices identités par lesquelles on a appliquer une opérations lignes.

Ainsi, si A peut être représenter par le produit de matrice élémentaires, elle est nécéssairement inversible. Donc, les matrices obtenus avec la méthode de Gauss sont inversibles

## Propriétés des matrices inversibles

1. (A^-1)^-1 = A
2. (AB)^-1 = B^-1 A^-1
3. (A^T)^-1 = (A^-1)^T

## Importance des matrices inversibles

La notion de matrice inversible revient lorsqu'on abordera la notion de diagonalisation. Essentiellement, on essait de trouver l'ensemble de valeurs pour lesquelles Ax=λx, c'est-à-dire l'ensemble de valeurs/vecteurs qui font ensorte qu'on perd une dimension (matrice non-inversible)
