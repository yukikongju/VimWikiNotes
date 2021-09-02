# IFT2105 - Week 1 Lecture 1 - Techniques de Preuves

## Overview

Le premier cours faisait un rappel sur les techniques de preuves:
- Preuve par contradition
- Preuve par induction/ reccurence généralisée
- Structure Récursive + Récurrence Structurelle
- Principe du Pigonnier
- Inclusion Mutuelle (axiome d'extensionalité)

## Techniques de Preuves

### Preuve par contradiction

Une preuve par contradiction est une preuve lorsqu'on montre que l'hypothèse et sa conclusion se contradise. Ainsi, pour que l'énoncé soit vrai, il faut que la conclusion soit fausse.

Ex: Montrer que sqrt(2) est irrationel

On suppose que sqrt(2) est un rationnel a/b, une fraction irréductible, et on montre que le fait que sqrt(2) est rationel est une contradiction avec le fait que pgcd(a,b)=1

### Preuve par induction / récurrence généralisée

Les preuves par induction se font toujours de la même façon:
1. Cas de base
2. Supposer que l'hypothèse est vraie et montrer pour n+1

La seule différence avec la récurrence et la récurrence généralisée est:
- récurrence: utilise P(n) pour montrer P(n+1) : uniquement le cas précédent
- Récurrence généralisé: peut utiliser tous les cas précédents

### Structure récursive et récurrence structurelle

La récurrence structurelle est importante parce qu'on utilisera cette technique de preuve pour les languages.

Tout d'abord, il est important de comprendre la notion de strucure récursive.

La structure récursive définit un alphabet et des règles pour construire de nouveaux éléments dans cet alphabet. La récurrence structurelle est la technique de preuve utilisée pour montrer que les règles définies vérifient une proposition quelconque. Pour ce faire, on fait une preuve par cas

#### Ex: Parenthésage

Structure récursive:
- alphabet : '(', ')'
- Règles:
  1. Entourer de parenthèse: (p)
  2. Concatener phrases: p=p_1 P_2

Récurrence Structurelle: la différence entre le nombre ouvert et fermés de parenthèses et toujours positifs
- R_1
- R_2

### Principe du pigonnier

Le principe du pigonnier nous dit que si on a n boites et n+1 objets, alors il y aura au moins une boite avec 2 objets.

Ce principe est simple, mais utile lorsqu'on est capable de reformuler le problème pour avoir l'énoncé.

#### Ex: Joueurs sur un terrain

Intuitivement, on essait de tracer un rayon autour de chaque joueur et de calculer l'aire minimum requis.

En utilisant le principe du pigonnier, on peut sépparer le terrain en 12, et on montre que l'hypothénuse du rectangle pour 12 joueurs est de 5

### Inclusion Mutuelle (axiome d'extensionalité)

Pour montrer que deux ensembles sont équivalents, il faut montrer que
``` A \inc B et B \inc A ```

#### Nombres fractionnaires sont des nombres periodiques

A = Nombre fractionnaires
B = Nombre periodique

A \inc B: division euclidienne
B \inc A: soustraction de puissances de nombre periodiques pour enlever la periode

