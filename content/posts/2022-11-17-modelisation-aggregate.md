---
title: "Atelier DDD : modélisons nos agrégats pour mieux les découper"
date: 2022-11-17T19:00:00+01:00
tags: ["ddd"]
---

- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/289315774/)
- [Board Miro](https://miro.com/app/board/uXjVPCDgBE8=/?share_link_id=484965691262)
- 16 présent·e·s

# Iteration 1 : Train reservation

On arrive globalement à la même solution : Aggregate train et des entités pour Wagon, seat, ...  
Il est cependant possible d'avoir un aggregte Train et un aggregate Wagon qui permet une meilleur scalabilité. Cela demande la création d'un service Reservation pour orchestrer le tout.  
Une autre solution est d'utiliser des domain events pour changer de règle de remplissage ce qui pose des soucis de cohérence a terme et qui peut créer de la frustration pour les usagés.  

# Iteration 2 : Team

## Groupe 1 :

- 1 aggregate personne
- 1 aggregate equipe avec 1 entity membre
- 1 aggregate projet
Orchestration via une Orchestration service

## Groupe 2 :

### Solution 1 :
- 1 aggregate Member
- 1 aggregate Project
- 1 aggregate Team avec 1 entity ProMember

### Solution 2 :
- 1 aggregate Member
- 1 aggregate Team avec 
  - 1 entity Project
  - 1 entity ProMember
Dans ce cas la création du projet ne peut pas se faire sans équipe

## Groupe 3 : 

### Variantes project: 

Project en ValueObject dans Team  
Project en Aggregate et lien dans Team  
Project en Aggregate et ValueObject de Team dans Project  

### Solution 1 : 

- 1 aggregate Team
  - 1 entity Member
- 1 aggregate Person

### Solution 2 : 

- 1 aggregate Person
  - 1 entity Membership
- 1 aggregate Team

# Retro

Pas une bonne idée de prendre "le train en route"  
Un exemple de code sur les exercices pourrait être une bonne idée  
Mettre l'exo 2 avant le 1 pourrait être une bonne idée  
Beaucoup de chose "devinées" sur le métier  

## ROTI

- 3/5 : 2
- 4/5 : 10
- 5/5 : 2
