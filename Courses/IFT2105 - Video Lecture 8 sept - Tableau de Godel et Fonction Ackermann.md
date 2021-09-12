# IFT2105 - Week 2 Lecture 2 - Video Lecture Notes

## Overview

1. Tableau avec codage de Godel (assignation, lecture des elements)
2. Les programmes repeter sont moins performants que les programmes Tant que

## Structure de donnees - Tableau avec Codage de Godel 

Encoder les valeur d'un tableau avec un nombre (meme principle avec liste de listes)

### Comment l'encodage de Godel encode les elements du tableau

Chaque element est l'exposant du i-eme nombre premier

Ex: [5,2,7,8,6] -> ``2^5 3^2 5^7 7^8 11^6`` 

Code pour l'assignation 
```

```

### Comment lire les elements du tableau a partir du nombre

## Part 2 - Les programmes repeter sont moins puissants que les programmes tant que

Pour montrer que les programmes repeter sont moins puissants, 
on veut definir une famille de fonctions, qu'on nomme Ackermann, qui ne peut pas etre calculee par les programmes REPETER

### Fonction d'Ackermann

On definit la fonction Ackermann B_i:
- x+1 si i=0
- B_{i-1} ^ {x+1} (1) si i>0

Pour se faire, on veut construire notre preuve avec les preuves suivantes:
1. Lemme: B_{i+1} est calculable par un programme repeter avec
    une profondeur de boucle i (preuve par recurrence sur i)
2. Theoreme:

### Lemme: B_{i+1} est calculable par un programme repeter avec une profondeur de boucle i (preuve par recurrence sur i)

En calculant les premiers B_i, on voit qu'on multiplie a chaque fois B_i(x) = 2^2^2^2^... -3

### Proprietes des fonctions Ackermann (x4)

On utilise ces proprietes pour montrer le theoreme suivant 

### Theoreme: Pour tout programme repeter P, si la profondeur de boucle B(P)=i, pour tous les registres, M(P, r_0, ...) est borne par B_{i+1}^<l(P)>(max registers)

M: Valeur maximale de tous les registres

Preuve par recurrence structurelle (S_0, R_1, R_2)

### Corollaire: Pour tout i>=0, il existe une fonction qui n'est pas calculable par un programme repeter de longueur i, mais qui est calculable avec un programme de boucle i+1

### Theoreme: A(i,x) n'est pas calculable par un programme repeter (preuve par contradiction)

On cree notre contradiction en montrant que 
- A(l+2, l) = B_{l+1}(2l) a l'aide du theoreme sur la borne des ligne
- A(l+2, l) a l'aide de la definition/ corollaire?

## En Resume

Le cours s'est fait en 2 parties;
1. Tableau dans un programme repeter a l'aide de l'encodage de Godel
2. Les programmes repeter ne peuvent pas calculer les fonctions Ackermann

### Part 1 - Tableau dans un programme repeter a l'aide de l'encodage de Godel

On veut encoder les tableaux a l'aide de nombres premiers. 
L'encodage de Godel nous dit que si le tableau est de taille n, le nombre cree est le produit des i-emes nombres premiers a l'exposant T[i]

Si on a le tableau [3,6,9], on obtient N=2^3 * 5^6 * 7^9 

- QUESTION: Comment decoder les valeurs dans le tableau d'un programme repeter a l'aide de lencodage de Godel?

Pour chaque case dans le tableau, on veut diviser par le i-eme nombre prime. Tant que le nombre est divisible, on incremente la valeur du nombre

```
for i in range(len(T)):
    prime <- find k-ieme prime number
    valeur=0
    while N % prime != 0:
	valeur++;
```
	
### Part 2 - Les programmes repeter ne peuvent pas calculer les fonctions Ackermann

On doit se souvenir que les programmes repeter ne sont pas autant puissants que les programmes tant que. On verra plus tard que ceux-ci permettent des boucles infinies.

Pour se faire, on veut montrer qu'ils existent des fonctions que les programmes repeter ne peuvent pas calculer: les fonctions Ackermann.

Une fonction Ackermann est definie de la facon suivante:
- si i=0: B_i(x) = x+1
- si i>=0: B_i(X) = B_{i-1} ^{i+1)}(1) 

Pour se faire, on veut construire cette preuve avec quelques lemmes/theoremes/corollaires:
1. Lemme: B_{i+1} est calculable avec un programme repeter avec une boucle de profondeur i 
=> la preuve se fait par induction (a revoir)
2. Theoreme: Pour tout programme repeter de profondeur B(P)=i, le nombre de lignes de se programmes P, noté M(P), est borne par la fonction Ackermann B_{i+1}^{nb le lignes} (1)
=> la preuve se fait avec les 4 proprietes et avec une preuve par recurrence structurelle: On montre que:
    1. S_0 est valide: les programmes repeter a une ligne sont bornees
    2. R_1 est valide: la concatenation est bornee
    3. R_2 est valide (plus difficile): un programme repeter P qui est repeter n fois est aussi bornee 
3. Corrolaire: Tout Programme Repeter qui n'est pas calculable avec une boucle de profondeur i peut etre calculee avec une boucle de profondeur i+1
4. Theoreme (but final!!): Les programmes repeter ne peuvent pas calculer les fonctions Ackermann
=> (preuve par contradiction): on se sert du theoreme sur la borne du nombre de lignes et du lemme/def pour montrer qu'il y a contradiction

