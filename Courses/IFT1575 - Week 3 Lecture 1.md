# IFT1575 - Week 3 Lecture 1: Algorithme du simplexe - Methode Algebrique et Methode Tableau 

## Overview

Ce cours focussait sur la resolution de problemes en programmation lineaire à 
l'aide de l'algorithme du simplexe. La méthode du simplexe peut s'exécuter 
sous 3 méthodes:
- méthode algébrique: résoudre un SEL
- méthode Tableau: les coefficients sont dans un tableau
- méthode Graphique: On trace les droites et on parcourt les points de rencontre

Ce cours-ci focusse sur les 2 premieres methodes: la méthode algébrique et la 
méthode tableau

## Part 1 - Algorithme du Simplexe - Méthode Algébrique

La méthode du simplexe est un algorithme itératif qui cherche à optimiser un 
système d'équations. L'algorithme existe sous sa forme "minimiser" et "maximiser", 
mais dans le cadre de notre cours, nous allons que nous concentrer sur l'algorithme 
qui minimise. Il suffit de mettre les problèmes dans leurs bonnes formes, qu'on 
nomme forme standard

Pour que l'algorithme fonctionne, il faut que le problème de programmation linéaire
soit exprimée sous forme:
- Standard: chaque ligne est une équation -> introduire des variables d'écart 
- Problème de minimisation -> [maximiser f(x) <=> minimiser -f(x)]

Les grandes étapes sont les suivantes:
1. Modéliser le problème en problème de programmation linéaire
2. Si le modèle est un problème de maximisation, le transformer en problème de 
   minimisation en multipliant sa fonction objectif par -1
3. Transformer le modèle sous sa forme standard en introduisant des variables 
   d'écarts
4. Itérer l'algorithme du simplexe jusqu'à ce qu'on ne puisse plus optimiser 
   la fonction objectif (ie les coefficients sont tous positifs)

Comment l'algorithme du simplexe fonctionne en général:
- Determiner les variables independantes et dependantes
- Determiner la variable d'entrée: c'est la variable indépendante dont le coefficient 
  minimise la fonction objectif z
- Déterminer la variable de sortie: c'est la variable dépendante qui limite l'augmentation 
  de la variable d'entrée

### Forme Standard d'un problème linéaire - Introduction des variables d'écarts

On dit qu'un problème de programmation linéaire est de forme standard si toutes 
les lignes sont des équations (pas des inéquations). Si notre problème avait 
initialement des inéquations, on veut les transformer en équations en introduisant 
des variables d'écarts.

### Itération de l'algorithme du Simplexe

Une fois que le problème de programmation linéaire est sous sa forme standard 
et sa fonction objectif tente de minimiser qqch, on peut itérer l'algorithme 
du simplexe jusqu'à ce que celle-ci n'ait plus de coefficients positifs

Comment une itération fonctionne:
1. Déterminer les variables indépendantes et dépendantes: initialement, les variables 
   indépendantes sont les variables de décisions et les variables dépendantes sont 
   les variables d'écarts  
2. Trouver le système d'équations linéaires: on exprimer les variables dépendantes 
   comme une combinaison linéaire des variables indépendantes en utilisant la 
   substitution si nécessaire  
3. Trouver la variable d'entrée


## Part 2 - Algorithme du Simplexe - Méthode Tableau

L'algorithme du simplexe qui roule avec la méthode du tableau se base sur la 
notion de pivot pour "rendre" un coefficient positif a chaque iteration.

Les etapes:
1. Déterminer les variables dépendantes et indépendantes: les variables de decisions 
   sont les variables independantes au debut; les variables d'écarts seront 
   les variables dépendantes  
2. Déterminer la variable d'entrée: c'est la variable indépendante ayant le 
   plus petit coefficient
3. Déterminer la variable de sortie: c'est la variable dépendant qui, mise à zéro, 
   minimise la valeur de la variable d'entrée  
4. Déterminer le coefficient qui sera le pivot: c'est l'intersection entre 
   la variable d'entrée et de sortie  
5. Swap la variable d'entrée et la variable de sortie: on divise la ligne du coefficient 
   par celui-ci  
6. Échelonner les autres lignes 
7. Déterminer si on doit faire une autre itération: regarder si les coefficients 
   de la fonction objective sont positifs

## Quelles sont les différences entre la méthode algébrique et la méthode du tableau (TODO)

