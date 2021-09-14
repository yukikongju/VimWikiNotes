# IFT2105 - Week 3 Lecture 1 - Definition d'une machine de Turing; Configuration des transitions

## Overview

On a commence le chapitre 3.1 - Les machines de Turings. 

Sections:
1. Qu'est-ce qu'une machine de Turing  
2. Definitions: alphabet, mot, language, ...  
3. Formulation d'un probleme de Turing

### Part 1 - Qu'est-ce qu'une machine de Turing  

Une machine de Turing est un modele qui utilise un ruban et des etats de 
transitions pour representer un programme. Plus generalement, on veut definir 
une fonction: Q x T = Q x T x {G,D}

Cette fonction de transition prend en input l'etat de depart et l'alphabet 
de ruban, qui nous permet de savoir dans quel etat transitionner, quoi ecrire 
sur le ruban et dans quelle direction se deplacer apres

- Inputs: etats de depart, alphabet de ruban 
- Outputs: etats final, alphabet de ruban, gauche/droite

### Part 2 - Definitions: alphabet, mot, language, ...  

On veut definir 4 definitions importantes:
- Alphabet: ensemble de symboles non-vide
- Mot: suite de symboles forme des "lettres" de l'alphabet (peut etre vide: \epsilon)
- \Sigma *: ensemble de tous les mots pouvant etre forme par l'alphabet
- Language: sous-ensemble de \sigma *

On peut aussi creer de nouveaux mots avec les symboles suivants:
- longueur de mot: |w|
- nombre d'occurences de la lettre a dans le mot w: |w| _ a
- inverser le mot: w^R
- concatenation: w=xy

Remarques:
- le mot vide \epsilon, ne fait pas partie du language vide {}

### Part 3 - Formulation d'un probleme de Turing

#### Machine de Turing - 6-Tuplets

Formellement, on designe une machine de Turing comme un 6-Tuplet:
- Q: les etats de transitions
- \sigma: l'alphabet
- \Gamma: l'alphabet de ruban
- \delta: la fonction d'etat
- F: Ensemble des etats finaux; F = {q_A, q_R}, ou q_A: etats acceptant; q_R: etats refusant
- q_0: l'etat initial

#### Configurations des transitions

On definit une transition comme un triplet [u,q,v]:
- u: l'alphabet ruban a gauche de l'etat present
- q: l'etat present
- v: l'alphabet ruban a droite de l'etat present

Pour noter la transition d'un triplet a un autre, on utilse les symboles:
- c |- c' : transition de l'etat c à c' en une étape de calcul
- c |-* c': transition de l'etat c à c' en 0 ou plus d'étape

### Comment déterminer si la machine de Turing accepte ou non les mots

La machine de Turing accepte les mots dépendemment si l'état de transition en 
output est un état acceptant ou un état refusant:  
- MT accepte si: (\espilon, q_0, w) |- * (u,q_A, v)
- MT refuse si: (\espilon, q_0, w) |- * (u,q_R, v)

