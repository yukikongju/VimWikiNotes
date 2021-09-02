# IFT2105 - Week 1 Lecture 2 - Notation Asymptotique et Modeles Calculatoires repeter

## Overview

Le cours abordait 2 sujets:
1. Notation Asymptotique: Big O, petit O, Grand Omega, petit Omega, Grand Theta
2. Chapitre 2 - Modèles calculatoires: programmes répéter

## Part 1 - Notation Asymptotique

## Part 2 - Modèles Calculatoires

Il existe 5 modèles calculatoires:
- programmes répéter
- programmes tant que
- machines de turing
- lambda calculus
- circuits booleens

Ce cours-ci, on s'est penché sur les programmes répéter

### les programmes répéter

Les programmes répéter sont formés de registres initialisés à 0 pouvant contenir uniquement des entiers positifs. Ces programmes ne supportent que 3 instructions:
- store: r_i <- r_j
- increment: INC(r_i)
- repeat: repeat r times <bloc>

Remarques:
- les programmes répéter ne peuvent pas faire de boucle infini. Le nombre d'itérations est une constante

#### Sucre Syntaxiques

Pour rendre le code plus facile à lire, on peut:
- PROC: remplacer du code
- BOOLEANS: vrai=1; faux=0

#### Exemples de programmes répéter

- addition
- multiplication
- exposant
- Décrementation
- Soustraction
- factorielle
- Bool: and, negation, or
