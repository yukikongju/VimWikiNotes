# IFT3700 - Week 4 Lecture 1: Données Structurées (types de données, CSV, MNIST et ADULT)

## Overview

Avant de faire notre analyse en science des données, il faut recueillir de 
l'information et les storer. Malgré qu'on ne verra pas comment faire la cueillette 
des données, il faut se souvenir que les dommages créés par une méthodologie 
mal faite durant la phase de collecte de données à des répercussions beacoup 
plus importantes que des erreurs dans la phase analyse.

1. Types de données
2. Modèle CSV
3. Dataset: MNIST et ADULT

## Part 1 - Types de données

On distingue 3 types de données:
- Binaire: Son, vidéo, pdf, image
- Catégorique: booléens, classes, on-hot encoding
- Numérique: discrète, continue (quasi continue), ordinale (les classes ont un ordre)

Remarques:
- on parle de variables quasi continue, car dans les faits, toutes les variables 
  sont discrètes, mais il est plus pratique de les traités comme continues
- Lorsqu'on identifie les variables, on veut connaitre:
    - type: str, bool, int, float
    - longeur de l'entrée: nom avec maximum 50 caractères
    - range: age non-négatif de 0-100
- Les one-hot encoding sont utilisées pour contrer les bad effects qui peuvent 
  se produire lorsqu'on encode des données ordinales avec des nombres (vu plus tard)

## Part 2 - Modèle CSV

Le modèle a suivre est le modèle CSV:
- comma separated

## Part 3 - Dataset: MNIST et ADULT

On a parlé de 2 datasets:
- MNIST: dataset d'images 28x28
    * Catégorisation avec booléens: puisque chaque pixel est une variable entre 
      0-256, on a trop d'information. Ainsi, pour simplifier, on remplace chaque 
      pixel par une variable binaire (1 si activé; 0 sinon)
- ADULT: donnée la situation socio-économique de la population
    * Anonymisation: on parle d'anonymisation lorsqu'on essaie de rendre des 
      données privées publiques. Naivement, on n'a qu'à enlever le nom de 
      la personne, mais dans les faits, il est quand même possible d'en 
      apprendre davantage sur une personne si on a quelques-une de ces infos.

