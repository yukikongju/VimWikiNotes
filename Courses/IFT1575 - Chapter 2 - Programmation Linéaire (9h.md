# IFT1575 - Chapter 2 - Programmation Linéaire (9h)

## Overview

Ce chapitre nous introduisait la notion de problèmes en programmation linéaire. 

Sections: 

* Hypothèses d'un problème de programmation linéaire:
    * Linéarité: additivité + proportionnalité
    * Non-négativité
    * Déterministe

* Modéliser un problème en programmation linéaire
    * Étapes:
	1. Identifier les variables de décisions  
	2. Identifier la fonction objectif
	3. Identifier les contraintes structurelles et les contraintes de non-négativité
	4. Réécrire le modèle

* Résoudre un problème de programmation linéaire avec l'algorithme du simplexe
    * Prerequisite: S'assurer que le problème est dans sa forme standard:
	* Problème de minimisation (si maximisation, multiplier la fonction objectif par -1)
	* Équations: introduire des variables d'écarts pour avoir des équations, pas inéquations
    * Méthodes de l'algorithme du Simplexe
	* Méthode Algébrique: On cherche la variable d'entrée en regardant le plus 
	  petit coefficient de la fonction objectif et on met toutes les variables 
	  sauf la variable d'entrée à zéro pour identifier la variable de sortie
	* Méthode Tableau: On essait de trouver le pivot, qui est le coefficient 
	  qui intersecte la variable d'entrée et de sortie 
	* Méthode Graphique

Remarques: 
- être capable d'écrire un problème avec des variables de décisions normales et binaires

