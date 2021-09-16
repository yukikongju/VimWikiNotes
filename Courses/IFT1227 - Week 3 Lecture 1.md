# IFT1227 - Week 3 Lecture 1: Blocs Combinatoires (Multiplexeur, Decodeur); Délai, Glitch et Horloge; Circuits Séquentiels

## Overview

Sections:  
1. Blocs Combinatoires (multiplexeur et décodeur)
2. Délais, Glitch et horloges
3. Circuits Séquentiels

## Part 1 - Blocs Combinatoires (multiplexeur et décodeur)

Les blocs Combinatoires sont une autre façon de représenter des circuits 
logiques. On discerne 2 types de blocs combinatoire: 
- Les multiplexeurs: prennent 2^n lignes 
- Les décodeurs: prennent n lignes en entrées et sortent 2^n output en sortie; one hot-encoding

À savoir:
1. Table de vérité
2. Représentation (design)

### Multiplexeurs

Un multiplexeur est un bloc combinatoire qui a un unique output, similaire 
à S, l'entrée. Ainsi, si :
- S=0 => D_0
- S=1 => D_1

On peut représenter les multiplexeurs de 3 façons:
1. Table de vérité + POS + tale de Karnaugh
2. Tampons à 3 états
3. Lookup Table

#### Lookup Table

Pour représenter les lookup tables, on doit se souvenir de quelques règles:
- les lignes qui output zéro sont reliés au ground, représenté par un triangle
- les lignes qui output un 1 sont reliés à la source, représentée par une barre

### Décodeurs

Un décodeur encode n entrées et 2^n sorties en format one-hot-encoding (toutes les valeurs à 0 sauf une seule à 1)

On connecte les sorties à une porte OR, qui relie les minterms set à 1


## Part 2 - Délais, Glitch et horloges

### Pourquoi y-a-t-il des délais lorsque les portes logiques changent de valeur

Lorsque les portes logiques changent de valeur (passe de 0 à 1 ou vice-versa), on assume que celles-ci changent de valeur immédiatement, mais dans les faits, il existe des délais

### Types de délais: propagation et contamination (TO REVIEW)

Il existe 2 types de délais:
- Délais de propagation: délai max entre premier changement et la stabilisation
- Délais de contamination: délai min entre premier changement et premiere sortie

### Comment peu-til y avoir des glitchs dans les circuits

Parfois, les circuits dont les chemins sont de longueur trop différentes peuvent créer des glitchs (ou aléas en français), car le signal fluctue trop 
rapidement. Ainsi, le signal devient illisible et le programme n'est pas déterministe.

Pour ce faire, on veut être capable de caractériser la longueur de ces chemins:
- chemin critique (chemin le plus long): sum delai de propagation de chaque porte t_pd
- chemin le plus court: sum délai de contamination t_{cd}

### Pourquoi a-t-on besoin d'horloge

Puisque le signal fluctue, il n'est pas toujours lisible. Ainsi, on veut le 
mesurer à intervalle régulier.

ON peut se synchroniser sur les fronts montants ou les fronts dessendants. Nous nous synchroniserons sur les fronts montants.

Clock cycle = intervalle entre 2 impulsions

## Part 3 - Circuits Séquentiels

Les circuits séquentiels sont des circuits logiques avec mémoire. On 
distingue 2 types de matériels:
- Circuit Bistable
- Latch SR (set/reset)

Il est important de savoir:
- design circuit
- le output dependemment des inputs

