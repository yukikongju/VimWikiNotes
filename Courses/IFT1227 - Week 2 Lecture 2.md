# IFT1227 - Week 2 Lecture 2

- [IFT1227 - Week 2 Lecture 2 - Notes de Cours](IFT1227 - Week 2 Lecture 2 - Notes de Cours)

## Overview

Ce cours nous montrait comment la methode Quine-McKlusey fonctionne

## Part 1 - Methode de Quine-McKlusey

Steps:
1. Tracer la table de verite a partir de la fonction donnee  
2. Repérer les lignes dont le output est des minterms (F=1) ou des don't care 
   et les regrouper par bit flippé
3. Pour toutes les sections adjacentes, comparer toutes les paires de lignes. 
   Si les 2 lignes ont 1 bit de difference, marquer par un X et l'ajouter dans 
   le tableau secondaire; Si des lignes n'ont pas pu etre simplifiee, marquer par *
4. Recommencer les etapes 2 et 3 jusqu'a temps qu'on ne puisse plus simplifier
5. Construire le tableaux des choix: les colonnes sont les minterms (F=1); 
   les lignes sont les lignes notées par une etoile (WHAT IS THE NAME)
6. Identiquer par un crochet si les lignes etoilees generer le minterm
7. Ecrire la fonction simplifie, qui sera donnee par les lignes etoilees dont les 
   colonnes n'ont qu'un unique crochet

