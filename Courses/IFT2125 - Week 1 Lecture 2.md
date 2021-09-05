# IFT2125 - Week 1 Lecture 2

## Overview

This lecture introduced us to the notion of:
- asymptotic complexity (big O, little O, Big Omega, little omega, Big Theta)
- 3 algorithms:
    * pgcd(euclid + linear combination: sa+tb)
    * Fourier Transform: calculate Mx and M^-1x where M is an Vandermonde matrix (inversible matrix)
    * Appartenance Permutations

## Part 1 - Asymptotic Complexity

Il faut retenir les definitions de:
- Big O: Borne superieure (<=) : il existe un c pour lequel tous n>n_0 -> f(n) <= c * g(n)
- Little O: Borne superieure (<) : pour tout c et n > n_0 -> f(n) <= c * g(n)
- Big Omega: Borne inferieure (>=) : g \elem Big-O(f)
- Little omega: Borne inferieure (>) : g \elem little-o(f)
- Big Theta: Egalite des bornes (=) : f \elem Big-O(f) && g \elem Big-O(f)

## Part 2 - 3 Algorithms: pgcd, fourier transform, appartenance permutations

La deuxieme partie du cours introduisait a 3 algorithmes utilises frequemment en CS.
Il est important de retenir qu'on veut etudier:
- complexite de l'algorithme
- possibilite de parallelisation
- preuve de convergence (plus tard)

### Algorithme: pgcd

On a vu deux saveur du pgcd:
- euclid: reste modulo diviseur
- combinaison lineaire: pgcd(a,b)=sa+bt

Malgre que l'algorithme de euclid est lineaire O(n), il nous permet pas de
paralleliser nos calculs

### Algorithme: Fourier Transform

On n'est pas entre dans les details, il faut jute se souvenir que cette
methode nous permet de calculer rapidement la transformations lineaire Mx et M^-1x
d'une matrice inversible

### Algorithme: Apartenance Permutations

Cette section nous introduit a:
1. Ecrire les permutations en cycle
2. Produit de permutations

Prochain cours: comment effectuer des produits de permutations intelligemment
