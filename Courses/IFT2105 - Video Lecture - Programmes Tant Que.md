# IFT2105 - Video Lecture - Programmes Tant Que

## Overview

Sections:
1. Programmes Tant Que  
2. Les programmes tant que sont plus puissants que les programmes repeter

## Part 1 - Programmes Tant Que  

Les programmes tant que sont des programmes repeter, mais dont les boucles sont definis de facon a permettre des boucles infinies.

``tant que r_i != r_j { ... }``

Le sucre syntaxique est les fonctions booleennes sont donc definies de la meme maniere

## Part 2 - Les programmes tant que sont plus puissants que les programmes repeter

Le cours dernier, nous avons montrer qu'il existait des programmes que les programmes repeter ne peuvent calculer: les fonctions Ackermann.

Pour montrer que les programmes tant que sont plus puissants que les programmes repeter, nous avons qu'a montrer que les programme tant que peuvent resoudre les fonctions Ackermann

### Preuve: les programmes tant que peuvent calculer les fonctions Ackermann (TO REVIEW)

On redefinit une fonction Ackermann A(i,x) et on travaille avec une pile:
- si i=0: x+1 -> remplace i par x+1
- si i>0 et x=0: A(i-1, 1)
- sinon: A(i-1, A(i, x-1)) -> add A(i, x-1) on top of the stack 

#### Pseudo code tant que (TO COMPLETE)


