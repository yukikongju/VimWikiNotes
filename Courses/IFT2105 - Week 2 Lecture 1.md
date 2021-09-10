# IFT2105 - Week 2 Lecture 1

## Overview

Le cours abordait les programmes REPETER:
1. Qu'est-ce qu'un programme repeter
2. Structure recursive d'un programme repeter
3. Exemples de programme repeter

## Part 1 - Qu'est-ce qu'un programme repeter

Un programme repeter est un programme qui:
- Contient un nombre fini de registres, initialise a zero
- les registres contiennent uniquement des valeurs entieres
- 3 instructions:
    - store: r_i <- r_j
    - increment: inc(r_i)
    - Repeat: repeat n times { ... }

## Part 2 - Structure recursive d'un programme repeter 

Un programme répéter admet les caractéristiques suivantes:
- S_0 : store et increment sont des programmes repeter
- R_1: Concatenation de programmes repeter est un programme repeter
- R_2: Si P est un programme repeter, repeat n times { P } est un programme repeter

## Part 3 - Exemples de programme repeter

On a vu quelques exemples de programmes repeter:
- addition, multiplication, exponentiation
- decrementation, soustraction
- boolean, operateur logiques(ET:mult, NEG:moins, OU: DeMorgan )
- Plus grand, division, modulo  
- estPremier, prochainPremier, premierK  

Ces exemples servent non seulement a se familiariser avec la structure des 
programmes repeter, mais servent aussi de building blocks pour les structures 
de donnees, ce qu'on va voir au prochain cours.

### Code pour les programmes repeter

#### Plus grand, division, modulo  

##### est Plus Grand: PG(x,y) = x > y

```
z = moins(x,y)
repeat z fois {
    r_o = vrai
}
```

##### Plus grand ou egal: PGE(x,y): x >= y

```
z = PG(y,x)
r_0 = NEG(z)
```

##### Division: DIV(a,b) = floor(a,b)

``` 
repeat a times {
    z = moins(a,b)
    pas_rendu = (z <= a)
    if pas_rendu, then {
	inc(r_0)
    }
}
```

##### Modulo: MOD(a,b) = a % b

My solution:
```
repeat a times {
    z = moins(a,b)
    est_rendu = (z < a)
    si est_rendu, alors {
	r_0 = z
    }
}
```

PP solution:
```
b = div(x,y)
c = mult(b,y)
r_0 = moins(x,c)
```

#### estPremier, prochainPremier, premierK  

- estPremier: return true si le nombre est premier  
- prochainPremier: retourne le prochaine nombre premier  
- premierK: retourne le k-ieme nombre premier 

##### estPremier

Un nombre est premier s'il n'est divisible que par 1 et lui-meme.

On teste si le modulo est nul pour chaque incrément

```
if (x>1){
    r_o <- vrai
    temp <- 1
    repeat (x-2) fois {
	inc(temp)
	mod <- MOD(x, temp)
	if (mod==0), alors r_0 = false
    }
}
```

##### ProchainPremier

Pour trouver le prochaine premier, on doit tester si le nombre est premier en incrementant chaque nombre et testant si ce dernier est premier.

```
max_iter <- FACT(x)
inc(max_iter)
pas_fini <- vrai
repeat max_iter {
    inc(x)
    est_premier <- PREMIER(x)
    if (pas_fini, estPremier), then {
	r_0 <- x
	pas_fini <- false 
    }
}
```

##### PremierK

```
inc(r_0)
repeat k fois {
    r_0 <- prochainPremier(r_0)
}
```

