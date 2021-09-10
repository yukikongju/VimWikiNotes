# IFT2125 - Week 2 Lecture 2

## Overview

This lecture was a continuation on the principle of TAMISAGE.

Sections:
1. Trace du Tamisage: que ce passe-t-il lorsqu'on entre dans le if/else 
2. Propriété du Tamisage #1: Le nombre de permutations generees par le tableau 
   est donne par le produit du (nombre de permutations par ligne +1)
3. Propriété #2: Toute permutation peut s'écrire comme le produit des permutations
   des lignes avant elles

## Rappel - Le probleme d'appartenance permutations et le principe de tamisage

Given a permutation, we want to find wether a bunch of permutations P_i 
generates that permutations. Naively, we can simulate all these permutations, 
but the results will be quite slow. Instead, we want to use TAMISATION.

### Principe de Tamisation

```python
tamisage(pi):
    while pi != epsilon:
	i <- min{index non-fixe}
	j <- mapping de la permutation de i
	if T[i,j] == epsilon:
	    T[i,j] = permutation pi
	else:
	    pi = pi * inverse T[i,j]
```

Principles:
- On veut rouler l'algorithme sur les index qui mappent a eux-memes, car on 
  va obtenir de nouvelles permutations

## QUESTION: Quelle est la condition d'arret pour l'algorithme du tamisage?

On n'obtient plus de nouvelles permutations

## Comment savoir si la permutation P est generer par les permutations P_i

Pour determiner si la permutation P est generer par les permutations P_i, 
on execute l'algorithme complet, puis on roule tamisage une derniere fois pour
obtenir une permutation, qui nous envoie vers T[i,j]:
- si T[i,j] == epsilon: (pas de collision) -> la permutation n'est pas généré
- si T[i,j] != epsilon: (collision) -> la permutation est généré

Pourquoi: voir preuve

## Preuve - Toute permutation peut s'ecrire comme le produit des permutations des lignes avant elle

Enonce: si m tours de la boucle suffisent pour tamiser la permutations pi, alors pi peut s'exprimer comme le produit des lignes precedantes

Cette preuve se fait par induction

### Cas de base

Par hypothese, la permutation pi n'est pas l'identite. Ainsi, trivialement, on ne rentre jamais dans la loop. L'enonce est donc faux, ce qui rend l'implication vraie.

### Pas d'induction

On doit gere 2 cas:
- T[i,j] == epsilon: on insere la permutation pi elle-meme; on peut ecrire pi comme le produit des autres permutations
- T[i,j] != espilon: on a une collision (a prouver !!)

#### Collision: T[i,j] != epsilon (TO REVIEW)



