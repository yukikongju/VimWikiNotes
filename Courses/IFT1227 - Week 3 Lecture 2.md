# IFT1227 - Week 3 Lecture 2: Circuits Sequentiel (Latch SR, Verrou D, Bascule D, Registers); Bascule avec signal (Enable, reset); circuits problématiques

## Overview 

Sections:
1. Circuits Séquentiels: Latch SR, Verrou D, Bascule D, registers
2. Bascules avec Signal (Enable, reset)
3. Circuits Problématiques

Le but de ce cours était de nous introduire aux circuits séquentiels, les cricuits 
avec mémoire à cours terme.

Dans un premier temps, on a vu les types de circuits séquentiels. Les nouveaux 
circuits introduits se servent des circuits définis auparavant ou cherchent à 
résoudre une problématique. On verra qu'on peut se servir de ces circuits pour 
implémenter des registres.

Dans un 2e temps, on veut introduire la notion de bascule

Finalement, on veut introduire quelques raisons qui peuvent rendre un circuit 
non fonctionnel.

## Part 1 - Circuits Séquentiels: Latch SR, Verrou D, Bascule D, registers

Il y a 4 éléments à se souvenir:
- Circuit bistable: 2 portes logiques NON dont l'output est l'input de l'autre
- Verrou SR (Latch SR): C'est un circuit bistable, mais on remplace les 2 portes 
  NON par des portes OU parce qu'on n'a pas de moyen de contrôler les états
- Verrou D (Latch D): La Latch SR possède une faille: il y a un état interdit 
  [S=1;R=1 produit Q=1 et Q'=1, ce qui est une contradiction]. La latch D est 
  une amélioration de la Latch SR, car elle enlève cet état interdit. Pour se 
  faire, on introduit un CLK, qui feed la latch SR
- Bascule D (Flip-Flop D): la Flip-Flop est le premier circuit qui a une 
  mémoire. Elle utilise 2 Latch D et sauvegarde la valeur de D au front montant
  (TO REVIEW)

À savoir:
1. Table de vérité
2. Circuit Interne
3. Symbole

## Part 2 - Registres et Bascules avec Signal (Enable, reset)

Puisque les Flip-Flops D possède une mémoire à court-terme, on peut les 
utiliser pour implémenter des registres. Plus généralement, on veut implémenter 
les bascules D en suivant 2 types de signal:
- Enable: Enable controle le moment lorsque le flip-flop store la nouvelle valeur
- Reset: si R=1 => Q est fixé à 0; si R=0 => flip-flop normal
- Set: si S=0 => Q est fixé à 1; si S=0 => flip-flop normal

## Part 3 - Circuits Problématiques (TODO)

Le circuit devient problématique lorsque:
- le signal oscille (à cause des inverseurs)
- Le circuit à un chemin cyclique

