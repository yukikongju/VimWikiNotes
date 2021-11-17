# IFT3700 - Week 4 Lecture 2: Nettoyage des données et puzzle sur les probabilité et statistiques

## Overview

Le cours s'est donné sur 2 axes:
1. Formattage des Données
2. Questions et Réponses sur les notions de probabilité et statistiques

## Part 1 - Nettoyage des données (TODO)

Il y a 3 grandes familles de raisons pourquoi il y aurait des erreurs dans nos 
données:
- Syntaxe
- Sémantique
- Couverture

### Comment Nettoyer les données
    * Nettoyage par parsing: regex, grammaire hors contexte
    * Standardisation: normaliser, cote z
    * Imputation pour les données manquantes

### Remarques

* Pourquoi préfère-t-on inventer des valeurs dans les cases manquantes plutôt que d'enlever la ligne
    * Biais: il y a une raison pourquoi certains individus ont des valeurs manquantes
    * Puissance des données: Plus de données est toujours préférable
* Les données aberrantes ne sont pas nécessairement des erreurs. Aut contraire, 
  on veut s'y intéresser, car ce sont elles nos sources d'erreurs
* Si jamais on décide d'enlever certaines lignes, on peut mesure l'impact de 
  ces effacements en mesurant la proportion de ligne enlevées par rapport au 
  nombres de données totales
* Pourquoi enlever les données dupliquées
    * Les données dupliqués biaisent la moyenne vers ses valeurs

## Part 2 - Curse of Dimensionality

Lorsqu'on essait de visualiser nos données en grande dimension, notre intuition 
nous joue des tours

## Part 3 - Puzzles sur les probabilités

* Loi de Benford: La plupart des nombres commence par 1,2 ou 3 -> utiliser 
  pour montrer qu'il y a eu fraudes
* Monty Hall: il est preferable de changer de porte
* Non transitivite des proba:
    * On tire une série de pile ou face, et chaque joueur choisit une séquence. 
      le premier joueur dont on voit la séquence gagne. Qui devrait jouer en 
      premier?
    * ????
* Empereur sexiste:
    * Mise en contexte: une loi est mise en place pour favoriser le nombre de 
      filles: chaque famille n'a que le droit d'avoir 1 seul garcon, mais peuvent 
      avoir autant de filles. Quelle va être la proportion de filles-gars?
    * Solution: la proportion reste la même au sein de la population, mais 
      la démographie par famille change. Cette loi agit sur le behavior des 
      parents, mais ne change pas la proba d'avoir une fille ou un gars
* Parier son portefeuille:
    * Mise en contexte: je mise que j'ai moins de cash dans mon portefeuille 
      que toi. Si j'ai raison, je gagne ton portefeuille; si j'ai tort, tu 
      gagnes le mien. Devrait-on jouer?
    * Solution: Non, il n'y a pas de gagnant. Par contradiction, on montre 
      que les 2 ont un avantage, mais il est impossible que les 2 joueurs 
      aillent un avantage sur l'autre, ce qui constitue une contradiction.
* Information Négative:
    * Mise en contexte: est-il possible qu'une question nous donne de l'information 
      négative?
    * Solution: NON, mais la réponse, elle, peut nous donner de l'information 
      négative

