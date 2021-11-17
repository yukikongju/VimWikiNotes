# IFT2125 - Week 3 Lecture 2

## Overview [J'ai manqué la deuxième partie du cours]

Sections:
1. Exemple de la règle de l'harmonie
2. Preuve de la Règle de l'harmonie
3. Opérations sur les Ordres
4. Master Theorem

## Part 1 - Exemple de la règle de l'harmonie

La règle de l'harmonie nous permet d'enlever la condition après la la condition 
d'ordre si la fonction est:
- évantuellement non-décroissante: t(n) <= t(n+1)
- Smooth: f(bn) <= O(f(n))

Ex: t(n) = 4*t((ceiling(n/2))) + 6n

On veut montrer que pour n=2^k (une puissance de 2), alors on peut appliquer le 
smoothness rule

Étapes:
1. Trouver la fonction t(2^k) par récurrence
2. Montrer que t(n) \elem \Theta (n^2 | n est une puissance de 2) en montrant que: (utiliser la récurrence t(2^k))
    1. t(n) \elem O(n^2 | n est une puissance de 2) :
    2. t(n) \elem \Omega(n^2 | n est une puissance de 2) :
3. Enlever la condition en vérifiant le smoothness rule:
    1. Montrer que t(n) est éventuellement non-décroissant par récurrence: t(n) <= t(n+1)
    2. Montrer que t(n) est smooth: t(bn) <= O(t(n)) [TO REVIEW]

## Part 2 - Preuve de la Règle de l'harmonie

La règle de l'harmonie nous dit que, sachant l'ordre conditionnelle d'une fonction t(n), 
on peut enlever la condition si:
- t(n) est éventuellement non-décroissante
- t(n) est smooth: t(bn) \elem O(t(n))

Pour se faire, on veut montrer que si t(n) répond à ces 2 critères, alors 
t(n) \elem \Theta (f(n)) => t(n) <= c f(n)

De plus, puisque le diviseur est une puissance de b, on sait que $n=b^{floor(log_b n)}$

L'argument: on utilise le fait que t(n) est O(f(n)) pour borner et trouver que 
$t(n) <= ac f(n)$

## Part 3 - Opérations sur les Ordres (TO REVIEW)

L'addition et multiplication des Big O (ou autres), nous dit que le Big O des 2 fonctions 
est la somme de 2 fonctions quelconques à l'intérieur de cette famille:
$O(f) +O(g)=h(n)$, ou h(n)=h_1(n) +h_2(n)

## Part 4 - Master Theorem

### Motivation derrière le master theorem

Lorsqu'on essait d'évaluer l'ordre de fonctions récursive, il est nécessaire 
d'énumérer toutes les occurences. On veut utiliser le master theorem afin 
d'éviter d'énumérer toutes les récurrences

### Rappel: comment évaluer l'ordre d'une fonction récursive (TODO)


### Le Master Theorem

Le Master Theorem nous dit que si T(n)=aT(n/b)+f(n^d), on doit considérer 
d=log_b a pour déterminer l'ordre de T(n):
- Cas 1: si d> log_b a, alors T(n) =O(n^d)
- Cas 2: si d = log_b a, alors T(n) O(n^d log n)
- Cas 3: si d<log_b a, alors T(n) = O(n^{log_b a})

Ressources:
- [what is the master theorem (5 min)](https://www.youtube.com/watch?v=2H0GKdrIowU&t=196s)
- [The Master Method (hard)](https://www.youtube.com/watch?v=zbf0llo3-YI)
- [Recursive Proof for Merge Sort](https://www.cs.mcgill.ca/~dprecup/courses/IntroCS/Lectures/comp250-lecture16.pdf)

