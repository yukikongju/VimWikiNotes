# IFT2105 - Week 4 Lecture 2

## Overview

Sections:
1. Opérations dans le lambda-calcul (suite): décrémentation, soustraction, égale à zéro, plus grand ou égal 
2. Boucles et Récursion dans le lambda-calcul  
3. Preuve: les machines de Turing et le lambda-calcul sont équivalent  
4. Languages Réguliers


## Part 1 - Opérations dans le lambda-calcul (suite): décrémentation, soustraction, égale à zéro, plus grand ou égal 

### Remarque sur le Théorème Church-Moses

Le théorème de Church-Moses stipule que d'exécuter des bétas réductions 
dans l'ordre qu'on veut ne change pas la solution. Par contre, on peut créer 
des boucles infinies, dépendemment de la façon dont on exécute nos fonctions.

PLus généralement, il existe 3 façons d'évaluer nos fonctions:
- à partir de la gauche
- évaluation appliquée (???)
- méthode paresseuse: on évalue les fonctions dont on a besoin (haskell)


## Part 2 - Boucles et récursion dans le lambda-calcul

Dans cette partie, on définit comment implémenter les boucles et récursions.

Pour construire notre fonction, initialement, on définit notre fonction avec 
elle-même, ce qui est mal défini. Par contre, pour régler ce problème de 
formattage, on utilise l'astuce suivante: on définit M' et on dit que 
$M:=M'M'$

### Boucles dans le lambda-calcul

Initialement, une boucle tant que est définit avec SAS de la facon suivante:
$ G:= \lambda x. SAS ( (x) (G(Fx)) (Rx) ) $. 

Rappel: SAS(si x, alors G(Fx); sinon (Rx))

Cependant, cette formulation est erronée, car on définit la fonction G à 
l'intérieur de la fonction qu'on essait de définir. Pour se faire, on 
doit définir la fonction G', qui est une fonction qui prend en fonction 

$ G':= \lambda f. \lambda x. SAS ( (x) (ffx) (Rx) )$; $G:=G'G'$

Ainsi, $G:= \lambda f. \lambda x. SAS ( (x) (G'G'x) (Rx) )$ = 
$G:= \lambda f. \lambda x. SAS ( (x) (Gx) (Rx) )$


### Fibonacci


## Part 3 - Montrer que les machines de Turing et le lambda-calcul sont equivalents

L'argument utilisé est le même que pour montrer que les fonctions tant que et 
les machines de turing sont équivalents: on montre qu'il est possible d'en 
exprimer une de la même façon que l'autre

### Montrer que le lambda calcul s'écrit avec une machine de turing

