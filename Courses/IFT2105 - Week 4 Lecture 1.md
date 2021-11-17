# IFT2105 - Week 4 Lecture 1

## Overview 

This lecture focussed on the operations we can perform on numbers encoded 
with Church encoding. Last lecture, we saw how to perform incrementation, 
addition, multiplication and exponentiation. In this lecture, we will focus on 
decrementation. However, to perform this operation, we need to define booleans 
and table.

Il faut se souvenir qu'on définit d'abord les opérations qu'on performe, puis ensuite, 
on performe des bétas réductions

## Part 1 - Rappel: Church Encoding et opérations de base: incr, add, mult, exp (TO REVIEW)

Church Encoding: f |-> f^<n>


## Part 2 - Operations on Church Encoding: booleans and logical Operations

On définit d'abord la fonction, puis on peut construire la "table de vérité" en faisant 
chacun des cas

* Booleans:
    * TRUE:= $\lambda xy.x$
    * FALSE:= $\lambda xy.y$
* Logical Operations:
    * NOT:= $\lambda p.p FAUX VRAI$
    * ET:= $\lambda pq.pqp$
    * OU:= $\lambda pq.ppq$
    * SAS:= $\lamda p.p$ (si alors, sino) (TO REVIEW)

## Part 3 - Tuples, Liste et Vide? (TODO)




## Part 4 - Decrementation (TODO)

1. Fonction Phi: on créé un tuple et le k-ieme tuple, on 


