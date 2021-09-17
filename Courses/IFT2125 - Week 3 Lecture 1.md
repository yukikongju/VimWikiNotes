# IFT2125 - Week 3 Lecture 1 - Retour sur les preuves du problème d'appartenance; Rappel sur les définitions de la notation asymptotique; ordre conditionnel et règle de l'harmonie

## Overview

La première portion du cours était un rappel des preuves sur l'algorithme 
de tamisage pour résoudre le problème d'appartenance de permutations.

La deuxième partie du cours était un rappel sur les propriétés asymptotiques 
des fonctions. On a revu les définitions de Big O, Big Omega, Big Theta, ainsi que les théorèmes limites.

La dernière partie du cours nous introduisait la notion d'ordre conditionnel. Parfois, la fonction définit nous permet que de donner une borne asymptotique pour certaine valeur de n. Pour pouvoir enlever ces conditions, on veut utiliser la règle harmonique, qui nous dit que si une fonction est:
- éventuellement non-decreasing 
- f(n) Big Theta f(bn)

alors on peut enlever le conditionnel

Sections:
1. Grandes lignes sur les preuves du problème d'appartenance permutations  
2. Révision de la notation asymptotique: définitions Big O, Big Omega, Big Theta; Théorèmes Limites
3. Ordre conditionnel et et règle de l'harmonie


## Part 1 - Grandes lignes sur les preuves du problème d'appartenance permutations (TO REVIEW) 

Il y a 5 propriétés à retenir:
1. Toutes permutations tamisée s'écrit sous la forme a_m * a_{m-1} * ... * a_1 -> les permutations s'écrivent comme le produit des permutations sur les lignes précédantes (**)
2. L'ensemble des permutations G=<P_1, ..., P_n> inclu dans {Q_i}
3. Tout Q_i s'écrit sous la forme (**)
4. Il existe une bijection entre G et les Q_i

## Part 2 - Révision de la notation asymptotique  

### Definitions de Big O, Big Theta, Big Omega

### Théorèmes Limites

Si lim f(n)/g(n):
- cst c: f(n) et g(n) croit à la même vitesse par un facteur constant -> Big Theta
- infini: f(n) croit plus vite -> Big O
- 0: g(n) croit plus vite -> Big Omega

## Part 3 - Ordre conditionnel et et règle de l'harmonie

### Qu'est-ce que l'ordre conditionnel

Parfois, certaines fonctions sont définies seulement pour certaines valeur de n, 
alors on ne connait que son comportement (et donc son ordre) que pour certaines 
valeurs.

- Définition de l'ordre conditionnel:

Remarques: à cause de l'implication, l'ordre conditionnel est toujours vrai si 
P(x) est faux.

### À quoi sert la règle de l'harmonie

La règle de l'harmonie sert à enlever la condition de l'ordre conditionnel. Pour 
se faire, on doit vérifier 2 propriétés:
1. la fonction t(n) doit être évantuellement non-décroissante  
2. La fonction t(n) doit être smooth, c-à-d indépendante de sa constante -> t(n) = t(2n)

Remarque: En général, la les fonctions exponentielles ne sont pas smooth

