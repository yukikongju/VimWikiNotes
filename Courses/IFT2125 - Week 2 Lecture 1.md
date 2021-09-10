# IFT2125 - Week 2 Lecture 1

## Overview 

Ce cours-ci continuait sur le sujet de probleme d'appartenance permutations.
On a vu l'algorithme intelligent utilisant la notion du tamisage

## Part 1 - Rappel du Probleme d'apartenance

- Comment representer une permutation cycliques
- Comment representer l'inverse d<une permutation: regarder les cycles dans les sens inverse
- Permutation identite = permutation * inverse

Probleme d'appartenance: given a permutation, we want to know wether we will 
get that permutations after product of some other permutations 

## Part 2 - Tamisage

Le tamisage est un "helper" method qui va nous aider dans l'algorithme intelligent.

Il marche de la facon suivante:
1. Initialiser un matrice rectangulaire T[i,j] a l'identite
2. tant que la matrice n'a pas fixe une permutation pour chaque case,
   on regarde les permutations. 
   => si le tableau a la position i et son mapping j a une identite, ajouter 
	cette permutation au tableau
   => s'il y a collision, on fait rien: (on entre dans le else et on recalcule
	une autre permutation donnee par pi <- pi * (T[i,j])^-1)

### Algorithme pour le tamisage

```python
Tamiser(pi):
    while pi != epsilon:
	i <- min{i: i^{pi} != i} # premier point non-fixé
	j <- i^{pi}		 # mapping du point i
	if T[i,j] == epsilon:	 # si la case à i et j est l'identité, alors on ajoute
	    T[i,j] <- pi
	else:			 # sinon, multiplier par l'inverse de ce qu'il y a dans la case
	    pi <- pi * (T[i,j])^-1
```
