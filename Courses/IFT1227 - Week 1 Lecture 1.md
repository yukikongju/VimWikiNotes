# IFT1227 - Week 1 Lecture 1

## Overview

1. Introduction
    a. Composantes d<un ordinateur
    b. Couches d'un ordinateur (high level lang to OS to microprocessor to logic gates)
2. Portes Logiques
3. Niveaux de Tension et bruit

## Part 1 - Introduction

### Composantes d'un ordi

Un ordi est compose de hardware (materiel: ecran, keyboard, CPU, ...) et de
software (programme qui ne se voit pas)

### Couches d'un ordi

Notre code subi plusieurs transformations avant d'etre interpreter par notre
ordinateur:
1. High level language -> compileur transforme high level to assembly code
2. Low level language -> assembleur transforme assembly code to machine code
3. Linker -> ajoute metadata + registers informations
4. Microarchitecture -> ???
5. Circuits logiques

Pour ce cours, on apprend de bottom-up

## Part 2 - Portes Logiques

On peut representer les portes logiques de 3 facons:
- table de verite
- fonction
- Symbole

Remarque:
- les portes logiques sont des circuits combinatoires -> pas de cycle permis + chaque porte = 1 output
- les portes logiques sont faits de transisteurs (x3)

## Part 3 - Niveaux de Tension et Bruit dans les transisteurs

Les transisteurs fonctionnent de facon analogue, c-a-d que le signal transmis
est continue. Par contre, il est pratique de le considerer discret. Ainsi,
on considere que le transiteur emet un 1 ou 0 dependemment s'il se trouve
a l'interieur d'un intervalle donne. S'il se trouve dans la zone interdite,
on n'est pas capable de determiner la nature du signal.

