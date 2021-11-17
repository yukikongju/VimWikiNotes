# IFT1227 - Week 4 Lecture 1: Finite State Machines pour definir des circuits sequentiels (représentation de Melay et de Moore)

## Overview

Le but du cours était de voir comment représenter des finites states machines 
pour définir des circuits séquentiels. Pour se faire, on veut écrire 
un graphe de transitions. Il existe 2 types:
- Représentation de Melay: on envoie l'entrée et la sortie à l'autre état
- Représentation de Moore: on envoie seulement l'entrée, la sortie est 
  sauvegardée à l'intérieur de l'état

## Qu'est-ce qu'un automate fini

Un automate fini est caractérisé par un nombre d'états fini (t, t+1)

## Quelles étapes doit-on suivre pour tracer notre circuit séquentiel à partir d'un graphe de transition

Pour ce faire, on doit suivre les étapes suivantes:
1. Boite noire: on prend quelques exemples et on essait de voir leurs behaviors
2. Tracer le graphe de transitions en utilisant la représentation de Melay ou de Moore
3. Tracer la table de transitions donnée par:
    * l'état courrant
    * l'entrée
    * l'état futur
    * la sortie
4. Tracer la table de vérité
5. Écrire les fonctions canoniques données par la table de vérité
6. Tracer le circuits séquentiels avec un encodeur et une horloge (on utilise 
    SOP et une porte ou pour connecter les minterms)

Objectifs:
    - Être capable de traduire un graphe de transitions en tableau de transitions 
      en table de vérité et vice-versa

Exemples:
    * Lecteur binaire: lire une chaine binaire et output 1 lorsqu'on voit le substring
    * Intersection Rue avec priorité

## Quelles sont les différences entre la représentation de Melay et la représentation de Moore?


## Quels sont les avantages et désavantages entre la représentaion de Melay et celle de Moore

Représentation de Melay:
    * Avantage: Moins d'états que Moore  
    * Inconvénient: Instabilité temporelle

Représentation de Moore:
    * Avantage: Plus de stabilité temporelle
    * Inconvénient: plus d'états à représenter que Melay
