# IFT1227 - Week 2 Lecture 1

## Overview

This lecture focussed on Simplification methods for combinatorial circuits
- Simplification using DeMorgan Methods (inversion de bulles)
- Simplification par observation pour les circuits combinatoires a priorite
- Table de Karnaugh

## Part 1 - Simplification using DeMorgan Methods (inversion de bulles)

Cette methode conciste a simplifier un circuit en utilisant les regles suivantes:
- inverser les outputs bulles pour des input bulles et simplifier
- inverser les portes logiques et/ou

Remarques:
- Pour ecrire la fonction d'un circuit logique, on lit le circuit de droite vers la gauche

## Part 2 - Simplification par observation pour les circuits combinatoires a priorite

Cette technique est utilisee pour simplifier des circuits a priorites, dont les outputs sont exacts au bit le plus significatif

Pour representer chaque output, on peut ecrire une fonction qui enleve les outputs qui ne sont pas utilises avec une negation

### Table de verite pour un encodeur de priorite

- Table de verite: le seul output correspond a l'input avec le bit le plus significatif

### Regles de conception pour un circuit d'un encodeur de priorite

- Input en haut a gauche; output en bas a droite
- Jonction with DOTS: ???

### Don't care

les don't care valent 2 lignes

Remarques:
- les X dans les tables de verite representent des don't care; dans les circuits, ca representent des conflits

## Part 3 - Table de Karnaugh

On utilise les tables de Karnaugh pour simplifier les tables de verite et
ainsi reecrire les fonctions canoniques simplifiees. Il est possible d'ecrire les fonctions canoniques en SOP ou en POS, mais pour le cours, on se concentrera sur le SOP.

On verra 3 types de resolutions pour les tables de Karnaugh:
- Tables de Karnaugh pour 3-4 entrees
- Tables de Karnaugh pour 3-4 entrees + don't care
- Tables de karnaugh pour 5-6 entrees: superposer les tables de Karnaugh 4

### Regles de simplification pour les tables de Karnaugh

- Ecrire les lignes et colonnes de la table en suivant le code grey: un seul bit change
- regroupement des "1" en suivant la regle des puissances de 2
- reecrire la fonction p/r aux entrees qui ne changent pas
- les colonnes et les coins sont relies. 
  
- Question: Dans les tables de Karnaugh, les lignes sont-elles connectees?

### Resolution des tables de Karnaugh

#### Tables de Karnaugh pour 3-4 entrees


#### Tables de Karnaugh pour 3-4 entrees + don't care

On considere les X et don't care comme des "1" s'ils permettent de former de regroupement de puissance 2

#### Tables de karnaugh pour 5-6 entrees: superposer les tables de Karnaugh 4

Puisqu'on ne peut pas representer les tables de Karnaugh en 3D ou 4D, 
on veut dessiner les tables de Karnaugh a 4 entrees et les superposer.

Pour les tables de Karnaugh a:
- 5 entrees: 2 tables de Karnaugh 4 entrees et les superposees
- 6 entrees: 4 tables de Karnaugh 4 entrees et les superposees
