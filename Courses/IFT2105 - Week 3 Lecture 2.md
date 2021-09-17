# IFT2105 - Week 3 Lecture 2 - Graphe Machine de Turing; Les machines de Turing sont équivalents aux programmes tant que; Lambda-Calcul

## Overview

Le 3e chapitre cherche à nous présenter la thèse de Church-Turing, qui nous 
dit que la représentation Machine de Turing et Lambda-Calcul sont équivalentes.
Pour ce faire, on veut d'abord se pencher sur comment les machines de Turing 
fonctionnent. On a donné un exemple en traçant les états de transitions représentant 
la fonction delta. Puis, on a montré que les machines de Turing sont équivalentes 
à des programmes tant que. Finalement, on a introduit la notion de lambda-calcul

Sections:
1. Exemple de Machine de Turing: Déterminer le nombre de zéros dans une string 
   est une puissance de 2 -> tracer le graphe et les états de transitions pour 
   la fonction delta
2. Preuve: Les machines de Turing peuvent simuler les programmes tant que
3. Lambda-Calcul

## Part 1 - Exemple de Machine de Turing: Déterminer si le nombre de zéros dans une string de zéros est une puissance de 2

Étapes:
1. Identifier l'alphabet et l'alphabet ruban; l'état acceptant et l'état refusant  
2. Dessiner le graphe des états de transition qui représente la fonction delta
3. Essayer le modèle avec des words

## Part 2 - Les machines de Turing sont équivalents aux programmes tant que

Au chapitre précédant, nous avons vu que les programmes tant que sont pas mal 
puissantes puisqu'elles arrivent à calculer des fonctions Ackermann, qui grandissent 
très rapidement. Ici, on essait de montrer que les machine de Turing font un 
travail semblable en montrant qu'elles sont équivalentes. 

La preuve qu'on fera prendra la forme de l'axiome d'extensionalité: (A=B <=> A \in B et B \in A)
- Montrer que toute machine de Turing peuvent simuler des programmes tant que
- Montrer que tout programme tant que peuvent simuler des machines de Turing

### Montrer que toute machine de Turing peuvent simuler des programmes tant que

Pour qu'une machine de Turing puisse simuler un programme tant que, il faut 
qu'on puisse reproduire les 3 instructions de base:
- incrémentation (inc(r_i))
- assignation (r_i <- r_j)
- boucle tant que ( tant que r_i != r_j )

Ainsi, on n'a qu'à définir les routines suivantes:
- incrémentation: routine qui incrémente la valeur et est capable de décaler les 
  registres
- assignation: routine qui déplace le ruban 
- boucle tant que: routine qui fait des allers-retour et est capable de faire 
  des tests

### Montrer que tout programme tant que peuvent simuler des machines de Turing

Pour montrer que tout programme tant que peuvent simuler des machines de Turing, 
on doit être capable de définir le 6-Tuples. Pour se faire, on veut storer 
certaines valeurs dans les registres:
- r_1: ruban encodé selon l'encodage de Godel
- r_2: état actuel de la machine
- r_3: position de la tête (position sur le ruban)

Puis, on définit la fonction delta dans la boucle tant que

### Part 3 - Lambda-Calcul (TO REVIEW)

Le lambda-calcul, inventée par Alonzo Church, est un programme équivalent aux 
machines de Turing. Cependant, alors que les machines de Turing définissent 
des languages et des états, le lambda-calcul, lui définit des fonctions.

Sections:
1. Qu'est-ce qu'un lambda terme
2. Opérations du lambda-calcul
3. Théorème de Church-Rosses: l'ordre sur lequel on fait des bétas réduction 
   n'a aucune incidence sur le résultat
4. Encodage de Church: Comment générer des nombres avec les fonctions définies 
   par le lambda-calcul
5. Arithmétique sur les entiers de Church

