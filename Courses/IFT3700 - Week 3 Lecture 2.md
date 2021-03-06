# IFT3700 - Week 3 Lecture 2: Modélisation; Biais Cognitifs; Specificité, Sensibilité et ROC 

## Overview

Sections: 
1. Modélisation  
2. Biais Congnits

## Part 1 - Modélisation  

En science des données, il faut se souvenir qu'on ne veut pas nécessairement 
expliquer ce qu'il s'est passé. On veut être capable de construire un 
modèle qui va pouvoir prédire le futur.

Notons que:
- On préfère avoir un modèle simple plutôt qu'un modèle compliqué, car celui-ci se généralise mieux -> no overfitting
- les sciences de données ne servent pas à prescrire/changer des comportements. Une prescription nécessite un effet causal que les sciences des données n'est pas nécessairement capable de nous donner.
- On se fie sur des peers reviews. Par contre, cela fait en sorte qu'on peut parfois manquer les cas extrêmes qu'on juge impossible. (ex: vagues ; gagner 72 fois à la roulette)
- Erreur de la modélisation: interpolation vs extrapolation -> il est correct d'intrapoler à l'intérieur des observations recueillis. Par contre, on ne peut pas extrapoler, car les données peuvent se comporter différement

### Évaluation du modèle: Spécificité, Sensibilité et ROC (TODO)

Pour évaluer le modèle, on peut utiliser 2 types de métriques:
- Sensibilité: Identify people with the disease (true positives)
- Spécificité:  Accurately identify people without the disease (true negatives)

Parfois, il existe une dichotomie entre la spécificité et la sensibilité. Tout 
dépendemment du problème, on préférera en prioriser un plutôt que l'autre. 

Par exemple, en médecine, on préfère avoir des faux positifs plutôt que de faux 
ngatifs. Ainsi, on voudra privilégier une plus forte sensibilité plutôt que 
spécificité.

Pour mesurer la "balance" entre la spécificité et la sensibilité, on utilise 
le modèle ROC

Ressources:
- [StatQuest ROC and AUC](https://www.youtube.com/watch?v=4jRBRDbJemM)
- [StatQuest - Confusion Matrix](https://www.youtube.com/watch?v=Kdsp6soqA7o)

### Lois de distributions de Rayleigh (TODO)

## Part 2 - Biais Congnifs

- Paréidolie: phenomene psychologique lorsqu'on associe des objets a des choses qu'on connait -> certains biais cognitifs peuvent nous donner de l'information sur ce qu'on cherche et n'est pas toujours present avec les chiffres (ex: illusions optiques)
- Erreur Systématique (proxy): les données recueillis ne répondent pas à la question qu'on se pose (ex: sondage -> on recolte les donnees des gens qui veulent repondre a la question, pas celle de la population)

### Liste de biais cognitifs en science des donnees (TODO)

